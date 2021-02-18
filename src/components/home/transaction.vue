<template>
  <div>
    <div
      style="padding-top: 32px; padding-bottom: 41px"
      class="shadow-sm rounded-md px-4 bg-white h-full"
    >
      <div class="flex justify-between">
        <p class="text-xl text-gray-500 capitalize">Transaction</p>
        <p class="text-sm text-blue-500 capitalize">View all</p>
      </div>
      <div
        class="my-2"
        v-for="(transaction, index) in transactions"
        :key="index"
      >
        <div class="flex flex-col ">
          <p class="text-sm text-gray-500 capitalize block">
            {{ transaction.date }}
          </p>
          <div
            v-for="(trans, index) in transaction.trans"
            :key="index"
            class="flex justify-start items-center w-full bg-white py-4 px-3 mb-3"
          >
            <div>
              <svg
                class="mr-8"
                width="20"
                height="20"
                viewBox="0 0 20 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <circle cx="10" cy="10" r="10" fill="#008080" />
              </svg>
            </div>
            <div
              class="text-gray-900 w-full"
              :class="{ 'border-custom': index < transaction.trans.length - 1 }"
            >
              <div class="flex justify-between">
                <div class="flex flex-col">
                  <p class="text-sm text-gray-500 block">
                    {{ trans.title }}
                  </p>
                  <p class="text-sm text-gray-500 block">
                    {{ trans.purpose }}
                  </p>
                </div>
                <p :class="trans.type == 1 ? 'text-green-500' : 'text-red-500'">
                  &#8358;
                  {{
                    trans.amount.toLocaleString("en-NG", {
                      minimumFractionDigits: 2,
                      maximumFractionDigits: 2,
                    })
                  }}
                </p>
              </div>
            </div>
            <hr />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      transactions: [
        {
          date: "Today",
          trans: [
            {
              title: "Bank Transfer",
              purpose: "Account funding",
              amount: 1000,
              type: 1,
            },
            {
              title: "CB User Transfer",
              purpose: "Account funding",
              amount: 1000,
              type: 1,
            },
          ],
        },
        {
          date: "Yesterday",
          trans: [
            {
              title: "Card",
              purpose: "Account withdrawal",
              amount: 1000,
              type: 2,
            },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.border-custom {
  position: relative;
}
.border-custom:after {
  content: "";
  position: absolute;
  top: 80%;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  height: calc(100% - 12px);
  border-bottom: 1px solid #e0e0e0;
}
</style>