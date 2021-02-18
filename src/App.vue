<template>
  <div id="app" class="font-sans">
    <Navbar />
    <main style="background: #f6f6f6" class="pt-12">
      <div class="container mx-auto mt-8 px-4 py-14 md:px-10 xl:px-32 mt-4">
        <div class="grid grid-cols-5 w-auto">
          <div class="col-span-1">
            <Sidebar />
          </div>
          <div class="col-span-4">
            <router-view></router-view>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import Navbar from "@/components/layout/Navbar";
import Sidebar from "@/components/layout/Sidebar";

export default {
  components: {
    Navbar,
    Sidebar,
  },
};
</script>


<style>
.router-link-exact-active li {
  border-radius: 10px;
  background: #fff;
  box-shadow: 0px 4px 5px 0px rgba(0, 0, 0, 0.25);
}
</style>
