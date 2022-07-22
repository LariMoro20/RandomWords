<template>
  <div class="footer bg-black">
    <div class="footer-logo text-center">
      <img class="footer-logo-img" src="/images/logo/logo-white.webp" /><br />
      <small class="copy"
        ><a href="https://larissa-santos.vercel.app" target="_blank">
          {{ year }} &copy; by Larissa Santos</a
        ></small
      >
    </div>
  </div>
</template>
<script>
import { defineComponent } from "vue";
export default defineComponent({
  setup() {
    return { year: new Date().getFullYear() };
  },
});
</script>

<style>
.footer {
  padding: 10px;
}
.footer-logo-img {
  width: 120px;
}
.copy,
.copy a {
  text-decoration: none;
  color: #fff;
}
</style>
