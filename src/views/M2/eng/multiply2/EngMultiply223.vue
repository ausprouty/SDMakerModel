<script>
import SQLiteService from '@/services/SQLiteService.js'
import { useFindSummaries, useFindCollapsible, usePopUp} from "@/assets/javascript/revealText.js"
import { useRevealMedia } from "@/assets/javascript/revealMedia.js"
import { useShare} from "@/assets/javascript/share.js"


export default {
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
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>23.</h1></div>
                        <div class="chapter_title ltr"><h1>Fishing for Men Expedition Six</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle"><span class="back">LOOKING BACK</span></div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2 class="back">+ Praise</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p class="back"><em>Read a scripture and sing worship songs.</em></p>

<ul>
	<li class="nobreak-final-final">(Optional) Jesus Christ is Lord, to the glory of God the Father. He wants all men to be saved and to come to the knowledge of the truth. For there is one God and one mediator also between God and man, the man Jesus Christ, who gave himself as a ransom for all. (<span class="popup-link" @click = "popUp('pop1')"> Philippians 2:11</span>b;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>and every tongue acknowledge that Jesus Christ is Lord,<br />
	&nbsp;&nbsp;&nbsp;&nbsp;to the glory of God the Father.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop2')"> 1 Timothy 2:4-6</span>a).&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>who wants all people to be saved and to come to a knowledge of the truth.<sup class="versenum">5&nbsp;</sup>For there is one God and one mediator between God and mankind, the man Christ Jesus,<sup class="versenum">6&nbsp;</sup>who gave himself as a ransom for all people.&nbsp;</p>
	</div>
	</li>
</ul>

</div>

<h2 class="back">Caring for each other</h2>

<p><em>Minister to one another&rsquo;s needs in prayer, biblical counsel and encouragement. </em></p>

<ul>
	<li>Ask each person to tell one highlight and explain one challenge they experienced this week.</li>
	<li>Ask, &ldquo;What do you want Jesus to do for you this week?&rdquo; Pray for each other&rsquo;s needs.</li>
</ul>

<h2 class="back">Celebrating&nbsp; Faithfulness</h2>

<p>Encourage loving accountability to obey Jesus</p>

<ul class="back">
	<li>Ask, &ldquo;What happened as you trusted God with your goals and I will statements?&rdquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2 class="back">+ Motivation and Encouragement</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p class="back"><em>Choose a way to cast vision for who they can become in Christ or what God can do through them by:</em></p>

<ul>
	<li class="back">a scripture that reminds them of the Father&rsquo;s Heart and of the end vision.</li>
	<li class="back">reflecting on the changes in their life since they started following Christ</li>
	<li class="back">reminding them of what God wants to do through them.</li>
</ul>

<p class="back"><span>Our vision is: <em> &ldquo;A church for every village and community, and the gospel for every person.&rdquo;</em></span></p>

<!-- begin note default -->
<div class="note-area">
    <form class = "auto_submit_item">
        <textarea class="textarea resize-ta" onkeyup= "addNote('note1Text')"  id ="note1Text" ></textarea>
    </form>
</div>
<!-- end note default -->


</div>

<ul>
</ul>



<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle"><span class="up">LOOKING UP</span></div>
</div>

<h2 class="up">Context</h2>

<ul>
	<li><span>Ask the group to tell the story from last week.</span></li>
</ul>

<h2 class="up">Read</h2>

<ul>
	<li class="up">Read or watch Luke 5:27-39 two times as others listen.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Read Luke 5:27-39</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<h3>Jesus Calls Levi and Eats With Sinners</h3>

<p><sup class="versenum">27&nbsp;</sup>After this, Jesus went out and saw a tax collector by the name of Levi sitting at his tax booth. &ldquo;Follow me,&rdquo; Jesus said to him,<sup class="versenum">28&nbsp;</sup>and Levi got up, left everything and followed him.</p>

<p><sup class="versenum">29&nbsp;</sup>Then Levi held a great banquet for Jesus at his house, and a large crowd of tax collectors and others were eating with them.<sup class="versenum">30&nbsp;</sup>But the Pharisees and the teachers of the law who belonged to their sect complained to his disciples, &ldquo;Why do you eat and drink with tax collectors and sinners?&rdquo;</p>

<p><sup class="versenum">31&nbsp;</sup>Jesus answered them, &ldquo;It is not the healthy who need a doctor, but the sick.<sup class="versenum">32&nbsp;</sup>I have not come to call the righteous, but sinners to repentance.&rdquo;</p>

<h3>Jesus Questioned About Fasting</h3>

<p><sup class="versenum">33&nbsp;</sup>They said to him, &ldquo;John&rsquo;s disciples often fast and pray, and so do the disciples of the Pharisees, but yours go on eating and drinking.&rdquo;</p>

<p><sup class="versenum">34&nbsp;</sup>Jesus answered, &ldquo;Can you make the friends of the bridegroom fast while he is with them?<sup class="versenum">35&nbsp;</sup>But the time will come when the bridegroom will be taken from them; in those days they will fast.&rdquo;</p>

<p><sup class="versenum">36&nbsp;</sup>He told them this parable: &ldquo;No one tears a piece out of a new garment to patch an old one. Otherwise, they will have torn the new garment, and the patch from the new will not match the old.<sup class="versenum">37&nbsp;</sup>And no one pours new wine into old wineskins. Otherwise, the new wine will burst the skins; the wine will run out and the wineskins will be ruined.<sup class="versenum">38&nbsp;</sup>No, new wine must be poured into new wineskins.<sup class="versenum">39&nbsp;</sup>And no one after drinking old wine wants the new, for they say, &lsquo;The old is better.&rsquo;&rdquo;</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/eng/video/multiply2/223.mp4" type="button" class="external-movie">
         Watch &nbsp;Luke 5:27-39&nbsp;</button>
    <div class="collapsed"></div>

<h2 class="up">Discovery Discussion (Everyone answers)</h2>

<ul class="up">
	<li><span>What caught your attention or what did you like best? Why?</span></li>
	<li><span>What is new or has developed at this point in Jesus story?</span></li>
	<li><span>What do we learn about the humanity or divinity of Jesus from this passage?</span></li>
	<li><span>How can we live differently now that we know this story?</span></li>
</ul>

<p><span>Additional Questions:</span></p>

<ul class="up">
	<li><span>What are his followers learning?</span></li>
	<li><span>What is Jesus modeling to us about life and ministry or godly leadership?</span></li>
</ul>

<!-- begin note default -->
<div class="note-area">
    <form class = "auto_submit_item">
        <textarea class="textarea resize-ta" onkeyup= "addNote('note2Text')"  id ="note2Text" ></textarea>
    </form>
</div>
<!-- end note default -->


<h2 class="up">Read, Tell and Correct</h2>

<ul class="up">
	<li>Read the story again. Have someone tell the story and ask the group to correct if necessary.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2 class="up">+ Summary</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p class="up">Matthew was also a Jew known as Levi, son of Alphaeus. He was powerful, commissioned, trusted, wealthy and protected by Rome to collect taxes from the people of Israel. But as a tax collector, he was a traitor and hated by his own people. He lived in Capernaum. He had been watching Jesus and had heard about all He was doing. Maybe He had already been considering giving up everything to follow Jesus. Clearly the Father had been preparing his heart because he responded to Jesus&rsquo; call to follow Him. Immediately, Matthew introduced Jesus to his tax collector friends. In this sixth outreach, Jesus risked His reputation by spending time with this group of hated tax collectors. Jesus demonstrated His love as He modeled extending grace to hated people. Jesus loved being known as a friend of sinners.</p>

</div>

<ul>
	<li class="nobreak-final-final"><span class="for-enrichment">Further Study: <span class="popup-link" @click = "popUp('pop3')"> Matthew 9:9-17</span>;&nbsp;</span>

	<div class="popup invisible" id="pop3"><span class="for-enrichment"><!-- begin bible --></span>

	<div>
	<div>
	<h3><span class="for-enrichment">The Calling of Matthew</span></h3>

	<p><span class="for-enrichment"><sup class="versenum">9&nbsp;</sup>As Jesus went on from there, he saw a man named Matthew sitting at the tax collector&rsquo;s booth. &ldquo;Follow me,&rdquo; he told him, and Matthew got up and followed him.</span></p>

	<p><span class="for-enrichment"><sup class="versenum">10&nbsp;</sup>While Jesus was having dinner at Matthew&rsquo;s house, many tax collectors and sinners came and ate with him and his disciples.<sup class="versenum">11&nbsp;</sup>When the Pharisees saw this, they asked his disciples, &ldquo;Why does your teacher eat with tax collectors and sinners?&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">12&nbsp;</sup>On hearing this, Jesus said, &ldquo;It is not the healthy who need a doctor, but the sick.<sup class="versenum">13&nbsp;</sup>But go and learn what this means: &lsquo;I desire mercy, not sacrifice.&rsquo; For I have not come to call the righteous, but sinners.&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">14&nbsp;</sup>Then John&rsquo;s disciples came and asked him, &ldquo;How is it that we and the Pharisees fast often, but your disciples do not fast?&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">15&nbsp;</sup>Jesus answered, &ldquo;How can the guests of the bridegroom mourn while he is with them? The time will come when the bridegroom will be taken from them; then they will fast.</span></p>

	<p><span class="for-enrichment"><sup class="versenum">16&nbsp;</sup>&ldquo;No one sews a patch of unshrunk cloth on an old garment, for the patch will pull away from the garment, making the tear worse.<sup class="versenum">17&nbsp;</sup>Neither do people pour new wine into old wineskins. If they do, the skins will burst; the wine will run out and the wineskins will be ruined. No, they pour new wine into new wineskins, and both are preserved.&rdquo;</span></p>
	</div>
	</div>
	<span class="for-enrichment"> <!-- end bible --> </span></div>
	<span class="for-enrichment">&nbsp;<span class="popup-link" @click = "popUp('pop4')"> Mark 2:14-22</span>.</span>

	<div class="popup invisible" id="pop4"><span class="for-enrichment"><!-- begin bible --></span>

	<div>
	<div>
	<p><span class="for-enrichment"><sup class="versenum">14&nbsp;</sup>As he walked along, he saw Levi son of Alphaeus sitting at the tax collector&rsquo;s booth. &ldquo;Follow me,&rdquo; Jesus told him, and Levi got up and followed him.</span></p>

	<p><span class="for-enrichment"><sup class="versenum">15&nbsp;</sup>While Jesus was having dinner at Levi&rsquo;s house, many tax collectors and sinners were eating with him and his disciples, for there were many who followed him.<sup class="versenum">16&nbsp;</sup>When the teachers of the law who were Pharisees saw him eating with the sinners and tax collectors, they asked his disciples: &ldquo;Why does he eat with tax collectors and sinners?&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">17&nbsp;</sup>On hearing this, Jesus said to them, &ldquo;It is not the healthy who need a doctor, but the sick. I have not come to call the righteous, but sinners.&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">18&nbsp;</sup>Now John&rsquo;s disciples and the Pharisees were fasting. Some people came and asked Jesus, &ldquo;How is it that John&rsquo;s disciples and the disciples of the Pharisees are fasting, but yours are not?&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">19&nbsp;</sup>Jesus answered, &ldquo;How can the guests of the bridegroom fast while he is with them? They cannot, so long as they have him with them.<sup class="versenum">20&nbsp;</sup>But the time will come when the bridegroom will be taken from them, and on that day they will fast.</span></p>

	<p><span class="for-enrichment"><sup class="versenum">21&nbsp;</sup>&ldquo;No one sews a patch of unshrunk cloth on an old garment. Otherwise, the new piece will pull away from the old, making the tear worse.<sup class="versenum">22&nbsp;</sup>And no one pours new wine into old wineskins. Otherwise, the wine will burst the skins, and both the wine and the wineskins will be ruined. No, they pour new wine into new wineskins.&rdquo;</span></p>
	</div>
	</div>
	<span class="for-enrichment"> <!-- end bible --> </span></div>
	</li>
</ul>

<p class="up"><em>Practice giving and communion here or in the Preparing for Mission section</em></p>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle"><span class="forward">LOOKING FORWARD</span></div>
</div>

<h2 class="forward">Preparing for the Mission</h2>

<ul class="forward">
	<li>Practice needed skills or previous topics to help prepare to minister to others:
	<ul>
		<li>Prayer, Care, Share</li>
		<li>Gospel</li>
		<li>Foundational Bible Studies.</li>
	</ul>
	</li>
</ul>

<h2 class="forward">Going on the Mission&nbsp;</h2>

<ul class="forward">
	<li>Identify people or places you will take the initiative to minister to this week.</li>
	<li>Write &ldquo;I will by when&rdquo; statements and share with your small group.</li>
</ul>

<!-- begin note default -->
<div class="note-area">
    <form class = "auto_submit_item">
        <textarea class="textarea resize-ta" onkeyup= "addNote('note3Text')"  id ="note3Text" ></textarea>
    </form>
</div>
<!-- end note default -->


<h2 class="forward">Praying For the Mission</h2>

<ul class="forward">
	<li>Commit everyone&#39;s goals to the Lord. Ask the Lord to help us be faithful and use us to start a movement of disciple-makers.</li>
</ul>

<h2>Benediction (optional)</h2>


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

			<td class="social" @click="share('lesson', 'Fishing for Men Expedition Six: ', '/content/M2/eng/multiply2/multiply223.html')">
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
</div><form>
<input type="hidden" name ="notes_page"  id ="notes_page" value="M2-eng-multiply2-multiply223.html">
</form><!--- Created by publishPage-->

</template>
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->