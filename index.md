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
		/*background: gray url("/images/tiny-squares/tiny-square.jpg") repeat 0 0;
		-webkit-animation: slide 20s linear infinite;
		-moz-animation: slide 20s linear infinite;*/
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

	#about-me, #achievements, #teaching, #updates, #past-roles, #publications, #latest-updates{
		border-bottom: 1px solid black;

	}

	.publication-row {
            display: flex;
            align-items: flex-start;
            margin-bottom: 20px;
        }

        .publication-image {
            width: 40%;
            max-height: 100%;
        }

        .publication-details {
            flex: 1;
            padding-left: 20px;
        }

        .publication-title {
            font-weight: bold;
            font-size: 18px;
        }

        .publication-coauthors {
            font-style: italic;
            margin-top: 5px;
        }

        .publication-publisher {
            margin-top: 5px;
        }

        .publication-sources {
            margin-top: 5px;
        }

        .publication-abstract {
            margin-top: 10px;
            font-size: 14px;
			text-align: justify
        }
		.support-of{
			font-size: 10px;
			
		}
		.underline{
			text-decoration: underline;
		}
        
        .update-text{
            
            color: red;
            font-style: bold
            
        }
</style>

##### **About Me**

<img class="pad-2" align="right" width="110" height="110" src="/images/RISHIRAJ.jpg">

Rishiraj is currently a **Research Data Scientist at Reliance**. He obtained his PhD in Computer Science from **IIT Gandhinagar** in January 2025, specializing in **Ubiquitous Computing**, particularly health sensing. For his doctoral work, he was awarded the **Commendation for Outstanding Research** at IIT Gandhinagar's 14th Convocation. His research has been featured in publications such as **ACM IMWUT, ACM HEALTH, ACM CSCW, and Ubicomp/ISWC**. Watch his PhD thesis defense on [YouTube](https://www.youtube.com/watch?v=mY8-mksl73o).
<br><br>

##### **Achievements**
- **Commendation for Outstanding Research in PhD** awarded during the 14th Convocation of IIT Gandhinagar.
- **Finalist** for the *UbiComp Gaetano Borriello Outstanding Student Award (2023)*.  
- **Fulbright Visiting Researcher** at Carnegie Mellon University's [SMASH Lab](https://smashlab.io/).
- **Presented a poster at the 11th Heidelberg Laureate Forum (HLF)** – [Watch on YouTube](https://youtu.be/1-aTRGvJzPQ?si=qBCEgWB5KEx4FYK9&t=3311).
- **Best poster award** in PhD Research Showcase at IIT Gandhinagar (2023).
- **Google Summer of Code (GSoC) Participant** – Contributed to making **TensorFlow Lite** more accessible for users.
- **Prime Minister's Research Fellowship** recipient.

<!--
<p class="support-of">Research Supported By</p>
<img align="left" src="/images/Fulbright_logo.png"><img align="left" src="/images/pmrf-logo.png"><br>
-->



<!--
##### **<span style="color: #f56607">Looking for research internship (May-July 2022)</span>**
I'm looking to work in Human-Computer Interaction, Ubiquitous Computing, Sensor-enabled Embedded Systems that can impact healthcare delivery or pave the path towards making healthcare more accessible.-->


##### **Publications**
<div class="publication-row">
        <div class="publication-image">
            <img src="/images/publication-hero-images/jouleseye.png" alt="Publication Image">
        </div>
        <div class="publication-details">
            <div class="publication-title">JoulesEye: Energy Expenditure Estimation and Respiration Sensing from Thermal Imagery While Exercising</div>
            <div class="publication-coauthors"><span class="underline">Rishiraj Adhikary</span>, Maite Sadeh, Nipun Batra and Mayank Goel</div>
            <div class="publication-publisher">ACM IMWUT 2024</div>
            <div class="publication-sources">
                <p>
                    <a href="/downloads/publications/jouleseye.pdf">PDF</a> |
                    <a href="https://dl.acm.org/doi/abs/10.1145/3631422">ACM DL</a> |
                    <a href="https://www.youtube.com/watch?v=5J9KqrDnj20">Video</a>|
                    <a href="https://www.youtube.com/watch?v=D8UEuQ8nSN4">Presentation</a>|
                </p>
        	</div>
    	</div>
</div>
<div class="publication-abstract">
	Smartphones and smartwatches have contributed significantly to fitness monitoring by providing real-time statistics, thanks to accurate tracking of physiological indices such as heart rate. However, the estimation of calories burned during exercise is inaccurate and cannot be used for medical diagnosis. In this work, we present JoulesEye, a smartphone thermal camera-based system that can accurately estimate calorie burn by monitoring respiration rate. We evaluated JoulesEye on 54 participants who performed high intensity cycling and running. The mean absolute percentage error (MAPE) of JoulesEye was 5.8%, which is significantly better than the MAPE of 37.6% observed with commercial smartwatch-based methods that only use heart rate. Finally, we show that an ultra-low-resolution thermal camera that is small enough to fit inside a watch or other wearables is sufficient for accurate calorie burn estimation. These results suggest that JoulesEye is a promising new method for accurate and reliable calorie burn estimation.
</div>

<div style="margin-top: 30px"></div>
<div class="publication-row">
        <div class="publication-image">
            <img src="/images/publication-hero-images/spiromask-hero.png" alt="Publication Image">
        </div>
        <div class="publication-details">
            <div class="publication-title">SpiroMask: Measuring Lung Function Using Consumer-Grade Masks</div>
            <div class="publication-coauthors"><span class="underline">Rishiraj Adhikary</span>, Dhruvi Lodhavia, Chris Francis, Rohit Patil, Tanmay Srivastava, Prerna Khanna, Nipun Batra, Joe Breda, Jacob Peplinski, Shwetak Patel</div>
            <div class="publication-publisher">In ACM HEALTH</div>
            <div class="publication-sources">
                <p>
                    <a href="/downloads/publications/spiromask.pdf">PDF</a> |
                    <a href="https://dl.acm.org/doi/10.1145/3570167">ACM Library</a>
                </p>
        	</div>
    	</div>
</div>
<div class="publication-abstract">
	According to the World Health Organisation (WHO), 235 million people suffer from respiratory illnesses which causes four
	million deaths annually. Regular lung health monitoring can lead to prognoses about deteriorating lung health conditions.
	This paper presents our system SpiroMask that retrofits a microphone in consumer grade masks (N95 and cloth masks) for
	continuous lung health monitoring. We evaluate our approach on 48 participants (including 14 with lung health issues)
	and find that we can estimate parameters such as lung volume and respiration rate within the approved error range by the
	American Thoracic Society (ATS). Further, we show that our approach is robust to sensor placement inside the mask.
</div>



<div style="margin-top: 30px"></div>
<div class="publication-row">
        <div class="publication-image">
            <img src="/images/publication-hero-images/aryan-hero.png" alt="Publication Image">
        </div>
        <div class="publication-details">
            <div class="publication-title">Towards Continuous Respiration Rate Detection While Walking</div>
            <div class="publication-coauthors"><span class="underline">Rishiraj Adhikary</span>, Aryan Varshney, Nipun Batra</div>
            <div class="publication-publisher">In UbiComp/ISWC 2022 (Adjunct)</div>
            <div class="publication-sources">
                <p>
                    <a href="/downloads/publications/Ubicomp2022_CO2_Mask.pdf">PDF</a> |
                    <a href="https://dl.acm.org/doi/10.1145/3544793.3560348">ACM Library</a>
                </p>
        	</div>
    	</div>
</div>
<div class="publication-abstract">
	Respiration rate is a vital sign to predict cardiac arrest, apnea, dyspnea and lung ailments. Past research has largely focused
on sensing respiration rate in a controlled environment with participants at rest. But disease prognosis requires continuous
everyday-life monitoring of respiration rate. In this work, we demonstrate how CO2 sensor placed inside N95 mask can
detect respiration rate during motion as well as rest with a better or comparable performance compared to previous work.
Our system weighs 16 grams, runs uninterrupted for 2 hours, generalises across participants, does not require any learning
algorithm and is reproducible
</div>



<div style="margin-top: 30px"></div>
<div class="publication-row">
        <div class="publication-image">
            <img src="/images/publication-hero-images/samachaar-hero.png" alt="Publication Image">
        </div>
        <div class="publication-details">
            <div class="publication-title">Samachar: Print News Media on Air Pollution in India</div>
            <div class="publication-coauthors">Karm Patel, <span class="underline">Rishiraj Adhikary</span>, Zeel B Patel, Nipun Batra, Sarath Guttikunda</div>
            <div class="publication-publisher">In COMPASS ‘22</div>
            <div class="publication-sources">
                <p>
                    <a href="/downloads/publications/compass22-samachaar.pdf">PDF</a> |
                    <a href="https://dl.acm.org/doi/10.1145/3530190.3534812">ACM Library</a>
                </p>
        	</div>
    	</div>
</div>
<div class="publication-abstract">
	Air pollution killed 1.67M people in India in 2019. Previous work has
shown that accurate public perception can help people identify the
health risks of air pollution and act accordingly. News media influence how the public defines a social problem. However, news media
analysis on air pollution has been on a small scale and regional. In
this work, we gauge print news media response to air pollution in
India on a larger scale. We curated a dataset of 17.4K news articles
on air pollution from two leading English daily newspapers spanning 11 years. We performed exploratory data analysis and topic
modeling to reveal the news media response to air pollution. Our
study shows that, although air pollution is a year-long problem
in India, the news media limelight on the issue is periodic (temporal bias). News media prefer to focus on the air pollution issue
of metropolitan cities rather than the cities which are worst hit
by air pollution (geographical bias). Also, the air pollution source
contributions discussed in news articles significantly deviate from
the scientific studies. Finally, we analyze the challenges raised by
our findings and suggest potential solutions as well as the policy
implications of our work. any learning
algorithm and is reproducible
</div>



<div style="margin-top: 30px"></div>
<div class="publication-row">
        <div class="publication-image">
            <img src="/images/publication-hero-images/hero-hmm.png" alt="Publication Image">
        </div>
        <div class="publication-details">
            <div class="publication-title">Exploring Hidden Markov Models</div>
            <div class="publication-coauthors">Kukunuri Rithwik, <span class="underline">Rishiraj Adhikary</span>, Mahika Om Jaguste, Nipun Batra and Ashish Tendulkar</div>
            <div class="publication-publisher">In VISxAI’21</div>
            <div class="publication-sources">
                <p>
                    <a href="https://nipunbatra.github.io/hmm/">Link</a>
                    
                </p>
        	</div>
    	</div>
</div>
<div class="publication-abstract">
	Have you ever wondered how the voice assistant in your phone works? Or, how your smartwatch counts your steps? These are applications of time-series data. In this article, we explore Hidden Markov Models or HMMs, which are often used for such applications. HMMs model the data as a sequence. Let us take an example to see why modeling as a sequence makes sense. A sentence like "I like playing …" would often be followed by "guitar," "football," etc. In such examples, the previous word helps us better guess the next word/words. This is an example of language modeling. Step counting algorithms use HMM to classify stationary and moving activities. Markov Chains mathematically describes a sequence of possible events. The probability of each event depends on past events. In this article, we discuss Markov chains, Hidden Markov Models, and the key problems of Hidden Markov Models. 
</div>


<div style="margin-top: 30px"></div>
<div class="publication-row">
        <div class="publication-image">
            <img src="/images/publication-hero-images/vartalaap-hero.png" alt="Publication Image">
        </div>
        <div class="publication-details">
            <div class="publication-title">Vartalaap: What Drives #AirQuality Discussions: Politics, Pollution or Pseudo-science?</div>
            <div class="publication-coauthors"><span class="underline">Rishiraj Adhikary</span>, Zeel Patel, Tanmay Srivastava, Nipun Batra, Mayank Singh, Udit Bhatia and Sarath Guttikunda</div>
            <div class="publication-publisher">In CSCW’21</div>
            <div class="publication-sources">
                <p>
                    <a href="/downloads/publications/vartalaap.pdf">PDF</a> | 
					<a href="https://dl.acm.org/doi/10.1145/3449170">ACM Library</a>
                    
                </p>
        	</div>
    	</div>
</div>
<div class="publication-abstract">
	Air pollution is a global challenge for cities across the globe. Understanding the public perception of air pollution can help policymakers engage better with the public and appropriately introduce policies. Accurate public perception can also help people to identify the health risks of air pollution and act accordingly. Unfortunately, current techniques for determining perception are not scalable: it involves surveying few hundred people with questionnaire-based surveys. Using the advances in natural language processing (NLP), we propose a more scalable solution called Vartalaap to gauge public perception of air pollution via the microblogging social network Twitter. We curated a dataset of more than 1.2M tweets discussing Delhi-specific air pollution. We find that (unfortunately) the public is supportive of unproven mitigation strategies to reduce pollution, thus risking their health due to a false sense of security. We also find that air quality is a year-long problem, but the discussions are not proportional to the level of pollution and spike up when pollution is more visible. The information required by Vartalaap is publicly available and, as such, it can be immediately applied to study different societal issues across the world.
</div>



<div style="margin-top: 30px"></div>
<div class="publication-row">
        <div class="publication-image">
            <img src="/images/publication-hero-images/campus-deployment-hero.png" alt="Publication Image">
        </div>
        <div class="publication-details">
            <div class="publication-title">Lessons from large scale campus deployment</div>
            <div class="publication-coauthors"><span class="underline">Rishiraj Adhikary</span>, Soham Pachpande, Nipun Batra. </div>
            <div class="publication-publisher">In Buildsys DATA ’20 Workshop</div>
            <div class="publication-sources">
                <p>
                    <a href="/downloads/publications/2020_Buildsys_Paper_Learning.pdf">PDF</a> | 
					<a href="https://dl.acm.org/doi/10.1145/3419016.3431490">ACM Library</a>
                </p>
        	</div>
    	</div>
</div>
<div class="publication-abstract">
	Large scale campus deployments in the past have resulted in energy conservation measures, data validation, and software architectures. Inspired by the success and learnings from such previous deployments, we present our work on deployment involving sensing various aspect of campus sustainability like water, electricity, solar produce, air quality, and parking lot occupancy. Our full deployment spanned more than 171 days. We used 469 sensors, collecting a maximum of 190 MB of data daily. We discuss the deployment challenges and the learnings obtained from them. We address the data collection challenges by providing best practices measures and provide insights from the installation of wireless radio communication modules. Our deployment can act as a reconnaissance guide for campus deployment, especially in developing countries.
</div>


<div style="margin-top: 30px"></div>
<div class="publication-row">
        <div class="publication-image">
            <img src="/images/publication-hero-images/naqaab-hero.png" alt="Publication Image">
        </div>
        <div class="publication-details">
            <div class="publication-title">Naqaab: Towards health sensing and persuasion via masks</div>
            <div class="publication-coauthors"><span class="underline">Rishiraj Adhikary</span>, Tanmay Srivastava, Prerna Khanna, Aabhas Senapati, Nipun Batra. </div>
            <div class="publication-publisher">In UbiComp/ISWC 2020 (Adjunct)</div>
            <div class="publication-sources">
                <p>
                    <a href="/downloads/publications/2020_Ubicomp_Poster_SmartMask.pdf">PDF</a> | 
					<a href="https://dl.acm.org/doi/10.1145/3410530.3414403">ACM Library</a>
                    
                </p>
        	</div>
    	</div>
</div>
<div class="publication-abstract">
	Given the pandemic and the high air pollution in large parts of the world, masks have become ubiquitous. In this poster, we present our vision and work-in-progress (WIP) towards leveraging the ubiquity of masks for health sensing and persuasion. We envision masks to monitor health-related parameters such as i) temperature; ii) lung activity, among others. We also envision that retrofitting masks with sensors and display to show localized pollution can create awareness about air pollution. In this WIP, we present a smart mask, Naqaab, that measures forced vital capacity (FVC) of the lung using a retrofitted microphone. We evaluated the measured lung parameter on eight persons using an Incentive Spirometer2 and found that our smart mask accurately measures incentive lung capacity. Naqaab also measures pollution exposure and indicates via different LED colours. We envision using such a system for eco feedback
</div>



<div style="margin-top: 30px"></div>
<div class="publication-row">
        <div class="publication-image">
            <img src="/images/publication-hero-images/breath-hero.png" alt="Publication Image">
        </div>
        <div class="publication-details">
            <div class="publication-title">Do We Breathe The Same Air? </div>
            <div class="publication-coauthors"><span class="underline">Rishiraj Adhikary</span>, Nipun Batra. </div>
            <div class="publication-publisher">In UbiComp/ISWC 2020 (Adjunct)</div>
            <div class="publication-sources">
                <p>
                    <a href="/downloads/publications/2020_Ubicomp_Breathe_Poster.pdf">PDF</a> | 
					<a href="https://dl.acm.org/doi/10.1145/3410530.3414414">ACM Library</a> | 
					<a href="https://www.youtube.com/watch?v=eRHxXTMms3w">Video</a> |
                </p>
        	</div>
    	</div>
</div>
<div class="publication-abstract">
	91% of the world’s population lives in areas where air pollution
	exceeds safety limits1. Research has focused on monitoring ambient
	air pollution, but individual exposure to air pollution is not equal to
	ambient and is thus important to measure. Our work (in progress)
	measures individual exposures of different categories of people on
	an academic campus. We highlight some anecdotal findings and
	surprising insights from monitoring, such as a) Indoor CO2 concentration of 1.8 times higher than the permissible limit. Over 10 times
	the WHO limit of PM2.5 exposure during b) construction related
	activities, and c) cooking (despite the use of exhaust). We also found
	that during transit, the PM2.5 exposure is at least two times higher
	than indoor. Our current work though in progress, already shows
	important findings affecting different people associated with an
	academic campus. In the future, we plan to do a more exhaustive
	study and reduce the form factor and energy needs for our sensors
	to scale the study.
</div>


<br><br>
<a href="/archived/">View Past Professional Updates</a>

[1]:{{ site.url }}/downloads/free-space-management-1.pdf
[2]:{{ site.url }}/downloads/machine-language-c.pdf
[3]:{{ site.url }}/downloads/machine-language-c-2020.pdf
[4]:{{ site.url }}/downloads/poster-aiims.pdf
[5]:{{ site.url }}/downloads/publications/2020_Ubicomp_Breathe_Poster.pdf
[6]:{{ site.url }}/downloads/publications/2020_Ubicomp_Breathe_Poster.pdf
[7]:{{ site.url }}/downloads/publications/Ubicomp-DC2020_Revised.pdf
[8]:{{ site.url }}/downloads/GSoC-Proposal.pdf


<script>
	//document.getElementsByTagName("body")[0].setAttribute("id", "background");
</script>
