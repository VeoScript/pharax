<template>
  <div class="card ml-32 mr-5 mt-5 px-10 py-5 rounded-xl bg-gray-900">
    <div class="flex items-center justify-between text-white">
      <div class="font-bold text-lg">Order No. <span class="font-black text-lg rounded-full text-yellow-900 px-3 bg-yellow-500 tracking-tight">#{{ order_no }}</span></div>
      <div>Cashier: <span class="font-bold">Lalisa Manoban</span></div>
    </div>
    <div class="flex mt-8 justify-between">
      <form @submit.prevent="" class="w-full">
        <span class="text-white text-sm">Enter Item Code</span>
        <input class="w-full px-5 py-1 mt-1 mb-1 text-lg bg-yellow-400 text-black rounded-lg focus:outline-none" type="text" />
        <span class="text-white text-sm">Enter Quantity</span>
        <div class="flex mt-1 items-center">
          <div class="bg-yellow-400 px-3 py-1 mr-2 w-1/2 font-bold text-sm rounded-md">
            Gatorade
          </div>
          <div class="bg-yellow-400 px-3 py-1 mr-2 w-1/4 font-bold text-sm rounded-md">
            &#8369; 10.00
          </div>
          <div class="flex items-center bg-yellow-400 px-3 py-1 w-1/2 font-bold text-sm rounded-md">
            <button class="minus focus:outline-none">
              <svg class="w-4 h-4 hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 12H4"></path></svg>
            </button>
            <input class="text-sm text-center focus:outline-none bg-yellow-400" type="text" v-model="txtqty" />
            <button class="plus focus:outline-none">
              <svg class="w-4 h-4 hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path></svg>
            </button>
          </div>
        </div>
        <div class="payment mt-5 justify-center">
          <span class="font-bold text-lg text-white">Payment</span>
          <div class="flex">
            <div class="mr-1">
              <span class="text-white text-sm">Amount Pay</span>
              <input class="w-full px-5 py-1 mt-1 mb-1 text-lg bg-yellow-400 text-black rounded-lg focus:outline-none" type="text" />
            </div>
            <div class="ml-1">
              <span class="text-white text-sm text">Change</span>
              <input class="w-full px-5 py-1 mt-1 mb-1 text-lg bg-yellow-400 text-black rounded-lg focus:outline-none" type="text" />
            </div>
          </div>
        </div>
      </form>
      <div class="w-full ml-5">
        <div class="card bg-yellow-400 h-96 p-5 rounded-xl">
          <div class="font-bold mb-5">The Orders</div>
          <div class="flex items-center justify-between px-5 mt-2 text-sm">
            <div class="w-1/2">Product</div>
            <div>Quantity</div>
            <div>Price</div>
            <div>Actions</div>
          </div>
          <div class="overflow-y-auto h-72">
            <div class="mt-1" v-for="(order, i) in orders" :key="i">
            <div class="flex items-center justify-between px-5 py-3 rounded-xl bg-gray-900 text-white text-xs">
              <div class="w-1/2">{{order.item_name}}</div>
              <div>{{ order.qty }}</div>
              <div>&#8369; {{order.item_price}}</div>
              <div>
                <button class="px-3 py-1 text-xs rounded-full"><svg class="w-5 h-5 text-red-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path></svg></button>
              </div>
            </div>
          </div>
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
      order_no: '3201',
      txtqty: '1',
      orders: [
        {
          item_id: '8992112086213',
          item_name: 'Biogesic',
          item_price: '10.00',
          qty: '12'
        },
        {
          item_id: '5000158100510 ',
          item_name: 'Neozep',
          item_price: '10.75',
          qty: '5'
        },
        {
          item_id: '8992112086213',
          item_name: 'Rexidol Forte',
          item_price: '10.25',
          qty: '220'
        },
        {
          item_id: '5000158100510 ',
          item_name: 'Solmux',
          item_price: '12.75',
          qty: '20'
        },
        {
          item_id: '8992112086213',
          item_name: 'Colagate',
          item_price: '20.00',
          qty: '1'
        },
        {
          item_id: '5000158100510 ',
          item_name: 'Green Cross Alcohol',
          item_price: '52.75',
          qty: '2'
        }
      ]
    }
  },
}
</script>
