<template>
  <div class="sidebar">
    <div class="title text-center">
     <img class="logo" src="@/assets/logo-modified.png" alt="logo"><b><span class="span">Website</span> </b>
    </div>
    <div class="menu-items">
      <router-link
        to="/"
        active-class="active"
        tag="button"
        exact
        class="side-btn"
      >
        <div class="link-container">
          <i class="bi bi-house-door-fill"></i
          ><span class="text-white span">Home </span>
        </div>
      </router-link>
      <router-link
        to="/search"
        active-class="active"
        tag="button"
        exact
        class="side-btn"
      >
        <div class="link-container">
          <b
            ><i class="bi bi-search"></i><span class="text-white span">Search</span>
          </b>
        </div>
      </router-link>
      <router-link
        to="/favourites"
        active-class="active"
        tag="button"
        exact
        class="side-btn"
      >
        <div class="link-container">
          <b
            ><i class="bi bi-star-fill"></i
            ><span class="text-white span">Favourites</span>
          </b>
        </div>
      </router-link>
      <router-link
        to="/profile"
        active-class="active"
        tag="button"
        exact
        class="side-btn"
      >
        <div class="link-container">
          <b
            ><i class="bi bi-person-circle"></i
            ><span class="text-white span">Profile</span>
          </b>
        </div>
      </router-link>
      <router-link
        to="/explore"
        active-class="active"
        tag="button"
        exact
        class="side-btn"
      >
        <div class="link-container">
          <b
            ><i class="bi bi-vector-pen"></i
            ><span class="text-white span">Explore</span>
          </b>
        </div>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
    
};
</script>
<style scoped>
a {
  text-decoration: no;
}
.title {
  color: rgb(255, 255, 255);
  font-size: 30px;
  margin-top: 10px;
  font-weight: 1000;
}
.menu-items {
  display: flex;
  flex-direction: column;
  margin-top: 40px;
  padding-left: 40px;
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
.side-btn:focus {
  outline: none;
}
.side-btn.active {
  position: relative;
  color: white;
  font-weight: 600;
}
a {
  text-decoration: none;
}
.span {
  margin-left: 10px;
}

.logo{
    width: 40px;
}
@media all and (max-width: 991px) {
  .menu-items {
    margin-top: 40px;
    padding-left: 20px;
  }
}
@media all and (max-width: 600px) {
.span {
  display: none;
}
.menu-items {
padding-left: 20px;
  }
  .side-btn {
  font-size: 25px;
}
}
</style>
