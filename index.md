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

	#about, #research-focus, #achievements, #teaching, #updates, #past-roles, #publications, #latest-updates{
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

        /* Main Layout */
        .top-row-grid {
            display: grid;
            grid-template-columns: 200px 1fr;
            gap: 30px;
            padding: 30px 0;
            border-bottom: 1px solid #eee;
            margin-bottom: 40px;
            align-items: center;
        }

        /* Left Column: Focused Profile */
        .hero-profile { text-align: center; }
        .hero-image {
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
            width: 100%;
            height: auto;
            margin-bottom: 15px;
        }

        .hero-info { display: flex; flex-direction: column; gap: 10px; }
        /* Header & LinkedIn Link */
        .name-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        .hero-info h1 { 
            margin: 0; 
            font-size: 2.em; 
            font-weight: 800; 
            color: #1a1a1a;
            letter-spacing: -1px;
        }
        .linkedin-icon {
            width: 28px;
            height: 28px;
            transition: transform 0.2s ease;
        }
        .linkedin-icon:hover {
            transform: scale(1.1);
        }
    
        .current-role {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: rgba(240, 240, 240, 0.5);
            backdrop-filter: blur(5px);
            padding: 6px 15px;
            border-radius: 50px;
            border: 1px solid #e0e0e0;
            width: fit-content;
            margin: 5px 0 15px 0;
        }
        .role-logo { height: 20px; width: auto; }
        .role-text { font-size: 0.9em; font-weight: 600; color: #333; }

        .mission-box {
            background: linear-gradient(to right, #ffffff, #fafafa);
            padding: 0;
            border-radius: 10px;
        }
        .mission-text {
            font-size: 1.1em;
            line-height: 1.7;
            color: #444;
            margin-bottom: 15px;
        }

        /* Interactive Achievement Cards */
        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        .achievement-link { text-decoration: none !important; color: inherit !important; }
        .achievement-card {
            background: #fff;
            padding: 25px 15px;
            border: 1px solid #eaeaea;
            border-radius: 12px;
            text-align: center;
            transition: all 0.3s cubic-bezier(0.165, 0.84, 0.44, 1);
        }
        .achievement-link:hover .achievement-card {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            border-color: #d9534f;
        }
        .logo-container { height: 50px; margin-bottom: 15px; display: flex; align-items: center; justify-content: center; }
        .logo-container img { max-height: 100%; max-width: 120px; object-fit: contain; }

        @media only screen and (max-width: 768px) {
            .top-row-grid { grid-template-columns: 1fr; text-align: center; }
            .name-container { justify-content: center; }
            .current-role { margin: 10px auto; }
            .hero-image { width: 180px; }
        }
</style>
<div class="top-row-grid">
    <div class="hero-profile">
        <img class="hero-image" src="/images/RISHIRAJ.jpg" alt="Rishiraj Adhikary">
        <p style="font-weight: bold; margin: 0; color: #555; font-size: 0.9em;">PhD in Computer Science<br>(IIT Gandhinagar)</p>
    </div>

    <div class="hero-info">
        <div class="name-container">
            <h1>Rishiraj Adhikary</h1>
            <a href="https://www.linkedin.com/in/rishiraj-in/" target="_blank">
                <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="LinkedIn" class="linkedin-icon">
            </a>
        </div>

        <div class="current-role">
            <img src="/images/work_logo.png" alt="Reliance" class="role-logo">
            <span class="role-text">Research Data Scientist @ Reliance</span>
        </div>

        <div class="mission-box">
            <p class="mission-text">
                I specialize in <strong>health sensing</strong>, developing systems that facilitate a paradigm shift from reactive to <strong>proactive healthcare</strong>. To achieve this, I leverage an interdisciplinary toolkit of <strong>signal processing, machine learning, and embedded systems</strong>. 
                <br><br>
                My research has been published in premier venues such as <strong>ACM IMWUT and ACM HEALTH</strong>, and has garnered prestigious recognitions including the <strong>Fulbright-Nehru Fellowship</strong>, the <strong>Prime Minister’s Research Fellowship (PMRF)</strong>, the <strong>UbiComp Gaetano Borriello Student Award</strong>, and the <strong>Commendation Medal for Outstanding Research</strong> from IIT Gandhinagar for my doctoral contributions.
                <br><br>
                Currently at Reliance, I use data science combined with LLM to drive insights from energy and mobile tower data. 
            </p>
            <a href="https://www.youtube.com/watch?v=mY8-mksl73o" style="color: #d9534f; font-weight: bold; text-decoration: none; font-size: 0.95em; border-bottom: 1px solid #d9534f; padding-bottom: 2px;">
                Watch My PhD Thesis Defense &rarr;
            </a>
        </div>
    </div>
</div>

<h5 style="border-bottom: 2px solid #333; display: inline-block; padding-bottom: 5px; margin-bottom: 25px;">Core Achievements</h5>

<div class="achievements-grid">
    <a href="https://smashlab.io/" class="achievement-link">
        <div class="achievement-card">
            <div class="logo-container"><img src="/images/Fulbright_logo.png" alt="Fulbright"></div>
            <strong>Fulbright Scholar</strong>
            <p style="font-size: 0.85em; color: #777; margin: 5px 0 0;">Visiting researcher at Carnegie Mellon University's SMASH lab</p>
        </div>
    </a>

    <a href="https://iitgn.ac.in/assets/pdfs/medals/List-of-awards-and-medals-2025.pdf" class="achievement-link">
        <div class="achievement-card">
            <div class="logo-container"><img src="/images/medal_logo.jpg" alt="IITGN"></div>
            <strong>Outstanding Research</strong>
            <p style="font-size: 0.85em; color: #777; margin: 5px 0 0;">Commendation Medal for research excellence during PhD</p>
        </div>
    </a>

    <a href="https://ubicomp.org/sc/awards.html" class="achievement-link">
        <div class="achievement-card">
            <div class="logo-container"><img src="/images/ubicomp_logo.jpg" alt="UbiComp"></div>
            <strong>Gaetano Borriello Award</strong>
            <p style="font-size: 0.85em; color: #777; margin: 5px 0 0;">Finalist for Outstanding Student Award in 2023</p>
        </div>
    </a>

    <a href="https://youtu.be/1-aTRGvJzPQ?si=qBCEgWB5KEx4FYK9&t=3311" class="achievement-link">
        <div class="achievement-card">
            <div class="logo-container"><img src="/images/hlf_logo.jpg" alt="HLF"></div>
            <strong>HLF Participant</strong>
            <p style="font-size: 0.85em; color: #777; margin: 5px 0 0;">One of the 50 poster presenter at 11th HLF. Click to watch</p>
        </div>
    </a>
</div>

<br><br>

<h5 style="border-bottom: 2px solid #333; display: inline-block; padding-bottom: 5px; margin-bottom: 25px;">Featured Publication</h5>

<div class="publication-row" style="background: #fdfdfd; padding: 20px; border-radius: 12px; border: 1px solid #eee;">
    <div class="publication-image">
        <img src="/images/publication-hero-images/jouleseye.png" alt="JoulesEye" style="border-radius: 8px;">
    </div>
    <div class="publication-details">
        <div class="publication-title" style="font-size: 1.25em;">JoulesEye: Energy Expenditure Estimation and Respiration Sensing from Thermal Imagery While Exercising</div>
        <div class="publication-coauthors"><span class="underline">Rishiraj Adhikary</span>, Maite Sadeh, Nipun Batra and Mayank Goel</div>
        <div class="publication-publisher"><strong>ACM IMWUT 2024</strong></div>
        <div class="publication-sources">
            <a href="/downloads/publications/jouleseye.pdf">PDF</a> | <a href="https://dl.acm.org/doi/abs/10.1145/3631422">ACM DL</a> | <a href="https://www.youtube.com/watch?v=5J9KqrDnj20">Video</a>
        </div>
    </div>
</div>

<div style="text-align: center; margin-top: 50px;">
    <a href="/publications/" style="text-decoration:none; font-weight: bold; background: #333; color: #fff; padding: 12px 30px; border-radius: 50px; font-size: 0.9em; transition: 0.3s;">
        View Complete Publication List
    </a>
</div>

##### **Other Achievements**
- **Best poster award** in PhD Research Showcase at IIT Gandhinagar (2023).
- **Google Summer of Code (GSoC) Participant** – Contributed to making **TensorFlow Lite** more accessible for users.
- **Prime Minister's Research Fellowship** recipient.


<div style="text-align: center; margin-top: 50px;">
    <a href="/archived/" style="text-decoration:none; font-weight: bold; background: #333; color: #fff; padding: 12px 30px; border-radius: 50px; font-size: 0.9em; transition: 0.3s;">
        View Past Professional Updates
    </a>
</div>

[1]:{{ site.url }}/downloads/free-space-management-1.pdf
[2]:{{ site.url }}/downloads/machine-language-c.pdf
[3]:{{ site.url }}/downloads/machine-language-c-2020.pdf
[4]:{{ site.url }}/downloads/poster-aiims.pdf
[5]:{{ site.url }}/downloads/publications/2020_Ubicomp_Breathe_Poster.pdf
[6]:{{ site.url }}/downloads/publications/2020_Ubicomp_Breathe_Poster.pdf
[7]:{{ site.url }}/downloads/publications/Ubicomp-DC2020_Revised.pdf
[8]:{{ site.url }}/downloads/GSoC-Proposal.pdf



