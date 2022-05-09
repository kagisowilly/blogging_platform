<template>
  <section class="contact-background" id="contact">
    <div class="cont container">
      <div class="formm">
        <div class="form-cont">
          <form @submit.prevent="login" class="contactMe container">
            <label class="text-black">Email:</label>
            <input
              class="form-input neu-border-inset"
              type="email"
              v-model="user_email"
            />
            <label class="text-black">Password:</label>
            <input
              class="form-input neu-border-inset"
              type="password"
              v-model="user_password"
            />

            <div class="submit">
              <button type="Submit" class="mb-3 btn button-body">
                <h5 id="sub" class="text-black mb-0">Login</h5>
              </button>
            </div>
            <div>
              <p class="pb-4">
                Not a member?
                <router-link :to="{ name: 'signup' }"
                  >Create an account</router-link
                >
              </p>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      user_email: "",
      user_password: "",
    };
  },
  methods: {
        login() {
        fetch("", {
        method: "PATCH",
        body: JSON.stringify({
          user_email: this.user_email,
          user_password: this.user_password,
        }),
        headers: {
          "Content-type": "application/json; charset=UTF-8",
        },
      })
        .then((response) => response.json())
        .then((json) => {
          if(json.jwt){
            localStorage.setItem("jwt", json.jwt);
          }
          if(localStorage.getItem("jwt")){
            this.$router.push({ name: "Service" });
          }
          else{
            alert("The Email or Password you entered are Incorrect");
          }
        })
        .catch((err) => {
          alert(err);
        });
    },
  }
};
</script>

<style scoped>
section {
  height: 100vh;
  z-index: 999;
}
form {
  width: 100%;
  margin: 30px auto;
  text-align: left;
  border-radius: 10px;
  background-color: white;
  box-shadow: -10px 13px 20px 9px rgba(220, 220, 220, 0.94);
  -webkit-box-shadow: -10px 13px 20px 9px rgba(220, 220, 220, 0.94);
  -moz-box-shadow: -10px 13px 20px 9px rgba(220, 220, 220, 0.94);
}
.form-cont {
  width: 50%;
}
label {
  color: rgb(0, 0, 0);
  display: inline-block;
  margin: 25px 0 15px;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}
input {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: 1px solid #ddd;
  color: rgb(0, 0, 0);
  background-color: rgba(233, 221, 221, 0.25);
}
.button-body {
  background: rgba(139, 102, 96, 0.924);
  border: 0;
  padding: 10px 20px;
  margin-top: 20px;
  color: rgb(255, 255, 255);
  border-radius: 10px;
  cursor: pointer;
  margin-bottom: 50px !important;
}
button:hover {
  opacity: 0.8;
  background: rgba(10, 81, 139, 0.979);
}
.submit {
  text-align: center;
}
#sub:hover {
  color: rgb(255, 255, 255) !important;
}
#sub {
  color: white;
}
.error {
  color: #ff0062;
  margin-top: 10px;
  font-size: 0.8em;
  font-weight: bold;
}
.contactMe {
  width: 100%;
  margin: 0px;
}
.contact-icons {
  font-size: 20px !important;
}
.formm {
  width: 100%;
  /* margin-top: 70px; */
  justify-content: center;
  align-items: center !important;
  display: flex;
  height: 100vh;
}
.cont {
  display: flex;
  flex-wrap: wrap;
  justify-content: center !important;
}
@media all and (max-width: 991px) {
  .form-cont {
    width: 60%;
  }
  label {
    color: rgb(0, 0, 0);
    display: inline-block;
    margin: 15px 0 15px;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
  }
  input {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: 1px solid #ddd;
    color: rgb(0, 0, 0);
    background-color: rgba(233, 221, 221, 0.25);
  }
  .button-body {
    background: rgba(139, 102, 96, 0.924);
    border: 0;
    padding: 10px 20px;
    margin-top: 20px;
    color: rgb(255, 255, 255);
    border-radius: 10px;
    cursor: pointer;
    margin-bottom: 20px !important;
  }
}
@media all and (max-width: 768px) {
  .form-cont {
    width: 70%;
  }
}
@media all and (max-width: 576px) {
  .form-cont {
    width: 80%;
  }
  .login-title {
    top: 110px;
  }
}
@media all and (max-width: 400px) {
}
</style>