<template>
  <form>
    <label>Email:</label>
    <input type="email" v-model="email" required />

    <label>Password:</label>
    <input type="password" v-model="password" required />

    <label>Role:</label>
    <select v-model="role">
      <option value="developer">Web Developer</option>
      <option value="designer">Web Designer</option>
    </select>

    <div class="terms">
      <input type="checkbox" v-model="terms" required />
      <label>Accept Terms and Conditions</label>
    </div>

    <div>
      <input type="checkbox" value="Ayushman" v-model="names" />
      <label>Ayushman</label>
    </div>
    <div>
      <input type="checkbox" value="Aman" v-model="names" />
      <label>Aman</label>
    </div>
    <div>
      <input type="checkbox" value="XenOn" v-model="names" />
      <label>XenOn</label>
    </div>
    <div>
      <input type="checkbox" value="Duoro" v-model="names" />
      <label>Duoro</label>
    </div>
  </form>
  <p>
    {{ email }} - {{ password }} -- {{ role }} -- {{ terms }} -- {{ names }}
  </p>
</template>

<script>
export default {
  name: "SignUp",
  data() {
    return {
      email: "",
      password: "",
      role: "designer",
      terms: false,
      names: [],
    };
  },
};
</script>

<style scoped>
form {
  max-width: 420px;
  margin: 30px auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
}
label {
  color: #aaa;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.6em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}
input,
select {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #ddd;
  color: #555;
}
input[type="checkbox"] {
  display: inline-block;
  width: 16px;
  margin: 0 10px 0 0;
  position: relative;
  top: 2px;
}
</style>