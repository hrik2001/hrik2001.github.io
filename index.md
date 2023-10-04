---
layout: index
title: Home
---
<div class="textbox">
  <p class="textbox-bar announce">Who am I?</p>
  <div class="textbox-content" markdown="1">
Hey there, I'm **Shatabarto Bhattacharya**, but most folks just call me **"Rik"**.

You will find me digging through things related to open source contributions, blockchain,
deep learning, finance (especially derivative markets in decentralized finance) and anything that
involves maths or physics.

An aspiring musician and a self proclaimed music connoisseur, listening to anything from
the soothing rhythms of Bossa Nova to the unique melodies of Tuvan throat singing.
Checkout my [listenbrainz profile](https://listenbrainz.org/user/riksucks/stats/?range=this_year)
to see what I have been listening to lately!

_**This site is still WIP**_

  </div>
</div>

<div class="flex-container">
<div class="mobile-box">
<div class="textbox">
  <p class="textbox-bar">Tech Blog</p>
  <div class="textbox-content" markdown="1">
Test
  </div>
</div>
</div>

<div class="mobile-box">
<div class="textbox">
  <p class="textbox-bar">Miscellaneous Blog</p>
  <div class="textbox-content" markdown="1">
```
Test
Test
```
  </div>
</div>
</div>
</div>

<script>
        // Get all the flex items
        const flexItems = document.querySelectorAll('.flex-container .textbox');
        console.log("Hi")

        // Calculate the maximum height among them
        let maxHeight = 0;
        flexItems.forEach(item => {
            const itemHeight = item.clientHeight;
            if (itemHeight > maxHeight) {
                maxHeight = itemHeight;
            }
        });
        console.log(maxHeight)

        // Set the same height for all flex items
        flexItems.forEach(item => {
            item.style.height = `${maxHeight}px`;
        });
</script>
