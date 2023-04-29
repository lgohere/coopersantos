<template>
  <v-container class="background h-100 d-flex justify-center">
    <v-col class="text-center" cols="12">
      <v-container class="logo">
        <v-img src="/logo.png" height="170"></v-img>
      </v-container>
      <v-btn
        class="botao"
        :loading="loading"
        @click="loading = !loading"
        block
        size="x-large"
        >INICIAR VIAGEM</v-btn
      >
    </v-col>
  </v-container>
</template>

<style scoped>
.background {
  padding-top: 20vh;
  background: linear-gradient(95.64deg, #e2e8d8 8.99%, #d0ebde 91.01%);
}

.botao {
  /*  
  background: #85ff66;
  - CRIAR VIAGEM: #85FF66
  - ENCERRAR VIAGEM: #FCFF5C 
*/

  box-sizing: border-box;
  border: 1px solid #443a81;
  box-shadow: 3px 3px 1px #007df1,
    inset -11px -5px 10px 5px rgba(70, 166, 255, 0.12);
  border-radius: 21px;
}

.logo {
  padding-bottom: 5vh;
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
