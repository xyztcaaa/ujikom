<template>
    <div class="content-container">
        <div class="row">
            <div class="col-md-3">
                <div class="card">
                    <div class="card-body">
                        <img :src="eskul.foto" :alt="eskul.judul" class="cover">
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <h2 class="text-center my-4">{{ eskul.judul }}</h2>
                <ul class="list-group list-group-flush">
                    <li class="list-group-item">Ketua: {{ eskul.ketua }}</li>
                    <li class="list-group-item">Deskripsi: {{ eskul.deskripsi }}</li>
                </ul>
            </div>
        </div>
        <nuxt-link to="eskul">
            <button type="submit" class="btn ms-3 btn-lg">KEMBALI</button>
        </nuxt-link>
    </div>
</template>

<script setup>
const supabase = useSupabaseClient();
const route = useRoute();
const eskul = ref({});

const geteskul = async () => {
    const { data, error } = await supabase.from('eskul').select(`*`).eq('id', route.params.id);
    if (error) console.error("Error fetching data:", error);
    if (data && data.length > 0) eskul.value = data[0];
};

onMounted(() => {
    geteskul();
});
</script>

<style scoped>
.content-container {
    margin-top: 150px; 
}

button {
    border: 1px solid #000;
    background-color: #72ceff;
    color: #fff;
    position: fixed;
    bottom: 30px;
    right: 30px;
    border-radius: 20px;
}

button:hover {
    background-color: #fff;
    color: #265cb5;
}

.cover {
    width: 100%;
}
</style>