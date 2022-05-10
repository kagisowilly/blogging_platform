<template>
  <section class="contact-background" id="contact">
    <div class="cont container">
      <div class="formm">
        <div class="form-cont">
                    <div class="sign container">
            <router-link
              to="/signup"
              active-class="active"
              tag="button"
              exact
              class="side-btn"
            >
              <div class="link-container">
                <b>
                  <span class="span">Sign up</span>
                </b>
              </div>
            </router-link>
            <router-link
              to="/login"
              active-class="active"
              tag="button"
              exact
              class="side-btn"
            >
              <div class="link-container">
                <b>
                  <span class="span">Login</span>
                </b>
              </div>
            </router-link>
          </div>
         <hr class="text-white">
          <form @submit.prevent="login" class="contactMe container">
            <label class="text-white">Email:</label>
            <input
              class="form-input neu-border-inset"
              type="email"
              v-model="user_email"
            />
            <label class="text-white">Password:</label>
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
              <p class="pb-4 text-white">
                Not a member?
                <router-link :to="{ name: 'signup' }"
                  >Create an account ?</router-link
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
a{text-decoration: none;
text-decoration: underline;}
hr{margin: 0;}
.sign {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  align-items: center;
  height: 50px;
  column-gap: 30px;
}
section {
  height: 100vh;
  z-index: 999;
}
form {
  width: 100%;
  margin: 30px auto;
  text-align: left;

}
.form-cont {
  width: 50%;
    border-radius: 14px;
    background-color:  rgba(51, 51, 51, 255);
  box-shadow: -2px 13px 20px 9px rgba(251, 104, 12, 0.94);
  -webkit-box-shadow: -2px 13px 20px 9px rgba(251, 104, 12, 0.94);
  -moz-box-shadow: 210px 13px 20px 9px rgba(251, 104, 12, 0.94);
}
label {
  color: rgb(0, 0, 0);
  display: inline-block;
  margin: 25px 0 15px;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;

}
.side-btn.active {
  position: relative;
  color: rgba(251, 104, 12, 0.94) !important;
  font-weight: 600;
}
.side-btn {
  color: rgba(255, 255, 255, 0.94) !important;
}
input {
  border-radius: 30px;
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: 1px solid #ddd;
  color: rgb(0, 0, 0);
  background-color: rgb(255, 255, 255);
}
.button-body {
  background: rgb(251, 104, 12);
  border: 0;
  padding: 10px 20px;
  margin-top: 20px;
  color: rgb(255, 255, 255);
  border-radius: 20px;
  cursor: pointer;
  margin-bottom: 50px !important;
}
button:hover {
  opacity: 0.8;
  background: rgba(251, 252, 253, 0.979);
}
.submit {
  text-align: start;
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
  }
  .button-body {
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