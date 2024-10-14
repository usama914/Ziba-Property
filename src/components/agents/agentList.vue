<template>
  <div class="agent-list">
    <agentCard v-for="author in authors" :key="author.id" :author="author" />
  </div>
</template>

<script setup>
const authors = [
  {
    id: 784,
    name: "Iqra Aslam ",
    nickname: "Iqra. ",
    email: "Iqraaslam886@gmail.com",
    phone: "+9234422221",
    mobile: "+923222221",
    listings: 55,
    avatar:
      "https://cdn.ziba-property.com/development/profile/images/VECQwoOiKeadXfcnSjs5dnfJatgoAzyn.jpg",
    usernickname: "Iqra. ",
  },
  {
    id: 4,
    name: "Devs ",
    nickname: "Dev. ",
    email: "dev@gmail.com",
    phone: "+9234411234",
    mobile: "+923211234",
    listings: 35,
    avatar:
      "https://cdn.ziba-property.com/development/profile/images/VECQwoOiKeadXfcnSjs5dnfJatgoAzyn.jpg",
    usernickname: "dev. ",
  },
  {
    id: 7434,
    name: "Programmer ",
    nickname: "Dev. ",
    email: "dev@gmail.com",
    phone: "+92344554344",
    mobile: "+9232554344",
    listings: 35,
    avatar:
      "https://cdn.ziba-property.com/development/profile/images/VECQwoOiKeadXfcnSjs5dnfJatgoAzyn.jpg",
    usernickname: "dev. ",
  },
  {
    id: 724,
    name: "Analog ",
    nickname: "Dev. ",
    email: "dev@gmail.com",
    phone: "+923445334214",
    mobile: "+92320334214",
    listings: 35,
    avatar:
      "https://cdn.ziba-property.com/development/profile/images/VECQwoOiKeadXfcnSjs5dnfJatgoAzyn.jpg",
    usernickname: "dev. ",
  },
];
import agentCard from "./agentCard.vue";
</script>

<style scoped>
.agent-list {
  display: flex;
  flex-direction: column;
  /* gap: 1rem; */
  background: #eaeaea;
  padding: 10px;
  max-width: 250px;
  border-radius: 10px;
  width: 100%;
  border-radius: 10px;
}
</style>
