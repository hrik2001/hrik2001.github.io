---
layout: index
title: Home
---
<div class="textbox">
  <p class="textbox-bar announce">Who am I?</p>
  <div class="textbox-content" markdown="1">
Hey there, I'm **Shatabarto Bhattacharya**, but most folks just call me **"Rik"**.

My day to day work involves working on **financial simulations** to help **quantify risks** for various
DeFi protocols, writing **ETL pipelines** and contributing to various **FOSS projects**.

In my short career, I have donned multiple hats, some of that include:
- Managing multiple specialized small engineering teams
- Data Engineer (architecting data pipelines)
- Data Science & Mathematics (Convex Optimization, Stochastic Calculus, Probability)
- Smart Contract Development and Testing (Symbolic and Fuzz testing)
- Backend Development (Mostly Python)
- Frontend Development (Typescript and React/Next.js)


</div>
</div>

<div class="flex-container">
<div class="mobile-box">
<div class="textbox">
  <p class="textbox-bar">Tech Blog</p>
  <div class="textbox-content" markdown="1">
  <ul>
    {% assign tech_posts = site.posts | where_exp: "post", "post.categories contains 'tech'" | limit:5 %}
    {% for post in tech_posts %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
  </div>
</div>
</div>

<div class="mobile-box">
<div class="textbox">
  <p class="textbox-bar">Miscellaneous Blog</p>
  <div class="textbox-content" markdown="1">
  <ul>
    {% assign non_tech_posts = 0 %}
    {% for post in site.posts %}
      {% unless post.categories contains 'tech' %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a>
        </li>
        {% assign non_tech_posts = non_tech_posts | plus: 1 %}
      {% endunless %}
      {% break if non_tech_posts == 5 %}  <!-- Limit to 5 non-tech posts -->
    {% endfor %}
  </ul>
  _In the works!_
  </div>
</div>
</div>


</div>




<div class="textbox">
  <p class="textbox-bar blue-bar">Frequently Asked Questions</p>
<div class="textbox-content" markdown="1">
* #### How should I contact you? Or schedule a meeting with you?
Feel free to contact me on [twitter](https://twitter.com/riksucks) or my email
rik61072 [at] gmail [dot] com. I am always down for a chat! Please don't mind if I happen to
reply late, as it is hard for me to juggle college, work, projects and life :)

* #### Are you down for gigs and consultancy work?<br />
Yes! In fact I can help you with these:
    - I can help you plan **tokenomics** and overall protocol economics along with **financial simulations**
    to aid you in further decision making down the line. The scope of the work can also include doing 
    analysis for **incentive distribution** and other methodologies to increase adoption/utilization.

    - I'm available for smart contract auditing gigs and bring hands-on experience from projects
    at _Timeswap Labs, open-source contributions and llamarisk (curveDAO)_. I specialize
    in **boosting code coverage** through
    **fuzz and invariant tests**, assisting in internal **security audits**, conducting **formal verification**
    of your smart contracts against your whitepaper and **preparing codebases** for large
    security audits. My passion, dedication, and practical expertise make me an asset in ensuring the
    security and reliability of your blockchain projects.

    - I can also help you with writing ETL pipelines to consume on-chain data in your backend. I will help you
    write fault tolerant services that will consume and index on-chain events, and can help you set up infrastructure
    around that.

   Let's collaborate to strengthen your ventures.

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
