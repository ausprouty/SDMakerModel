<script>
import SQLiteService from '@/services/SQLiteService.js'
import { useFindSummaries, useFindCollapsible, usePopUp} from "@/assets/javascript/revealText.js"
import { useRevealMedia } from "@/assets/javascript/revealMedia.js"
import { useShare} from "@/assets/javascript/share.js"
import VueImageZoomer from '@/components/VueImageZoomer.vue'
import '@/assets/styles/vueImageZoomer.css';


export default {
  components: {
    VueImageZoomer
  },
   methods:{
    async addNote(noteid){
       var noteText = document.getElementById(noteid).value
       var noteHeight = await SQLiteService.addNote(noteid, this.$route.name, noteText)
       document.getElementById(noteid).style.height = noteHeight
    },
    goToPageAndSetReturn(gotoPath){
      localStorage.setItem("returnpage", this.$route.name);
      this.$router.push({
        path: gotoPath,
      })
    },
    pageGoBack(returnto){
      if (localStorage.getItem("returnpage")) {
        returnto = localStorage.getItem("returnpage");
        localStorage.removeItem("returnpage")
      }
      this.$router.push({
        name: returnto,
      })
    },
    popUp(verse){
      usePopUp(verse)
    },
    share(what, v1, v2){
      useShare(what, v1, v2)
    },
    vuePush(id){
      this.$router.push({
        name: id,
      })
    },
  },
  async mounted() {
    useFindSummaries()
    useFindCollapsible()
    useRevealMedia()
    await SQLiteService.notes(this.$route.name)
  },
}
</script>
<template>
  <div id="nav">
    <div class="nav full internal-link" @click="this.pageGoBack('index.html')">
        <img src="@/assets/sites/mc2/images/ribbons/back-ribbon-mc2.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<h1>Period 5: Sending, Multiplying and Coaching Movements</h1>
<div id="showVideoOptions"></div>
  <h2>3rd Missionary Journey from Antioch</h2>

<p>   
    <div class="zoom-image">
    <vue-image-zoomer
    regular="home/globa544/mc2.capacitor/eng/public/images/zoom//sites/mc2/content/M2/eng/multiply3/Trip3.png" 
    zoom="home/globa544/mc2.capacitor/eng/public/images/zoom//sites/mc2/content/M2/eng/multiply3/Trip3.png" :zoom-amount="3" img-class="img-fluid" alt="">
    <img src="@/assets/sites/mc2/content/M2/eng/multiply3/Trip3.png" img-class="img-fluid" />
    </vue-image-zoomer>
    </div></p>

<p>[52 -57 AD]</p>

<h2>Summary</h2>

<p>This period covers about five years. Several movement centers have already been multiplying disciples and churches for over 6 years. During this period, a large mission-sending movement center is established in Ephesus. While church planting work is taking root in Ephesus, leaders are being sent out and existing churches are being coached. The period is marked by daily training, dramatic miracles, letter writing and Kingdom expansion so that the entire Eastern part of the Roman Empire can eventually be reached.</p>

<h2>Letters written during this period</h2>

<ul>
	<li>1 Corinthians, 55 AD</li>
	<li>2 Corinthians, 56 AD</li>
	<li>Romans, 57 AD</li>
</ul>


<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social" @click="share('languages', '', '')">
				  <img class="social" src="@/assets/sites/mc2/images/menu/languages.png" />
			  </td>
			  
			<td class="social"  @click="share('android', 'eng', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Period 5: Sending, Multiplying and Coaching Movements: ', '/content/M2/eng/multiply3/multiply3intro5.html')">
				<img class="social" src="@/assets/sites/mc2/images/standard/Share.png" />
			</td>
		</tr>
	</tbody>
</table>
<div class="footer">
<p class="footer">MC2</p>
<p class="footer" @click="share('website', 'https://GlobalChurchMovements.org', '')"> GlobalChurchMovements.org</p>
</div>

<!-- end mc2 sdcard languageFooter -->
</div><!--- Created by publishPage-->

</template>
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->