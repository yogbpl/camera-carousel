# camera-carousel
#HTML
<pre>
    <code class="language-html" data-lang="html">
<span class="nt">&lt;div</span> <span class="na">class=</span><span class="s">"fluid_container"</span><span class="nt">&gt;</span>
    <span class="nt">&lt;div</span> <span class="na">class=</span><span class="s">"camera_wrap"</span> <span class="na">id=</span><span class="s">"camera_wrap"</span><span class="nt">&gt;</span> 
    
    <span class="c">&lt;!--IMAGE SLIDER-1 WORK START --&gt;</span>
    
    <span class="nt">&lt;div</span> <span class="na">data-src=</span><span class="s">"images/background/slider_1.jpg"</span><span class="nt">&gt; &lt;/div&gt;</span>
    
    <span class="c">&lt;!--IMAGE SLIDER-1 WORK END--&gt; </span>
    
    <span class="c">&lt;!--IMAGE SLIDER-2 WORK START --&gt;</span>
    
    <span class="nt">&lt;div</span> <span class="na">data-src=</span><span class="s">"images/background/slider_1.jpg"</span><span class="nt">&gt; &lt;/div&gt;</span>
    
   <span class="c"> &lt;!--IMAGE SLIDER-2 WORK END--&gt; </span>
    
    <span class="nt">&lt;/div&gt;</span>
<span class="nt">&lt;/div&gt;</span>
    </code>
</pre>
#JAVASCRIPT
<pre>
    <code class="language-js" data-lang="js">
<span class="s">&lt;script&gt;</span>
function <span class="na">camera()</span>
{
    jQuery(<span class="s">'#camera_wrap'</span>)<span class="na">.camera(</span>{
        height: <span class="nt">'40%'</span>,
        loader: <span class="nt">'bar'</span>,
        pagination: <span class="nt">false</span>,
        thumbnails: <span class="nt">false</span>,
        playPause: <span class="nt">false</span>,
    }<span class="na">)</span>;
}
function <span class="na">cameraFullScreen()</span>
{
    jQuery(<span class="s">'#camera_wrap'</span>)<span class="na">.camera(</span>{
        height: '<span class="nt">auto</span>',
        loader: '<span class="nt">bar</span>',
        pagination: <span class="nt">false</span>,
        thumbnails: <span class="nt">false</span>,
        playPause: <span class="nt">false</span>,
        hover: <span class="nt">false</span>,
        fx: '<span class="nt">random</span>'
	}<span class="na">)</span>;

	<span class="na">fullCameraSettings()</span>;
}
function <span class="na">fullCameraSettings()</span>
{
    var h=jQuery(<span class="s">window</span>).<span class="na">height()</span>,
    fc=jQuery(<span class="s">'.fluid_container'</span>),
    cw=jQuery(<span class="s">'#camera_wrap'</span>);

    fc.<span class="na">css(</span>{
        'bottom': '0',
        'height':h,
    }<span class="na">)</span>;
    
    cw.<span class="na">css(</span>{
        'bottom': <span class="nt">'0'</span>,
        'height': <span class="nt">'100%'</span>,
        'left': <span class="nt">'0'</span>,
        'margin-bottom': <span class="nt">'0!important'</span>,
        'position': <span class="nt">'relative'</span>,
        'right': <span class="nt">'0'</span>,
        'top': <span class="nt">'0'</span>
    }<span class="na">)</span>;
}
<span class="s">&lt;/script&gt; </span>
<span class="s">&lt;script&gt;</span>
jQuery(<span class="na">function()</span>{
	<span class="c">&lt;!--comment  camera script which you do not want to run--&gt;</span>

    <span class="c">/*FULL SCREEN CAMERA*/</span>
    
    <span class="na">cameraFullScreen()</span>;
    
    jQuery(<span class="s">window</span>).<span class="na">resize(function()</span>{
    	<span class="na">fullCameraSettings()</span>;
    }<span class="na">)</span>;
    
    <span class="c">/*FIXED HEIGHT CAMERA*/</span>
    
    <span class="c">//camera();</span>

});

<span class="s">&lt;/script&gt;</span>
    </code>
</pre>

#noConfilct Method

<h3>master file (index.html)</h3>
<pre>
<span class="nt">&lt;!doctype html&gt;</span>
<span class="nt">&lt;html&gt;</span>
<span class="nt">&lt;head&gt;</span>
<span class="nt">&lt;meta</span> <span class="na">charset=</span><span class="s">"utf-8"</span><span class="nt">&gt;</span>
<span class="nt">&lt;link</span> <span class="na">href=</span><span class="s">"vendor/css/camera.css"</span> <span class="na">rel=</span><span class="s">"stylesheet"</span><span class="nt">&gt;</span>
<span class="nt">&lt;/head&gt;</span>

<span class="nt">&lt;body&gt;</span>
<span class="nt">&lt;div</span> <span class="na">class=</span><span class="s">"fluid_container"</span><span class="nt">&gt;</span>
    <span class="nt">&lt;div</span> <span class="na">class=</span><span class="s">"camera_wrap"</span> <span class="na">id=</span><span class="s">"camera_wrap"</span><span class="nt">&gt;</span> 
    
    <span class="c">&lt;!--IMAGE SLIDER-1 WORK START --&gt;</span>
    
    <span class="nt">&lt;div</span> <span class="na">data-src=</span><span class="s">"images/background/slider_1.jpg"</span><span class="nt">&gt; &lt;/div&gt;</span>
    
    <span class="c">&lt;!--IMAGE SLIDER-1 WORK END--&gt; </span>
    
    <span class="c">&lt;!--IMAGE SLIDER-2 WORK START --&gt;</span>
    
    <span class="nt">&lt;div</span> <span class="na">data-src=</span><span class="s">"images/background/slider_1.jpg"</span><span class="nt">&gt; &lt;/div&gt;</span>
    
   <span class="c"> &lt;!--IMAGE SLIDER-2 WORK END--&gt; </span>
    
    <span class="nt">&lt;/div&gt;</span>
<span class="nt">&lt;/div&gt;</span>
<span class="s">&lt;script</span> <span class="na">type=</span><span class="s">'text/javascript'</span> <span class="na">src=</span><span class="s">'vendor/scripts/jquery.min.js'</span><span class="s">&gt;&lt;/script&gt;</span>
<span class="s">&lt;script</span><span class="na"> type=</span><span class="s">'text/javascript'</span> <span class="na">src=</span><span class="s">'vendor/scripts/jquery.mobile.customized.min.js'</span><span class="s">&gt;&lt;/script&gt;</span> 
<span class="s">&lt;script</span> <span class="na">type=</span><span class="s">'text/javascript'</span> <span class="na">src=</span><span class="s">'vendor/scripts/jquery.easing.1.3.js'</span><span class="s">&gt;&lt;/script&gt; </span>
<span class="s">&lt;script</span> <span class="na">type=</span><span class="s">'text/javascript'</span> <span class="na">src=</span><span class="s">'vendor/scripts/camera.min.js'</span><span class="s">&gt;&lt;/script&gt; </span>
<span class="s">&lt;script&gt;</span>
function <span class="na">camera()</span>
{
    jQuery(<span class="s">'#camera_wrap'</span>)<span class="na">.camera(</span>{
        height: <span class="nt">'40%'</span>,
        loader: <span class="nt">'bar'</span>,
        pagination: <span class="nt">false</span>,
        thumbnails: <span class="nt">false</span>,
        playPause: <span class="nt">false</span>,
    }<span class="na">)</span>;
}
function <span class="na">cameraFullScreen()</span>
{
    jQuery(<span class="s">'#camera_wrap'</span>)<span class="na">.camera(</span>{
        height: '<span class="nt">auto</span>',
        loader: '<span class="nt">bar</span>',
        pagination: <span class="nt">false</span>,
        thumbnails: <span class="nt">false</span>,
        playPause: <span class="nt">false</span>,
        hover: <span class="nt">false</span>,
        fx: '<span class="nt">random</span>'
	}<span class="na">)</span>;

	<span class="na">fullCameraSettings()</span>;
}
function <span class="na">fullCameraSettings()</span>
{
    var h=jQuery(<span class="s">window</span>).<span class="na">height()</span>,
    fc=jQuery(<span class="s">'.fluid_container'</span>),
    cw=jQuery(<span class="s">'#camera_wrap'</span>);

    fc.<span class="na">css(</span>{
        'bottom': '0',
        'height':h,
    }<span class="na">)</span>;
    
    cw.<span class="na">css(</span>{
        'bottom': <span class="nt">'0'</span>,
        'height': <span class="nt">'100%'</span>,
        'left': <span class="nt">'0'</span>,
        'margin-bottom': <span class="nt">'0!important'</span>,
        'position': <span class="nt">'relative'</span>,
        'right': <span class="nt">'0'</span>,
        'top': <span class="nt">'0'</span>
    }<span class="na">)</span>;
}
<span class="s">&lt;/script&gt; </span>
<span class="s">&lt;script&gt;</span>
jQuery(<span class="na">function()</span>{
	<span class="c">&lt;!--comment  camera script which you do not want to run--&gt;</span>

    <span class="c">/*FULL SCREEN CAMERA*/</span>
    
    <span class="na">cameraFullScreen()</span>;
    
    jQuery(<span class="s">window</span>).<span class="na">resize(function()</span>{
    	<span class="na">fullCameraSettings()</span>;
    }<span class="na">)</span>;
    
    <span class="c">/*FIXED HEIGHT CAMERA*/</span>
    
    <span class="c">//camera();</span>

});

<span class="s">&lt;/script&gt;</span>
<span class="nt">&lt;/body&gt;</span>
<span class="nt">&lt;/html&gt;</span>

</pre>
<h3>noConflict file (camera-noConflict.html)</h3>
<pre>
<code>
&lt;!doctype html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;meta charset="utf-8"&gt;
&lt;title&gt;Camera Carousel&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;div id="slider"&gt;&lt;/div&gt;

&lt;script src="js/jquery-1.11.1.min.js"&gt;&lt;/script&gt;

&lt;script&gt;
jQuery(function(){
	jQuery.ajax({
		type:"GET",
		url:"index.html",
		data:"",
		success: function(data){
			$('#slider').html(data);
		}
	});
	})
&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
</code>
</pre>

#view demo
<a href="#">View Demo</a>
