<template>
  <div>
    <Navbar/>
    <div class="container-fluid">
      <div class="row">
      <Sidebar/>
        <main role="main" class="col-md-9 ml-sm-auto col-lg-10 pt-3 px-4">
          <router-view></router-view>
        </main>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import Sidebar from "@/components/Sidebar";
export default {
  components: {
    Navbar,
    Sidebar,
  }
}
</script>

