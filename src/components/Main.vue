<template>
  <main>

        <div>
            <Search :info="filter"/>
        </div>
        
      <div v-if="!loading" class="cards">
          
        <div v-for="artist in artists" 
        :key="artist.id"
         class="box">

            <Artists :info="artist"/>
            
        </div>
      </div>

      <div v-else class="loader">Loading...</div>

  </main>
</template>

<script>
import axios from 'axios';
import Artists from '@/components/Artists.vue';
import Search from '@/components/Search.vue';


export default {
    name: 'Main',
    components: {
        Artists,
        Search,
    },
    data() {
        return {
            apiURL: 'https://flynn.boolean.careers/exercises/api/array/music',
            artists: [],
            loading: true,
            
        }
    },
    created() {
        this.getArtists();
    },
    methods: {
        getArtists() {
            /**
             * API CALL
             */
            axios.get(this.apiURL)
            .then(res => {
                console.log(res.data);
                this.artists = res.data.response;
                this.loading = false;
            })
            .catch(err => {
                console.log('Error', err);
            })
        }
    }
}
</script>


<style scoped lang="scss">
    @import '@/scss/general.scss';

    main {
        background: $main-bg-color;
        height: 1000px;
    }

    main {
        .cards {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            padding: 50px;
        }
    }

    main {
        .cards {
            .box {
                padding: 0 30px;
                margin: 10px;
                background: #2e3a46;
            }
        }
    }

</style>