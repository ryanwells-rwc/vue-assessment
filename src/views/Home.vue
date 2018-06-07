<template>
  <div class="home">
    <UserProfile />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import UserProfile from '@/components/UserProfile.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    UserProfile
  }
}
</script>
