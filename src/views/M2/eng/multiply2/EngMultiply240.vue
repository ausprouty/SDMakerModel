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
                        <div class="chapter_number ltr"><h1>40.</h1></div>
                        <div class="chapter_title ltr"><h1>Multiplication by Narrowing Focus</h1></div>
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

<p><em>Encourage loving accountability to obey Jesus</em></p>

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

<p class="back"><span><span>Our vision is: <em> &ldquo;A church for every village and community, and the gospel for every person.&rdquo;</em></span></span></p>

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
	<li><span><span>Ask the group to tell the story from last week.</span></span></li>
</ul>

<h2 class="up">Read</h2>

<p class="up">Read or watch Luke 9:28-36 two times as others listen.</p>

<button id="Button0" type="button" class="collapsible bible">Read Luke 9:28-36</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<h3>The Transfiguration</h3>

<p><sup class="versenum">28&nbsp;</sup>About eight days after Jesus said this, he took Peter, John and James with him and went up onto a mountain to pray.<sup class="versenum">29&nbsp;</sup>As he was praying, the appearance of his face changed, and his clothes became as bright as a flash of lightning.<sup class="versenum">30&nbsp;</sup>Two men, Moses and Elijah, appeared in glorious splendor, talking with Jesus.<sup class="versenum">31&nbsp;</sup>They spoke about his departure, which he was about to bring to fulfillment at Jerusalem.<sup class="versenum">32&nbsp;</sup>Peter and his companions were very sleepy, but when they became fully awake, they saw his glory and the two men standing with him.<sup class="versenum">33&nbsp;</sup>As the men were leaving Jesus, Peter said to him, &ldquo;Master, it is good for us to be here. Let us put up three shelters&mdash;one for you, one for Moses and one for Elijah.&rdquo; (He did not know what he was saying.)</p>

<p><sup class="versenum">34&nbsp;</sup>While he was speaking, a cloud appeared and covered them, and they were afraid as they entered the cloud.<sup class="versenum">35&nbsp;</sup>A voice came from the cloud, saying, &ldquo;This is my Son, whom I have chosen; listen to him.&rdquo;<sup class="versenum">36&nbsp;</sup>When the voice had spoken, they found that Jesus was alone. The disciples kept this to themselves and did not tell anyone at that time what they had seen.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/eng/video/multiply2/240.mp4" type="button" class="external-movie">
         Watch &nbsp;Luke 9:28-36&nbsp;</button>
    <div class="collapsed"></div>

<h2 class="up">Discovery Discussion (Everyone answers)</h2>

<ul class="up">
	<li><span><span>What caught your attention or what did you like best? Why?</span></span></li>
	<li><span><span>What is new or has developed at this point in Jesus story?</span></span></li>
	<li><span><span>What do we learn about the humanity or divinity of Jesus from this passage?</span></span></li>
	<li><span><span>How can we live differently now that we know this story?</span></span></li>
</ul>

<p><span><span>Additional Questions:</span></span></p>

<ul class="up">
	<li><span><span>What are his followers learning?</span></span></li>
	<li><span><span>What is Jesus modeling to us about life and ministry or godly leadership?</span></span></li>
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

<p class="up">Six days after Peter&rsquo;s confession about who Jesus is, Jesus begins teaching about suffering as part of expanding the Kingdom. Jesus selects three of the twelve leaders and sets them apart. Peter, James, and John come even closer so that Jesus may reveal more of who He is and give them special instruction as the leaders of the leaders. He leaves the nine and takes the three up to the top of a mountain and allows them to see His full glory revealed. On the mountain top they hear the voice of the Father affirming Jesus, His Son. Even though Moses and Elijah were heroes for the Jewish people, the Father sets Jesus higher than all others and tells the three to &ldquo;listen to Him.&rdquo;</p>

</div>

<ul>
	<li class="nobreak-final-final"><span class="for-enrichment">For Further Study: <span class="popup-link" @click = "popUp('pop3')"> Matthew 17:1-13</span>;&nbsp;</span>

	<div class="popup invisible" id="pop3"><span class="for-enrichment"><!-- begin bible --></span>

	<div>
	<div>
	<p><span class="for-enrichment"><sup class="versenum">1 </sup>After six days Jesus took with him Peter, James and John the brother of James, and led them up a high mountain by themselves.<sup class="versenum">2&nbsp;</sup>There he was transfigured before them. His face shone like the sun, and his clothes became as white as the light.<sup class="versenum">3&nbsp;</sup>Just then there appeared before them Moses and Elijah, talking with Jesus.</span></p>

	<p><span class="for-enrichment"><sup class="versenum">4&nbsp;</sup>Peter said to Jesus, &ldquo;Lord, it is good for us to be here. If you wish, I will put up three shelters&mdash;one for you, one for Moses and one for Elijah.&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">5&nbsp;</sup>While he was still speaking, a bright cloud covered them, and a voice from the cloud said, &ldquo;This is my Son, whom I love; with him I am well pleased. Listen to him!&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">6&nbsp;</sup>When the disciples heard this, they fell facedown to the ground, terrified.<sup class="versenum">7&nbsp;</sup>But Jesus came and touched them. &ldquo;Get up,&rdquo; he said. &ldquo;Don&rsquo;t be afraid.&rdquo;<sup class="versenum">8&nbsp;</sup>When they looked up, they saw no one except Jesus.</span></p>

	<p><span class="for-enrichment"><sup class="versenum">9&nbsp;</sup>As they were coming down the mountain, Jesus instructed them, &ldquo;Don&rsquo;t tell anyone what you have seen, until the Son of Man has been raised from the dead.&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">10&nbsp;</sup>The disciples asked him, &ldquo;Why then do the teachers of the law say that Elijah must come first?&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">11&nbsp;</sup>Jesus replied, &ldquo;To be sure, Elijah comes and will restore all things.<sup class="versenum">12&nbsp;</sup>But I tell you, Elijah has already come, and they did not recognize him, but have done to him everything they wished. In the same way the Son of Man is going to suffer at their hands.&rdquo;<sup class="versenum">13&nbsp;</sup>Then the disciples understood that he was talking to them about John the Baptist.</span></p>
	</div>
	</div>
	<span class="for-enrichment"> <!-- end bible --> </span></div>
	<span class="for-enrichment"><span class="popup-link" @click = "popUp('pop4')"> Mark 9:2-13</span>.&nbsp;</span>

	<div class="popup invisible" id="pop4"><span class="for-enrichment"><!-- begin bible --></span>

	<div>
	<div>
	<p><span class="for-enrichment"><sup class="versenum">2&nbsp;</sup>After six days Jesus took Peter, James and John with him and led them up a high mountain, where they were all alone. There he was transfigured before them.<sup class="versenum">3&nbsp;</sup>His clothes became dazzling white, whiter than anyone in the world could bleach them.<sup class="versenum">4&nbsp;</sup>And there appeared before them Elijah and Moses, who were talking with Jesus.</span></p>

	<p><span class="for-enrichment"><sup class="versenum">5&nbsp;</sup>Peter said to Jesus, &ldquo;Rabbi, it is good for us to be here. Let us put up three shelters&mdash;one for you, one for Moses and one for Elijah.&rdquo;<sup class="versenum">6&nbsp;</sup>(He did not know what to say, they were so frightened.)</span></p>

	<p><span class="for-enrichment"><sup class="versenum">7&nbsp;</sup>Then a cloud appeared and covered them, and a voice came from the cloud: &ldquo;This is my Son, whom I love. Listen to him!&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">8&nbsp;</sup>Suddenly, when they looked around, they no longer saw anyone with them except Jesus.</span></p>

	<p><span class="for-enrichment"><sup class="versenum">9&nbsp;</sup>As they were coming down the mountain, Jesus gave them orders not to tell anyone what they had seen until the Son of Man had risen from the dead.<sup class="versenum">10&nbsp;</sup>They kept the matter to themselves, discussing what &ldquo;rising from the dead&rdquo; meant.</span></p>

	<p><span class="for-enrichment"><sup class="versenum">11&nbsp;</sup>And they asked him, &ldquo;Why do the teachers of the law say that Elijah must come first?&rdquo;</span></p>

	<p><span class="for-enrichment"><sup class="versenum">12&nbsp;</sup>Jesus replied, &ldquo;To be sure, Elijah does come first, and restores all things. Why then is it written that the Son of Man must suffer much and be rejected?<sup class="versenum">13&nbsp;</sup>But I tell you, Elijah has come, and they have done to him everything they wished, just as it is written about him.&rdquo;</span></p>
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

			<td class="social" @click="share('lesson', 'Multiplication by Narrowing Focus: ', '/content/M2/eng/multiply2/multiply240.html')">
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
<input type="hidden" name ="notes_page"  id ="notes_page" value="M2-eng-multiply2-multiply240.html">
</form><!--- Created by publishPage-->

</template>
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->