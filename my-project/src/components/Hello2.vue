<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links 2</h2>
    <ul>
    <li v-for="todo in todos">
      {{ todo.text }}
    </li>
    <br>
    </ul>
     <h2>Ecosystem2</h2>
    <ul>
     <input type="text" autocomplete="off" :placeholder="123"  @focus="selectAll"></input>
    </ul>
      <div v-if="isDomReady"><span>测试 computed 当Dom加载完成自动运行 computed方法，相当于ready</span></div>
  </div>

</template>

<script>
export default {
  name: 'hello2',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App 2th page',
      todos: [
      { text: '学习 JavaScript' },
      { text: '学习 Vue' },
      { text: '整个牛项目' }
    ]
    }
  },
  methods: {
    selectAll(){
      alert('aaa')
      debugger
      return null
    }
  },
  computed:{
    isDomReady(){
      debugger
      return true
    }
  }
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
