<template>
<section>
<form @submit.prevent="submitData">
    <div>
        <label> Name: </label>

        <input v-model="name" type="text" />
      </div>
          <div>
        <label> Age: </label>

        <input v-model="age" type="number" />
      </div>

      <div>
          <button>save</button>
      </div>

</form>

</section>
</template>

<script>
export default {
  emits: [],
  data() {
    return {
     name:'',
     age:''
    };
  },
  methods: {
  
  },
};
</script>