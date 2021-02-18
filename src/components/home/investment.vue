<template>
  <div>
    <div
      style="padding-top: 20px; padding-bottom: 10px"
      class="shadow-sm rounded-md px-4 bg-white h-full"
    >
      <div class="flex justify-between">
        <p class="text-md text-gray-500 capitalize">Investment</p>
        <p class="text-md text-blue-500 capitalize">0229238715</p>
      </div>
      <div class="flex items-center justify-center py-2">
        <span class="text-gray-500 text-lg pr-1">&#8358;</span>
        <p class="text-3xl text-gray-700 font-semibold">
          {{ amount[0] }}<span class="text-sm">.{{ amount[1] }}</span>
        </p>
      </div>
      <div class="flex justify-between">
        <p class="text-md text-blue-500 capitalize">8.18%</p>
        <p class="text-md text-gray-500 capitalize">
          {{ new Date(Date.now()).toLocaleString().split(",")[0] }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    type: String,
  },

  data() {
    return {
      amount: (+10000.98)
        .toLocaleString("en-NG", {
          minimumFractionDigits: 2,
          maximumFractionDigits: 2,
        })
        .toString()
        .split("."),
    };
  },
};
</script>