<template>
    <input v-model="new_todo_content" />
    <button v-on:click="add_todo()" >추가</button>
    
    <div class="todos">
        <div v-for="(todo) in todos" :key="todo.id">
                {{todo.completed}} {{todo.content }}
                <button v-on:click="delete_todo(todo.id)" >삭제</button>
        </div>
    </div>
    <button v-on:click="test_print()">테스트 출력</button>
</template>

<script>
export default {
    name: 'TodoApp',
    data() {
        return {
            todos: [{id: 0, completed: 'false', content: "독서"}],
            new_todo_content: "",
        }
    },
    methods: {
        add_todo() {
            this.todos.push({id: this.todos.length, completed: 'false', content: this.new_todo_content});
            this.new_todos = "";
        },
        delete_todo(id) {
            console.log('delete!');
            console.log(id);
            this.todos.map((ele, index) => {
                console.log(ele.id);
                if(ele.id === id) {
                    this.todos.splice(index, 1)
                }
            })
        },
        test_print() {
            console.log(this.new_todo_content);
        }
    }
}
</script>
