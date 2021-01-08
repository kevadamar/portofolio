<template>
  <div>
    <div class="mb-5">
      <div class="title my-3">Front-End Languages</div>
      <div class="flex-logos">
        <div><img src="@/assets/hjs.png" alt="html css js logo"></div>
      </div>
    </div>

    <div class="mb-5">
      <div class="title">Front-End Frameworks</div>
      <div class="flex-logos">
        <div><img src="@/assets/logo.png" alt="vue.js logo"></div>
        <div><img src="@/assets/chartjs.svg" alt="chart.js logo"></div>
        <div><img src="@/assets/bootstrap.png" alt="bootstrap logo"></div>
        <div><img src="@/assets/logo.svg" alt="vuetify logo"></div>
      </div>
    </div>

    <div class="mb-5">
      <div class="title">Database</div>
      <div class="flex-logos">
        <div><img src="@/assets/mysql.png" alt="mysql logo"></div>
      </div>
    </div>

    <div class="mb-5">
      <div class="title">Version Control</div>
      <div class="flex-logos">
        <div><img src="@/assets/git.png" alt="git logo"></div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .flex-logos {
    display: flex;
    flex-wrap: wrap;
    justify-items: center;
    justify-content: center;
  }
  .flex-logos div {
    margin: 10px;
  }
  .flex-logos img {
    width: 120px;
    height: 100px;
    object-fit: contain;
  
  }
</style>