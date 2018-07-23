<template>
    <section class="single-recipe">
        <h1>{{recipe.title}}</h1>
        <div>
            <img :src="recipe.thumbnail" :alt="recipe.title" />
        </div>
        <p>{{recipe.description}}</p>
    </section>
</template>

<style scoped>
h1 {
    padding: 20px 0;
    color: grey;
}
.single-recipe {
    padding: 20px;
}

img {
    width: 100%;
}
</style>

<script>
export default {
    asyncData(context) {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                    resolve({
                        recipe:[
                            {
                                title: "Kebab",
                                thumbnail: "https://errantdiner.files.wordpress.com/2014/05/20140519_120237.jpg",
                                previewText: "Paki food",
                                description: "Great after a night out",
                                id: "1"
                            },
                            {
                                title: "Injeera",
                                thumbnail: "https://www.seriouseats.com/recipes/images/2016/08/20160801-seekh-kebab-recipe-48-1500x1125.jpg",
                                previewText: "This is a great injera",
                                description: "The food of heroes",
                                id: "2"
                            }
                        ].find(el => el.id === context.params.id)
                    })
            }, 1500);
        });
    }
}
</script>