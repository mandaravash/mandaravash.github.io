<script>
export default {
    data() {
        return {
            students: [
        { num:'1', name: 'a', id: 'b223539334', gender: 'male', phone:'0978290888' },
        { num:'2', name: 'b', id: 'b223539334', gender: 'female', phone:'0978290888' },
        { num:'3', name: 'c', id: 'b223539334', gender: 'female', phone:'0978290888' },
        { num:'4', name: 'd', id: 'b223539334', gender: 'male', phone:'0978290888' },
      ]
        };

    },
    // 放涵式的地方
    methods: {
        removeStudent(index) {
            this.students.splice(index, 1);
        }
    }
};
</script>

<template>
    <div>
        <h1>PRACTICE</h1>
        <table border="1">
            <thead>
                <tr>
                    <th>編號</th>
                    &nbsp
                    <th>姓名</th>
                    &nbsp
                    <th>身分證</th>
                    &nbsp
                    <th>性別</th>
                    &nbsp
                    <th>電話</th>
                    &nbsp
                    <th>功能</th>
                </tr>
            </thead>
            <tbody>
                <!-- 使用 v-for 迴圈來迭代學生資訊陣列 -->
                <tr v-for="(student, index) in students" :key="student.num">
                    <td>{{ student.num }}</td>
                    &nbsp &nbsp &nbsp 
                    <td>{{ student.name }}</td>
                    &nbsp &nbsp &nbsp 
                    <td>{{ student.id }}</td>
                    &nbsp &nbsp &nbsp 
                    <td>{{ student.gender === 'male'? '男' : '女' }}</td>
                    &nbsp &nbsp &nbsp 
                    <td>{{ student.phone }}</td>
                    &nbsp &nbsp &nbsp 
                    <td>
                        <button class=" bg-gray-500" @click="removeStudent(index)">delete</button>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
    <!-- <h1>hello</h1>
    &nbsp; &nbsp; &nbsp;
    <RouterLink to="/practice-one">practice1</RouterLink>
    &nbsp; &nbsp; &nbsp;
    <!-- v-for迴圈 -->
    <!-- <div>
        <div v-for="(item, index) in arr" :key="index" class="text-xl border border-white">
            num{{ index }}
        </div> -->

    <!-- 練習:印出1-99在畫面上 -->
    <!-- <div >
            <div v-for="num in 10" :key="num" class="text-lg border border-white">
                {{ num }}
            </div>
        </div> -->

    <!-- <div >
            <div v-for="(value, key, index) in myObj" :key="index" class="text-lg border border-white">
                {{ key }} {{ value }}
            </div>
        </div> -->
    <!-- <br>
        <!-- 練習題 -->
    <!-- <button type="button" @click="addItem()">新增</button>
        &nbsp; &nbsp; &nbsp;
        <button type="button" @click="deleteItem()">刪除</button>
    </div>  -->
</template>

<style scoped></style>