<template>
  <nav>
<div class="sign container-fluid">
          <div class="text-center d-flex">
          <i class="bi noti-ico icon bi-bell-fill"></i
          ><b
            >
            </b
          >
        </div>
      <router-link
        to="/signup"
        active-class="active"
        tag="button"
        exact
        class="side-btn"
      >
        <div class="link-container">
          <b
            > <span class="text-white span">Sign up</span> <i class="bi bi-person-plus-fill"></i>
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
          <b
            > <span class="text-white span">Login</span> <i class="bi bi-box-arrow-in-right"></i>
          </b>
        </div>
      </router-link>    
</div>
  </nav>
</template>

<script>
export default {

}
</script>

<style scoped>
.icon {
  color: rgb(251, 104, 12);
  font-size: 18px;
}
.icon2 {
  color: rgb(251, 104, 12);
}

nav{
    height: 50px;
    border-bottom: solid 2px rgb(230, 230, 230);
}
.sign{
    display: flex;
    flex-wrap: wrap;
    justify-content:flex-end ;
    align-items: center;
    height: 50px;
    column-gap:30px ;
}
a {
  text-decoration: none;
}
.side-btn {
  border: none;
  padding: 16px 0px;
  cursor: pointer;
  font-size: 18px;
  font-weight: 500;
  color: rgb(251, 104, 12);
  background-color: transparent;
}
.side-btn.active {
  position: relative;
  color: white;
  font-weight: 600;
}
@media all and (min-width:431px) {
.noti-ico{
  display: none !important;
}
}
</style>