
<template>
  <div class="hello">
    <button v-on:click="date">click me</button>
    <button v-on:click="square(2)">2</button>
    <button v-on:click="square(3)">3</button>
    {{ text }}
    <button v-on:click="newWorld">new world</button>
    <button v-on:click="otherNewWorld">other new world</button>
    <p>{{ cost }}</p>
    <p>{{ amount }}</p>
    <p>{{ price }}</p>
  </div>
</template>


<script>
  export default{
      data(){
        return{
          cost:12,
          amount:4,
          text: 'wild and running'
        };
      },
      methods:{
        date: function(){
          let day = ['sunday', 'monday', 'tuesday', 'wensday', 'thursday', 'friday', 'saturday'];
          let date2 = new Date();
          let date3 = date2.getDay();
          alert(day[date3]);
        },
        show: function(){
          let num2 = this.dayWeek(this.numm);
          alert(num2);
        },
        dayWeek:function(num3){
          let arr = ['sunday', 'monday', 'tuesday', 'wensday', 'thursday', 'friday', 'saturday'];
          for(let i = 0; i<6; i++){
            if(num3 == i){
              return arr[i];
            }
          };
        },
        square:function(num){
          alert(num*num)
        },
        newWorld:function(){
          this.text = 'fearlessness is burning bright'
        },
        otherNewWorld:function(){
          this.text = 'we knew nothing, cause out of sight is out of mind'
        },
        computed:{
          price:function(){
            return this.cost * this.amount;
          }
        }
      }
  };
</script>
<style scoped>
.hello{
  font-size: 2em;
}
</style>