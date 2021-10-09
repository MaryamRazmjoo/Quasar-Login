<template>
  <div class="flex flex-center">
    <q-card
      class="signIn-card"
    >
      <q-card-section>
        <q-form class="form-signIn">
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
            bottom-slots
            v-model="text"
            placeholder="کدملی"
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
          label="ثبت نام"
        />
      </q-card-actions>
    </q-card>
  </div>
</template>

<script>
export default {
  name: 'signIn'
}
</script>
<style lang="scss" scoped>
.signIn-card{
  margin-top: 200px;
  .form-signIn {
    width: 500px;
  }
}
</style>
