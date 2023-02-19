<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer">
      <v-sheet color="green-lighten-5">
        <div class="d-flex py-8 px-8 flex-row justify-center">
          <h3>COOPERSANTOS</h3>
        </div>
      </v-sheet>
      <v-sheet class="pa-4">
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

    <v-main>
      <v-container fluid>
        <v-row>
          <v-col cols="6" style="background-color: #c8e6c92b" class="pa-7">
            <v-row>
              <v-col class="d-flex flex-row justify-space-between">
                <h2 class="font-weight-medium">Gerenciador de Carregamento</h2>
                <v-btn class="box-shadow" variant="outlined" color="primary"
                  >Adicionar Ordem</v-btn
                >
              </v-col>
            </v-row>
            <v-row>
              <v-col id="botoesMonitoramento">
                <v-btn class="mr-2" variant="outlined"
                  >Ver Todos<v-sheet class="ml-2">30</v-sheet></v-btn
                >
                <v-btn class="mr-2" variant="outlined"
                  >Em Andamento <v-sheet class="ml-2">18</v-sheet></v-btn
                >
                <v-btn class="mr-2" variant="outlined"
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
              <v-col
                style="background-color: #e8f5e9"
                class="d-flex flex-row pa-7 justify-space-between"
              >
                <h2 class="font-weight-medium">ABC-4558</h2>
                <v-btn class="box-shadow" variant="outlined" color="primary">
                  Whatsapp</v-btn
                >
              </v-col>
            </v-row>
            <v-row>
              <v-col>
                <v-card>
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
                      <v-card color="basil" flat>
                        <v-card-title class="pt-6">
                          Ocupação da Carga
                        </v-card-title>
                      </v-card>
                      <div class="d-flex">
                        <v-img width="100" src="@/assets/truck-perfil.svg">
                          <div
                            style="position: relative; z-index: 1; height: 100%"
                          >
                            <div
                              style="
                                position: relative;
                                z-index: 2;
                                top: 8px;
                                display: flex;
                                place-content: center;
                                align-items: center;
                                flex-flow: row nowrap;
                                margin-left: 16vh;
                                margin-right: 2vh;
                                height: 14vh;
                              "
                            >
                              <v-progress-linear
                                v-model="skill"
                                color="blue-grey"
                                height="100%"
                              >
                                <template v-slot:default="{ value }">
                                  <strong>{{ Math.ceil(value) }}%</strong>
                                </template>
                              </v-progress-linear>
                            </div>
                          </div>
                        </v-img>
                      </div>
                    </v-window-item>
                  </v-window>
                </v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<style scoped>
.v-btn {
  text-transform: none;
  letter-spacing: none;
}

.caminhao {
  background-image: url("@/assets/truck-perfil.svg");
}

.v-progress-linear {
  /* top: 17px;
  height: 128px;
  --v-progress-linear-height: 67px;
  left: 60%;
  transform: translateX(-50%);
  position: absolute;
  width: 74%; */
}
/* width: 74%;
    margin-top: 20px;
    margin-left: 172px;
    height: 11vh;
} */
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
    items: ["Informações", "Veículo", "Companhia", "Adiantamentos"],
    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
  }),
};
</script>
