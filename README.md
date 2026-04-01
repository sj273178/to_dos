# TODOS


### Moisha
===============================
- please use the buttons ruth created, the outline button you added looks good, please pass the code to Esther, make sure the border is the primary color and at first transparent like at an alpha of 0.6 then to 1 when hovered.
- let the second button be exactly as that in the nav bar.
for colors.

this is the css you should use after pulling to achieve the design I have just shared in the group

.hero {
  background-color: var(--base-color);
  min-height: calc(100vh - 75px);
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
  padding: 60px 20px;
}

.hero::before {
  background-color: rgba(52, 152, 219, 0.503);
  content: "";
  position: absolute;
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, #3498db59 0%, rgba(52, 152, 219, 0) 70%);
  top: -100px;
  right: -150px;
  border-radius: 50%;
  animation: float 8s ease-in-out infinite;
}

.hero::after {
  content: "";
  position: absolute;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, #2ecc7159 0%, transparent 70%);
  bottom: -50px;
  left: -100px;
  border-radius: 50%;
  animation: float 6s ease-in-out infinite reverse;
}

@keyframes float {
  0%,
  100% {
    transform: translateY(0) scale(1);
  }
  50% {
    transform: translateY(-30px) scale(1.05);
  }
}

.hero-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
  width: 100%;
  position: relative;
  z-index: 1;
}

.hero-left {
  flex: 1;
  max-width: 560px;
}

.hero-badge {
  display: inline-block;
  border: 1px solid rgba(52, 211, 153, 0.5);
  color: rgba(52, 211, 153, 0.9);
  font-size: 13px;
  font-weight: 500;
  padding: 8px 18px;
  border-radius: 30px;
  margin-bottom: 28px;
  background: rgba(52, 211, 153, 0.07);
  letter-spacing: 0.02em;
}

.hero-title {
  font-size: clamp(2rem, 4vw, 3rem);
  font-weight: 800;
  color: #ffffff;
  line-height: 1.2;
  margin-bottom: 24px;
}

.hero-gradient-text {
  background: var(--gradient-color);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-description {
  font-size: 16px;
  color: rgba(255, 255, 255, 0.65);
  line-height: 1.8;
  margin-bottom: 40px;
  max-width: 440px;
}

.hero-buttons {
  display: flex;
  align-items: center;
  gap: 16px;
  flex-wrap: wrap;
}

.hero-btn-primary {
  background-color: #111;
  color: #fff;
  padding: 14px 32px;
  border-radius: 30px;
  font-weight: 700;
  font-size: 15px;
  transition:
    background 0.3s ease,
    transform 0.2s ease,
    box-shadow 0.3s ease;
}
.hero-btn-primary:hover {
  background-color: #222;
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.4);
}

.hero-btn-outline {
  border: 1.5px solid rgba(255, 255, 255, 0.55);
  color: #fff;
  padding: 13px 32px;
  border-radius: 30px;
  font-weight: 600;
  font-size: 15px;
  transition:
    border-color 0.3s ease,
    background 0.3s ease,
    transform 0.2s ease;
}
.hero-btn-outline:hover {
  border-color: rgba(255, 255, 255, 0.9);
  background: rgba(255, 255, 255, 0.06);
  transform: translateY(-2px);
}

.hero-right {
  flex: 0 0 420px;
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.hero-card {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 16px;
  padding: 20px 24px;
  position: relative;
  overflow: hidden;
  display: flex;
  align-items: center;
  gap: 18px;
  transition:
    transform 0.2s ease,
    background 0.2s ease;
}
.hero-card:hover {
  transform: translateX(4px);
  background: rgba(255, 255, 255, 0.08);
}

.hero-card-border {
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 3px;
  border-radius: 16px 0 0 16px;
}
.hero-card-border--blue {
  background: var(--primary-color);
}
.hero-card-border--green {
  background: var(--secondary-color);
}
.hero-card-border--purple {
  background: var(--base-color-light);
}

.hero-card-icon-box {
  width: 52px;
  height: 52px;
  border-radius: 14px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  font-size: 26px;
}
.hero-card-icon-box--blue {
  background: #1a2a3a;
}
.hero-card-icon-box--green {
  background: #1a2e20;
}
.hero-card-icon-box--purple {
  background: #1e1a30;
}

.hero-card-text {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.hero-card h3 {
  font-size: 16px;
  font-weight: 700;
  color: #ffffff;
  margin: 0;
}

.hero-card p {
  font-size: 13.5px;
  color: rgba(255, 255, 255, 0.5);
  line-height: 1.5;
  margin: 0;
}

/* Laptops / Small Desktops */
@media (max-width: 1279px) {
}

/* Tablets (Landscape) */
@media (max-width: 1023px) {
  .hero-container {
    flex-direction: column;
    text-align: center;
  }
  .hero-left {
    max-width: 100%;
  }
  .hero-description {
    max-width: 100%;
  }
  .hero-buttons {
    justify-content: center;
  }
  .hero-right {
    flex: unset;
    width: 100%;
    max-width: 480px;
  }
}

/* Tablets (Portrait) */
@media (max-width: 767px) {
}

/* Mobile (Landscape) */
@media (max-width: 932px) and (orientation: landscape) {
}

/* Small (sm): 640px and down */
@media (max-width: 639px) {
}

/* Mobile (Portrait) */

@media (max-width: 480px) and (orientation: portrait) {
}





### Jeslor
================================
- update the theme and create a repo to share the todos
- fix the css and add the right gradients





#### Ruth
================================
- Work on the responsiveness of the navbar using the media queries



### Esther
================================
- Please add a secondary button with bg white and on hover the primary color
- add an outline button with a primary color border of opacity of 0.6 and on hover it goes to 1, please cordinate with moisha
- Use the gradient I have added as the bacground of the primary button on hover

### Hillary
================================
Home page lecture updates, This includes a calendar and 4 simplified cards of the upcoming lectures

### Rogers
================================
- Rogers is working on the login page

### Elly
================================
- Build the create user page

### Suban
================================
- Communication cards

### Natasha
================================
- Footer

### Swabula
================================
- Results cards

### Hassan
================================
- Setting up the results page

### Sifa
================================
- Lecturer cards

### John
================================
- Organise and setup the lecture page

### Milly
================================
- Lecture page hero section

### Abel
================================
- Commuinication hero section








