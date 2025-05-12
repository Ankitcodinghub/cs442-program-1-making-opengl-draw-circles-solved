# cs442-program-1-making-opengl-draw-circles-solved
**TO GET THIS SOLUTION VISIT:** [CS442 Program 1-Making OpenGL Draw Circles Solved](https://www.ankitcodinghub.com/product/cs442-program-1-making-opengl-draw-circles-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91751&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS442 Program 1-Making OpenGL Draw Circles Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Making OpenGL Draw Circles

OpenGL does not draw curved lines. Even when drawing Bezier curves or NURBS surfaces (we’ll discuss these later in the course), ultimately OpenGL is drawing straight lines (including triangle edges). It is possible, however, to approximate a circle by drawing a regular polygon with a large enough value of n, the number of sides.

A traditional rule of thumb in graphics when doing this is to let n be a fixed value (typically 50), but we’re going to do better than that by drawing a polygon that (a) is indistinguishable from a circle on the output hardware and (b) is drawn with the minimum number of lines needed to satsify (a) according to the circle’s radius.

We can think of a circle as a regular polygon with an infinite number of sides, but we are too impatient to actually let n be infinite! Instead, we’ll realize that the resolution of our display is not infinitesimal — in the end, we’re setting pixels on and off — and find the value of n that lets us draw a regular polygon that comes within half a pixel of the true circle, and then just draw a regular polygon with that many sides with that value.

This figure shows the approximation problem for n = 6:

r

D

D is the maximum departure of the polygon from circularity. Perform these steps:

<ol>
<li>Derive a trigonometric formula relating D to r and n. (Note the dependence on r: Approximating bigger circles requires more sides than little ones.)</li>
<li>Let P be the resolution of the screen in NDC coordinates per pixel and solve D = P/2 for n. Using this value of n (or greater) will guarantee that your circle is within a half-pixel of exactness.</li>
<li>Incorporate your newly-discovered formula into Circle::tesselate(), making it tesselate the circle into a regular polygon as a (closed) PolyLine with n sides. (Use ceil(3) to make sure n is an integer.)</li>
<li>Make other changes as instructed in the ASSIGNMENT comments.</li>
</ol>
Assume that P is 0.00119. This is the ratio of the width of the window in NDC coordinates (2.0) to a typical window width in pixels (1680).

</div>
</div>
</div>
