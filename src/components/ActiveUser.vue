<template>
<section>
    <h2>{{userName}}</h2>
    <h3>{{age}}</h3>
</section>
</template>

<script>
export default {
  emits: [],
  data() {
    return {
     userName:'test user name',
     age: 27
    };
  },
  methods: {
  
  },
};
</script>