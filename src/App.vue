<template>
  <v-app>
    <nav-bar />
    <v-main class="custom-main">
      <div class="flex-container">
        <v-sheet class="flex-item bg-item-1">
          <div class="logo-container">
            <img
              :src="require('./assets/RealEstateCare/RealEstateCareMetLogo.png')"
              alt="Real Estate Care Logo"
              class="real-estate-care-logo"
            />
          </div>
          <div class="container1">
            <v-sheet class="ma-2 pa-2">
              <div class="logo-container-mail">
                <div class="logo-mail" v-html="svgCodeMail"></div>
                <div class="ma-2">info@loremipsumdolor.nl</div>
              </div>
            </v-sheet>
            <v-sheet class="ma-2 pa-2">
              <div class="logo-container-location">
                <div class="logo-mail" v-html="svgCodeLocation"></div>
                <div class="ma-2">Dummy Road 125x <br />Street Location, City, Area</div>
              </div>
            </v-sheet>
            <v-sheet class="ma-2 pa-2">
              <div class="logo-container-phone">
                <div class="logo-mail" v-html="svgCodePhone"></div>
                <div class="ma-2">+00 1234 5678 9012</div>
              </div>
            </v-sheet>
          </div>
        </v-sheet>
        <v-sheet class="flex-item bg-item-2"></v-sheet>
        <v-sheet class="flex-item bg-item-3"></v-sheet>
        <div class="circle-container">
          <div class="circle1"></div>
          <div class="circle2"></div>
          <div class="circle3"></div>
          <div class="circle4"></div>
        </div>
      </div>
      <div class="flexbox-on-top">
        <div class="text-container">
          <h2>RealEstateCare</h2>
          <p>Is een dienstverlenende organisatie die voor verschillende opdrachtgever zoals woningcorporaties en vastgoedontwikkelaars woningen onderhoudt, verbetert en inspecteert. Hier spelen veel en ingewikkelde bedrijfsprocessen en wordt veel data verwerkt. Eén aspect van deze bedrijfsprocessen is het op locatie inspecteren van een pand en bet opnemen van schade (door huurders, ongedierte of calamiteiten), achterstallig onderbood, verouderde installaties, brandgevaarlijke situaties en al dan niet ongewenste modificaties van huurders. </p>
          <br />
          <p>Van oudsher werd dit met specifieke formulieren gedaan, maar enkele jaren geleden is de overstap gemaakt naar een specifieke webapplicatie voor deze workflow. Inspecteurs konden zelf vanaf de eigen werkplek via de webapplicatie rapportages maken en digitale foto's uploaden. </p>
          <br />
          <p>Echter, de tijden veranderen en er wordt nu gekeken boe deze workflow nóg beter geïntegreerd kan worden met de andere workflows, zoals bet uitbrengen van offertes voor onderbood en er een koppeling met bet crm-systeem ontsmet waardoor de inspecties direct gekoppeld zijn aan de huurderaccounts. Om dit te kunnen stroomlijnen en flexibel in te richten (ook met bet oog op toekomstige aanpassingen) moet de nieuw te omwikkelen mobiele webapplicatie via een (reeds ontwikkelde) web API (restful API) met de backend communiceren. Via deze API moeten inspectierapporten direct verwerkt worden in de backend zodat offertes voor onderhoud of aanpassingen vrijwel direct aangemaakt en gespecificeerd kunnen worden, huurders aangeschreven kunnen worden en eventueel derden ingeschakeld kunnen worden voor metingen, ontruimingen etc. </p>
        </div>
      </div>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      svgCodeMail: `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
        <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
      </svg>`,
      svgCodeLocation: `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
        <path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
        <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
      </svg>`,
      svgCodePhone: `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
        <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z" />
      </svg>`,
    };
  },
};
</script>

<style>
  .ma-2.small-font {
    font-size: 4px;
  }
.ma-2 {
  font-size: 14px;
}

.custom-main {
  position: relative;
  overflow: hidden;
  height: 100vh;
}

.flex-container {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.flex-item {
  flex: 1;
}

.bg-item-1 {
  background-color: #F5F5F5;
}

.bg-item-2 {
  background-color: #FAFAFA;
}

.bg-item-3 {
  background-color: #FFFFFF;
}

.circle-container {
  position: absolute;
  top: 20px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  justify-content: space-evenly;
}

@media screen and (min-width: 640px) and (max-width: 750px) {
  .flexbox-on-top {
  display: flex;
  position: absolute;
  top: 690px;
  left: 70px;
  width: 520px;
  height: 100px;
  align-items: center;
  justify-content: center;
}

.ma-2 {
  background-color: transparent;
}

.logo-container-phone {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-phone {
  width: 20px;
  height: 20px;
}

.logo-container-location {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-location {
  width: 20px;
  height: 20px;
}

.logo-container-mail {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-mail {
  width: 20px;
  height: 20px;
}

  .container1 {
  position: relative;
  width: 400px;
  height: 100px;
  background-color: transparent; 
  right: -360px;
  top: 90px;
}

.container1 .ma-2 {
  background-color: transparent;
}

  .real-estate-care-logo {
  position: absolute;
  left: 100px; /* Adjust the left position as per your preference */
  top: 17%;
  transform: translateY(-50%);
  max-width: 80%;
  max-height: auto;
  width: 200px; /* Set the desired width for the image */
}

  .circle1 {
  position: absolute;
  width: 380vw;
  height: 30vh;
  top: -8vh;
  left: -110vh;
  border-radius: 50%;
  background-image: linear-gradient(rgba(71, 94, 108, 1), rgba(20, 27, 31, 1));
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle2 {
  width: 440vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 1;
  position: absolute;
  top: -7vh;
  left: -120vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle3 {
  position: absolute;
  width: 600vw;
  height: 30vh;
  top: 102vh;
  left: 180vh;
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle4 {
  width: 500vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: #F5F5F5;
  z-index: 1;
  position: absolute;
  top: 102vh;
  left: 140vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}
}

@media screen and (min-width: 750px) and (max-width: 768px) {
  .flexbox-on-top {
  display: flex;
  position: absolute;
  top: 700px;
  left: 110px;
  width: 600px;
  height: 100px;
  align-items: center;
  justify-content: center;
}

.ma-2 {
  background-color: transparent;
}

.logo-container-phone {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-phone {
  width: 20px;
  height: 20px;
}

.logo-container-location {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-location {
  width: 20px;
  height: 20px;
}

.logo-container-mail {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-mail {
  width: 20px;
  height: 20px;
}

  .container1 {
  position: relative;
  width: 400px;
  height: 100px;
  background-color: transparent; 
  right: -470px;
  top: 120px;
}

.container1 .ma-2 {
  background-color: transparent;
}

  .real-estate-care-logo {
  position: absolute;
  left: 100px; /* Adjust the left position as per your preference */
  top: 17%;
  transform: translateY(-50%);
  max-width: 80%;
  max-height: auto;
  width: 200px; /* Set the desired width for the image */
}

  .circle1 {
  position: absolute;
  width: 400vw;
  height: 30vh;
  top: -8vh;
  left: -110vh;
  border-radius: 50%;
  background-image: linear-gradient(rgba(71, 94, 108, 1), rgba(20, 27, 31, 1));
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle2 {
  width: 460vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 1;
  position: absolute;
  top: -7vh;
  left: -120vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle3 {
  position: absolute;
  width: 600vw;
  height: 30vh;
  top: 102vh;
  left: 180vh;
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle4 {
  width: 500vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: #F5F5F5;
  z-index: 1;
  position: absolute;
  top: 102vh;
  left: 140vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}
}

@media screen and (min-width: 768px) and (max-width: 828px) {
  .flexbox-on-top {
  display: flex;
  position: absolute;
  top: 690px;
  left: 90px;
  width: 600px;
  height: 100px;
  align-items: center;
  justify-content: center;
}

.ma-2 {
  background-color: transparent;
}

.logo-container-phone {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-phone {
  width: 20px;
  height: 20px;
}

.logo-container-location {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-location {
  width: 20px;
  height: 20px;
}

.logo-container-mail {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-mail {
  width: 20px;
  height: 20px;
}

  .container1 {
  position: relative;
  width: 400px;
  height: 100px;
  background-color: transparent; 
  right: -470px;
  top: 100px;
}

.container1 .ma-2 {
  background-color: transparent;
}

  .real-estate-care-logo {
  position: absolute;
  left: 100px; /* Adjust the left position as per your preference */
  top: 17%;
  transform: translateY(-50%);
  max-width: 80%;
  max-height: auto;
  width: 200px; /* Set the desired width for the image */
}

  .circle1 {
  position: absolute;
  width: 290vw;
  height: 30vh;
  top: -8vh;
  left: -110vh;
  border-radius: 50%;
  background-image: linear-gradient(rgba(71, 94, 108, 1), rgba(20, 27, 31, 1));
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle2 {
  width: 360vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 1;
  position: absolute;
  top: -7vh;
  left: -120vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle3 {
  position: absolute;
  width: 470vw;
  height: 30vh;
  top: 102vh;
  left: 180vh;
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle4 {
  width: 400vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: #F5F5F5;
  z-index: 1;
  position: absolute;
  top: 102vh;
  left: 140vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}
}

@media screen and (min-width: 828px) and (max-width: 1080px) {
  .flexbox-on-top {
  display: flex;
  position: absolute;
  top: 880px;
  left: 110px;
  width: 600px;
  height: 100px;
  align-items: center;
  justify-content: center;
}

.ma-2 {
  background-color: transparent;
}

.logo-container-phone {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-phone {
  width: 20px;
  height: 20px;
}

.logo-container-location {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-location {
  width: 20px;
  height: 20px;
}

.logo-container-mail {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-mail {
  width: 20px;
  height: 20px;
}

  .container1 {
  position: relative;
  width: 400px;
  height: 100px;
  background-color: transparent; 
  right: -470px;
  top: 190px;
}

.container1 .ma-2 {
  background-color: transparent;
}

  .real-estate-care-logo {
  position: absolute;
  left: 100px; /* Adjust the left position as per your preference */
  top: 17%;
  transform: translateY(-50%);
  max-width: 80%;
  max-height: auto;
  width: 200px; /* Set the desired width for the image */
}

  .circle1 {
  position: absolute;
  width: 500vw;
  height: 30vh;
  top: -8vh;
  left: -110vh;
  border-radius: 50%;
  background-image: linear-gradient(rgba(71, 94, 108, 1), rgba(20, 27, 31, 1));
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle2 {
  width: 560vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 1;
  position: absolute;
  top: -7vh;
  left: -120vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle3 {
  position: absolute;
  width: 750vw;
  height: 30vh;
  top: 102vh;
  left: 180vh;
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle4 {
  width: 620vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: #F5F5F5;
  z-index: 1;
  position: absolute;
  top: 102vh;
  left: 140vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}
}

@media screen and (min-width: 1080px) and (max-width: 1366px) {
  .flexbox-on-top {
  display: flex;
  position: absolute;
  top: 900px;
  left: 130px;
  width: 810px;
  height: 100px;
  align-items: center;
  justify-content: center;
}

.ma-2 {
  background-color: transparent;
}

.logo-container-phone {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-phone {
  width: 20px;
  height: 20px;
}

.logo-container-location {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-location {
  width: 20px;
  height: 20px;
}

.logo-container-mail {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-mail {
  width: 20px;
  height: 20px;
}

  .container1 {
  position: relative;
  width: 400px;
  height: 100px;
  background-color: transparent; 
  right: -650px;
  top: 220px;
}

.container1 .ma-2 {
  background-color: transparent;
}

  .real-estate-care-logo {
  position: absolute;
  left: 190px; /* Adjust the left position as per your preference */
  top: 17%;
  transform: translateY(-50%);
  max-width: 80%;
  max-height: auto;
  width: 200px; /* Set the desired width for the image */
}

  .circle1 {
  position: absolute;
  width: 410vw;
  height: 30vh;
  top: -8vh;
  left: -110vh;
  border-radius: 50%;
  background-image: linear-gradient(rgba(71, 94, 108, 1), rgba(20, 27, 31, 1));
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle2 {
  width: 460vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 1;
  position: absolute;
  top: -7vh;
  left: -120vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle3 {
  position: absolute;
  width: 620vw;
  height: 30vh;
  top: 102vh;
  left: 180vh;
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle4 {
  width: 510vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: #F5F5F5;
  z-index: 1;
  position: absolute;
  top: 102vh;
  left: 140vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}
}

@media screen and (min-width: 1366px) and (max-width: 1536px) {
  .flexbox-on-top {
  display: flex;
  position: absolute;
  top: 490px;
  left: 90px;
  width: 1200px;
  height: 100px;
  align-items: center;
  justify-content: center;
}

.ma-2 {
  background-color: transparent;
}

.logo-container-phone {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-phone {
  width: 20px;
  height: 20px;
}

.logo-container-location {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-location {
  width: 20px;
  height: 20px;
}

.logo-container-mail {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-mail {
  width: 20px;
  height: 20px;
}

  .container1 {
  position: relative;
  width: 400px;
  height: 100px;
  background-color: transparent; 
  right: -1080px;
  top: 20px;
}

.container1 .ma-2 {
  background-color: transparent;
}

  .real-estate-care-logo {
  position: absolute;
  left: 100px; /* Adjust the left position as per your preference */
  top: 20%;
  transform: translateY(-50%);
  max-width: 80%;
  max-height: auto;
  width: 200px; /* Set the desired width for the image */
}

  .circle1 {
  position: absolute;
  width: 160vw;
  height: 30vh;
  top: -8vh;
  left: -110vh;
  border-radius: 50%;
  background-image: linear-gradient(rgba(71, 94, 108, 1), rgba(20, 27, 31, 1));
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle2 {
  width: 200vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 1;
  position: absolute;
  top: -7vh;
  left: -120vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle3 {
  position: absolute;
  width: 250vw;
  height: 30vh;
  top: 102vh;
  left: 180vh;
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle4 {
  width: 230vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: #F5F5F5;
  z-index: 1;
  position: absolute;
  top: 102vh;
  left: 140vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}
}

@media screen and (min-width: 1536px) and (max-width: 1668px) {
  .flexbox-on-top {
  display: flex;
  position: absolute;
  top: 950px;
  left: 180px;
  width: 1200px;
  height: 100px;
  align-items: center;
  justify-content: center;
}

.ma-2 {
  background-color: transparent;
}

.logo-container-phone {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-phone {
  width: 20px;
  height: 20px;
}

.logo-container-location {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-location {
  width: 20px;
  height: 20px;
}

.logo-container-mail {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-mail {
  width: 20px;
  height: 20px;
}

  .container1 {
  position: relative;
  width: 400px;
  height: 100px;
  background-color: transparent; 
  right: -970px;
  top: 250px;
}

.container1 .ma-2 {
  background-color: transparent;
}

  .real-estate-care-logo {
  position: absolute;
  left: 300px; /* Adjust the left position as per your preference */
  top: 17%;
  transform: translateY(-50%);
  max-width: 80%;
  max-height: auto;
  width: 200px; /* Set the desired width for the image */
}

  .circle1 {
  position: absolute;
  width: 290vw;
  height: 30vh;
  top: -8vh;
  left: -110vh;
  border-radius: 50%;
  background-image: linear-gradient(rgba(71, 94, 108, 1), rgba(20, 27, 31, 1));
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle2 {
  width: 350vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 1;
  position: absolute;
  top: -7vh;
  left: -120vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle3 {
  position: absolute;
  width: 460vw;
  height: 30vh;
  top: 102vh;
  left: 180vh;
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle4 {
  width: 380vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: #F5F5F5;
  z-index: 1;
  position: absolute;
  top: 102vh;
  left: 140vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}
}

@media screen and (min-width: 1668px) and (max-width: 1920px) {
  .flexbox-on-top {
  display: flex;
  position: absolute;
  top: 1000px;
  left: 210px;
  width: 1250px;
  height: 100px;
  align-items: center;
  justify-content: center;
}

.ma-2 {
  background-color: transparent;
}

.logo-container-phone {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-phone {
  width: 20px;
  height: 20px;
}

.logo-container-location {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-location {
  width: 20px;
  height: 20px;
}

.logo-container-mail {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-mail {
  width: 20px;
  height: 20px;
}

  .container1 {
  position: relative;
  width: 400px;
  height: 100px;
  background-color: transparent; 
  right: -1000px;
  top: 290px;
}

.container1 .ma-2 {
  background-color: transparent;
}

  .real-estate-care-logo {
  position: absolute;
  left: 300px; /* Adjust the left position as per your preference */
  top: 17%;
  transform: translateY(-50%);
  max-width: 80%;
  max-height: auto;
  width: 200px; /* Set the desired width for the image */
}

  .circle1 {
  position: absolute;
  width: 320vw;
  height: 30vh;
  top: -8vh;
  left: -110vh;
  border-radius: 50%;
  background-image: linear-gradient(rgba(71, 94, 108, 1), rgba(20, 27, 31, 1));
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle2 {
  width: 370vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 1;
  position: absolute;
  top: -7vh;
  left: -120vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle3 {
  position: absolute;
  width: 500vw;
  height: 30vh;
  top: 102vh;
  left: 180vh;
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle4 {
  width: 410vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: #F5F5F5;
  z-index: 1;
  position: absolute;
  top: 102vh;
  left: 140vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}
}

@media screen and (min-width: 1920px) and (max-width: 2560px) {
  .flexbox-on-top {
  display: flex;
  position: absolute;
  top: 540px;
  left: 210px;
  width: 1500px;
  height: 100px;
  align-items: center;
  justify-content: center;
}

.ma-2 {
  background-color: transparent;
}

.logo-container-phone {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-phone {
  width: 20px;
  height: 20px;
}

.logo-container-location {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-location {
  width: 20px;
  height: 20px;
}

.logo-container-mail {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-mail {
  width: 20px;
  height: 20px;
}

  .container1 {
  position: relative;
  width: 400px;
  height: 100px;
  background-color: transparent; 
  right: -1300px;
  top: 70px;
}

.container1 .ma-2 {
  background-color: transparent;
}

  .real-estate-care-logo {
  position: absolute;
  left: 200px; /* Adjust the left position as per your preference */
  top: 17%;
  transform: translateY(-50%);
  max-width: 80%;
  max-height: auto;
  width: 200px; /* Set the desired width for the image */
}

  .circle1 {
  position: absolute;
  width: 100vw;
  height: 30vh;
  top: -8vh;
  left: -110vh;
  border-radius: 50%;
  background-image: linear-gradient(rgba(71, 94, 108, 1), rgba(20, 27, 31, 1));
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle2 {
  width: 150vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 1;
  position: absolute;
  top: -7vh;
  left: -120vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle3 {
  position: absolute;
  width: 150vw;
  height: 30vh;
  top: 102vh;
  left: 180vh;
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle4 {
  width: 150vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: #F5F5F5;
  z-index: 1;
  position: absolute;
  top: 102vh;
  left: 140vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}
}

@media screen and (min-width: 2560px){
  .flexbox-on-top {
  display: flex;
  position: absolute;
  top: 650px;
  left: 280px;
  width: 2000px;
  height: 100px;
  align-items: center;
  justify-content: center;
}

.ma-2 {
  background-color: transparent;
}

.logo-container-phone {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-phone {
  width: 20px;
  height: 20px;
}

.logo-container-location {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-location {
  width: 20px;
  height: 20px;
}

.logo-container-mail {
  display: flex;
  align-items: center;
  margin-right: 10px;
}

.logo-mail {
  width: 20px;
  height: 20px;
}

  .container1 {
  position: relative;
  width: 400px;
  height: 100px;
  background-color: transparent; 
  right: -1900px;
  top: 130px;
}

.container1 .ma-2 {
  background-color: transparent;
}

  .real-estate-care-logo {
  position: absolute;
  left: 270px; /* Adjust the left position as per your preference */
  top: 17%;
  transform: translateY(-50%);
  max-width: 80%;
  max-height: auto;
  width: 200px; /* Set the desired width for the image */
}

  .circle1 {
  position: absolute;
  width: 65vw;
  height: 30vh;
  top: -8vh;
  left: -110vh;
  border-radius: 50%;
  background-image: linear-gradient(rgba(71, 94, 108, 1), rgba(20, 27, 31, 1));
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle2 {
  width: 100vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 1;
  position: absolute;
  top: -7vh;
  left: -120vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle3 {
  position: absolute;
  width: 100vw;
  height: 30vh;
  top: 102vh;
  left: 180vh;
  border-radius: 50%;
  background-color: rgba(0, 170, 162, 1);
  z-index: 2;
  transform: translate(-50%, -50%);
  transform-origin: center;
}

.circle4 {
  width: 100vw; /* Adjust the width using viewport units */
  height: 30vh; /* Adjust the height using viewport units */
  border-radius: 50%;
  background-color: #F5F5F5;
  z-index: 1;
  position: absolute;
  top: 102vh;
  left: 140vh;
  transform: translate(-50%, -50%);
  transform-origin: center;
}
}

</style>