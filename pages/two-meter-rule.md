---
title: Two Meter Rule  
nav_order: -1
layout: page
permalink: /two-meter-rule
---

<script
  src="https://code.jquery.com/jquery-3.6.0.min.js"
  integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4="
  crossorigin="anonymous"></script>

Two meters horizontally, is the **arbitrary** cut-off distance for transmission that the west has been using during the pandemic. What science is this incorrect **arbitrary** distance did this come from?

## Study: "Two metres or one"

Study: [Two metres or one: what is the evidence for physical distancing in COVID-19?](https://www.bmj.com/content/370/bmj.m3223), by Jones, Qureshi, Temple, Larwood, Greenhalgh, Bourouiba .. during the 
pandemic (Aug 2020).

The historical studies they reviewed and their conclusions:

* Wells (1955): didn't conclude that 2 meters (or so) was significant, or a cut off for transmission
* Flugge (1897): didn't conclude that 2 meters (or so) was significant, or a cut off for transmission

## Booklet: Ectypa Pestilentis

![](https://user-images.githubusercontent.com/82182/132994217-17a31fb1-b4e6-4127-8536-4a6b22b4ad14.png){: .image_on_left}

{: .text_on_right}
☜ The likely origin of the  **six feet rule** is<br> published by a doctor in a book after a <br>plague in the mid 1500's. Doubtless passed from generation to generation of medical professional as fact. <br><br> Read more [in a BBC article from 8th Jan 2021](https://www.bbc.com/future/article/20210107-the-432-year-old-manual-on-social-distancing)<br><br> The US CDC themselves included a discussion<br> [in a September 2013 edition](https://wwwnc.cdc.gov/eid/article/19/9/12-0311_article) <br>of their 'Emerging Infection Diseases' magazine. 

<br><br>

## Research toward a safe distance?

Wells confirmed TB was airborne with hamsters in the middle of the last century and struggled to get that accepted. No studies since that used hamsters to see if there was anything special about six feet / two meters in respect of airborne virus infections.

<script>
$("p.text_on_right").each(function(ix) {
      let img = $("img.image_on_left").first();
      let imgHtml = img.get(0).outerHTML.replace("image_on_left", "ml-3");
      let textHtml = $(this).get(0).outerHTML.replace("text_on_right", "media-body p-4");
      $('<div class="media">' + imgHtml + textHtml + '</div>').insertBefore(this); 
      img.remove();
      $(this).remove();
});
</script>