<template>
  <div class="hello">
<<<<<<< HEAD
    <h1 v-text="msg"></h1>
    <input v-model="newItem" v-on:keyup.enter="addNew">
    <ul>
      <li v-for="item in items"
          v-bind:class="{finished:item.isFinished}" v-on:click="toggleFinished(item)">
        {{item.label}}
      </li>
    </ul>
=======
    <h1>{{ msg }}</h1>
>>>>>>> 888f5d30fbd3dda76054d7a541e46c206bbf3d95
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
<<<<<<< HEAD
      msg: 'Hello World',
      items: [
        {
          label: 'coding',
          isFinished: true
        },
        {
          label: 'walking',
          isFinished: true
        },
        {
          label: 'eating',
          isFinished: true
        }
      ]
    }
  },
  methods: {
    getMessage () {
      this.$http.get('message').then(r => {
        this.msg = r.data.message
      })
    },
    toggleFinished: function (item) {
      item.isFinished = !item.isFinished
    },
    addNew: function () {
      this.items.push({
        label: this.newItem,
        isFinished: true
      })
      this.newItem = ''
    }
=======
      msg: 'App-manager'
    }
  },
  methods: {
>>>>>>> 888f5d30fbd3dda76054d7a541e46c206bbf3d95
  }
}
</script>

<style scoped>
.finished{
  color: #2ab27b;
  font-size: 30px;
}
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {

  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
