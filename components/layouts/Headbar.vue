<template>
  <div class="flex ml-32 mr-10 pt-5">
    <div class="card shadow-lg flex w-full bg-yellow-500 px-10 py-5 rounded-xl">
      <div class="flex-auto text-white">
        <div class="text-4xl font-medium">Hello, Lalisa!</div>
        <div class="mt-1 ml-1 text-lg">Welcome back to Pharax</div>
      </div>
      <div class="clock flex-col items-center">
        <div class="time text-4xl font-bold text-gray-800">{{ hours }}{{ minutes }}{{ sec }}&nbsp;{{ ampm }}</div>
        <div class="date mt-1 text-right text-gray-800"><span v-for="(day, i) in days" :key="i" class="capitalize font-bold" :class="{hidden:day.active}">{{ day.text }},</span> {{ month }} {{ date }}, {{ year }}</div>
      </div>
    </div>
    <div class="card flex w-full justify-end px-10 py-5 rounded-full">
      <div class="flex text-white items-center">
        <div class="text-4xl font-medium">
          <svg class="w-9 h-9 hover:text-yellow-500 text-yellow-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"></path></svg>          </div>
        <div class="text-4xl font-medium">
          <svg class="w-9 h-9 mx-5 hover:text-yellow-500 text-yellow-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
        </div>
        <div class="mt-2 ml-1 text-lg">
          <nuxt-link to="/">
            <img class="h-14 w-14 transform hover:scale-95 ring-4 ring-yellow-300 rounded-full" src="https://pbs.twimg.com/media/ExakeKmVgAUgkft?format=jpg&name=large" alt="profile_picture">
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      days: [
        {text:"sun", active: true},
        {text:"mon", active: true},
        {text:"tue", active: true},
        {text:"wed", active: true},
        {text:"thu", active: true},
        {text:"fri", active: true},
        {text:"sat", active: true}
      ],
      months: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
      ampm:'',
      hours: '',
      minutes:'',
      sec: '' ,
      month:'',
      date: '',
      year: ''
    }
  },
  methods:{
    startClock(){
      var THIS = this;

      setInterval(() => {
        var a = new Date().getTime() / 1e3,
            b = new Date,
            c = b.getHours(),
            d = b.getMinutes(),
            e = b.getSeconds(),
            f = b.getMilliseconds(),
            g = f.toString().slice(0, -2),
            h = b.getDay(),
            i = 12 <= c ? 'PM' : 'AM',
            j = b.getMonth(),
            k = b.getDate(),
            l = b.getFullYear();
        THIS.$data.ampm = i;
          12 < c && (c %= 12), 
          0 == c && (c = 12), 
          9 >= e && (e = '0' + e), 
          9 >= d && (d = '0' + d), 
          THIS.$data.hours = c, 
          THIS.$data.minutes = `:${d}:`, 
          THIS.$data.sec = e, 
          THIS.$data.month = THIS.$data.months[j], 
          THIS.$data.date = k, 
          THIS.$data.year = l;
          THIS.$data.days[h].active = false;
    }, 100)
    }
  },
  created() {
    this.startClock();
  }
}
</script>
