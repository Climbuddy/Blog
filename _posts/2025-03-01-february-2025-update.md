---
layout: post
title:  "February 2025 Update"
category: update
---

It has been a **long** while!

With Tom's master thesis successfully defended, we've been hard at work on a number of issues, with the major focus on admin-related UI improvements, such as statistics and general gym information.
So far, we've been mostly focused on user experience and managed the admin-related things ourselves, but the worker has finally gotten to a point where it produces stable results, meaning that we're **getting ready to the first early release for the gyms...**

<div class="spacer"></div>

{: .tiny}
or we could also just do a Rust rewrite and start from scratch 🦀...

<div class="spacer"></div>

With intrusive thoughts out of the way, **let's review!**


## App

### Charts & Stats

We've implemented a couple of interactive charts for the gym owners (and for the users) to be able to view data gathered by users of the platform, as well as other useful things.
These are the following:

- **User Activity** -- breakdown of user activity per a given time period, which can be either a _time interval_ (i.e. a day/week/month), or _modular_ (day of the week, month of the year, etc...).

- **Route Popularity** -- since we also allow users to like/dislike routes, and rate them softer/harder than the setter's grade, we have a chart that shows the breakdown of these, and allow sorting based on these values/limit to best/worst.

- **Difficulty Breakdown** -- finally, we have a simple per-difficulty breakdown, with information about what success on these difficulties looks like; that is, _out of the people who did something on a route of the difficulty, what is their result_.

<figure class="figures-wrapper">
<div class="figures-container">
  <figure class="center">
    <img src="/assets/2025-02-chart-activity.webp" alt="">
  </figure>

  <figure class="center">
    <img src="/assets/2025-02-chart-popularity.webp" alt="">
  </figure>

  <figure class="center">
    <img src="/assets/2025-02-chart-difficulty.webp" alt="">
  </figure>
</div>
<figcaption>Charts with sample data depicting <strong>User Activity</strong>, <strong>Route Popularity</strong> and <strong>Difficulty Breakdown</strong>.</figcaption>
</figure>

Let us know if you'd like to see more charts, they're really fun to make!

### Gym Overview

We've been ignoring gym overview for a while (to be 100% honest, we've just hardcoded the values).
That changes now, with the gym overview (i.e. what the user sees when looking at the profile of the gym) looking as follows:

<figure class="figures-wrapper">
<div class="figures-container">
  <figure class="center">
    <img src="/assets/2025-02-wall-overview-view.webp" alt="">
  </figure>

  <figure class="center">
    <img src="/assets/2025-02-wall-overview-edit.webp" alt="">
  </figure>
</div>
<figcaption>Gym preview, viewed as the <strong>user</strong> (left) and editable as the <strong>gym</strong> (right).</figcaption>
</figure>

While there are certainly some attributes to be implemented in the future (facilities, news/announcements), we're happy with this state for the next update and will revisit this in consultation with the gyms and users.

### Localization

**We're officially multi-lingual** (jsme oficiálně vícejazyční; Wir sind offiziell mehrsprachig)!

As the Climbuddy team is based in Germany/Czechia, giving users the opportunity to switch to their language of choice is a must.
That's why we've added **Czech 🇨🇿** and **German 🇩🇪**, with more coming in the near future!

<figure class="figures-wrapper">
<div class="figures-container">
  <figure class="center">
    <img src="/assets/2025-02-language-pick.webp" alt="">
  </figure>

  <figure class="center">
    <img src="/assets/2025-02-language-en.webp" alt="">
  </figure>

  <figure class="center">
    <img src="/assets/2025-02-language-cs.webp" alt="">
  </figure>
</div>
<figcaption><strong>Language picker</strong> (left) and the <strong>about section</strong> (middle) <strong>translated to Czech</strong> (right).</figcaption>
</figure>

### Tutorial

From user feedback, we've seen new users struggle controls of the Climbuddy, especially by not realizing that you can **click** on routes and **rotate** the camera.
These are admittedly not immediately obvious, so we've **added a simple tutorial**, which displays the actions you should make to move around, disappearing when they have all been completed.
Additionally, we've added a highlight on routes that you are looking at to further underline that they are interactable.

<figure class="figures-wrapper">
<div class="figures-container">
  <figure class="center">
    <img src="/assets/2025-02-tutorial.webp" alt="">
  </figure>

  <figure class="center">
    <img src="/assets/2025-02-tutorial-hover.webp" alt="">
  </figure>
</div>
<figcaption><strong>Tutorial bar</strong> (left) and <strong>hover outline</strong> (right).</figcaption>
</figure>

### Privacy Policy & Terms of Use

To conclude the UI changes, we've got a final, rather boring one: **privacy policy & terms of use**.
These will both be made available with the release of the new update and reflect our dedication to privacy and openness -- **your information is private** and stays with us, you will be getting **no marketing emails** and sale reminders, and you will **not get diabetes** (i.e. no tracking cookies; only essential ones).


<figure class="figures-wrapper">
<div class="figures-container">
  <figure class="center">
    <img src="/assets/2025-02-terms-of-use.webp" alt="">
  </figure>

  <figure class="center">
    <img src="/assets/2025-02-privacy-policy.webp" alt="">
  </figure>
</div>
<figcaption><strong>Terms of Use</strong> (left) and <strong>Privacy Policy</strong> (right).</figcaption>
</figure>

## Tech

Since this month's focus has been mainly on the UI side of things, we don't have any significant things to show from the backend/worker side of things.
That is not to say that there has been no progress -- we've improved **hyperparameter optimization** for our machine learning models (hold detection/classification), made progress on a more **scalable machine learning pipeline** an implemented an initial **diffing algorithm** for determining which routes were added/removed/kept between old state and a new state.

More details in the next update!

{: .right}
_Team Climbuddy_
