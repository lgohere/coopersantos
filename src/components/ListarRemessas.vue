<template>
  <v-container fluid class="background fill-height">
    <v-row class="text-center flex-column">
      <!-- LogoGestor -->
      <v-container block class="d-flex justify-center align-center logo">
        <v-img src="/logo-mg.png" height="120"></v-img>
      </v-container>
      <div class="card pt-5">
        <v-layout>
          <v-row justify="center">
            <v-col cols="11" sm="8" md="6" lg="4" xl="3">
              <!-- LoginBotao -->
              <v-btn class="sombra mb-5" size="x-large" block>NOVAS</v-btn>
              <br />
              <v-btn class="sombra mb-5" size="x-large" block>PAUSADAS</v-btn>
              <br />
              <v-btn class="sombra mb-5" size="x-large" block
                >EM ANDAMENTO</v-btn
              >
              <br />
              <v-btn class="sombra" size="x-large" block>CONCLUÍDAS</v-btn>
              <br />
            </v-col>
          </v-row>
        </v-layout>
      </div>
    </v-row>
  </v-container>
</template>

<style scoped>
.background {
  padding-bottom: 10vh;
  background: linear-gradient(95.64deg, #e2e8d8 8.99%, #d0ebde 91.01%);
}

.sombra {
  box-sizing: border-box;
  border: 1px solid #443a81;
  box-shadow: 3px 3px 1px #007df1,
    inset -11px -5px 10px 5px rgba(70, 166, 255, 0.12);
}

.logo {
  padding-top: 5vh;
}

.card {
  min-height: 38vh;
  max-height: 38vh;
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
