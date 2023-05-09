<template>
    <div id="app" class="container">
    <h1>Daftar Kegiatan</h1>
    <form id="todo-form" @submit.prevent="addTodo">
      <input type="text" id="todo-input" placeholder="Tambahkan kegiatan baru" v-model="newTodo">
      <button type="submit" id="todo-submit">Tambah Kegiatan</button>
    </form>
    <ul id="todo-list">
      <li v-for="(todo, index) in todos" :key="index">
        <input type="checkbox" :checked="todo.done" @change="toggleDone(index)">
        <span :class="{ done: todo.done }">{{ todo.text }}</span>
        <button @click="deleteTodo(index)">Hapus</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
    data() {
    return {
      newTodo: '',
      todos: [],
    }
  },
  methods: {
    addTodo() {
      if (this.newTodo.trim() !== '') {
        this.todos.push({
          text: this.newTodo,
          done: false,
        });
        this.newTodo = '';
      }
    },
    toggleDone(index) {
      this.todos[index].done = !this.todos[index].done;
    },
    deleteTodo(index) {
      this.todos.splice(index, 1);
    },
  },
  computed: {
    doneTodos() {
      return this.todos.filter(todo => todo.done);
    },
    undoneTodos() {
      return this.todos.filter(todo => !todo.done);
    },
  },
}
</script>

<style>
.container {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #FFF;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1 {
  text-align: center;
  margin-bottom: 30px;
  color: #1abc9c;
}

ul {
  list-style-type: none;
  margin-bottom: 30px;
}

li {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}

input[type="checkbox"] {
  margin-right: 10px;
  cursor: pointer;
}

.done {
  text-decoration: line-through;
}

input[type="text"] {
  padding: 10px;
  border: none;
  border-radius: 5px;
  margin-right: 10px;
  font-size: 16px;
  color: #333;
  background-color: #FFF;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
  width: 70%;
}

button[type="submit"],
button {
  padding: 10px;
  border: none;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
}

button[type="submit"] {
  background: linear-gradient(135deg, #1abc9c, #16a085);
  color: #FFF;
  width: 30%;
}

button[type="submit"]:hover {
  background: linear-gradient(135deg, #16a085, #1abc9c);
}

button {
  background-color: #FFF;
  color: #333;
  border: 1px solid #1abc9c;
}

button:hover {
  background: linear-gradient(135deg, #16a085, #1abc9c);
  color: #FFF;
  border: 1px solid #16a085;
}
</style>