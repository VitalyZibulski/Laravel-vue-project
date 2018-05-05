<template>
    <div id="app-component">
        <table class="table">
            <thead>
            <tr>
                <th>Task Ttitle</th>
                <th>Priority</th>
                <th>Action</th>
            </tr>
            </thead>
            <tbody>
            <task-component v-for="task in tasks" :key="task.id" :task="task"></task-component>
            <tr>
                <td><input type="text" id="task" class="form-control"></td>
                <td>
                    <select id="select" class="form-control">
                        <option>Low</option>
                        <option>Medium</option>
                        <option>High</option>

                </select>
                </td>

                <td><button class="btn btn-primary">ADD</button></td>
            </tr>
            </tbody>
        </table>
    </div>
</template>

<script>

    import TaskComponent from './Task.vue'

    export default{
        data(){
            return{
                tasks:[

                    {id:1, title:'Task 1 ', priority:'low'},
                    {id:2, title:'Task 2 ', priority:'high'},
                    {id:3, title:'Task 3 ', priority:'low'}
                ],

                message: 'MESSAGE'
            }
        },
        components:{TaskComponent}
    }


</script>


<style>



</style>