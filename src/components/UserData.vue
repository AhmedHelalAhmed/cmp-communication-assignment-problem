<template>
  <section>
    <form @submit.prevent="submitData">
      <div>
        <label> Name: </label>

        <input v-model="nameEntered" type="text" />
      </div>
      <div>
        <label> Age: </label>

        <input v-model="ageEntered" type="number" />
      </div>

      <div>
        <button>save</button>
      </div>
    </form>
  </section>
</template>

<script>
export default {
  props: {
    userName: {
      type: String,
      required: true,
    },
    age: {
      type: Number,
      required: true,
    },
  },
  emits: ["update-data"],
  data() {
    return {
      nameEntered: this.userName,
      ageEntered: this.age,
    };
  },
  methods: {
    submitData() {
      this.$emit("update-data", this.nameEntered, this.ageEntered);
    },
  },
};
</script>
