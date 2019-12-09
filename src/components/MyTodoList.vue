<template>
    <div>
        <h1>{{title1}}</h1>

        <ul id="all-tasks">
            <li v-for="task in tasks" v-bind:key="task.description">{{ task.description }}</li>
        </ul>

        <h1>{{title2}}</h1>

        <ul id="completed-tasks">
            <li v-for="task in completedTasks" v-bind:key="task.description" v-on:click="task.completed = false">{{ task.description }}</li> 
        </ul>

        <h1>{{title3}}</h1>

        <ul id="not-completed-tasks">
            <li v-for="task in incompleteTasks" v-bind:key="task.description" v-on:click="task.completed = true">{{ task.description }}</li>
        </ul>

        <label for="taskDesc">New task</label>
        <input name="taskDesc" id="newTaskDesc" v-model="newTodo" type="text">

        <button class="btn btn-primary" v-on:click="addNewTodo">Add new task</button>
        </div>
</template>

<script>
export default {
    data() {
        return {
            title1: 'All tasks',
                title2: 'Completed tasks',
                title3: 'Tasks to be completed',
                newTodo: '',
                tasks: [
                    { description: 'Go to the store', completed: true },

                    { description: 'Watch some Youtube', completed: false },

                    { description: 'Drink some coffee', completed: true },

                    { description: 'Clear inbox', completed: false },

                    { description: 'Learn Vue.js', completed: false }
                ]
        }
    },
    methods: {
        addNewTodo: function () {
            this.tasks.push({
                description: this.newTodo,
                completed: false
            })
            this.newTodo = ''
        }
    },
    computed: {
        incompleteTasks() {
            return this.tasks.filter(task => ! task.completed);  
            },
        completedTasks() {
            return this.tasks.filter(task => task.completed);
        }
        },
}
</script>

<style scoped>
    ul {
        padding: 0px;
    }
    li {
        list-style: none;
    }
</style>