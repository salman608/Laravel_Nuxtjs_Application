<template>
    <div class="mt-5 container">
        <div class="card">
            <div class="card-header">
                <h3>Create Student <NuxtLink to="/" class="btn btn-warning float-end">BanK</NuxtLink>
                </h3>
            </div>
            <div class="card-body">
                <div v-if="isLoading">
                   <Loading :title="isLoading" />
                </div>
                <div v-else>
                    <form @submit.prevent="saveStudent">
                    <div class="mb-3">
                        <label for="">Name</label>
                        <input type="text" class="form-control" v-model="student.name" placeholder="Enter name....">
                    </div>
                    <div class="mb-3">
                        <label for="">Course</label>
                        <input type="text" class="form-control" v-model="student.course" placeholder="Enter course....">
                    </div>
                    <div class="mb-3">
                        <label for="">Email</label>
                        <input type="text" class="form-control" v-model="student.email" placeholder="Enter email....">
                    </div>
                    <div class="mb-3">
                        <label for="">Phone</label>
                        <input type="text" class="form-control" v-model="student.phone" placeholder="Enter phone....">
                    </div>

                    <div class="mb-3">
                        <button type="submit" class="btn btn-primary">Save Data</button>
                    </div>
                </form>
                </div>
            </div>
        </div>
    </div>
</template>

<script  >
export default {
    name: "studentCreate",
    data() {
        return {
            student: {
                name: '',
                course: '',
                email: '',
                phone: '',
            },
            isLoading: false,
            isLoadingTitle: 'Loading'
        }
    },
    methods: {
        saveStudent() {
            this.isLoading = true;
            this.isLoading = "Saving";
            // alert('i am here');
            axios.post().then(res=>)
        }
    }
}
</script>

<style></style>