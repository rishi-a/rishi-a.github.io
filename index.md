---
# example line
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
output:
  html_document:
    css: style.css
    self_contained: no
layout: page

---

<style>

	@-webkit-keyframes slide {
	    from { background-position: 0 0; }
	    to { background-position: -400px 0; }
	}
	#background{
		background: gray url("/images/tiny-squares/tiny-square.jpg") repeat 0 0;
		-webkit-animation: slide 20s linear infinite;
		-moz-animation: slide 20s linear infinite;
	}
	p{text-align: justify;}
	li{text-align: justify;}

	@media only screen and (max-width: 500px) {
	  	.pad-1 {
	   		 padding: 10px;
	  	}
	  	.pad-2 {
	   		 padding:10px;
	   		 border-radius: 50%
	  	}

  	}

	@media only screen and (min-width: 501px) {
	  	.pad-1 {
	   		 padding-left: :10px;
	  	}
	  	.pad-2 {
	   		 padding-left:10px; padding-right: 10px;
	   		 border-radius: 50%
	  	}

	}

	#about-me, #teaching, #updates, #past-roles{
		border-bottom: 1px solid black;

	}
</style>

##### **About Me**

<img class="pad-2" align="right" width="110" height="110" src="/images/RISHIRAJ.jpg">
<!--<img class="pad-1" align="right" width="200" height="170" src="/images/IMG-20190202-WA0001.jpg">
-->I’m a Ph.D. candidate (PMRF) in the CSE discipline of [IIT Gandhinagar](https://iitgn.ac.in). Prof. [Nipun Batra](https://nipunbatra.github.io/) advises me. I was a Fulbright Visiting Researcher at the [SMASH Lab](https://smashlab.io/) of [Carnegie Mellon University](https://cmu.edu). My research interest is in Ubiquitous Computing. My current focus is on designing wearables that measure health parameters. I did my schooling in Shillong, India and grew up there, although I was born in the Indian state of Assam.

<!--
##### **<span style="color: #f56607">Looking for research internship (May-July 2022)</span>**
I'm looking to work in Human-Computer Interaction, Ubiquitous Computing, Sensor-enabled Embedded Systems that can impact healthcare delivery or pave the path towards making healthcare more accessible.-->


<div style="margin-top: 50px"></div>

##### **Updates**
**2022**
- **October 28** Our paper _**Spiromask**_ got accepted in ACM HEALTH.
    - [Paper Summary](https://twitter.com/nipun_batra/status/1586205718880739328)
    - [Background Story of the paper](https://twitter.com/rishihere/status/1586521223952928770)

<a href="/archived/">Previous Updates</a>

[1]:{{ site.url }}/downloads/free-space-management-1.pdf
[2]:{{ site.url }}/downloads/machine-language-c.pdf
[3]:{{ site.url }}/downloads/machine-language-c-2020.pdf
[4]:{{ site.url }}/downloads/poster-aiims.pdf
[5]:{{ site.url }}/downloads/publications/2020_Ubicomp_Breathe_Poster.pdf
[6]:{{ site.url }}/downloads/publications/2020_Ubicomp_Breathe_Poster.pdf
[7]:{{ site.url }}/downloads/publications/Ubicomp-DC2020_Revised.pdf
[8]:{{ site.url }}/downloads/GSoC-Proposal.pdf


<script>
	document.getElementsByTagName("body")[0].setAttribute("id", "background");
</script>
