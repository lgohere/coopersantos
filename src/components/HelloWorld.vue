<template>
  <v-app class="main-bg">
    <v-sheet>
      <v-navigation-drawer v-model="drawer">
        <div
          class="d-flex pt-10 pb-4 px-4 flex-column align-center justify-center"
        >
          <v-img src="/cooper-icon.png" style="width: 35%; height: 35%"></v-img>
          <h3 class="brand-color">COOPERSANTOS</h3>
        </div>
        <v-sheet class="py-6 px-4">
          <div class="py-4 d-flex flex-row justify-space-around align-center">
            <v-avatar color="grey-darken-1" size="40"></v-avatar>
            <div>
              <div><span class="font-weight-bold">Luiz</span></div>
              <div>john@google.com</div>
            </div>
          </div>
        </v-sheet>

        <!-- <v-divider></v-divider> -->

        <v-list class="pa-4">
          <v-list-item
            class="py-4"
            v-for="[icon, text] in links"
            :key="icon"
            link
          >
            <template v-slot:prepend>
              <v-icon>{{ icon }}</v-icon>
            </template>

            <v-list-item-title class="font-weight-bold">{{
              text
            }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </v-sheet>

    <v-main>
      <div>
        <v-container fluid>
          <v-row>
            <v-col xl="5" lg="5" md="6" sm="12" xs="12" class="pa-6 glass">
              <v-row>
                <v-col class="px-0 py-6 d-flex flex-row justify-space-between">
                  <h2 class="title-responsive font-weight-medium">
                    Gerenciador de Carregamento
                  </h2>
                  <v-btn
                    class="box-shadow glass btn-responsive"
                    color="green"
                    variant="outlined"
                    >Adicionar Ordem</v-btn
                  >
                </v-col>
              </v-row>
              <v-row>
                <v-row>
                  <v-col class="d-flex flex-column">
                    <v-btn class="mb-2" variant="outlined"
                      >Ver Todos<v-sheet
                        color="green"
                        style="border-radius: 25px"
                        class="ml-2 pa-1"
                        >30</v-sheet
                      ></v-btn
                    >
                    <v-btn class="mb-2" variant="outlined"
                      >Em Andamento
                      <v-sheet
                        class="ml-2 pa-1"
                        color="green"
                        style="border-radius: 25px"
                        >18</v-sheet
                      ></v-btn
                    >
                    <v-btn class="mb-2" variant="outlined"
                      >Pendentes
                      <v-sheet
                        class="ml-2 pa-1"
                        color="green"
                        style="border-radius: 25px"
                        >12</v-sheet
                      ></v-btn
                    >
                  </v-col>
                </v-row>
              </v-row>
              <v-row>
                <v-col cols="12" xs="12" lg="6" md="12" sm="6">
                  <v-card style="border-radius: 7px">
                    <v-row class="d-flex pa-4">
                      <v-col cols="8">
                        <h3 class="font-weight-medium">Ordem</h3>
                        <h2>ABC-4558</h2>
                      </v-col>
                      <v-col class="d-flex flex-column justify-start" cols="4">
                        <v-img width="80" src="@/assets/truck.svg"></v-img>
                      </v-col>
                    </v-row>

                    <v-divider></v-divider>
                    <div
                      style="border-radius: 7px"
                      class="pa-4 d-flex flex-column"
                    >
                      <h4>Santos, SP</h4>
                      <h5>Porto Rei Pelé</h5>
                      <v-space> <br /> </v-space>
                      <h4>São Paulo, SP</h4>
                      <h5>Armazem Fulano de Tal</h5>
                    </div>
                    <v-divider></v-divider>
                    <div
                      style="border-radius: 7px"
                      class="pa-4 d-flex flex-column"
                    >
                      <h5>Cliente</h5>
                      <h4>Luiz Gouveia</h4>
                      <h5>Santos/SP</h5>
                    </div>
                  </v-card>
                  <v-divider></v-divider>
                </v-col>
                <v-col cols="12" xs="12" lg="6" md="12" sm="6">
                  <v-card style="border-radius: 7px">
                    <v-row class="d-flex pa-4">
                      <v-col cols="8">
                        <h3 class="font-weight-medium">Ordem</h3>
                        <h2>ABC-4558</h2>
                      </v-col>
                      <v-col class="d-flex flex-column justify-start" cols="4">
                        <v-img width="80" src="@/assets/truck.svg"></v-img>
                      </v-col>
                    </v-row>

                    <v-divider></v-divider>
                    <div
                      style="border-radius: 7px"
                      class="pa-4 d-flex flex-column"
                    >
                      <h4>Santos, SP</h4>
                      <h5>Porto Rei Pelé</h5>
                      <v-space> <br /> </v-space>
                      <h4>São Paulo, SP</h4>
                      <h5>Armazem Fulano de Tal</h5>
                    </div>
                    <v-divider></v-divider>
                    <div
                      style="border-radius: 7px"
                      class="pa-4 d-flex flex-column"
                    >
                      <h5>Cliente</h5>
                      <h4>Luiz Gouveia</h4>
                      <h5>Santos/SP</h5>
                    </div>
                  </v-card>
                  <v-divider></v-divider>
                </v-col>
              </v-row>
            </v-col>
            <v-col
              style="background: grey; height: 100vh"
              class="px-1 py-lg-0 pt-md-0 d-flex justify-center"
              cols="12"
              xl=""
              lg="7"
              md="6"
              sm="12"
              xs="12"
            >
              <!-- aqui vai o mapa -->
              <v-col
                id="shipment-info-text"
                class="pa-6 d-flex flex-column justify-center glass"
              >
                <v-row
                  style="position: relative; z-index: 2"
                  class="d-flex justify-center"
                >
                  <v-card
                    style="
                      top: 2vh;
                      height: 8vh;
                      width: 90%;
                      border-radius: 15px;
                    "
                    class="glass d-flex"
                  >
                    <v-row class="d-flex">
                      <v-col
                        class="d-flex flex-column align-center justify-center"
                        cols="3"
                      >
                        <div class="d-flex flex-column">
                          <h4>Posição Atual</h4>
                          <h5 class="font-weight-medium">Km 206</h5>
                        </div>
                      </v-col>
                      <v-col
                        class="d-flex align-center justify-center"
                        cols="3"
                      >
                        <div class="d-flex flex-column">
                          <h4>Ultima Parada</h4>
                          <h5 class="font-weight-medium">2 hrs atrás</h5>
                        </div>
                      </v-col>
                      <v-col
                        class="d-flex align-center justify-center"
                        cols="3"
                      >
                        <div class="d-flex flex-column">
                          <h4>Distancia</h4>
                          <h5 class="font-weight-medium">250 km</h5>
                        </div>
                      </v-col>
                      <v-col
                        class="d-flex align-center justify-center"
                        cols="3"
                      >
                        <div class="d-flex flex-column">
                          <h4>Velocidade</h4>
                          <h5 class="font-weight-medium">90 km/h</h5>
                        </div>
                      </v-col>
                    </v-row>
                  </v-card>
                </v-row>

                <v-row
                  style="position: relative; z-index: 2"
                  class="d-flex align-end justify-center"
                >
                  <v-card
                    style="
                      height: 20vh;
                      width: 90%;
                      position: relative;
                      border-radius: 15px;
                      bottom: 2vh;
                    "
                    class="glass"
                  >
                    <v-tabs
                      v-model="tab"
                      bg-color="transparent"
                      color="basil"
                      grow
                    >
                      <v-tab v-for="item in items" :key="item" :value="item">
                        {{ item }}
                      </v-tab>
                    </v-tabs>

                    <v-window v-model="tab">
                      <v-window-item
                        v-for="item in items"
                        :key="item"
                        :value="item"
                      >
                        <v-card class="glass">
                          <v-card-text>{{ text }}</v-card-text>
                        </v-card>
                      </v-window-item>
                    </v-window>
                  </v-card>
                </v-row>
              </v-col>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </v-main>
  </v-app>
</template>

<style scoped>
@media (max-width: 400px) {
  .title-responsive {
    font-size: 22px;
  }
  .btn-responsive {
    width: 45%;
  }
}

@media (max-width: 1347px) {
  #shipment-info-text {
    font-size: 90%;
  }
}

.botoesStatus {
  display: flex;
}

.v-btn {
  text-transform: none;
  letter-spacing: none;
  background: linear-gradient(
    to right bottom,
    rgb(109 200 146 / 25%),
    rgb(53 179 104 / 35%)
  );
}

.caminhao {
  background-image: url("@/assets/truck-perfil.svg");
}

.main-bg {
  background: rgba(37, 214, 108, 0.8);
  background: linear-gradient(
    to right bottom,
    rgb(7, 66, 31),
    rgb(255, 255, 255)
  );
}

.glass {
  background: white;
  background: linear-gradient(
    to right bottom,
    rgba(255, 255, 255, 0.7),
    rgba(255, 255, 255, 0.76)
  );
  backdrop-filter: blur(4px);
}

.brand-color {
  color: #35b368;
}

.mapa {
  color: white;
  background: #8080808a;
}
</style>

<script>
export default {
  computed: {
    cols() {
      const { lg, sm } = this.$vuetify.display;
      return lg ? [5, 7] : sm ? [12] : [12];
    },
  },
  data: () => ({
    ordens: [
      {
        status: "Em Andamento",
        placas: ["CBJ 5501", "TXE 8954"],
      },
      {
        status: "Pendentes",
        placas: ["JFG 5541", "UIW 4556"],
      },
    ],
    drawer: null,
    links: [
      ["mdi-inbox-arrow-down", "Dashboard"],
      ["mdi-send", "Rotas"],
      ["mdi-delete", "Cronograma"],
      ["mdi-alert-octagon", "Entregues"],
    ],
    tab: "Appetizers",
    items: ["Informações", "Motorista", "Veículo", "Contratante", "Documentos"],
    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
  }),
};
</script>
