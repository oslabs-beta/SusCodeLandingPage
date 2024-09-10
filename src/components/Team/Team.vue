<script lang="ts">
import { defineComponent } from 'vue';
import Member from "./Member.vue"
import { team } from "../../assets/db.json"

export default defineComponent({
    name: 'Team',
    components: {
      Member
    },
    data() {
      return {team: team}
    }
});
  
</script>

<template>
  <section class="team">
    <!-- <Member msg={{ db.team[0]}}/> -->
    <Member
      v-for="(member) in team"
      :key="member.id"
      :name="member.name"
      :github="member.github"
      :image="member.imagePath"
    />
  </section>
</template>

<style scoped>
  .team {
    margin: 10em 1em;
    border: .5em solid;
    border-radius: 2em;
    padding: 2em;

    display: flex;
    flex-wrap:wrap;
    /* justify-content: center; */
    justify-content: space-evenly;
  }
</style>