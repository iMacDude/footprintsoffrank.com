---
layout: default
title: "Say Hello"
permalink: /contact/
description: "Write to Frank the zebra — frank@footprintsoffrank.com, or use the form."
---

<style>
.contact{max-width:42em;margin:0 auto;padding:clamp(2rem,5vw,4rem) 0 2rem;color:var(--fg)}
.contact-label{font-family:'Bebas Neue',sans-serif;letter-spacing:.22em;font-size:.82rem;color:var(--red);margin-bottom:.9rem}
.contact-title{font-family:'Bebas Neue',sans-serif;font-size:clamp(2.4rem,6vw,3.6rem);letter-spacing:.06em;color:var(--fg);line-height:1;margin-bottom:1.2rem}
.contact-lede{font-family:'Fraunces',serif;font-style:italic;font-size:1.12rem;color:var(--fg2);line-height:1.6;margin-bottom:2.4rem;max-width:32em}
.contact-form{display:grid;gap:1.15rem;margin-bottom:2.6rem}
.cf-row{display:grid;grid-template-columns:1fr 1fr;gap:1.15rem}
.cf-group{display:flex;flex-direction:column;gap:.45rem;min-width:0}
.cf-group label{font-family:'Bebas Neue',sans-serif;letter-spacing:.18em;font-size:.76rem;color:var(--fg2)}
.cf-group input,.cf-group textarea{
  font-family:'Lora',serif;font-size:1rem;color:var(--fg);
  background:rgba(255,255,255,.03);border:1px solid var(--edge);
  padding:.78rem .9rem;width:100%;transition:border-color .2s,background .2s}
.cf-group input:focus,.cf-group textarea:focus{outline:none;border-color:var(--red);background:rgba(255,255,255,.05)}
.cf-group input::placeholder,.cf-group textarea::placeholder{color:var(--fg3)}
.cf-group textarea{resize:vertical;min-height:8.5rem;line-height:1.6}
.cf-send{
  justify-self:start;font-family:'Bebas Neue',sans-serif;letter-spacing:.2em;font-size:.95rem;
  color:var(--fg);background:transparent;border:1px solid var(--red);
  padding:.8rem 2.1rem;cursor:pointer;transition:background .25s,color .25s}
.cf-send:hover{background:var(--red);color:var(--fg)}
.cf-send:focus-visible{outline:2px solid var(--red);outline-offset:3px}
.contact-or{display:flex;align-items:center;gap:1rem;margin:2.4rem 0 1.6rem;
  font-family:'Bebas Neue',sans-serif;letter-spacing:.2em;font-size:.78rem;color:var(--fg3)}
.contact-or::before,.contact-or::after{content:'';flex:1;height:1px;background:var(--edge)}
.contact-direct{display:grid;gap:.9rem}
.contact-direct a{font-family:'Bebas Neue',sans-serif;letter-spacing:.14em;font-size:1rem;color:var(--fg2);text-decoration:none;
  display:flex;align-items:center;gap:.8rem;transition:color .2s}
.contact-direct a:hover{color:var(--red)}
.contact-direct .cd-key{color:var(--fg3);min-width:6.4rem;font-size:.78rem;letter-spacing:.2em}
.contact-note{font-family:'Fraunces',serif;font-style:italic;font-size:.92rem;color:var(--fg3);line-height:1.6;margin-top:2.4rem;border-left:2px solid var(--edge);padding-left:1.1rem}
@media(max-width:640px){.cf-row{grid-template-columns:1fr}}
</style>

<div class="contact">

  <div class="contact-label">Say hello</div>
  <h1 class="contact-title">Frank reads his own mail.</h1>
  <p class="contact-lede">
    Dad helps with the typing, and the spelling, and reaching the keyboard.
    But the enthusiasm is all mine.
  </p>

{% if site.formspree_id and site.formspree_id != "" %}
  <form class="contact-form" action="https://formspree.io/f/{{ site.formspree_id }}" method="POST">
    <div class="cf-row">
      <div class="cf-group">
        <label for="cf-name">Your name</label>
        <input type="text" id="cf-name" name="name" placeholder="Someone nice" required>
      </div>
      <div class="cf-group">
        <label for="cf-email">Email</label>
        <input type="email" id="cf-email" name="email" placeholder="you@example.com" required>
      </div>
    </div>
    <div class="cf-group">
      <label for="cf-subject">Subject</label>
      <input type="text" id="cf-subject" name="subject" placeholder="Where you spotted a zebra">
    </div>
    <div class="cf-group">
      <label for="cf-message">Message</label>
      <textarea id="cf-message" name="message" placeholder="Tell Frank something good." required></textarea>
    </div>
    <button class="cf-send" type="submit">Send it &rarr;</button>
  </form>

  <div class="contact-or">or just</div>
{% endif %}

  <div class="contact-direct">
    <a href="mailto:frank@footprintsoffrank.com">
      <span class="cd-key">Email</span>frank@footprintsoffrank.com
    </a>
    <a href="https://www.instagram.com/footprintsoffrank/" target="_blank" rel="noopener">
      <span class="cd-key">Instagram</span>@footprintsoffrank
    </a>
    <a href="https://www.facebook.com/footprintsoffrank/" target="_blank" rel="noopener">
      <span class="cd-key">Facebook</span>/footprintsoffrank
    </a>
  </div>

  <p class="contact-note">
    If you met Frank somewhere and took a picture, send it. That is how most of
    this started &mdash; strangers with cameras and no particular reason.
  </p>

</div>
