---
layout: home
---

<div class="hero">
  <img src="{{ '/assets/images/educaido-logo.png' | relative_url }}" alt="Educaido" class="app-icon" width="128" height="128">

  <h1>Educaido</h1>

  <div class="lang-toggle" role="group" aria-label="Sprache / Language">
    <button type="button" class="lang-btn active" data-lang-btn="de" aria-pressed="true">DE</button><button type="button" class="lang-btn" data-lang-btn="en" aria-pressed="false">EN</button>
  </div>

  <p data-lang="de">Klausurenphase und schon wieder alle Plätze voll? Educaido zeigt dir die über 25 Bibliotheksgebäude in Tübingen, deren Ausstattung, hilfreiche Links und die aktuelle Auslastung. Weniger als 40MB, für iOS und Android.</p>
  <p data-lang="en">Exam season again and every seat is taken? Educaido shows you all 25+ library buildings in Tübingen, their facilities, helpful links, and current occupancy. Under 40MB, for iOS and Android.</p>

  <div class="store-links">
    <a class="store-button" href="https://apps.apple.com/de/app/educaido/id6504367738" target="_blank" rel="noopener">
      <span data-lang="de">Im App Store laden</span><span data-lang="en">Download on the App Store</span>
    </a>
    <a class="store-button" href="https://play.google.com/store/apps/details?id=com.ottenhaus.educado" target="_blank" rel="noopener">
      <span data-lang="de">Jetzt bei Google Play</span><span data-lang="en">Get it on Google Play</span>
    </a>
  </div>
</div>

<script>
  (function () {
    var buttons = document.querySelectorAll('[data-lang-btn]');
    buttons.forEach(function (btn) {
      btn.addEventListener('click', function () {
        var isEn = btn.getAttribute('data-lang-btn') === 'en';
        document.body.classList.toggle('lang-en', isEn);
        buttons.forEach(function (b) {
          var active = b === btn;
          b.classList.toggle('active', active);
          b.setAttribute('aria-pressed', active);
        });
      });
    });
  })();
</script>
