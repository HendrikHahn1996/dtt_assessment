<template>
    <NavBar />
    <TopBar />
    <HomeCard />
</template>

<script>
import NavBar from '@/compontents/NavBar.vue'
import TopBar from '@/compontents/TopBar.vue'
import HomeCard from '@/compontents/HomeCard.vue'

export default {
    name: 'Home',
      components: {
        NavBar,
        TopBar,
        HomeCard
  },
}
</script>