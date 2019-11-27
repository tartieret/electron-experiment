<template>
    <div>
        <h1>Todo list</h1>
        <ol class="list-group">
            <li
                v-for="(item, index) in items"
                :key="index"
                class="list-group-item"
                @click="changeStatus(index)"
            >{{ item.name }}</li>
        </ol>
    </div>
</template>

<script>
export default {
  name: 'Todolist',
  data() {
    return {
      items: [{ name: 'task 1', done: false }],
    };
  },
  methods: {
    changeStatus(index) {
      this.items[index].done = !this.items[index].done;
    },
  },
};
</script>

<style scoped>
.done {
}
</style>