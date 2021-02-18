<template>
  <div class="h-full">
    <div
      style="padding-top: 32px; padding-bottom: 41px"
      class="shadow-sm rounded-md px-4 bg-white h-full"
    >
      <div class="flex justify-between">
        <p class="text-md text-gray-500 capitalize">Breakdown</p>
        <p class="text-sm text-gray-400 capitalize">Yesterday</p>
      </div>
      <div class="flex items-center justify-center pt-8 pb-3">
        <svg
          width="150"
          height="151"
          viewBox="0 0 150 151"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <circle
            cx="75"
            cy="76"
            r="60"
            fill="white"
            stroke="#27AE60"
            stroke-width="30"
          />
          <path
            d="M127 22C116 9.99997 93.5 0.5 75 1.00001L76 31C90 31 102.833 39.6667 107 44.5L127 22Z"
            fill="#DB261B"
          />
        </svg>
      </div>
      <div class="flex flex-col">
        <div class="my-1">
          <p class="text-md text-black-500 capitalize">Total Money Recieved</p>
          <p class="text-green-500">
            &#8358;
            {{
              (2000).toLocaleString("en-NG", {
                minimumFractionDigits: 2,
                maximumFractionDigits: 2,
              })
            }}
          </p>
        </div>

        <div class="my-1">
          <p class="text-md text-black-500 capitalize">Total Money Spent</p>
          <p class="text-red-500">
            &#8358;
            {{
              (900).toLocaleString("en-NG", {
                minimumFractionDigits: 2,
                maximumFractionDigits: 2,
              })
            }}
          </p>
        </div>
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