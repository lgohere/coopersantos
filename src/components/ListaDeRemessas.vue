<template>
  <v-container fluid class="background fill-height d-flex align-start">
    <v-row class="text-center flex-column">
      <!-- LogoGestor -->
      <div>
        <v-container block>
          <v-img src="/logo-mg.png" height="70"></v-img>
        </v-container>
      </div>
      <div class="mb-5">Pausadas</div>
      <div>
        <v-row justify="center">
          <v-col cols="11" sm="8" md="6" lg="4" xl="3">
            <v-card class="remessa-card px-6 py-5 mb-5">
              <h4>SANTOS - SAO PAULO</h4>
            </v-card>
            <v-card class="px-6 py-5 mb-5">
              <h4>SANTOS - PIRACICABA</h4>
            </v-card>
            <v-card class="remessa-card px-6 py-5 mb-5">
              <h4>SANTOS - CURITIBA</h4>
            </v-card>
            <v-card class="px-6 py-5 mb-5">
              <h4>SANTOS - RIO DE JANEIRO</h4>
            </v-card>
            <v-card class="remessa-card px-6 py-5 mb-5">
              <h4>SANTOS - SAO PAULO</h4>
            </v-card>
            <v-card class="px-6 py-5 mb-5">
              <h4>SANTOS - PIRACICABA</h4>
            </v-card>
            <v-card class="remessa-card px-6 py-5 mb-5">
              <h4>SANTOS - SAO PAULO</h4>
            </v-card>
            <v-card class="px-6 py-5 mb-5">
              <h4>SANTOS - PIRACICABA</h4>
            </v-card>
          </v-col>
        </v-row>
      </div>
    </v-row>
  </v-container>
</template>

<style scoped>
.background {
  padding-top: 5vh;
  background: linear-gradient(95.64deg, #e2e8d8 8.99%, #d0ebde 91.01%);
}

.remessa-card {
  font-weight: 300;
}

.sombra {
  /*  
  background: #85ff66;
  - CRIAR VIAGEM: #85FF66
  - ENCERRAR VIAGEM: #FCFF5C 
*/

  box-sizing: border-box;
  border: 1px solid #443a81;
  box-shadow: 3px 3px 1px #007df1,
    inset -11px -5px 10px 5px rgba(70, 166, 255, 0.12);
  /* border-radius: 21px; */
}
</style>

<script>
export default {
  data: () => ({
    loading: false,
  }),

  watch: {
    loading(val) {
      if (!val) return;

      setTimeout(() => (this.loading = false), 1000);
    },
  },
};
</script>
