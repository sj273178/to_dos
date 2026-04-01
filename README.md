# TODOS
### Moisha
- please use the buttons ruth created, the outline button you added looks good, please pass the code to Esther, make sure the border is the primary color and at first transparent like at an alpha of 0.6 then to 1 when hovered.
- let the second button be exactly as that in the nav bar.
for colors.

this is the css you should use after pulling to achieve the design I have just shared in the group

.hero {
  background-color: var(--base-color);
  background: radial-gradient();
  min-height: calc(100vh - 75px);
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
  padding: 60px 20px;
}

.hero::before {
  content: "";
  position: absolute;
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(45, 140, 60, 0.25), transparent 70%);
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
  background: radial-gradient(
    circle,
    rgba(230, 126, 34, 0.15),
    transparent 70%
  );
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




### Jeslor
- update the theme and create a repo to share the todos
- fix the css and add the right gradients


#### Ruth
- Work on the responsiveness of the navbar using the media queries



### Esther
- Please add a secondary button with bg white and on hover the primary color
- add an outline button with a primary color border of opacity of 0.6 and on hover it goes to 1, please cordinate with moisha
- Use the gradient I have added as the bacground of the primary button on hover
