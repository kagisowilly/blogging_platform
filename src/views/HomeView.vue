<template>
<Navbar />
  <div class="w-100 home d-flex justify-content-center">
    <div class="mt-5 row container">
      <div class="col-11">
        <div class="home-content">
          <div class="text-center">
            <i class="bi icon bi-house-fill"></i
            ><b><span class="text-white notification-subtitle">Home</span></b>
          </div>
          <div class="row mt-3">
            <div class="col-md-5 mx-auto">
              <div class="input-group">
                <input
                  class="form-control border-end-0 border bg-transparent text-center"
                  type="search"
                  placeholder="What's on your mind?"
                  id="example-search-input"
                />
                <span class="input-group-append">
                  <button
                    class="btn btn-outline-secondary bg-transparent border-start-0 border ms-n5 type-button"
                    type="button"
                  >
                    <i class="bi icon2 bi-pencil-square"></i>
                  </button>
                </span>
              </div>
              <div class="d-flex my-2 text-white">
                <i class="bi bi-images"></i>
                <i class="bi mx-5 bi-filetype-gif"></i>
                <i class="bi bi-emoji-smile"></i>
              </div>
            </div>
          </div>

          <div class="card-bg d-flex justify-content-center">
            <div class="card mb-3">
              <h5 class="card-title text-white my-2">Card title</h5>
              <img
                src="https://images.pexels.com/photos/247399/pexels-photo-247399.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
                class="card-img-top"
                alt="..."
              />
              <div class="card-body">
                <h5 class="card-title text-white">Card title</h5>
                <p class="card-text text-white">
                  This is a wider card with supporting text below as a natural
                  lead-in to additional content. This content is a little bit
                  longer.
                </p>
              </div>
            </div>
          </div>
         <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab harum
          illum omnis sint mollitia illo, ducimus magnam. Voluptatibus
          necessitatibus quisquam eveniet illo ab, fugit nemo, ex porro cumque
          nam magni amet rerum optio itaque, fuga suscipit asperiores. Odio
          soluta voluptate optio, maxime distinctio praesentium aut molestiae
          totam, veritatis modi a. Modi optio voluptates ab, corrupti impedit,
          inventore, tenetur dolores doloremque asperiores necessitatibus quo?
          Repellat, assumenda. In sequi omnis facilis? Consequatur obcaecati
          iure ut ab ducimus reiciendis exercitationem suscipit eveniet, magni
          unde repudiandae aliquam aut vel eaque mollitia molestias labore
          deleniti? Quae non ea voluptate, sint molestiae exercitationem sunt
          accusamus veritatis officia iste odio et! Perspiciatis exercitationem
          ad eius laborum id, earum iure odit necessitatibus fugit fugiat! Harum
          sunt ipsum, inventore placeat possimus nulla iste. Praesentium quidem
          voluptatem expedita minus repellat asperiores aliquam odio unde
          labore, doloribus totam magni inventore. Accusamus velit dolor,
          necessitatibus totam qui ea delectus minima suscipit nostrum
          voluptatem sed animi, nobis ab? Modi a provident saepe veniam eligendi
          ad velit est maiores voluptates consequuntur vero quibusdam dicta
          molestias iste impedit, repudiandae non fuga vel illo! Nam architecto
          eum molestiae, explicabo quo autem non aut illum eligendi labore quos
          accusamus eaque dolorum ipsa ipsum accusantium provident ea quibusdam
          id. Laborum sunt dolores saepe dolor. Quibusdam illum debitis,
          architecto neque est reprehenderit nesciunt laboriosam animi
          voluptatem quisquam ipsum. Delectus ipsa animi at laudantium
          architecto doloremque omnis quidem incidunt sit consectetur dolorem
          excepturi pariatur libero minus quis, hic voluptatem in cupiditate quo
          eius consequuntur! Aut illum, sint ad qui fugiat beatae quae totam
          provident fuga facilis animi velit assumenda accusamus ullam?
          Temporibus exercitationem nobis accusamus. Officia, aut, optio
          cupiditate quibusdam itaque odit sed ducimus nesciunt aliquid beatae
          dignissimos molestiae commodi esse veniam omnis laudantium illum
          eveniet excepturi ipsum veritatis. Repellendus praesentium, totam
          optio dicta quaerat eius? Iste beatae, quos qui provident cum ipsum
          sed fugit ipsam illo nobis aspernatur cumque nesciunt rem et
          architecto ducimus id repellat nulla, sit modi! Quia ipsam accusantium
          eaque numquam. Dolores totam consequuntur quasi eum aut, mollitia sint
          asperiores! Tempora consectetur nisi accusantium voluptas, odit porro
          exercitationem soluta laborum at quis. Modi illo vel est omnis
          corporis incidunt, optio laborum? Quam repudiandae adipisci architecto
          accusantium rem dolore consequuntur! Iusto error dolore neque odio
          dolorem provident alias sed, necessitatibus beatae in labore, ratione
          aliquam eveniet delectus modi quos repellendus nisi molestias id
          laboriosam maiores consectetur quod? Voluptates reprehenderit ullam
          optio beatae qui quam cum consequuntur quibusdam animi fuga
          repudiandae unde impedit corporis quis numquam doloribus quas, nemo
          quos corrupti assumenda aut. Cumque praesentium itaque veniam ea,
          provident voluptatibus cupiditate iste fugiat nobis perferendis quo
          beatae consequatur temporibus nulla sed, amet nostrum impedit fugit
          recusandae ducimus similique voluptate alias. Beatae esse aliquam
          dolores unde fuga nostrum ut optio eveniet, quae qui labore eum
          commodi reprehenderit. Fugit dolore laborum sapiente, non soluta rem
          quia velit tenetur perferendis beatae libero, illum id earum eos! Cum
          nesciunt possimus similique unde dolorum molestiae ut quos, magni
          porro ea recusandae labore quia delectus rem pariatur. Ullam, laborum
          ex beatae modi quaerat iusto!</p> 
        </div>
      </div>
      <div class="col-1">
        <div class="text-center d-flex">
          <i class="bi noti-ico icon bi-bell-fill"></i
          ><b
            ><span class="text-white notification-subtitle2 notification-subtitle"
              >Notifications</span
            ></b
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
// @ is an alias to /src
export default {
  name: "HomeView",
  components:
  {Navbar}
};
</script>
<style scoped>
.home {
  overflow-x: hidden;
  overflow-y: auto;
  min-height: 100%;
}
.card-bg {
  background-color: rgb(81, 81, 81);
  width: 80%;
  margin: auto;
}
.card {
  width: 60%;
  background-color: rgb(81, 81, 81);
  border: none;
}
img {
  width: 100%;
}
.home-content {
  width: 100%;
  height: 500px;
}
.notifications {
  width: 200px;
  height: 500px;
  margin: auto;
}
/* ICONS */
.icon {
  color: rgb(251, 104, 12);
  font-size: 25px;
}
.icon2 {
  color: rgb(251, 104, 12);
}
.notifi-subtitle {
  margin: auto !important;
}
.notification-subtitle2 {
  font-size: 25px;
  font-weight: bolder;
  display: none;
}
.notification-item {
  font-size: 18px;
  padding: 5px 0px;
  margin-left: 5px;
}
.notification-content {
  display: flex;
  flex-direction: column;
}
.form-control {
  border-top-left-radius: 20px;
  border-bottom-left-radius: 20px;
}
.type-button {
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
}
@media all and (max-width:992px) {
  .card {
  width: 80%;
  background-color: rgb(81, 81, 81);
}
.card-bg {
  background-color: rgb(81, 81, 81);
  width: 90%;
  margin: auto;
}
}
@media all and (max-width:767px) {
    .card {
  width: 90%;
  background-color: rgb(81, 81, 81);
  
}
.card-bg {
  background-color: rgb(81, 81, 81);
  width: 95%;
  margin: auto;
}
.notification-subtitle{
  display: none !important;
}
}
@media all and (max-width:576px) {
   .card {
  width: 100%;
  background-color: rgb(81, 81, 81);
}
.card-bg {
  background-color: rgb(81, 81, 81);
  width: 100%;
  margin: auto;
} 
}
@media all and (max-width:430px) {
.noti-ico{
  display: none !important;
}
}
</style>
