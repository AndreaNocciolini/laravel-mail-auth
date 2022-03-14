<template>
  <div>
    <div class="row">
      <div class="col">
          Contact Us
      </div>
    </div>
    <div class="row">
        <div class="col">
            <form @submit.prevent="sendForm">

                <div class="form-group">
                    <label for="name">Nome</label>
                    <input v-model="name" type="text" class="form-control" id="name" name="name">
                </div>

                <div class="form-group">
                    <label for="email">Email</label>
                    <input v-model="email" type="email" class="form-control" id="email" name="email" placeholder="name@example.com">
                </div>

                <div class="form-group">
                    <label for="message">Messaggio</label>
                    <textarea v-model="message" class="form-control" id="message" name="message" rows="3"></textarea>
                </div>

                <button type="submit" class="btn btn-primary">Send</button>

            </form>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'Contact',
    data() {
        return {
            name: null,
            email: null,
            message: null,
        }
    },
    methods: {
        sendForm(){
            axios.post('/api/contact', 
                {
                    'name': this.name,
                    'email': this.email,
                    'message': this.message,
                }
            )
            .then((result)=>
                console.log(result.data)
                
            )
            .catch((error) =>
                console.log(error)
            )
        }
    }
}
</script>

<style>

</style>