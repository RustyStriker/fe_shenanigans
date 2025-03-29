<script lang="ts">
import TopBar from './components/TopBar.vue'
import GroupCard from './components/GroupCard.vue'

export default {
  data() {
    return {
      groups: [
        { 
          title: 'ski trip', 
          imageUrl: "https://www.snowmagazine.com/images/features/focus-on/Piste%20skiing%20Whistler%20Canada%20CREDIT%20Tourism%20Whistler_Guy%20Fattal.jpg",
          cost: "$$",
          date: "17 December 2029 - 23 December 2029"
        },
        { 
          title: 'Trip to Venice', 
          imageUrl: "http://foundtheworld.com/wp-content/uploads/2014/07/Venice-Italy-9.jpg",
          cost: "$$$",
          date: "22 October 2029 - 23 October 2029"
        },
        { 
          title: 'Trip to Venice', 
          imageUrl: "http://foundtheworld.com/wp-content/uploads/2014/07/Venice-Italy-9.jpg",
          cost: "$$$",
          date: "22 October 2029 - 23 October 2029"
        },
        { 
          title: 'ski trip', 
          imageUrl: "https://www.snowmagazine.com/images/features/focus-on/Piste%20skiing%20Whistler%20Canada%20CREDIT%20Tourism%20Whistler_Guy%20Fattal.jpg",
          cost: "$$",
          date: "17 December 2029 - 23 December 2029"
        },
      ]
    }
  },
  components: { GroupCard, TopBar }
}
</script>

<template>
  <header style="margin: 16px;">
    <TopBar title="My groups" />
  </header>
  <main style="display: flex; flex-wrap: wrap; margin: 8px;">
    <GroupCard v-for="g in groups" :title="g.title" :image-url="g.imageUrl" :cost="g.cost" :date="g.date" />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
