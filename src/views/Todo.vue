<template>
  <div class="home">

    <field-add-task />

    <list-tasks
      v-if="$store.state.tasks.length"
    />

    <no-task
      v-else
    />

  </div>
</template>

<script>
export default {
  name: 'Todo',
  data() {
    return {
      newTaskTitle: '',
    }
  },
  components: {
    'field-add-task': require('@/components/Todo/FieldAddTask.vue').default,
    'list-tasks': require('@/components/Todo/ListTasks.vue').default,
    'no-task': require('@/components/Todo/NoTask.vue').default
  }
}
</script>