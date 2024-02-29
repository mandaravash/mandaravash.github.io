<script>
export default {
  // 放變數的地方
  data() {
    return {
      count: 1,
      color: 'bg-blue-500',
      password: 'password',
      showPassword: false,
    };
  },
  methods: {
    addCount() {
      this.count = this.count++;
    },
    changeColor() {
      this.color = 'bg-red-500';
    },
    changeDisplay() {
      this.showPassword = !this.showPassword;
      // if (this.password === 'password') {
      //   this.password = 'text';
      // } else {
      //   this.password = 'password';
      // }
    }
  },
};
</script>

<template>
  <div class="flex flex-col gap-y-2">
    <h1 class="text-8xl font-bold">{{ count }}</h1>
    <button type="button" v-on:click="count++">plus</button>

    <br>
    <button type="button" @click="changeColor()">changecolor</button>
    <div class="w-[100px] h-[100px] text-2xl" :class="color"></div>
    {{ color === 'bg-blue-500' ? 'blue' : 'red' }}
  </div>

  <br>
  <button type="button" class="border border-white" @click="changeDisplay()">顯示/關閉密碼</button>
  <br>
  <input :type="showPassword? 'text' : 'password'" class="text-black">
  <div></div>

</template>

<style scoped></style>
