<template>
   <div>
       <div class="row">
            <div class="col">
                <h1 class=" text-uppercase font-weight-bold title is-1">Contact Me</h1>
                <h2 class=" font-weight-light title is-3">Get in touch</h2>
                <p>You'll find us in Westminister, on a fresh, modern campus that is home to over 2500 students and staff. Look around and see what we have to offer. You won't be disappointed.</p>
                    <section>
                        <b-field label="Name" placeholder="Your Name">
                            <b-input placeholder="Your Name"></b-input>
                        </b-field>

                        <b-field label="Email Address"
                            type=""
                            message="We will keep your email safe will us.">
                            <b-input type="email"
                                placeholder="Your Email"
                                maxlength="30">
                            </b-input>
                        </b-field>

                        <b-field label="Username"
                            type="is-success"
                            message="This username is available">
                            <b-input 
                            placeholder="Username" maxlength="30"></b-input>
                        </b-field>

                        <b-field label="Password">
                            <b-input type="password"
                                value="iwantmytreasure"
                                password-reveal>
                            </b-input>
                        </b-field>

                        <b-field label="Message">
                            <b-input maxlength="200" type="textarea"></b-input>
                        </b-field>

                            <b-button type="is-primary is-light" class="mb-5" >Send Message</b-button>
                    </section>
            </div>
            <div class="col text-center mt-5">
                      <img alt="logo" src="../assets/logo1.png">

            </div>
        </div>
    </div>
    
</template>

<script>

export default {
  name: 'contact',
  components: {
    
  }
}
</script>

<style>

 
</style>