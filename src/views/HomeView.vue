<template>
<div class="w-100 d-flex justify-content-center">
<div class="home mt-5 row container" >
  <div class="col-lg-9">
    <div class="home-content">
   <div class="text-center "><i class="bi icon bi-house-fill"></i><b><span class="text-white notification-subtitle">Home</span></b>
  </div>
<div class="row mt-3">
        <div class="col-md-5 mx-auto">
            <div class="input-group">
                <input class="form-control border-end-0 border bg-transparent text-center" type="search" placeholder="What's on your mind?" id="example-search-input">
                <span class="input-group-append">
                    <button class="btn btn-outline-secondary bg-transparent border-start-0 border ms-n5 type-button" type="button">
                        <i class="bi icon2 bi-pencil-square"></i>
                    </button>
                </span>
            </div>
        </div>
    </div>
    <div class="d-flex">
      
    </div>
    </div>
  </div>
  <div class="col-lg-3">
   <div class="text-center "><i class="bi icon bi-bell-fill"></i><b><span class="text-white notification-subtitle">Notifications</span></b>
  </div>

  </div>
</div>
</div>

</template>

<script>
// @ is an alias to /src
export default {
  name: 'HomeView',
}
</script>
<style scoped>
.home-content{
  
  width: 100%;
  height: 500px;
}
.notifications{
  background-color: rgb(81, 81, 81);
  width: 200px;
  height: 500px;
  margin: auto;
}
/* ICONS */
.icon{
  color: rgb(251, 104, 12);
  font-size: 25px;
}
.icon2{
  color: rgb(251, 104, 12);
}
.notifi-subtitle{
  margin: auto !important;
}
.notification-subtitle{
font-size: 25px;
font-weight: bolder;  
}
.notification-item{
  font-size: 18px;
   padding:5px 0px;
   margin-left: 5px;
}
.notification-content{
  display: flex;
  flex-direction: column;
}
.form-control{
  border-top-left-radius: 20px;
  border-bottom-left-radius: 20px;}
.type-button{
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
}
</style>
