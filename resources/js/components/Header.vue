<template>
  <div class="row">
      <div class="col">
        <div class="w-50 m-auto">
            <ul class="navbar-nav mr-auto flex-row justify-content-around fs-5">
                <li class="nav-item" v-for="(item, index) in menuItems" :key="index">
                    <router-link class="nav-link" :to="{name: item.route}">{{item.label}}</router-link>
                </li>
            </ul>
        </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Header',
    data(){
      return {
        menuItems: [
          {
              label: 'Home',
              route: 'home'
          },
          {
              label: 'Contact Us',
              route: 'contact'
          },
        ]
      }
    }
}
</script>

<style>

</style>