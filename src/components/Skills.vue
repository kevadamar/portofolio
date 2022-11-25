<template>
  <div>
    <div class="mb-5 mt-5">
      <span class="title">Frontend</span>
      <v-container fluid>
        <div class="flex-logos">
          <div>
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-img
                  v-bind="attrs"
                  v-on="on"
                  width="150"
                  src="@/assets/hjs.png"
                  lazy-src="@/assets/hjs.png"
                ></v-img>
              </template>
              <h5>HTML, CSS, JavaScript</h5>
            </v-tooltip>
          </div>
          <div>
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-img
                  v-bind="attrs"
                  v-on="on"
                  width="110"
                  src="@/assets/logo.png"
                  lazy-src="@/assets/logo.png"
                ></v-img>
              </template>
              <h5>VueJS</h5>
            </v-tooltip>
          </div>
          <div>
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-img
                  v-bind="attrs"
                  v-on="on"
                  width="110"
                  src="@/assets/chartjs.svg"
                  lazy-src="@/assets/chartjs.svg"
                ></v-img>
              </template>
              <h5>ChartJS</h5>
            </v-tooltip>
          </div>
          <div>
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-img
                  v-bind="attrs"
                  v-on="on"
                  width="110"
                  src="@/assets/bootstrap.png"
                  lazy-src="@/assets/bootstrap.png"
                ></v-img>
              </template>
              <h5>Bootstrap</h5>
            </v-tooltip>
          </div>
          <div>
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-img
                  v-bind="attrs"
                  v-on="on"
                  width="110"
                  src="@/assets/logo.svg"
                  lazy-src="@/assets/logo.svg"
                ></v-img>
              </template>
              <h5>Vuetify</h5>
            </v-tooltip>
          </div>
          <div>
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-img
                  v-bind="attrs"
                  v-on="on"
                  width="150"
                  height="90"
                  class="pt-3"
                  src="@/assets/tailwind.png"
                  lazy-src="@/assets/tailwind.png"
                ></v-img>
              </template>
              <h5>Tailwind CSS</h5>
            </v-tooltip>
          </div>
          <div>
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-img
                  v-bind="attrs"
                  v-on="on"
                  width="120"
                  src="@/assets/reactjs.png"
                  lazy-src="@/assets/reactjs.png"
                ></v-img>
              </template>
              <h5>ReactJS</h5>
            </v-tooltip>
          </div>
          <div>
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-img
                  v-bind="attrs"
                  v-on="on"
                  width="127"
                  height="93"
                  src="@/assets/nuxtjs.png"
                  lazy-src="@/assets/nuxtjs.png"
                ></v-img>
              </template>
              <h5>NuxtJS</h5>
            </v-tooltip>
          </div>
        </div>
      </v-container>
    </div>

    <div class="mb-5">
      <span class="title">Backend</span>
      <div class="flex-logos">
        <div>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-img
                v-bind="attrs"
                v-on="on"
                width="110"
                src="@/assets/php.svg"
                lazy-src="@/assets/php.svg"
              ></v-img>
            </template>
            <h5>PHP</h5>
          </v-tooltip>
        </div>
        <div>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-img
                v-bind="attrs"
                v-on="on"
                width="110"
                src="@/assets/nodejs.png"
                lazy-src="@/assets/nodejs.png"
              ></v-img>
            </template>
            <h5>NodeJS</h5>
          </v-tooltip>
        </div>
        <div>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-img
                v-bind="attrs"
                v-on="on"
                width="90"
                src="@/assets/nestjs.png"
                lazy-src="@/assets/nestjs.png"
              ></v-img>
            </template>
            <h5>NestJS</h5>
          </v-tooltip>
        </div>
      </div>
    </div>

    <div class="mb-5">
      <span class="title">Database</span>
      <div class="flex-logos">
        <div>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-img
                v-bind="attrs"
                v-on="on"
                width="110"
                src="@/assets/mysql.png"
                lazy-src="@/assets/mysql.png"
              ></v-img>
            </template>
            <h5>MySQL</h5>
          </v-tooltip>
        </div>
        <div>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-img
                v-bind="attrs"
                v-on="on"
                width="110"
                src="@/assets/sqlserver.webp"
                lazy-src="@/assets/sqlserver.webp"
              ></v-img>
            </template>
            <h5>SQL Server</h5>
          </v-tooltip>
        </div>
      </div>
    </div>

    <div class="mb-5">
      <span class="title">Version Control</span>
      <div class="flex-logos">
        <div>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-img
                v-bind="attrs"
                v-on="on"
                width="110"
                src="@/assets/git.png"
                lazy-src="@/assets/git.png"
              ></v-img>
            </template>
            <h5>GIT</h5>
          </v-tooltip>
        </div>
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
