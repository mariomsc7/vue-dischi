<template>
  <div class="container">
      <div class="disc">
        <img :src="info.poster" :alt="info.title">
        <h2>{{ info.title }}</h2>
        <h3>{{ info.author }}</h3>
        <h4>{{ info.year }}</h4>
        <h5>{{ info.genre }}</h5>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Artists',
    props: ['info'],
}
</script>

<style scoped lang="scss">

    .container {
        margin: 30px 0;
        
    }

    .disc {
        max-width: 128px;
        display: flex;
        flex-direction: column;
        text-align: center;
    }

    .disc {
        img {
            width: 128px;
            cursor: pointer;
        }
    }

    .disc {
        h2 {
            margin: 20px 0;
            font-size: 1.1rem;
            
            text-transform: uppercase;
        }
    }

    .disc {
        h3 {
            margin: 5px 0;
            font-size: .9rem;
            color: #797e7b;
        }
    }

    .disc {
        h4 {
            margin: 5px 0;
            font-size: .8rem;
            color: #797e7b;
        }
    }

    .disc {
        h5 {
            margin: 5px 0;
            font-size: .8rem;
        }
    }
    

</style>