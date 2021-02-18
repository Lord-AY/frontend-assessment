<template>
  <div class="py-5">
    <p class="text-3xl text-gray-700 font-bold">Obinna</p>
    <p class="text-md text-gray-500">
      Good morning, it’s a good day to save 🤑
    </p>

    <div class="grid grid-cols-3 gap-3 my-3">
      <account type="Savings" :amount="2000" />
      <account type="Business" :amount="0" />
      <Investment />
    </div>
    <p class="text-md text-gray-500">Announcement</p>
    <div class="flex flex-col my-3">
      <Announcement detail="Finish your KYC" />
      <Announcement detail="Follow us on our social media platforms" />
      <Announcement detail="Request for a CloudBank mastercard" />
    </div>
    <div class="grid grid-cols-3 gap-3 my-3">
      <div class="col-span-2">
        <Transaction />
      </div>
      <div class="col-span-1 h-full">
        <Breakdown />
      </div>
    </div>
    <div class="grid grid-cols-4 my-6">
      <div class="col-span-4">
        <Statistics />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import account from "@/components/home/account";
import Investment from "@/components/home/investment";
import Announcement from "@/components/home/announcement";
import Transaction from "@/components/home/transaction";
import Breakdown from "@/components/home/breakdown";
import Statistics from '@/components/home/statistics';
export default {
  name: "Home",
  components: {
    account,
    Investment,
    Announcement,
    Transaction,
    Breakdown,
    Statistics,
  },
};
</script>
