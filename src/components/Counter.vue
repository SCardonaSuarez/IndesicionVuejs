<template>
  <h2>{{ customTitle }} </h2>
  <p>{{ counter }} <sup>2</sup> = {{ squareCounter }}</p>


  <div>
    <button @click="increase()"> + 1 </button>
    <button @click="decresease()">- 1 </button>
  </div>


</template>

<script>
export default {

    props: {
        title: String,
        start: {
            type: Number,
            default: 100,
            validator(value){
                return value >= 0
            }
            // required: true

        }
    },

  data() {
    return {
      counter: this.start
    }
  },
  methods:{
    getSquare(){

        return this.counter * this.counter
    },
    increase(){
        return this.counter ++
    },
    decresease(){
        return this.counter --
    }
  },
  computed:{
    squareCounter(){
        return this.counter * this.counter
    },
    customTitle(){

        // return this.title ? this.title : 'Counter'
        return this.title || 'Counter'
    }
  }
};
</script>

<style>
button{
    background-color: #64B687;
    margin: 0 5px;
    border-radius: 5px;
    border: 1px solid #fff;
    cursor: pointer;
    padding: 5px 15px;
    color: #fff;
    transition: 0.3s ease-in-out;
}

button:hover{
    background-color: #5aa67b;
    transition: 0.3s ease-in-out;

}


</style>
