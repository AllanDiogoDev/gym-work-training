<template>
  <div class="flex flex-col sm:flex-row bg-black">
    
    <div class="lg:flex sm:w-1/2">
      <!-- PEITO -->
      <section v-for="item in exercices" v-bind:key="item.nome" class="flex flex-col bg-black 
      bg-no-repeat lg:w-1/2 h-72 lg:h-80 justify-center items-center bg-cover md:bg-center" 
      style="background-image: url('chest.png')">      
        <ol v-for="chest in item.chest" v-bind:key="chest.nome" class="text-cyan-400">
          <a :href="chest.link" target="_blank">
            <li class="text-xl xl:text-2xl py-4 md:py-2 shadow"> {{chest.nome}} </li>
          </a>
        </ol>
      </section>
      
      <!-- COSTAS -->
      <section v-for="item in exercices" v-bind:key="item.nome" class="flex flex-col bg-black 
      bg-no-repeat lg:w-1/2 h-72 lg:h-80 justify-center items-center bg-cover md:bg-center" 
      style="background-image: url('back.png')">      
        <ol v-for="back in item.back" v-bind:key="back.nome" class="text-cyan-400">
          <a :href="back.link" target="_blank">
            <li class="text-xl xl:text-2xl py-4 md:py-2 shadow"> {{back.nome}} </li>
          </a>
        </ol>
      </section>
    </div>
    
    <div class="lg:flex sm:w-1/2">
      <!-- BICEPS -->
      <section v-for="item in exercices" v-bind:key="item.nome" class="flex flex-col bg-black 
      bg-no-repeat lg:w-1/2 h-72 lg:h-80 justify-center items-center bg-cover md:bg-center" 
      style="background-image: url('biceps.png')">      
        <ol v-for="biceps in item.biceps" v-bind:key="biceps.nome" class="text-cyan-400">
          <a :href="biceps.link" target="_blank">
            <li class="text-xl xl:text-2xl py-4 md:py-2 shadow"> {{biceps.nome}} </li>
          </a>
        </ol>
      </section>

      
      <!-- PERNAS -->
      <section v-for="item in exercices" v-bind:key="item.nome" class="flex flex-col bg-black 
      bg-no-repeat lg:w-1/2 h-72 lg:h-80 justify-center items-center bg-cover md:bg-center" 
      style="background-image: url('legs.png')">      
        <ol v-for="legs in item.legs" v-bind:key="legs.nome" class="text-cyan-400">
          <a :href="legs.link" target="_blank">
            <li class="text-xl xl:text-2xl py-4 md:py-2 shadow"> {{legs.nome}} </li>
          </a>
        </ol>
      </section>
    </div>

  </div>
</template>

<script>
export default {
data () {
  return {
    exercices:[{
      chest:[ 
        { nome: 'Supino Reto', link:'' }, 
        { nome: 'Supino Inclinado', link:'' },
        { nome: 'Supino Declinado', link:'' }
      ],
      legs:[ 
        { nome: 'Leg Press', link:''},
        { nome: 'Agachamento Smith', link:'' },
        { nome: 'Cadeira Abdutora', link:'' }
      ],
      back:[ 
        { nome: 'Barra Fixa', link:'' },
        { nome: 'Remada Unilateral', link:''},
        { nome: 'Remada Curvada', link:'' }
      ],
      biceps:[ 
        { nome: 'Rosca Martelo', link:''},
        { nome: 'Rosca Direta', link:'' },
        { nome: 'Rosca no Cross', link:'' }
      ]
    }]
    }
  },
name: 'SectionTypesExercises',
components: {
}
}
</script>

<style scoped>

.shadow{
  filter: drop-shadow(0.25rem 0.25rem 0.1rem rgb(0, 0, 0));
}

</style>