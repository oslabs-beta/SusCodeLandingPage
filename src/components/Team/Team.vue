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
  <section id="team">
    <div>
      <span class="team-heading">MEET OUR TEAM</span>
    </div>

    <div class="team">
      <Member
        v-for="(member) in team"
        :key="member.id"
        :name="member.name"
        :github="member.github"
        :linkedin="member.linkedin"
        :image="member.imagePath"
        class="member"
      />
    </div>
  </section>
</template>

<style scoped>
body, html {
  overflow-x: hidden;
  margin: 0;
  padding: 0;
}

#team {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100vw;
  padding: 0;
  margin: 0;
  scroll-margin-top: 125px;
}

.team {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: space-evenly;
  align-items: center;
  width: 100vw;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  overflow-x: hidden;
}

.member {
  flex: 1 0 calc(20% - 1rem);
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.member img {
  width: 100%;
  height: auto;
  display: block;
}

.team-heading {
  display: inline;
  font-size: 5rem;
  font-weight: bold;
  background: linear-gradient(142deg, rgba(122,164,212,1) 0%, rgba(4,48,111,1) 35%, rgba(4,94,222,1) 100%);
  background-clip: text;
  color: transparent;
  margin-top: -2rem;
}

@media (max-width: 768px) {
  .team {
    flex-wrap: wrap;
  }
  .member {
    flex: 1 1 45%;
  }
}

@media (max-width: 480px) {
  .team {
    flex-wrap: wrap;
  }
  .member {
    flex: 1 1 90%;
  }
}
</style>
