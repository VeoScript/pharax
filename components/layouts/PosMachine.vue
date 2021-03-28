<template>
  <div class="card ml-32 mr-5 mt-5 px-10 py-5 rounded-xl bg-gray-900">
    <div class="flex items-center justify-between text-white">
      <div class="font-bold text-lg">Order No. <span class="font-black text-lg rounded-full text-yellow-900 px-3 bg-yellow-500 tracking-tight">#{{ order_no }}</span></div>
      <div>Cashier: <span class="font-bold">Lalisa Manoban</span></div>
    </div>
    <div class="flex mt-8 justify-between">
      <div class="w-full">
        <input class="w-full px-5 py-3 bg-gray-100 rounded-xl focus:outline-none" type="text" placeholder="Enter item code..." />
      </div>
      <div class="w-full ml-5">
        <div class="card bg-gray-700 p-5 rounded-xl">
          <div class="text-white font-bold mb-5">Queued Orders</div>
          <div class="flex items-center justify-between px-5 mt-2 text-sm text-white">
            <div>Product</div>
            <div>Price</div>
            <div>Actions</div>
          </div>
          <div class="mt-1" v-for="(order, i) in orders" :key="i">
            <div class="flex items-center justify-between px-5 py-3 rounded-xl bg-gray-900 text-white text-xs">
              <div>{{order.item_name}}</div>
              <div>&#8369; {{order.item_price}}</div>
              <div>
                <button class="px-3 py-1 text-xs rounded-full bg-red-600 hover:bg-red-500">Delete</button>
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
      orders: [
        {
          item_id: '8992112086213',
          item_name: 'Biogesic',
          item_price: '10.00'
        },
        {
          item_id: '5000158100510 ',
          item_name: 'Strepsils',
          item_price: '52.75'
        }
      ]
    }
  },
}
</script>
