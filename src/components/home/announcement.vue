<template>
  <div>
    <div
      class="flex justify-start w-full bg-white shadow-sm rounded-md py-4 px-3 mb-3"
    >
      <div>
        <svg
          class="mr-3"
          width="25"
          height="25"
          viewBox="0 0 25 25"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <circle
            cx="12.5"
            cy="12.5"
            r="11.5"
            fill="white"
            stroke="#008080"
            stroke-width="2"
          />
        </svg>
      </div>
      <div class="text-gray-900">{{ detail }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    detail: String,
  },
};
</script>