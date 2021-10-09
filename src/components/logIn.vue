<template>
  <div class="flex flex-center">
    <q-card
      class="logIn-card"
    >
      <q-card-section>
        <q-form class="form-logIn">
          <q-input
            class="q-mb-md"
            bottom-slots
            v-model="text"
            placeholder="شماره همراه"
            counter
          >
            <template v-slot:append>
              <q-icon name="close" @click="text = ''" class="cursor-pointer"/>
            </template>

            <template v-slot:hint>
              Field hint
            </template>
          </q-input>
          <q-input
            class="q-mb-md"
            type="password"
            bottom-slots
            v-model="text"
            placeholder="رمز ورود"
            counter
          >
            <template v-slot:append>
              <q-icon name="close" @click="text = ''" class="cursor-pointer"/>
            </template>

            <template v-slot:hint>
              Field hint
            </template>
          </q-input>
        </q-form>
      </q-card-section>
      <q-card-actions>
        <q-btn
          class="full-width"
          color="yellow"
          text-color="black"
          label="ورود"
        />
      </q-card-actions>
    </q-card>
  </div>
</template>

<script>
export default {
  name: 'logIn'
}
</script>

<style lang="scss" scoped>
.logIn-card{
  margin-top: 200px;
  .form-logIn {
    width: 500px;
  }
}
</style>
