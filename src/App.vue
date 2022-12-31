<template>
  <div>Hello {{ message }}</div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      message: "default"
    };
  },
  async mounted() {
    //const { text } = await (await fetch("/api/RewriteEmail")).json();
    const text = await (await fetch("/api/RewriteEmail")).text();
    this.message = text;
  }
};
</script>
