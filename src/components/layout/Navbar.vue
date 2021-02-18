<template>
  <div>
    <div
      class="flex fixed w-full z-50 top-0 items-center justify-between bg-white px-4 py-3 shadow-md"
    >
      <div class="w-10/12 flex items-center justify-between mx-auto">
        <div class="flex">
          <router-link :to="{ name: 'Home' }" class="flex">
            <img
              src="@/assets/images/cloudbank 1.png"
              alt=""
              class="h-auto w-24"
            />
          </router-link>
        </div>

        <div class="flex space-x-2 items-center">
          <img
            src="https://thumbs.dreamstime.com/b/default-avatar-profile-image-vector-social-media-user-icon-potrait-182347582.jpg"
            alt=""
            class="h-12 w-auto mr-2"
          />
          Ezekwesili Obinna
        </div>
      </div>
    </div>
  </div>
</template>