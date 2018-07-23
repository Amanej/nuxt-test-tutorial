<template>
    <section class="recipes">
        <Recipe 
            v-for="recipe in recipes"
            :key="recipe.id"
            :title="recipe.title" 
            :thumbnail="recipe.thumbnail" 
            :previewText="recipe.previewText" 
            :id="recipe.id" 
        />
    </section>
</template>

<script>


import Recipe from '@/components/Recipe'
export default {
    components: {
        Recipe
    },
    asyncData() {
        return new Promise((resolve, reject) => {

        setTimeout(() => {
                resolve({
                    recipes:[
                        {
                            title: "Kebab",
                            thumbnail: "https://errantdiner.files.wordpress.com/2014/05/20140519_120237.jpg",
                            previewText: "Paki food",
                            id: 1
                        },
                        {
                            title: "Injeera",
                            thumbnail: "https://www.seriouseats.com/recipes/images/2016/08/20160801-seekh-kebab-recipe-48-1500x1125.jpg",
                            previewText: "This is a great injera",
                            id: 2
                        }
                    ]
                })
            }, 500);
        });
    }
}
</script>


<style scoped>
.recipes {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
}
</style>