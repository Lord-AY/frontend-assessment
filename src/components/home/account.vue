<template>
  <div>
    <div
      style="padding-top: 31px; padding-bottom: 31px"
      class="shadow-sm rounded-md px-4 bg-white h-full"
    >
      <p class="text-md text-gray-500 capitalize">{{ type }} Account</p>
      <div class="flex items-center py-2">
        <span class="text-gray-500 text-lg pr-1">&#8358;</span>
        <p class="text-3xl text-gray-700 font-semibold">
          {{
            (+amount).toLocaleString("en-NG", {
              minimumFractionDigits: 2,
              maximumFractionDigits: 2,
            })
          }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    type: String,
    amount: Number,
  },
};
</script>