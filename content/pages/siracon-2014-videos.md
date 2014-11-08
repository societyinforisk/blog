Title: SIRAcon 2014 Videos
Date: 2014-11-08 10:05:00
Category: news
Tags: SIRAcon2014Videos
Slug: siracon-2014-videos
status: hidden
Author: SIRA


<link rel="stylesheet" href="http://woosterwebdesign.com/experiments/css/font-awesome.min.css" />

<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.3/jquery.min.js"></script>

<style type="text/css">

	body {
		margin: 30px;
		padding: 0;
		background: #ddd;
		font-family: Arial, Helvetica, sans-serif;
	}

	.title {
		width: 100%;
		max-width: 854px;
		margin: 0 auto;
	}

	.caption {
		width: 100%;
		max-width: 854px;
		margin: 0 auto;
		padding: 20px 0;
	}

	.container {
		width: 100%;
		max-width: 800px;
		min-width: 440px;
		background: #fff;
		margin: 0 auto;
	}


	/*  VIDEO PLAYER CONTAINER
############################### */
	.vid-container {
    position: relative;
    padding-bottom: 52%;
    padding-top: 30px; 
    height: 0; 
}
 
.vid-container iframe,
.vid-container object,
.vid-container embed {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}


/*  VIDEOS PLAYLIST 
############################### */
.vid-list-container {
	width: 92%;
	overflow: hidden;
	margin-top: 20px;
	margin-left:4%;
	padding-bottom: 20px;
}

.vid-list {
	width: 1400px;
	position: relative;
	top:0;
	left: 0;
}

.vid-item {
	display: block;
	width: 148px;
	height: 168px;
	float: left;
	margin: 0;
	padding: 10px;
}

.thumb {
	/*position: relative;*/
	overflow:hidden;
	height: 84px;
}

.thumb img {
	width: 100%;
	position: relative;
	top: -13px;
}

.vid-item .desc {
	color: #21A1D2;
	font-size: 15px;
	margin-top:5px;
}

.vid-item:hover {
	background: #eee;
	cursor: pointer;
}

.arrows {
	position:relative;
	width: 100%;
}

.arrow-left {
	color: #fff;
	position: absolute;
	background: #777;
	padding: 15px;
	left: -25px;
	top: -130px;
	z-index: 99;
	cursor: pointer;
}

.arrow-right {
	color: #fff;
	position: absolute;
	background: #777;
	padding: 15px;
	right: -25px;
	top: -130px;
	z-index:100;
	cursor: pointer;
}

.arrow-left:hover {
	background: #CC181E;
}

.arrow-right:hover {
	background: #CC181E;
}


@media (max-width: 624px) {
	body {
		margin: 15px;
	}
	.caption {
		margin-top: 40px;
	}
	.vid-list-container {
		padding-bottom: 20px;
	}

	/* reposition left/right arrows */
	.arrows {
		position:relative;
		margin: 0 auto;
		width:96px;
	}
	.arrow-left {
		left: 0;
		top: -17px;
	}

	.arrow-right {
		right: 0;
		top: -17px;
	}
}

</style>


<div class="container">

	<!-- THE YOUTUBE PLAYER -->
	<div class="vid-container">
    <iframe id="vid_frame" src="http://www.youtube.com/embed/t_PNncHWDtI?rel=0&showinfo=0&autohide=1" frameborder="0" width="100%" height="315"></iframe>
</div>

<!-- THE PLAYLIST -->
<div class="vid-list-container">
<div class="vid-list">

<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/t_PNncHWDtI?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/t_PNncHWDtI/default.jpg?v=5457c99e"></div>
  <div class="desc">Stuart Layton - Effectiveness of Controls against Spoofing Attacks</div>
</div>

<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/​gvM3ctqmzGA?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/gvM3ctqmzGA/default.jpg"></div>
  <div class="desc">Russell Thomas - Estimating Aggregate Perf Indexes from Messy Ground Truth Data</div>
</div>

<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/hFkIW18UKA​?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/-hFkIW18UKA/default.jpg?v=5457c919"></div>
  <div class="desc">Rachel Lininger - Conflict Resolution Styles in Info Security & Risk Mgmt</div>
</div>

<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/​MMYvcElNLSI?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/MMYvcElNLSI/default.jpg?v=5457c914"></div>
  <div class="desc">Timothy Peacock - Automation and Disruption in Stolen Payment Card Markets</div>
</div>


<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/​kGjFKINZ2Rc?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/kGjFKINZ2Rc/default.jpg?v=5458cf12"></div>
  <div class="desc">Alex Pinto - Secure Because Math: A Deep Dive on Machine Learning-Based Monitoring</div>
</div>


<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/​tbjI9nxgnLA?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/tbjI9nxgnLA/default.jpg?v=5458cf5a"></div>
  <div class="desc">Allison Miller - When Algorithms are our Co-pilots</div>
</div>


<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/4kRQ-krxC0k​?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/4kRQ-krxC0k/default.jpg?v=5458cf7f"></div>
  <div class="desc">Power Panel - SIRACon 2014
</div>
</div>


<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/​vsjAx8YCppk?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/vsjAx8YCppk/default.jpg?v=545adf2d"></div>
  <div class="desc">Doug Hubbard - SIRACon 2014</div>
</div>


<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/FLAVFLDBvqk​?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/FLAVFLDBvqk/default.jpg"></div>
  <div class="desc">Evan Wheeler - Stop Calling My Baby Ugly : Elements of a Mature IT Risk Program</div>
</div>


<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/​0nDZetzWJps?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/0nDZetzWJps/default.jpg?v=545b81c1"></div>
  <div class="desc">Jack Jones - Let's get explicit...</div>
</div>


<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/​D7UvSmFg6Kc?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/D7UvSmFg6Kc/default.jpg"></div>
  <div class="desc">Michael Roytman - The Power Law of Information Security - Nothing is Linear</div>
</div>


<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/8NlFC199pN0​?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/8NlFC199pN0/default.jpg"></div>
  <div class="desc">Trey Ford - Executive Reporting in the age of Continuous Compromise</div>
</div>



<div class="vid-item" onClick="document.getElementById('vid_frame').src='http://youtube.com/embed/rD4gOHuYAdg​?autoplay=1&rel=0&showinfo=0&autohide=1'">
  <div class="thumb"><img src="http://i.ytimg.com/vi/rD4gOHuYAdg/default.jpg?v=545d4deb"></div>
  <div class="desc">Jay Jacobs - How I Learned to Stop Worrying and Love the Math.</div>
</div>


</div>
</div>

<!-- LEFT AND RIGHT ARROWS -->
<div class="arrows">
<div class="arrow-left"><i class="fa fa-chevron-left fa-lg"></i></div>
<div class="arrow-right"><i class="fa fa-chevron-right fa-lg"></i></div>
</div>

</div>

<!-- JS FOR SCROLLING THE ROW OF THUMBNAILS -->
<script type="text/javascript">
	$(document).ready(function () {
    $(".arrow-right").bind("click", function (event) {
        event.preventDefault();
        $(".vid-list-container").stop().animate({
            scrollLeft: "+=336"
        }, 750);
    });
    $(".arrow-left").bind("click", function (event) {
        event.preventDefault();
        $(".vid-list-container").stop().animate({
            scrollLeft: "-=336"
        }, 750);
    });
});
</script>

<center><a href="http://www.youtube.com/playlist?list=PL5upitoDtl4vYMZMII6XGr7PImGtsZWiN">Direct Playlist Link</a></center>

