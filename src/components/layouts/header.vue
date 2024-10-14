<template>
  <header class="header">
    <div class="menu-icon">
      <img src="../../assets/menu-icon.png" alt="" />
    </div>
    <div class="logo">
      <img src="../../assets/ziba-logo.svg" alt="Ziba Property Logo" />
    </div>
    <nav aria-label="breadcrumb">
      <ol class="breadcrumb">
        <li class="breadcrumb-item">Home</li>
        <li class="breadcrumb-item active" aria-current="page">
          Businesses & Services
        </li>
      </ol>
    </nav>
  </header>
</template>

<style scoped>
.header {
  display: flex;
  align-items: baseline;
  justify-content: flex-start;
  gap: 1.5rem;
  padding: 15px 30px;
}
.breadcrumb-item {
  color: gray;
}
.active {
  color: black;
}
.menu-icon img {
  width: 20px;
}
.logo img {
  width: 100px;
}
</style>
