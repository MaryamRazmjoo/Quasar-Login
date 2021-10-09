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
            placeholder="شماره همراه"
            v-model="enteredData.phone"
          >
          </q-input>
          <q-input
            class="q-mb-md"
            bottom-slots
            placeholder="کدملی"
            v-model="enteredData.nationalCode"
          >
          </q-input>
        </q-form>
      </q-card-section>
      <q-card-actions>
        <q-btn
          class="full-width q-mb-md"
          color="yellow"
          text-color="black"
          label="ثبت نام"
          @click="signIn"
        />
      </q-card-actions>
    </q-card>
  </div>
</template>
<script>
import axios from 'axios'

export default {
  name: 'signIn',
  data () {
    return {
      enteredData: {
        phone: null,
        nationalCode: null
      }
    }
  },
  methods: {
    signIn () {
      axios.post('alaatv.com/api/v2/login', {
        mobile: this.enteredData.phone,
        password: this.enteredData.nationalCode
      })
        .then(response => {
          console.log('res: ', response)
        })
        .catch(error => {
          console.log('err: ', error)
        })
    }
  }
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
