<template>
  <div class="card ml-32 shadow-xl mr-5 mt-5 rounded-xl bg-yellow-400">
    <div class="machine px-5 py-5">
      <div class="w-full">
        <input class="w-full px-5 py-3 mt-1 mb-1 text-sm ring-4 ring-yellow-600 bg-gray-100 text-black rounded-lg focus:outline-none" type="text" placeholder="Enter Item Code" />
      </div>
      <div class="flex">
        <table class="table-auto mt-5 w-full ring-4 ring-yellow-600 rounded-lg">
          <thead class="text-left ml-20">
            <tr class="h-14 border-b-4 border-yellow-600">
              <th class="px-5 py-3">Product</th>
              <th class="px-5 py-3">Quantity</th>
              <th class="px-5 py-3">Price</th>
              <th class="px-5 py-3">Actions</th>
            </tr>
          </thead>
          <tbody v-for="(order, i) in orders" :key="i">
            <tr class="bg-yellow-300 font-medium border-b-2 border-yellow-600 hover:bg-yellow-400">
              <td class="px-5 py-3">{{ order.item_name }}</td>
              <td class="px-5 py-3 text-left">{{ order.qty }}</td>
              <td class="px-5 py-3">&#8369; {{ order.item_price }}</td>
              <td class="px-5">
                <button class="px-3 py-1 text-xs text-white bg-red-600 rounded-full focus:outline-none">Delete</button>
              </td>
            </tr>
          </tbody>
          <tfooter>
            <div class="flex items-center px-5 py-2">
              <div class="text-xs">Pharax &copy; {{ new Date().getFullYear() }}. VEOSCRIPT</div>
            </div>
          </tfooter>
        </table>
        <div class="paymentcard ml-5 mt-5 px-5 py-3 w-full ring-4 ring-yellow-600 bg-yellow-400 rounded-lg">
          <div class="font-bold">Payment</div>
          <div class="flex space-x-4">
            <div class="w-full mt-5">
              <span>Total Amount</span>
              <input class="w-full rounded-xl px-3 py-3 font-bold tracking-wider text-right text-3xl focus:outline-none" type="text" v-model="totalamount" disabled />
            </div>
            <div class="w-full mt-5">
              <span>Changed</span>
              <input class="w-full rounded-xl px-3 py-3 font-bold tracking-wider text-right text-3xl focus:outline-none" type="text" v-model="totalchange" disabled />
            </div>
          </div>
          <div class="flex">
            <div class="w-full mt-5">
              <input class="w-full rounded-xl px-3 py-3 text-right text-2xl focus:outline-none" type="text" placeholder="Amount Pay" v-model="amountpay" />
            </div>
          </div>
          <div class="flex">
            <div class="flex w-full mt-5 justify-end space-x-2">
              <button class="bg-red-600 px-5 py-2 rounded-xl text-white focus:outline-none">Cancel Transaction</button>
              <button class="bg-gray-900 px-5 py-2 rounded-xl text-white focus:outline-none">Save Transaction</button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="h-5 bg-gray-100"></div>
 </div>
</template>

<script>
export default {
  data() {
    return {
      order_no: '3201',
      txtqty: '1',
      totalamount: '500.75',
      orders: [
        {
          item_id: '8992112086213',
          item_name: 'Biogesic',
          item_price: '10.00',
          qty: '15'
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
          qty: '20'
        },
        {
          item_id: '5000158100510 ',
          item_name: 'Solmux',
          item_price: '12.75',
          qty: '12'
        },
        {
          item_id: '8992112086213',
          item_name: 'Colgate',
          item_price: '20.00',
          qty: '1'
        },
        {
          item_id: '5000158100510 ',
          item_name: 'Green Cross Alcohol',
          item_price: '52.75',
          qty: '2'
        },
        {
          item_id: '5000158100510 ',
          item_name: 'Gatorade',
          item_price: '30.50',
          qty: '3'
        },
        {
          item_id: '5000158100510 ',
          item_name: 'Safeguard',
          item_price: '20.75',
          qty: '2'
        }
      ]
    }
  },
}
</script>
