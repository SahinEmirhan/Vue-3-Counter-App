Vue.createApp({
data(){
    return{
        counter : 0,
        counter2 : 0,

    }

},
methods:{

},
computed : {
    getCounterResult(){
        console.log('Counter 1 Çalıştı');
      return this.counter > 5 ? 'Greater than 5' : 'Less than or equal to 5'
    },
    getCounter2Result(){
        console.log('Counter 2 Çalıştı');
        return this.counter2 > 5 ? 'Greater than 5' : 'Less than or equal to 5'
      }
},
watch:{
    counter(newValue,oldValue){
        console.log('Counter',oldValue,'=>',newValue);
    },
    getCounterResult(newValue,oldValue){
        console.log('Result',oldValue,'=>',newValue);
    }

}




}).mount('#app')