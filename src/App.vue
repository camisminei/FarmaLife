<template>
  <v-app>
    <v-app-bar
    app
    color="white"
    height="80">
      <v-avatar
        class="mr-3"
        size="70">
        <v-img
        contain
        max-height="70%"
        src="https://guiadafarmacia.com.br/wp-content/uploads/2017/10/favicon-g.png"></v-img>
      </v-avatar>
      <v-toolbar-title>
        <span class="farma">Farma</span>
        <span class="life">Life</span>
      </v-toolbar-title>
    </v-app-bar>

    <v-content>
      <section id="welcome-s1">
        <v-row no-gutters>
          <v-img
            gradient="to top right, rgba(92, 92, 92, 0.534), rgba(92, 92, 92, 0.534)"
            class="imagem-background"
            :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
            src="https://images.unsplash.com/photo-1581091014534-898da33e356e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80">

            <v-theme-provider dark>
              <v-container fill-height>
                <v-row
                align="center"
                justify="center"
                class="text-center">
                  <v-col
                  class="text-center"
                  cols="12"
                  tag="h1">
                    <span class="welcome-to">
                      Welcome To
                    </span>
                    <br>
                    <span class="welcome-farmalife">FarmaLife</span>
                  </v-col>

                  <v-btn
                    class="align-self-end"
                    fab
                    outlined
                    @click="$vuetify.goTo('#about-us')"
                  >
                    <v-icon>mdi-chevron-double-down</v-icon>
                  </v-btn>

                </v-row>
              </v-container>
            </v-theme-provider>
          </v-img>
        </v-row>
      </section>

      <section id="about-us">
        <div class="py-12"></div>
        <v-container class="text-center">
          <h2 class="title-about-us">ABOUT US</h2>

          <v-responsive
          class="mx-auto mb-8"
          width="85">
          <v-divider class="mb-1"></v-divider>
          <v-divider class="m-top-div"></v-divider>
          </v-responsive>

          <v-responsive
          class="mx-auto text-about-us"
          max-width="720">
          Lorem ipsum tortor eros nullam lacinia fringilla consequat urna, sed purus sodales ultricies maecenas consectetur per, porttitor volutpat justo ante dolor luctus commodo. nunc et ligula at dictum sagittis aliquet rhoncus erat posuere leo lectus pretium, eget mattis suscipit per placerat habitasse donec tempus quisque consectetur. 
          diam nostra lobortis cubilia fringilla convallis netus duis aliquet sociosqu fringilla tincidunt ultricies arcu rhoncus, ornare habitasse augue per curabitur elementum lorem tempus quisque faucibus tortor purus. malesuada ligula dapibus felis interdum urna tempor vel nulla malesuada tempus, mattis enim quam placerat inceptos fermentum 
          eu orci sodales purus in, lacinia in elit luctus leo porttitor mattis volutpat per. 
          </v-responsive>
        </v-container>
        <div class="py-12"></div>
      </section>

      <section id="stats">
        
       <v-parallax
          dark
          :height= "$vuetify.breakpoint.smAndDown ? 700 : 500"
          src="https://images.unsplash.com/photo-1579154392013-64f6ab5c2aa3?ixlib=rb-1.2.1&auto=format&fit=crop&w=1394&q=80"
        >
          <v-container fill-height>
            <v-row class="mx-auto">
              <v-col
                v-for="[value, title] of stats"
                :key="title"
                cols="12"
                md="3"
              >
                <div class="text-center">
                  <div
                    class="display-3 font-weight-black mb-4"
                    v-text="value"
                  ></div>

                  <div
                    class="title font-weight-regular text-uppercase"
                    v-text="title"
                  ></div>
                </div>
              </v-col>
            </v-row>
          </v-container>
        </v-parallax>
      </section>


      <section id="work-with-us">
        <div class="py-12"></div>
        <v-container class="text-center">
          <h2 class="title-work-with-us">WORK WITH US</h2>

          <v-responsive
          class="mx-auto mb-8"
          width="85">
          <v-divider class="mb-1"></v-divider>
          <v-divider class="m-top-div"></v-divider>
          </v-responsive>

          <v-responsive
          class="mx-auto text-work-with-us"
          max-width="720">
          <h3 class="font-italic">Come join our team!</h3><br>
          Lorem ipsum tortor eros nullam lacinia fringilla consequat urna, sed purus sodales ultricies maecenas consectetur per, porttitor volutpat justo ante dolor luctus commodo. nunc et ligula at dictum sagittis aliquet rhoncus erat posuere leo lectus pretium, eget mattis suscipit per placerat habitasse donec tempus quisque consectetur. 
          </v-responsive>

          <v-responsive
          class="mx-auto text-work-with-us"
          max-width="720">
          
          <h3 class="mt-10 font-italic">Benefits</h3><br>

          <p>Career path;</p> 
          <p>Training and qualification of employees;</p>
          <p>Market compatible wage;</p>
          <p>Health / dental plan;</p>
          <p>Meal or food aid;</p>
          <p>Group life insurance;</p>
          <p>Transportation vouchers;</p>
          <p>Profit sharing and Pharmacy discount.</p>
          </v-responsive>

        </v-container>
        <div class="py-12"></div>
      </section>
      
      <v-sheet
        id="contact"
        color="#616161"
        dark
        tag="section"
        >
          <div class="py-12"></div>

          <v-container class="text-center">
              <h2 class="title-contact">CONTACT</h2>
              <v-responsive
              class="mx-auto mb-8"
              width="85">
              <v-divider class="mb-1"></v-divider>
              <v-divider class="m-top-div"></v-divider>
              </v-responsive>
          <v-theme-provider light>

            <v-col cols="12" sm="12" md="12">

            <v-text-field
              label="Solo"
              placeholder="Name"
              solo>
            </v-text-field>

              <v-text-field
              label="Solo"
              placeholder="Email"
              solo>
            </v-text-field>

            <v-text-field
              label="Solo"
              placeholder="Number"
              solo>
            </v-text-field>
          
            <v-textarea
              solo
              name="input-7-4"
              label="Solo"
              placeholder="Message"
            ></v-textarea>
          </v-col>

          </v-theme-provider>
          </v-container>
      </v-sheet>

      <v-footer
      class="rodape"
      color="#EF5350"
      height="60vh">

        <div class="rodape">
          {{ new Date().getFullYear()}} - <strong>Vuetify</strong> - Made with ♥  by itsmneii
        </div>

      </v-footer>
    </v-content>
  </v-app>
</template>

<script>
export default {
  
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Exo+2:wght@700;900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Archivo:wght@400;700&amp;family=Poppins:wght@400;600&amp;display=swap');


span{
  font-family: 'Exo 2', sans-serif;
  font-weight: 700;
  font-size: 1.8rem;
}

.farma{
  color: red;
}

.life{
  color: rgb(100, 100, 100);
  
}

.welcome-to{
  font-weight: 100;
  font-size: 2.8rem;
  color: rgba(255, 254, 254, 0.966);
}

.welcome-farmalife{
  font-weight: 700;
  font-size: 5.6rem;
  color: rgba(255, 255, 255, 0.966);;
}

h2{
  font-family: Archivo;
  font-size: 3rem;
}

.title-about-us,
.title-work-with-us{
  color: rgb(124, 124, 124);
}

.title-contact{
  color: rgba(255, 251, 251, 0.932);
}

.text-about-us,
.text-work-with-us{
  font-family: Archivo;
  font-size: 1.2rem;
  justify-content: center;
  text-align: center;
  color: rgb(124, 124, 124);
}

.m-top-div{
  margin-top: 0.9rem;
}

.v-application p {
  margin-bottom: 0;
}

.rodape{
  text-align: center;
  justify-content: center;
  color:rgba(255, 251, 251, 0.932);
}


</style>


