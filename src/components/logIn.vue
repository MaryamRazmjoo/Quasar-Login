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
            v-model="enteredData.phone"
            placeholder="شماره همراه"
          >
          </q-input>
          <q-input
            class="q-mb-md"
            type="password"
            bottom-slots
            v-model="enteredData.password"
            placeholder="رمز ورود"
          >
          </q-input>
        </q-form>
      </q-card-section>
      <q-card-actions>
        <q-btn
          class="full-width q-mb-md"
          color="yellow"
          text-color="black"
          label="ورود"
          @click="logIn"
        />
      </q-card-actions>
    </q-card>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'logIn',
  data () {
    return {
      enteredData: {
        phone: null,
        password: null
      }
    }
  },
  methods: {
    logIn () {
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
.logIn-card{
  margin-top: 200px;
  .form-logIn {
    width: 500px;
  }
}
</style>
