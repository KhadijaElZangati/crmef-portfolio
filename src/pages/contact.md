---
layout: layouts/base.njk
title: Contact
---

<section class="section">
  <h2>Contact</h2>
  <div class="card">
    <p class="muted">Tu peux me contacter via ce formulaire.</p>

    <form name="contact" method="POST" data-netlify="true">
      <p>
        <label>Nom<br/><input name="name" required /></label>
      </p>
      <p>
        <label>Email<br/><input type="email" name="email" required /></label>
      </p>
      <p>
        <label>Message<br/><textarea name="message" rows="6" required></textarea></label>
      </p>
      <button class="btn btn--primary" type="submit">Envoyer</button>
    </form>
  </div>
</section>
