<template>
  <div class="home">
    <UserProfile :imageUrl="imageUrl" :showForm="showForm" :firstName="firstName" :lastName="lastName" :phone="phone" :email="email" :rate="rate"/>
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
  },
  data() {
    return {
      // imageUrl: require('../assets/chris.jpg'),
      imageUrl: 'imageURLHere',
      showForm: false,
      firstName: 'Ryan',
      lastName: 'O\'Boyle',
      phone: '(949) 838-9929',
      email: 'ryanoboyles_email@gmail.com',
      rate: '35'
    }
  }
}
</script>
