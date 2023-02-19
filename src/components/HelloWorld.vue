<template>
  <v-app class="main-bg">
    <v-sheet>
      <v-navigation-drawer v-model="drawer">
        <div class="d-flex pt-10 pb-4 px-4 flex-row justify-center">
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
      <v-container fluid>
        <v-row>
          <v-col cols="5" class="pt-8 glass" style="height: 100vh">
            <v-row>
              <v-col class="d-flex flex-row justify-space-between">
                <h2 class="font-weight-medium">Gerenciador de Carregamento</h2>
                <v-btn
                  class="box-shadow glass"
                  variant="outlined"
                  color="primary"
                  >Adicionar Ordem</v-btn
                >
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12" class="d-flex justify-start">
                <v-btn class="mr-2 glass" variant="outlined"
                  >Ver Todos<v-sheet class="ml-2">30</v-sheet></v-btn
                >
                <v-btn class="mr-2 glass" variant="outlined"
                  >Em Andamento <v-sheet class="ml-2">18</v-sheet></v-btn
                >
                <v-btn class="mr-2 glass" variant="outlined"
                  >Pendentes <v-sheet class="ml-2">12</v-sheet></v-btn
                >
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="6">
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
              <v-col cols="6">
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
          <v-col>
            <v-row>
              <v-sheet style="height: 100vh; width: 100%" class="glass">
                <!-- Fundo -->
                <v-col cols="12" class="d-flex justify-center mapa">
                  Mapa tempo real
                  <v-card
                    style="
                      height: 8vh;
                      position: absolute;
                      width: 40%;
                      border-radius: 15px;
                      z-index: 2;
                      top: 7vh;
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
                  <v-card
                    style="
                      height: 20vh;
                      width: 45%;
                      position: absolute;
                      border-radius: 15px;
                      top: 75vh;
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
                        <v-card style="height: 100vh" class="glass">
                          <v-card-text>{{ text }}</v-card-text>
                        </v-card>
                      </v-window-item>
                    </v-window>
                  </v-card>
                </v-col>
              </v-sheet>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<style scoped>
.botoesStatus {
  display: flex;
}

.v-btn {
  text-transform: none;
  letter-spacing: none;
}

.caminhao {
  background-image: url("@/assets/truck-perfil.svg");
}

.main-bg {
  background: rgba(37, 214, 108, 0.5);
  background: linear-gradient(
    to right bottom,
    rgba(37, 214, 108, 0.7),
    rgba(0, 0, 0, 0.3)
  );
}

.glass {
  background: white;
  background: linear-gradient(
    to right bottom,
    rgba(255, 255, 255, 0.7),
    rgba(255, 255, 255, 0.3)
  );
}

.brand-color {
  color: #35b368;
}

.mapa {
  color: white;
  background: #8080808a;
  height: 100vh;
  z-index: 1;
}
</style>

<script>
export default {
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
