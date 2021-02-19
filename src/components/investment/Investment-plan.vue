<template>
  <div class="rounded-2xl">
    <div
      style="background: #008080"
      class="pt-6 flex flex-col items-center rounded-t-xl"
    >
      <p class="text-white">{{ type }}</p>
      <p class="text-white text-4xl pb-2">
        {{ interest }}
        <span class="text-2xl">% P/A</span>
      </p>
      <p class="text-white">{{ days }}</p>
      <svg
        viewBox="0 0 500 150"
        preserveAspectRatio="none"
        style="height: 100%; width: 100%"
      >
        <path
          d="M-2.03,149.30 C0.23,-4.64 504.74,132.53 502.48,3.26 L503.05,150.29 L-2.03,150.29 Z"
          style="stroke: none; fill: #fff"
        ></path>
      </svg>
    </div>
    <div class="bg-white flex flex-col items-center rounded-b-xl pb-6">
      <p class="my-2 text-gray-400">
        <span class="mr-2"
          ><svg
            class="inline"
            width="10"
            height="8"
            viewBox="0 0 10 8"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M10 1.43589L3.58975 7.84614L0 4.28205L1.46156 2.84616L3.58975 4.94874L8.53849 0L10 1.43589Z"
              fill="#3BB54A"
            />
          </svg> </span
        >Automatically Renewable
      </p>
      <p class="my-2 text-gray-400">
        <span class="mr-2"
          ><svg
            class="inline"
            width="10"
            height="8"
            viewBox="0 0 10 8"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M10 1.43589L3.58975 7.84614L0 4.28205L1.46156 2.84616L3.58975 4.94874L8.53849 0L10 1.43589Z"
              fill="#3BB54A"
            />
          </svg> </span
        >Automatically Renewal Options
      </p>
      <p class="my-2 text-gray-400">
        <span class="mr-2"
          ><svg
            class="inline"
            width="10"
            height="8"
            viewBox="0 0 10 8"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M10 1.43589L3.58975 7.84614L0 4.28205L1.46156 2.84616L3.58975 4.94874L8.53849 0L10 1.43589Z"
              fill="#3BB54A"
            />
          </svg> </span
        >Cancel Renewal Anytime
      </p>
      <p class="my-2 text-gray-400">
        <span
          ><svg
            class="inline"
            width="10"
            height="8"
            viewBox="0 0 10 8"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M10 1.43589L3.58975 7.84614L0 4.28205L1.46156 2.84616L3.58975 4.94874L8.53849 0L10 1.43589Z"
              fill="#3BB54A"
            />
          </svg> </span
        >Fast Automated Payout
      </p>
      <button
        style="background: rgba(0, 128, 128, 1);"
        class="my-2 text-white w-3/5 rounded-md text-center tracking-wide px-4 py-3"
      >
        Make Investment
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    type: String,
    interest: Number,
    days: Number,
  },
};
</script>