# T10

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>getebook.ai | Write an ebook once, let it earn forever</title>

<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #ffffff;
  --text: #3c302a;
  --heading: #352923;
  --accent: #ff7658;
  --accent-dark: #eb6549;
  --muted: #928983;
  --border: #eeeae6;
  --card: #ffffff;
  --green: #648c68;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: "DM Sans", sans-serif;
  background: #fff;
  color: var(--text);
  line-height: 1.7;
  overflow-x: hidden;
}

a {
  text-decoration: none;
  color: inherit;
}

button {
  font-family: inherit;
}

.container {
  width: min(1120px, calc(100% - 48px));
  margin: auto;
}

/* =========================
   NAVIGATION
========================= */

.nav-wrapper {
  position: sticky;
  top: 0;
  z-index: 1000;
  background: rgba(255,255,255,.96);
  backdrop-filter: blur(15px);
  border-bottom: 1px solid #f2efec;
}

nav {
  height: 86px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  display: flex;
  align-items: center;
  gap: 11px;
  font-size: 27px;
  font-weight: 800;
  letter-spacing: -1px;
  color: #382e29;
}

.logo-icon {
  font-size: 33px;
  color: var(--accent);
}

.logo span:last-child {
  color: var(--accent);
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 28px;
  font-size: 14px;
  font-weight: 600;
}

.nav-links a:hover {
  color: var(--accent);
}

.nav-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 12px 21px;
  border-radius: 10px;
  font-weight: 700;
  font-size: 14px;
  border: none;
  cursor: pointer;
  transition: .2s;
}

.btn-primary {
  color: white;
  background: var(--accent);
}

.btn-primary:hover {
  background: var(--accent-dark);
  transform: translateY(-2px);
}

.btn-outline {
  border: 1px solid var(--border);
  background: white;
}

.menu-button {
  display: none;
  font-size: 27px;
  border: 0;
  background: none;
  cursor: pointer;
  color: var(--heading);
}

/* =========================
   HERO
========================= */

.hero {
  padding: 95px 0 75px;
  text-align: center;
}

.hero-badge {
  display: inline-flex;
  padding: 7px 17px;
  border: 1px solid var(--border);
  border-radius: 50px;
  background: #fff;
  color: var(--muted);
  font-size: 13px;
  margin-bottom: 26px;
}

.hero h1 {
  font-size: clamp(42px, 6vw, 68px);
  line-height: 1.12;
  letter-spacing: -2.5px;
  color: var(--heading);
  font-weight: 800;
  margin-bottom: 22px;
}

.hero-description {
  max-width: 650px;
  margin: auto;
  color: #81766f;
  font-size: 19px;
}

.examples {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 10px;
  margin: 30px 0;
}

.example {
  padding: 9px 16px;
  border: 1px solid var(--border);
  background: #fff;
  border-radius: 50px;
  font-size: 13px;
  color: #746b65;
}

.hero-note {
  color: var(--muted);
  font-size: 13px;
  margin-bottom: 23px;
}

.hero-buttons {
  display: flex;
  justify-content: center;
  gap: 13px;
  flex-wrap: wrap;
  margin-bottom: 42px;
}

.btn-large {
  padding: 15px 27px;
  font-size: 15px;
  border-radius: 11px;
}

.platform-label {
  font-size: 11px;
  letter-spacing: 2px;
  color: var(--muted);
  margin-bottom: 15px;
}

.platforms {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 35px;
  color: #635951;
  font-weight: 800;
  font-size: 17px;
}

/* =========================
   BOOK PREVIEW
========================= */

.book-section {
  padding: 65px 0 100px;
  text-align: center;
  background: #fff;
}

.section-label {
  color: var(--accent-dark);
  font-size: 12px;
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-bottom: 10px;
}

.book-section h2,
.how h2,
.testimonials h2,
.pricing h2,
.faq h2 {
  color: var(--heading);
  font-size: clamp(29px, 4vw, 39px);
  line-height: 1.2;
  letter-spacing: -1px;
}

.section-description {
  color: var(--muted);
  max-width: 600px;
  margin: 16px auto 38px;
  font-size: 16px;
}

.book-carousel {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 25px;
}

.book-card {
  width: 300px;
  background: white;
  border: 1px solid var(--border);
  padding: 20px;
  border-radius: 18px;
  box-shadow: 0 8px 35px rgba(0,0,0,.04);
}

.book-cover {
  height: 260px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  color: white;
  background: linear-gradient(140deg,#315f42,#163d2c);
  font-size: 25px;
  font-weight: 800;
  padding: 25px;
  line-height: 1.2;
}

.book-cover.second {
  background: linear-gradient(140deg,#e6a66d,#9a5439);
}

.book-cover small {
  font-size: 12px;
  margin-top: 15px;
  letter-spacing: 2px;
}

.book-title {
  font-weight: 800;
  margin-top: 17px;
}

.book-meta,
.page-indicator {
  color: var(--muted);
  font-size: 13px;
}

/* =========================
   FEATURES
   SCREENSHOT-INSPIRED DESIGN
========================= */

.features {
  padding: 75px 0 100px;
  background: #fff;
}

.features-heading {
  text-align: center;
  margin-bottom: 65px;
}

.features-tabs {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 14px;
  margin-bottom: 34px;
  font-size: 17px;
}

.features-pill {
  display: inline-block;
  background: var(--accent);
  color: white;
  font-weight: 800;
  padding: 5px 19px;
  border-radius: 50px;
}

.features-tab-text {
  color: #a19a96;
  font-weight: 500;
}

.features-heading h2 {
  color: #382d28;
  font-size: clamp(34px, 5vw, 49px);
  line-height: 1.2;
  letter-spacing: -1.7px;
  max-width: 760px;
  margin: auto;
  font-weight: 800;
}

.features-heading p {
  color: #99918c;
  font-size: 18px;
  max-width: 700px;
  margin: 24px auto 0;
  line-height: 1.75;
}

.feature-list {
  display: flex;
  flex-direction: column;
  gap: 48px;
  max-width: 940px;
  margin: auto;
}

.feature-card {
  padding: 42px;
  border: 1px solid #efedea;
  border-radius: 32px;
  background: #fff;
  box-shadow: 0 12px 35px rgba(45,35,25,.035);
  transition: .3s;
}

.feature-card:hover {
  box-shadow: 0 16px 40px rgba(45,35,25,.065);
  transform: translateY(-3px);
}

.feature-top {
  display: flex;
  align-items: flex-start;
  gap: 26px;
  margin-bottom: 38px;
}

.feature-icon {
  width: 80px;
  height: 80px;
  min-width: 80px;
  border-radius: 22px;
  background: #fff0ed;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--accent-dark);
}

.feature-icon svg {
  width: 34px;
  height: 34px;
  stroke: currentColor;
  fill: none;
  stroke-width: 2;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.feature-text h3 {
  font-size: 26px;
  color: #382e29;
  font-weight: 800;
  letter-spacing: -.5px;
  margin-bottom: 12px;
  line-height: 1.3;
}

.feature-text p {
  font-size: 18px;
  line-height: 1.75;
  color: #99918c;
  max-width: 650px;
}

/* Illustration containers */

.feature-visual {
  min-height: 330px;
  border: 1px solid #f0ece7;
  border-radius: 25px;
  background:
    radial-gradient(ellipse at top, #fff0e9 0%, #fffaf7 34%, #fff 75%);
  padding: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

/* Illustration 1 */

.idea-demo {
  width: 100%;
  display: flex;
  justify-content: space-around;
  align-items: center;
  gap: 25px;
}

.idea-left {
  flex: 1;
  max-width: 400px;
}

.demo-label {
  color: #bf8d79;
  font-size: 10px;
  font-weight: 800;
  letter-spacing: 2px;
}

.idea-left h4 {
  color: #392d27;
  font-size: 20px;
  margin: 8px 0 15px;
}

.idea-input {
  border: 2px solid #e9b7a4;
  background: white;
  border-radius: 9px;
  padding: 13px;
  font-size: 12px;
  box-shadow: 0 3px 10px rgba(0,0,0,.04);
}

.idea-arrow {
  font-size: 35px;
  color: #dc9278;
}

.mini-book {
  width: 135px;
  min-height: 200px;
  border-radius: 7px;
  background: #155234;
  color: white;
  padding: 17px 10px;
  text-align: center;
  box-shadow: 8px 10px 18px rgba(0,0,0,.16);
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: space-between;
}

.mini-book strong {
  font-size: 15px;
  line-height: 1.2;
}

.mini-book span {
  font-size: 12px;
}

.mini-book .plant {
  font-size: 65px;
}

.ready-label {
  background: #e9f0e5;
  color: #64865e;
  border-radius: 20px;
  font-size: 10px;
  padding: 5px 10px;
  margin-top: 12px;
}

/* Illustration 2 */

.cover-demo {
  width: 100%;
  text-align: center;
}

.cover-demo-heading {
  font-size: 22px;
  font-weight: 800;
  color: #40332d;
  margin-bottom: 40px;
}

.cover-demo-heading span {
  color: var(--accent);
}

.cover-books {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 8px;
}

.cover-book {
  width: 145px;
  height: 205px;
  padding: 14px 9px;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  color: white;
  font-weight: 800;
  font-size: 18px;
  line-height: 1.15;
  box-shadow: 0 10px 18px rgba(0,0,0,.13);
}

.cover-book small {
  font-size: 9px;
  line-height: 1.4;
}

.cover-book.one {
  background: linear-gradient(145deg,#d94c2f,#a82b23);
  transform: rotate(-6deg);
}

.cover-book.two {
  background: linear-gradient(145deg,#123b43,#071f31);
  border: 3px solid #f1b3a0;
  transform: translateY(-12px);
}

.cover-book.three {
  background: linear-gradient(145deg,#f58a42,#c75d25);
  transform: rotate(6deg);
}

/* Illustration 3 */

.formats-demo {
  width: 100%;
  text-align: center;
}

.formats-demo h4 {
  font-size: 24px;
  color: #42332c;
  margin-bottom: 35px;
}

.format-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0,1fr));
  gap: 18px;
  max-width: 590px;
  margin: auto;
}

.format-item {
  background: white;
  border: 1px solid #f0e9e4;
  border-radius: 14px;
  padding: 20px 10px;
  box-shadow: 0 6px 20px rgba(0,0,0,.035);
}

.format-item span {
  font-size: 32px;
  display: block;
  margin-bottom: 8px;
}

.format-item strong {
  font-size: 13px;
  color: #4a3930;
}

/* Illustration 4 */

.export-demo {
  width: 100%;
  max-width: 620px;
  text-align: center;
}

.export-demo h4 {
  font-size: 24px;
  margin-bottom: 25px;
}

.export-options {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
}

.export-file {
  width: 140px;
  padding: 25px 12px;
  background: white;
  border: 1px solid #eee5df;
  border-radius: 13px;
  box-shadow: 0 7px 20px rgba(0,0,0,.04);
}

.export-file span {
  display: block;
  font-size: 36px;
  color: var(--accent);
  margin-bottom: 10px;
}

.export-file strong {
  font-size: 15px;
}

/* =========================
   HOW IT WORKS
========================= */

.how {
  padding: 90px 0;
  background: #fffaf7;
}

.how h2 {
  text-align: center;
  margin-bottom: 55px;
}

.steps {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 28px;
}

.step {
  text-align: center;
  padding: 28px;
}

.step-number {
  width: 52px;
  height: 52px;
  margin: 0 auto 18px;
  border-radius: 50%;
  background: var(--accent);
  color: white;
  display: grid;
  place-items: center;
  font-weight: 800;
  font-size: 20px;
}

.step h3 {
  color: var(--heading);
  margin-bottom: 10px;
  font-size: 20px;
}

.step p {
  color: var(--muted);
  font-size: 15px;
}

/* =========================
   TESTIMONIALS
========================= */

.testimonials {
  padding: 90px 0;
}

.testimonials h2 {
  text-align: center;
}

.testimonial-sub {
  text-align: center;
  color: var(--muted);
  margin: 13px 0 40px;
}

.testimonial-grid {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 20px;
}

.testimonial {
  border: 1px solid var(--border);
  border-radius: 17px;
  padding: 24px;
  background: white;
}

.testimonial-header {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 15px;
}

.avatar {
  width: 43px;
  height: 43px;
  border-radius: 50%;
  background: #fff0e9;
  display: grid;
  place-items: center;
  font-weight: 800;
}

.testimonial-name {
  font-weight: 800;
}

.testimonial-role {
  font-size: 12px;
  color: var(--muted);
}

.stars {
  color: #f1a94c;
  letter-spacing: 2px;
  margin-bottom: 10px;
}

.testimonial p {
  font-size: 14px;
  color: #726760;
}

.testimonial-result {
  margin-top: 15px;
  font-weight: 800;
  font-size: 13px;
  color: var(--green);
}

/* =========================
   PRICING
========================= */

.pricing {
  padding: 90px 0;
  background: #fffaf7;
  text-align: center;
}

.pricing h2 {
  margin-bottom: 15px;
}

.pricing-sub {
  color: var(--muted);
  margin-bottom: 50px;
}

.price-card {
  max-width: 470px;
  margin: auto;
  background: white;
  border: 2px solid var(--accent);
  border-radius: 20px;
  padding: 38px;
  position: relative;
  text-align: left;
}

.popular-label {
  position: absolute;
  top: -14px;
  left: 50%;
  transform: translateX(-50%);
  padding: 5px 17px;
  background: var(--accent);
  color: white;
  border-radius: 30px;
  font-size: 11px;
  font-weight: 800;
  white-space: nowrap;
}

.price-card h3 {
  font-size: 24px;
}

.price {
  font-size: 49px;
  font-weight: 800;
  color: var(--heading);
}

.price span {
  font-size: 15px;
  color: var(--muted);
  font-weight: 500;
}

.credits {
  color: var(--muted);
  font-size: 14px;
}

.price-features {
  list-style: none;
  margin: 25px 0;
}

.price-features li {
  padding: 8px 0;
  font-size: 14px;
}

.price-features li::before {
  content: "✓";
  color: var(--green);
  font-weight: 800;
  margin-right: 10px;
}

.price-card .btn {
  width: 100%;
}

.tier-heading {
  margin: 55px 0 20px;
}

.tiers {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 12px;
}

.tier {
  padding: 15px 22px;
  border: 1px solid var(--border);
  border-radius: 12px;
  background: white;
  font-weight: 700;
  font-size: 14px;
}

.tier.active {
  border-color: var(--accent);
  background: #fff2ed;
}

/* =========================
   FAQ
========================= */

.faq {
  padding: 90px 0;
}

.faq h2 {
  text-align: center;
  margin-bottom: 40px;
}

.faq-list {
  max-width: 750px;
  margin: auto;
}

.faq-item {
  border-bottom: 1px solid var(--border);
  padding: 20px 0;
}

.faq-question {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
  font-weight: 700;
  font-size: 16px;
  cursor: pointer;
}

.faq-question span {
  color: var(--accent);
  font-size: 23px;
}

.faq-answer {
  display: none;
  color: var(--muted);
  font-size: 14px;
  padding-top: 13px;
}

.faq-item.open .faq-answer {
  display: block;
}

/* =========================
   FINAL CTA
========================= */

.final-cta {
  text-align: center;
  padding: 95px 20px;
  background: linear-gradient(180deg,#fff,#fff4ee);
}

.final-cta h2 {
  font-size: clamp(30px,4vw,43px);
  line-height: 1.2;
  color: var(--heading);
  margin-bottom: 15px;
}

.final-cta p {
  max-width: 540px;
  color: var(--muted);
  margin: 0 auto 28px;
}

.final-notes {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 25px;
  color: var(--muted);
  font-size: 13px;
  margin-top: 23px;
}

/* =========================
   FOOTER
========================= */

footer {
  padding: 60px 0 25px;
  border-top: 1px solid var(--border);
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.5fr repeat(3,1fr);
  gap: 35px;
  margin-bottom: 45px;
}

.footer-brand {
  font-size: 23px;
  font-weight: 800;
  margin-bottom: 10px;
}

footer p,
footer a {
  color: var(--muted);
  font-size: 13px;
}

footer h4 {
  font-size: 13px;
  margin-bottom: 15px;
  text-transform: uppercase;
}

footer ul {
  list-style: none;
}

footer li {
  margin-bottom: 10px;
}

footer a:hover {
  color: var(--accent);
}

.copyright {
  text-align: center;
  border-top: 1px solid var(--border);
  padding-top: 22px;
  color: var(--muted);
  font-size: 12px;
}

/* =========================
   MOBILE RESPONSIVE
========================= */

@media(max-width: 768px) {

  .container {
    width: calc(100% - 38px);
  }

  nav {
    height: 76px;
  }

  .logo {
    font-size: 23px;
  }

  .logo-icon {
    font-size: 29px;
  }

  .nav-links,
  .nav-actions {
    display: none;
  }

  .menu-button {
    display: block;
  }

  .mobile-menu {
    display: none;
    background: white;
    border-top: 1px solid var(--border);
    padding: 15px 22px 22px;
  }

  .mobile-menu.open {
    display: flex;
    flex-direction: column;
    gap: 15px;
  }

  .mobile-menu a {
    font-weight: 600;
    padding: 5px 0;
  }

  .hero {
    padding: 58px 0 55px;
  }

  .hero h1 {
    font-size: 43px;
    letter-spacing: -1.5px;
  }

  .hero-description {
    font-size: 16px;
  }

  .platforms {
    gap: 18px;
    font-size: 14px;
  }

  .book-section {
    padding: 45px 0 65px;
  }

  .book-card {
    width: 100%;
    max-width: 330px;
  }

  .features {
    padding: 45px 0 70px;
  }

  .features-heading {
    margin-bottom: 55px;
  }

  .features-tabs {
    margin-bottom: 35px;
    font-size: 17px;
    gap: 13px;
  }

  .features-pill {
    padding: 4px 17px;
  }

  .features-heading h2 {
    font-size: 37px;
    letter-spacing: -1.3px;
    line-height: 1.23;
  }

  .features-heading p {
    font-size: 17px;
    line-height: 1.8;
    margin-top: 25px;
  }

  .feature-list {
    gap: 48px;
  }

  .feature-card {
    padding: 42px 25px;
    border-radius: 30px;
  }

  .feature-top {
    gap: 25px;
    margin-bottom: 36px;
  }

  .feature-icon {
    width: 80px;
    height: 80px;
    min-width: 80px;
    border-radius: 22px;
  }

  .feature-text h3 {
    font-size: 25px;
    line-height: 1.35;
    margin-bottom: 12px;
  }

  .feature-text p {
    font-size: 17px;
    line-height: 1.8;
  }

  .feature-visual {
    min-height: 320px;
    padding: 20px 13px;
    border-radius: 23px;
  }

  .idea-demo {
    gap: 9px;
  }

  .idea-left h4 {
    font-size: 15px;
  }

  .idea-input {
    font-size: 10px;
    padding: 10px;
  }

  .idea-arrow {
    font-size: 24px;
  }

  .mini-book {
    width: 105px;
    min-height: 165px;
    padding: 12px 7px;
  }

  .mini-book strong {
    font-size: 12px;
  }

  .mini-book .plant {
    font-size: 48px;
  }

  .cover-demo-heading {
    font-size: 18px;
  }

  .cover-book {
    width: 30%;
    height: 175px;
    font-size: 14px;
  }

  .format-grid {
    gap: 9px;
  }

  .format-item {
    padding: 16px 5px;
  }

  .format-item span {
    font-size: 26px;
  }

  .format-item strong {
    font-size: 11px;
  }

  .export-file {
    width: 105px;
  }

  .steps,
  .testimonial-grid {
    grid-template-columns: 1fr;
  }

  .step {
    padding: 18px;
  }

  .footer-grid {
    grid-template-columns: 1fr 1fr;
    gap: 30px 20px;
  }

  .price-card {
    padding: 30px 23px;
  }
}

@media(max-width: 390px) {

  .features-heading h2 {
    font-size: 33px;
  }

  .feature-card {
    padding: 30px 19px;
  }

  .feature-top {
    gap: 16px;
  }

  .feature-icon {
    width: 62px;
    height: 62px;
    min-width: 62px;
  }

  .feature-icon svg {
    width: 27px;
    height: 27px;
  }

  .feature-text h3 {
    font-size: 21px;
  }

  .feature-text p {
    font-size: 15px;
  }

  .feature-visual {
    min-height: 265px;
  }

  .mini-book {
    width: 85px;
  }

  .cover-book {
    height: 145px;
    font-size: 12px;
  }
}

</style>
</head>

<body>

<!-- NAVIGATION -->

<div class="nav-wrapper">
  <div class="container">
    <nav>

      <a href="#" class="logo">
        <span class="logo-icon">📖</span>
        getebook<span>.ai</span>
      </a>

      <div class="nav-links">
        <a href="#how">How it works</a>
        <a href="#features">Features</a>
        <a href="#pricing">Pricing</a>
        <a href="#faq">FAQ</a>
      </div>

      <div class="nav-actions">
        <a href="#cta" class="btn btn-outline">Log in</a>
        <a href="#cta" class="btn btn-primary">Start building, free</a>
      </div>

      <button class="menu-button" id="menuButton" aria-label="Open menu">
        ☰
      </button>

    </nav>
  </div>

  <div class="mobile-menu" id="mobileMenu">
    <a href="#how">How it works</a>
    <a href="#features">Features</a>
    <a href="#pricing">Pricing</a>
    <a href="#faq">FAQ</a>
    <a href="#cta">Start building, free</a>
  </div>
</div>


<!-- HERO -->

<section class="hero">
  <div class="container">

    <div class="hero-badge">
      Loved by 12,000+ creators publishing with AI
    </div>

    <h1>
      Write it once.<br>
      Let it earn forever.
    </h1>

    <p class="hero-description">
      Just tell Booker what you know. Watch it write every chapter
      and design your cover, building your finished ebook live
      in front of you.
    </p>

    <div class="examples">
      <span class="example">A meal-prep guide for busy parents</span>
      <span class="example">Side-hustle 101 for complete beginners</span>
      <span class="example">A productivity system that actually sticks</span>
    </div>

    <p class="hero-note">
      No credit card to start · Cancel anytime · Plans from $29/mo
    </p>

    <div class="hero-buttons">
      <a href="#cta" class="btn btn-primary btn-large">
        Start building, free
      </a>

      <a href="#books" class="btn btn-outline btn-large">
        See how it works ↓
      </a>
    </div>

    <div class="platform-label">PUBLISH AND SELL ON</div>

    <div class="platforms">
      <span>Amazon KDP</span>
      <span>Etsy</span>
      <span>Apple Books</span>
      <span>Gumroad</span>
      <span>Shopify</span>
    </div>

  </div>
</section>


<!-- BOOK PREVIEW -->

<section class="book-section" id="books">
  <div class="container">

    <div class="section-label">Flip through a real book</div>

    <h2>See exactly what you'll create</h2>

    <p class="section-description">
      Preview the kind of ebooks you can create with your ideas.
      From professional guides to beautifully designed books.
    </p>

    <div class="book-carousel">

      <div class="book-card">

        <div class="book-cover">
          MEAL PREP
          <small>MADE EASY FOR PARENTS</small>
          <span style="font-size:55px;margin-top:20px;">🥗</span>
        </div>

        <div class="book-title">
          Meal Prep Made Easy for Parents
        </div>

        <div class="book-meta">
          eBook · Cover + 10 pages
        </div>

        <div class="page-indicator">1 of 12</div>

      </div>

      <div class="book-card">

        <div class="book-cover second">
          PIP'S GARDEN
          <small>TEA PARTY</small>
          <span style="font-size:55px;margin-top:20px;">🌷</span>
        </div>

        <div class="book-title">
          Pip's Garden Tea Party
        </div>

        <div class="book-meta">
          Coloring book · Cover + 10 pages
        </div>

        <div class="page-indicator">1 of 12</div>

      </div>

    </div>
  </div>
</section>


<!-- FEATURES -->

<section class="features" id="features">

  <div class="container">

    <div class="features-heading">

      <div class="features-tabs">
        <span class="features-pill">Features</span>
        <span class="features-tab-text">What you get</span>
      </div>

      <h2>
        Everything you need to<br>
        publish and profit
      </h2>

      <p>
        No writing degree, no design skills, no ghostwriter invoice.
        Just your idea and a few minutes.
      </p>

    </div>


    <div class="feature-list">


      <!-- FEATURE 1 -->

      <div class="feature-card">

        <div class="feature-top">

          <div class="feature-icon">

            <svg viewBox="0 0 24 24">
              <path d="M12 20h9"/>
              <path d="M16.5 3.5a2.1 2.1 0 0 1 3 3L8 18l-4 1 1-4Z"/>
            </svg>

          </div>

          <div class="feature-text">

            <h3>From idea to finished book</h3>

            <p>
              Type one sentence about what you know.
              getebook turns it into a titled, chaptered,
              fully written ebook.
            </p>

          </div>

        </div>

        <div class="feature-visual">

          <div class="idea-demo">

            <div class="idea-left">

              <div class="demo-label">YOUR IDEA</div>

              <h4>From idea to finished book.</h4>

              <div class="idea-input">
                How to grow tomatoes in small spaces
              </div>

            </div>

            <div class="idea-arrow">→</div>

            <div>

              <div class="mini-book">

                <strong>
                  THE BACKYARD<br>
                  MEDICINAL<br>
                  GARDEN GUIDE
                </strong>

                <span>Grow, harvest and preserve</span>

                <div class="plant">🌿</div>

              </div>

              <div class="ready-label">
                ✓ Full ebook ready
              </div>

            </div>

          </div>

        </div>

      </div>


      <!-- FEATURE 2 -->

      <div class="feature-card">

        <div class="feature-top">

          <div class="feature-icon">

            <svg viewBox="0 0 24 24">
              <rect x="3" y="3" width="18" height="18" rx="2"/>
              <circle cx="8.5" cy="8.5" r="1.5"/>
              <path d="m21 15-5-5L5 21"/>
            </svg>

          </div>

          <div class="feature-text">

            <h3>Covers that earn the click</h3>

            <p>
              Get a professional cover designed for you,
              the kind that stands out on a crowded store page.
            </p>

          </div>

        </div>

        <div class="feature-visual">

          <div class="cover-demo">

            <div class="demo-label">COVER STUDIO</div>

            <div class="cover-demo-heading">
              Covers that <span>earn the click</span>
            </div>

            <div class="cover-books">

              <div class="cover-book one">
                <div>
                  DATING<br>
                  MASTERY
                </div>
                <small>FOR MEN OVER 50</small>
                <span style="font-size:35px;">👨</span>
              </div>

              <div class="cover-book two">
                <div>
                  THE SMALL<br>
                  INVESTOR'S<br>
                  BLUEPRINT
                </div>
                <span style="font-size:35px;">📈</span>
                <small>MASTER YOUR MONEY</small>
              </div>

              <div class="cover-book three">
                <div>
                  BALANCED<br>
                  & BRILLIANT
                </div>
                <span style="font-size:35px;">🌟</span>
                <small>A BETTER DAILY LIFE</small>
              </div>

            </div>

          </div>

        </div>

      </div>


      <!-- FEATURE 3 -->

      <div class="feature-card">

        <div class="feature-top">

          <div class="feature-icon">

            <svg viewBox="0 0 24 24">
              <rect x="3" y="3" width="7" height="7" rx="1"/>
              <rect x="14" y="3" width="7" height="7" rx="1"/>
              <rect x="3" y="14" width="7" height="7" rx="1"/>
              <rect x="14" y="14" width="7" height="7" rx="1"/>
            </svg>

          </div>

          <div class="feature-text">

            <h3>Ebooks and coloring books</h3>

            <p>
              Lead magnets, guides, reports, workbooks,
              courses, and novels, plus a studio for
              print-ready coloring books. Pick what fits your goal.
            </p>

          </div>

        </div>

        <div class="feature-visual">

          <div class="formats-demo">

            <div class="demo-label">ONE TOOL</div>

            <h4>Six formats, <span style="color:var(--accent)">one tool</span></h4>

            <div class="format-grid">

              <div class="format-item">
                <span>📘</span>
                <strong>eBooks</strong>
              </div>

              <div class="format-item">
                <span>🎨</span>
                <strong>Coloring books</strong>
              </div>

              <div class="format-item">
                <span>📚</span>
                <strong>Workbooks</strong>
              </div>

              <div class="format-item">
                <span>📝</span>
                <strong>Guides</strong>
              </div>

              <div class="format-item">
                <span>📖</span>
                <strong>Novels</strong>
              </div>

              <div class="format-item">
                <span>🎓</span>
                <strong>Courses</strong>
              </div>

            </div>

          </div>

        </div>

      </div>


      <!-- FEATURE 4 -->

      <div class="feature-card">

        <div class="feature-top">

          <div class="feature-icon">

            <svg viewBox="0 0 24 24">
              <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8Z"/>
              <path d="M14 2v6h6"/>
              <path d="M8 13h8"/>
              <path d="M8 17h8"/>
            </svg>

          </div>

          <div class="feature-text">

            <h3>Store-ready in one click</h3>

            <p>
              Export a clean, typeset PDF or EPUB that is ready
              for KDP, Etsy, or Apple Books the same day.
            </p>

          </div>

        </div>

        <div class="feature-visual">

          <div class="export-demo">

            <div class="demo-label">YOUR FINISHED BOOK</div>

            <h4>Ready to publish and share</h4>

            <div class="export-options">

              <div class="export-file">
                <span>📕</span>
                <strong>PDF</strong>
              </div>

              <div class="export-file">
                <span>📗</span>
                <strong>EPUB</strong>
              </div>

              <div class="export-file">
                <span>📘</span>
                <strong>DOCX</strong>
              </div>

            </div>

          </div>

        </div>

      </div>


    </div>

  </div>

</section>


<!-- HOW IT WORKS -->

<section class="how" id="how">

  <div class="container">

    <div class="section-label" style="text-align:center">
      IDEA TO SELLABLE EBOOK, LIVE
    </div>

    <h2>Three steps from your idea to a published ebook</h2>

    <div class="steps">

      <div class="step">

        <div class="step-number">1</div>

        <h3>Tell Booker your idea</h3>

        <p>
          Describe what you know in a sentence.
          Booker turns it into a titled, chaptered ebook brief.
          That is the whole setup.
        </p>

      </div>

      <div class="step">

        <div class="step-number">2</div>

        <h3>Watch it build live</h3>

        <p>
          Booker writes every chapter and designs your cover.
          Preview the whole ebook, cover to cover,
          and edit anything before you commit.
        </p>

      </div>

      <div class="step">

        <div class="step-number">3</div>

        <h3>Go Pro, download and sell</h3>

        <p>
          Unlock downloads with Pro.
          Export a store-ready PDF, EPUB, or DOCX
          and list it on your preferred platform.
        </p>

      </div>

    </div>

  </div>

</section>


<!-- TESTIMONIALS -->

<section class="testimonials">

  <div class="container">

    <div class="section-label" style="text-align:center">
      CREATOR STORIES
    </div>

    <h2>Real creators. Real experiences.</h2>

    <p class="testimonial-sub">
      Sample testimonials — replace with verified customer reviews before launch.
    </p>

    <div class="testimonial-grid">


      <div class="testimonial">

        <div class="testimonial-header">
          <div class="avatar">BH</div>
          <div>
            <div class="testimonial-name">Ben H.</div>
            <div class="testimonial-role">Side-hustle creator</div>
          </div>
        </div>

        <div class="stars">★★★★★</div>

        <p>
          "I turned a topic I already knew well into a short guide
          over a weekend. The process made creating my first ebook
          much easier."
        </p>

        <div class="testimonial-result">Idea to first guide</div>

      </div>


      <div class="testimonial">

        <div class="testimonial-header">
          <div class="avatar">DR</div>
          <div>
            <div class="testimonial-name">David R.</div>
            <div class="testimonial-role">Newsletter writer</div>
          </div>
        </div>

        <div class="stars">★★★★★</div>

        <p>
          "I always meant to write an ebook and never did.
          Having a structured writing process helped me
          finally get started."
        </p>

        <div class="testimonial-result">More books created</div>

      </div>


      <div class="testimonial">

        <div class="testimonial-header">
          <div class="avatar">SK</div>
          <div>
            <div class="testimonial-name">Sofia K.</div>
            <div class="testimonial-role">Marketing consultant</div>
          </div>
        </div>

        <div class="stars">★★★★★</div>

        <p>
          "The cover and formatting are what I liked most.
          Having everything in one workflow saves time."
        </p>

        <div class="testimonial-result">Simpler publishing workflow</div>

      </div>


    </div>

  </div>

</section>


<!-- PRICING -->

<section class="pricing" id="pricing">

  <div class="container">

    <div class="section-label">START FREE, PAY ONLY IF YOU PUBLISH</div>

    <h2>Plans from $29/mo</h2>

    <p class="pricing-sub">
      Choose the monthly credits that fit your needs.
    </p>

    <div class="price-card">

      <div class="popular-label">MOST POPULAR</div>

      <h3>Pro</h3>

      <div class="price">
        $29 <span>/mo</span>
      </div>

      <div class="credits">
        300 credits every month
      </div>

      <p style="font-size:13px;color:var(--muted);margin-top:12px">
        Cancel anytime · Billed monthly
      </p>

      <ul class="price-features">
        <li>Download every ebook you build</li>
        <li>Monthly credit refresh</li>
        <li>Export PDF, EPUB and DOCX</li>
        <li>Commercial license, subject to applicable terms</li>
        <li>Regenerate chapters, titles and covers</li>
        <li>Cancel anytime</li>
      </ul>

      <a href="#cta" class="btn btn-primary">
        Get Pro — $29/mo
      </a>

    </div>

    <h3 class="tier-heading">Choose your Pro plan</h3>

    <div class="tiers">

      <div class="tier active">$29/mo<br>300 credits</div>
      <div class="tier">$39/mo<br>500 credits</div>
      <div class="tier">$49/mo<br>750 credits</div>
      <div class="tier">$59/mo<br>1000 credits</div>
      <div class="tier">$79/mo<br>1500 credits</div>
      <div class="tier">$99/mo<br>2000 credits</div>

    </div>

    <p style="color:var(--muted);font-size:13px;margin-top:22px">
      Pricing examples for the planned product. Subscription functionality is not connected yet.
    </p>

  </div>

</section>


<!-- FAQ -->

<section class="faq" id="faq">

  <div class="container">

    <h2>Questions? We've got answers.</h2>

    <div class="faq-list">


      <div class="faq-item">

        <div class="faq-question">
          How is this different from writing it myself or using ChatGPT?
          <span>+</span>
        </div>

        <div class="faq-answer">
          The goal is to combine outlining, chapter writing,
          cover design, editing and book export in one workflow,
          rather than requiring multiple separate tools.
        </div>

      </div>


      <div class="faq-item">

        <div class="faq-question">
          Who is getebook for?
          <span>+</span>
        </div>

        <div class="faq-answer">
          Coaches, consultants, course creators, solopreneurs
          and self-publishers who want to turn their knowledge
          into ebooks.
        </div>

      </div>


      <div class="faq-item">

        <div class="faq-question">
          Can I make coloring books too?
          <span>+</span>
        </div>

        <div class="faq-answer">
          The planned product includes a dedicated workflow
          for creating coloring books alongside regular ebooks.
        </div>

      </div>


      <div class="faq-item">

        <div class="faq-question">
          Is the AI writing good enough to sell?
          <span>+</span>
        </div>

        <div class="faq-answer">
          AI-generated content should always be reviewed,
          fact-checked and edited before publishing.
          Quality depends on the topic, instructions and editing.
        </div>

      </div>


      <div class="faq-item">

        <div class="faq-question">
          Do I own what I create?
          <span>+</span>
        </div>

        <div class="faq-answer">
          Usage and commercial rights will be explained in
          the final product's terms and applicable AI-provider terms.
        </div>

      </div>


      <div class="faq-item">

        <div class="faq-question">
          What can I realistically expect to earn?
          <span>+</span>
        </div>

        <div class="faq-answer">
          Earnings are not guaranteed. Results depend on book quality,
          demand, pricing, marketing and publishing platform policies.
        </div>

      </div>


    </div>

  </div>

</section>


<!-- FINAL CTA -->

<section class="final-cta" id="cta">

  <div class="container">

    <h2>Your knowledge is worth more than you think.</h2>

    <p>
      Tell Booker your idea, watch it build your ebook,
      then unlock your download when you're ready.
    </p>

    <a href="#" class="btn btn-primary btn-large">
      Start building, free
    </a>

    <div class="final-notes">
      <span>Plans from $29/mo</span>
      <span>Cancel anytime</span>
      <span>Review before publishing</span>
    </div>

  </div>

</section>


<!-- FOOTER -->

<footer>

  <div class="container">

    <div class="footer-grid">

      <div>

        <div class="footer-brand">
          getebook.ai
        </div>

        <p>Publish once. Earn on repeat.</p>

      </div>


      <div>

        <h4>Product</h4>

        <ul>
          <li><a href="#how">How it works</a></li>
          <li><a href="#features">Features</a></li>
          <li><a href="#pricing">Pricing</a></li>
          <li><a href="#books">Examples</a></li>
        </ul>

      </div>


      <div>

        <h4>Resources</h4>

        <ul>
          <li><a href="#features">Features</a></li>
          <li><a href="#faq">FAQs</a></li>
          <li><a href="#books">Book examples</a></li>
        </ul>

      </div>


      <div>

        <h4>Company</h4>

        <ul>
          <li><a href="mailto:support@getebook.ai">Contact</a></li>
          <li><a href="#faq">Privacy</a></li>
          <li><a href="#faq">Terms</a></li>
        </ul>

      </div>

    </div>

    <div class="copyright">
      © 2026 getebook.ai. All rights reserved.
    </div>

  </div>

</footer>


<!-- JAVASCRIPT -->

<script>

// MOBILE MENU

const menuButton = document.getElementById("menuButton");
const mobileMenu = document.getElementById("mobileMenu");

menuButton.addEventListener("click", () => {

  mobileMenu.classList.toggle("open");

  menuButton.textContent =
    mobileMenu.classList.contains("open") ? "✕" : "☰";

});


// CLOSE MOBILE MENU AFTER CLICKING

document.querySelectorAll(".mobile-menu a").forEach(link => {

  link.addEventListener("click", () => {

    mobileMenu.classList.remove("open");
    menuButton.textContent = "☰";

  });

});


// FAQ ACCORDION

document.querySelectorAll(".faq-question").forEach(question => {

  question.addEventListener("click", () => {

    const currentItem = question.parentElement;
    const wasOpen = currentItem.classList.contains("open");

    document.querySelectorAll(".faq-item").forEach(item => {

      item.classList.remove("open");
      item.querySelector(".faq-question span").textContent = "+";

    });

    if (!wasOpen) {

      currentItem.classList.add("open");
      question.querySelector("span").textContent = "−";

    }

  });

});


// SMOOTH SCROLL

document.querySelectorAll('a[href^="#"]').forEach(link => {

  link.addEventListener("click", event => {

    const target = document.querySelector(
      link.getAttribute("href")
    );

    if (target) {

      event.preventDefault();

      target.scrollIntoView({
        behavior: "smooth",
        block: "start"
      });

    }

  });

});

</script>

</body>
</html>
