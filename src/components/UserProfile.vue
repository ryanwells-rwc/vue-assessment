<template>
  <div id="container">
    <div id="row">
      <div id="col1" v-if="imageUrl == require('../assets/chris.jpg')">
        <img :src="imageUrl">
      </div>
      <div id="col2">
        <h1>{{ name }}</h1>
        <a :href="`tel:${phone}`">{{ phone }}</a> -
        <a :href="`mailto:${email}`">{{ email }}</a>
        <p>Rate: ${{ rate }}</p>
      </div>
      <button id="editProfile" v-on:click="showForm = !showForm">Edit Profile</button>
    </div>
    <form v-if="showForm">
      <h2>Editing Profile...</h2>
      <label for="txtImageUrl">Image URL: </label>
      <input type="text" id="txtImageUrl" v-model="imageUrl">
      <label for="txtName">Name: </label>
      <input type="text" id="txtName" v-model="name">
      <label for="txtEmail">Email: </label>
      <input type="email" id="txtEmail" v-model="email">
      <label for="txtPhone">Phone: </label>
      <input type="text" id="txtPhone" v-model="phone">
      <label for="txtRate">Rate: </label>
      <input type="text" id="txtRate" v-model="rate">
    </form>
  </div>
</template>

<script>
export default {
  name: 'UserProfile',
  data() {
    return {
      imageUrl: require('../assets/chris.jpg'),
      showForm: false,
      name: 'Chris Guadarrama',
      phone: '(949) 939-3901',
      email: 'kristop78@gmail.com',
      rate: '25'
    }
  }
}
</script>

<style scoped lang="scss">
  @import url('https://fonts.googleapis.com/css?family=Exo+2:400,100,200,300,700,500,600,800,100italic,200italic,300italic,400italic,500italic,600italic,700italic,800italic');

  h1, a, p {
    font-weight: 300;
  }

  h1, button {
    text-transform: uppercase;
  }

  a, button {
    color: #41bcee;
  }

  a, p {
    font-size: 24px;
  }

  form, input, button, #row {
    font-family: 'Exo 2';
  }
  
  h1 {
    margin-top: 15px;
    font-size: 40px;
    letter-spacing: 6px;
  }

  h2 {
    /*text-align: center;*/
    font-weight: 400;
  }

  p {
    margin-top: 0;
  }

  input {
    display: block;
    margin: 5px 0;
  }

  #col1, #col2 {
    display: inline-block;
    margin: 30px 45px;
    vertical-align: top;
  }

  #col1 {
    width: 180px;
    height: 180px;
    overflow: hidden;
    border-radius: 50%;
    img {
      margin: 0 0 0 -30px;
      height: 100%;
      width: auto;
    }
  }

  #col2 {
    width: 600px;
  }

  #editProfile {
    display: block;
    position: relative;
    left: 40px;
    /*font-family: inherit;*/
    font-size: 20px;
    background-color: #ececec;
    border: none;
    width: 200px;
    padding: 15px;
  }

</style>
