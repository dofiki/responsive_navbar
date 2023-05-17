# Responsive Navbar

### HTML
- **navbar** contains **nav-branding**, **nav-menu** and **hamburger**.
- **nav-branding** is text which contains link to homepage.
- **nav-menu** is unordered list which contains three nav items and each **nav-item** contains **nav-link**.
- **hamburger** contains three **bar** which are span element.

### CSS
- At first CSS for computer screen is written.
- **hamburger** is set to `display:none;` as we don't need it in computer screen.
- **bar** of **hamburger** is drawn and transition is added.
- Media query is added and CSS is written for mobile device.
- **hamburger** is set to `display:block` as we need it stacked.
- **hamburger.active** is defined.
- **bar** is transformed.
- **nav-menu** for mobile device is created and `top:-170px` is set to remove from current screen and transition is added, position is fixed as we want it to be fixed when we scroll, display is set top flex, flex-direction is set to column.
- **nav-menu.active** is defined, it contains `transform:translateY(240px);` to make it visible in screen.

### JavaScript
- **hamburger** and **nav-menu** is seclected.
- Event Listener is added to **hamburger**.
- When **hamburger** is clicked a function is triggered, which
toggles **active** class of **hamburger** and **nav-menu**. 
`hamburger.addEventListener("click", ()=>{`
   ` hamburger.classList.toggle("active");`
 `   navMenu.classList.toggle("active");`
`})`
- For removing mobile **nav-menu** when **nav-link** is clicked, following code is added: 
`document.querySelectorAll('.nav-link').forEach(n => n` `addEventListener('click', ()=> {`
`    hamburger.classList.remove("active");`
    `navMenu.classList.remove("active");`
`}));`
here when link is clikced active class from **hamburger** and **nav-menu** is removed.