<template>
  <v-container fluid class="background fill-height">
    <v-row class="text-center flex-column">
      <!-- LogoGestor -->
      <div>
        <v-container block class="d-flex justify-center align-baseline logo">
          <v-img src="/logo-mg.png" height="120"></v-img>
        </v-container>
      </div>
      <div>
        <v-layout>
          <v-row justify="center">
            <v-col cols="11" sm="8" md="6" lg="4" xl="3">
              <!-- CardBranco -->
              <v-card class="card px-6 py-8 mb-5 sombra">
                <v-form v-model="form" @submit.prevent="onSubmit">
                  <v-text-field
                    v-model="email"
                    :readonly="loading"
                    :rules="[required]"
                    class="mb-2"
                    clearable
                    label="Nome"
                  ></v-text-field>

                  <v-text-field
                    v-model="password"
                    :readonly="loading"
                    :rules="[required]"
                    clearable
                    label="Senha"
                    placeholder="Insira sua senha"
                  ></v-text-field>
                  <!-- LoginBotao -->
                  <v-btn
                    class="sombra"
                    size="x-large"
                    block
                    :loading="loading"
                    @click="loading = !loading"
                    type="submit"
                    >LOGIN</v-btn
                  >
                </v-form>
              </v-card>
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

.texto-ft {
  font-weight: 500;
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

.logo {
  padding-top: 5vh;
}

.card {
  min-height: 38vh;
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
