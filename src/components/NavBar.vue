<template>
    <nav class="w-full flex flex-col justify-center items-center h-20 bg-zinc-900">
        <div class="flex w-11/12 h-12">
            <section class="flex w-2/12 justify-center items-center">
                <img class="w-20" src="logo-nav.png"/>
                <span class="text-white text-xl pl-2">THE <br>LEGENDS</span>
            </section>
            <section class="flex w-10/12 justify-end">
                <ul class="flex items-center" v-for="option in options" v-bind:key="option">
                    <li class="text-white px-4 text-md uppercase"> {{option.nome}} </li>
                </ul>
            </section>
        </div>
    </nav>
</template>

<script>

export default {
data () {
  return {
    options:[
        { nome: 'Campeonatos', link:'' }, 
        { nome: 'Atletas', link:'' },
        { nome: 'Lorem', link:'' }, 
        { nome: 'Ipsum', link:'' },
        { nome: 'Lorem', link:'' }, 
        { nome: 'Ipsum', link:'' }
    ]
  }
},
name: 'NavBar',
components: {
    
}
}

</script>

<style scoped>

</style>