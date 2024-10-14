<template>
  <div class="filter_tab mb-2">
    <ul class="nav nav-underline">
      <li class="nav-item" v-for="(tab, index) in tabs" :key="index">
        <a
          :class="['nav-link', { active: activeTab === index }]"
          href="#"
          @click="setActiveTab(index)"
        >
          <img :src="tab.icon" alt="" /> {{ tab.label }}
        </a>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from "vue";
import listingIcon from "../../assets/listings.png";
import servicesIcon from "../../assets/services.png";
import buySellIcon from "../../assets/buysell.png";
import agentsIcon from "../../assets/agents.png";

const tabs = [
  { label: "Property Listings", icon: listingIcon },
  { label: "Business & Services", icon: servicesIcon },
  { label: "Buy-Sell-Wanted", icon: buySellIcon },
  { label: "Find Agents", icon: agentsIcon },
];

const activeTab = ref(0);

const setActiveTab = (index) => {
  if (!tabs[index].disabled) {
    activeTab.value = index;
  }
};
</script>

<style scoped>
.filter_tab {
  background: #f2fbff;
  padding: 10px;
  height: 50px;
  border-bottom: 1px solid #c9ebfb;
}

.nav-underline .nav-link.active {
  font-weight: bold;
  color: #0a58ca;
  border-bottom: 2px solid #0a58ca;
}

.nav-underline .nav-link {
  color: gray;
}

ul {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

img {
  width: 20px;
}

.nav-link {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 5px;
  text-decoration: none;
}

.nav-link.active {
  color: #0a58ca;
}

.nav-link.disabled {
  pointer-events: none;
  opacity: 0.6;
}
</style>
