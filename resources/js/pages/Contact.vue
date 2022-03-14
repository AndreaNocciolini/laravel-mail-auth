<template>
  <div>
    <div class="row">
      <div class="col">
          Contact Us
      </div>
    </div>
    <div class="row">
        <div class="col">
            <form @submit.prevent="">

                <div class="form-group">
                    <label for="name">Nome</label>
                    <input type="text" class="form-control" id="name" name="name">
                </div>

                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" class="form-control" id="email" name="email" placeholder="name@example.com">
                </div>

                <div class="form-group">
                    <label for="message">Messaggio</label>
                    <textarea class="form-control" id="message" name="message" rows="3"></textarea>
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
}
</script>

<style>

</style>