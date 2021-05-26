<template>
  <head>
    <title>Font Awesome Icons</title>
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"
    />
  </head>
  <body>
    <div class="header">
      <span class="login-signup">
        <ul>
          <li class="menuItem">Login</li>
          <li class="menuItem">Sign up</li>
          <i
            class="fa fa-shopping-cart"
            style="font-size: 48px; color: brown"
          ></i>
          <strong> 0 </strong>
        </ul>
      </span>
      <span class="company-name">
        <h1><strong> PVR Mobile </strong></h1>
      </span>
      <span class="menu">
        <ul>
          <li class="menuItem">Our Plans</li>
          <li class="menuItem">Shop</li>
          <li class="menuItem">iPhone</li>
          <li class="menuItem">Android</li>
          <li class="menuItem">Repair</li>
          <li class="menuItem">Students</li>
        </ul>
      </span>
    </div>
    <br />
  </body>
</template>


<script>
export default {
  components: {},
  // Emits the user name and password in an object upon clicking the submit button.
  emits: ["userInfo"],
  data() {
    return {
      userName: null,
      password: null,
      valid: true,
    };
  },
  methods: {
    submitForm() {
      if (
        this.userName == null ||
        this.password == null ||
        this.userName.length < 5 ||
        this.password.length < 5
      ) {
        this.valid = false;
        return;
      }
      const userInfo = { userName: this.userName, password: this.password };
      this.$emit("userInfo", userInfo);
      this.valid = true;
    },
  },
};
</script>


<style>
body {
  /* background: url("../../assets/clouds.jpg") no-repeat fixed center; */
  font-family: Tahoma, sans-serif;
}

.header {
  /* background: white; */
  display: inline-block;
  margin: 10px 10px;
  padding: 10px 10px;
  width: 96%;
}

.header .button {
  display: inline-block;
  width: 100px;
  text-align: center;
  border: solid 1px white;
  padding: 20px 20px;
  color: maroon;
  border-radius: 25px;
  background-color: pink;
}

.header .button:hover {
  cursor: pointer;
  font-size: 20px;
  color: yellow;
}

.header .menu {
  float: left;
  width: 400px;
}

.header .menu .menuItem,
.header .login-signup .menuItem {
  display: inline-block;
  list-style: none;
  padding: 20px 20px;
}

.header .menu .menuItem:hover,
.header .login-signup .menuItem:hover {
  font-size: 22px;
  color: pink;
  cursor: pointer;
}

.header .company-name h1 {
  text-align: center;
  font-size:30px;

  display: inline-block;
  width: 200px;
  margin-left: 275px;
}

.header .login-signup {
  float: right;
}
</style>

