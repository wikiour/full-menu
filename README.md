# FULL Nav Menu & Burger
## 🍁 Mega menu for the site
###### This is an extended version of "menu-complete". This version of the "full menu" adds a burger menu and customizable modules. This menu has additional functional modules that will expand this menu. If you need a basic script, you can install it from our <a href="https://www.npmjs.com/package/menu-full">"menu-full"</a> npm package or from our <repository href="https://github.com/wikiour">GitHub</a> <a href="https://github.com/wikiour/menu-full">"menu-full"</a>.

If you are looking for a library to create a complete menu for your site, then "full-menu" might be a great choice for you. This library provides an easy and convenient way to create beautiful and functional menus on your web pages.

One of the features of "full-menu" is its ease of use. No special programming knowledge is required to create a menu, as the library provides a simple and intuitive interface. All you need to do is just install the npm package and add it to your project. In your navigation menu, add the nav-menu class and then our script will do the rest. You can create menus with unlimited nested items, dropdowns, animations and more.

If you want to add a navigation menu to your site, you can do so with our "full-menu" library, which can be installed into your project via npm or downloaded from our GitHub repository.

This menu works on any device and works both on hover and on click, so you can be sure that the user will open this menu on any site. It also thought out all the user actions that help to work with this menu. The burger is configured as follows - when clicking on the burger, the header-menu gets the open class, since the div with the burger class also has a span.

##### Here is an example of what your html code might look like:
```
<div class="header-menu"> // Wrap your menu to make the burger work in a div with a class "header-menu"
      <nav class="nav-menu"> // Add a tech class "nav-menu" to your menu
        <ul>
          <li>Home</li>
          <li>Catalog
            <ul>
              <li>Category
                <ul>
                  <li>Products</li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </nav>
</div>
// Add a burger to your code
<div class="burger"><span class="burger"></span></div>
```

Our JavaScript will add all the necessary classes to your menu so that you can do CSS-only styling of your menu however you want. It adds extra classes as soon as the submenu appears in your html so you don't have to worry about automating the process. It will automatically assign an extra class to the nav (nav-sub-menu) which will mean the menu contains a submenu, it will also assign the li which contains the submenu the class nav-menu-li and wrap your li content in a span with the class nav-menu-span , will additionally assign the class nav-menu-ul to the nested ul element. On click or hover, the active class will be added and removed for the nav-menu-li, av-menu-span, nav-menu-ul elements, allowing you to customize any behavior of the menu. 

##### Here is how the same code will look like after being processed by our script:
```
<div class="header-menu">
     <nav class="nav-menu nav-sub-menu">
        <ul>
          <li>Home</li>
          <li class="nav-menu-li">
           <span class="nav-menu-span">Catalog</span>
            <ul class="nav-menu-ul">
              <li class="nav-menu-li">
              <span class="nav-menu-span">Category</span>
                <ul class="nav-menu-ul">
                  <li>Products</li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </nav>
</div>
<div class="burger"><span class="burger"></span></div>
```
##### Active elements
In the active phase, all key menu items receive a class "active". In the active phase, the burger adds an additional class for body lock-menu".
```
<div class="header-menu open">
     <nav class="nav-menu nav-sub-menu">
        <ul>
          <li>Home</li>
          <li class="nav-menu-li active">
           <span class="nav-menu-span active">Catalog</span>
            <ul class="nav-menu-ul active">
              <li class="nav-menu-li active">
              <span class="nav-menu-span active">Category</span>
                <ul class="nav-menu-ul active">
                  <li>Products</li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </nav>
</div>
<div class="burger open"><span class="burger open"></span></div>
```

Our "full-menu" library has a fast and optimized code that guarantees fast loading of your website. This makes our JavaScript a great choice for sites of any size and scale. Install right now and see the simplicity and quality of our code.

##### Connecting via npm
```
npm i -D full-menu
```

##### Connecting to the project
```
import navMenu from 'full-menu';
navMenu();
```

##### Customize the menu the way you want
```
// Initialize your menu
const settingsMenu = new navMenu({
  // # Settings Menu
});
```
```
// const settingsMenu = new navMenu({
  // --------------------------------
  // # Settings Menu
  // --------------------------------
  // New class Menu = You can change all classes as you wish.
  // --------------------------------
  // Class for nav
  // navMenu: 'new-nav-menu', // Default = nav-menu
  // Class for all nav if menu contains submenu
  // navSubMenu: 'new-nav-sub-menu', // Default = nav-sub-menu
  // Class for all spans that have submenus
  // navMenuSpan: 'new-nav-menu-span', // Default = nav-menu-span
  // Class for all li's that have a submenu
  // navMenuLi: 'new-nav-menu-li', // Default = nav-menu-li
  // Class for all ul's that have a submenu
  // navMenuUl: 'new-nav-menu-ul', // Default = nav-menu-ul
  // Class for all active submenus
  // navMenuActive: 'new-active', // Default = active
  // Class for all div mega menu
  // megaMenu: 'new-mega-menu', // Default = mega-menu
  // Class for all span Open more
  // openMore: 'new-open-more', // Restrict Span Class Default = open-more
  // ## Modifications - extensions for your menu
  // Enable Hover Effect for Entire Menu
  // hoverEnabled: true, // Enable Hover Menu
  // If you need to add date attributes to all menu items
  // addAttributeEnabled: true, // Enable Data Attribute
  // Do you want to change the default values? Here's how to do it
  // dataUl: 'new-data-ul', // Default = data-ul + index
  // dataLi: 'new-data-li', // Default = data-li + index
  // dataSpan: 'new-data-span', // Default = data-span + index
  // dataDiv: 'new-data-div', // Default = data-div + index
  // Add extra classes for all your menu items
  // If the elements contain a date attribute, then its value will be assigned, otherwise the current index
  // addClassEnabled: true, // Enable Add Class
  // classUl: 'new-ul', // Add Class  Default = ul-index
  // classLi: 'new-li', // Add Class  Default = li-index
  // classSpan: 'new-span', // Add Class  Default = span-index
  // classDiv: 'new-div', // Add Class  Default = div-index
  // If you want to globally include a Mega Menu which will wrap your nested uls in a div with class mega-menu
  // megaMenuEnabled: true, // Enable Mega Menu Global
  // If you want to enable a Mega Menu on a specific element which will wrap your nested ul in a div with class mega-menu
  // megaMenuOneEnabled: true, // Enable Mega Menu One
  // Determine the serial number for Mega Menu One
  // liIndex: 0, // Mega Menu One Enable Index Li Default = 0
  // Enable Hover Effect for Mega Menu One
  // hoverMegaMenuEnabled: true, // Enable Hover Mega Menu
  // Restrict submenu output for Mega Menu One
  // restrictMegaMenuEnabled: true, // Enable Restrict Content
  // Number of displayed submenus for Mega Menu One
  // maxiRestrict: 2, // Restrict Default = 10
  // Text details for Mega Menu One
  // textRestrict: 'Open more ...', // Restrict Text Default = Open more
  // --------------------------------
  // # Settings Burger
  // --------------------------------
  // If you want to activate Burger menu
  // burgerEnabled: true, // Enable Burger
  // ## New class Burger
  // The class for your div that contains nav.nav-menu
  // headerMenu: 'new-header-menu', // Default = header-menu
  // Class for active menu
  // open: 'new-open', // Default = open
  // Class for body when menu is active
  // lockMenu: 'new-lock-menu', // Default = lock-menu
  // Class for your Burger
  // burger: 'new-burger', // Default = burger
  // --------------------------------
// });
```

The "full-menu" library is a great choice for those who are looking for an easy, fast and flexible way to create a complete menu on their website. With it, you can quickly create a beautiful and functional menu that will work on all devices and match your design.

##### Here is an example of basic CSS for your menu
```
nav.nav-menu.nav-sub-menu ul > li > ul.active {
  opacity: 1;
  visibility: visible;
}
@media (max-width: 768px) {
  nav.nav-menu.nav-sub-menu ul > li > ul.active {
    display: block;
  }
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul.active {
  display: block;
}
nav.nav-menu > ul {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: flex-start;
  align-content: flex-start;
  align-items: left;
  gap: 0.3125rem 0.625rem;
  text-align: left;
  text-transform: uppercase;
}
@media (max-width: 768px) {
  nav.nav-menu > ul {
    width: 100%;
    min-height: 80vh;
    flex-wrap: nowrap;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    align-items: center;
    gap: 1.25rem;
  }
}
nav.nav-menu.nav-sub-menu {
  font-family: Georgia, "Times New Roman", Times, serif;
  font-weight: calc(calc(0.875 * 1rem) + calc(2) * ((100vw - 20rem) / 960));
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.0625rem;
  color: #d1effc;
}
nav.nav-menu.nav-sub-menu a {
  color: #d1effc;
}
nav.nav-menu.nav-sub-menu a:hover {
  color: #ffff00;
}
nav.nav-menu.nav-sub-menu a:active {
  color: #ffff00;
}
nav.nav-menu.nav-sub-menu button {
  color: #232b32;
  text-transform: uppercase;
  letter-spacing: 0.09375rem;
}
nav.nav-menu.nav-sub-menu > ul {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: flex-start;
  align-content: flex-start;
  align-items: left;
  gap: 0.3125rem 0.625rem;
  text-align: left;
}
@media (max-width: 768px) {
  nav.nav-menu.nav-sub-menu > ul {
    flex-direction: column;
    width: 100%;
  }
}
nav.nav-menu.nav-sub-menu > ul > li > ul {
  opacity: 0;
  visibility: hidden;
  position: absolute;
  top: 95%;
  left: 0;
  width: 18.75rem;
  padding: 1.5625rem 0 0 0;
  text-transform: none;
}
@media (max-width: 768px) {
  nav.nav-menu.nav-sub-menu > ul > li > ul {
    display: none;
    position: relative;
    top: 0;
    padding: 0.3125rem 0 0.3125rem;
    width: 100%;
  }
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul {
  display: none;
}
nav.nav-menu.nav-sub-menu li {
  position: relative;
  cursor: pointer;
}
@media (max-width: 768px) {
  nav.nav-menu.nav-sub-menu li {
    width: 100%;
  }
}
nav.nav-menu.nav-sub-menu ul > li > ul > li {
  background-color: #232b32;
  padding: 0 0.625rem 0.3125rem 0.625rem;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li:first-child {
  padding: 0.625rem 0.625rem 0.3125rem 0.625rem;
  border-top-left-radius: 0.3125rem;
  border-top-right-radius: 0.3125rem;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li:last-child {
  padding: 0 0.625rem 0.625rem 0.625rem;
  border-bottom-left-radius: 0.3125rem;
  border-bottom-right-radius: 0.3125rem;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li:only-child {
  padding: 0.625rem 0.625rem 0.625rem 0.625rem;
  border-radius: 0.3125rem;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul > li {
  padding: 0 0 0.3125rem 0.3125rem;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul > li:first-child {
  padding: 0.3125rem 0 0.3125rem 0.3125rem;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul > li:last-child {
  padding: 0 0 0 0.3125rem;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul > li:only-child {
  padding: 0.3125rem 0 0 0.3125rem;
  border-radius: 0;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul > li > ul > li {
  padding: 0 0 0.3125rem 0;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul > li > ul > li:first-child {
  padding: 0.3125rem 0 0.3125rem 0;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul > li > ul > li:last-child {
  padding: 0 0 0 0;
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul > li > ul > li:only-child {
  padding: 0.3125rem 0 0 0;
}
nav.nav-menu.nav-sub-menu span.nav-menu-span {
  display: block;
  position: relative;
  padding: 0 1.5625rem 0 0;
}
nav.nav-menu.nav-sub-menu span.nav-menu-span::after {
  content: "⬇️";
  position: absolute;
  top: -0.125rem;
  right: 0;
  width: auto;
  height: auto;
}
nav.nav-menu.nav-sub-menu span.nav-menu-span.active::after {
  content: "⬆️";
}
@media (max-width: 768px) {
  nav.nav-menu.nav-sub-menu > ul > li > span.nav-menu-span {
    margin: 0 0.625rem 0 0;
  }
}
```

##### Here is an example of a basic CSS for your burger
```
.burger {
  display: none;
  position: relative;
  z-index: 103;
  cursor: pointer;
  width: 1.5625rem;
  height: 1.25rem;
}
@media (max-width: 768px) {
  .burger {
    display: block;
  }
}
.burger:after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 0.15625rem;
  background-color: #d1effc;
  transition: all 0.3s;
}
.burger.open:after {
  top: 45%;
  transform: rotate(45deg);
}
.burger:before {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 0.15625rem;
  background-color: #d1effc;
  transition: all 0.3s;
}
.burger.open:before {
  bottom: 45%;
  transform: rotate(-45deg);
}
.burger span.burger:before {
  content: "";
  position: absolute;
  top: 45%;
  left: 0;
  width: 100%;
  height: 0.15625rem;
  background-color: #d1effc;
}
.burger span.burger.open {
  opacity: 0;
}
```

You can modify this CSS to suit your needs as you wish.

###### We will also be posting updates and additions to this menu on GitHub so stay tuned.

__________________________________________________________
* Author: WikiOur
* Author website: https://wikiour.com
* GitHub: https://github.com/wikiour
* Patreon: https://patreon.com/wikiour
* YouTube: https://youtube.com/@wikiour
* Facebook: https://facebook.com/wikiour
* Instagram: https://instagram.com/wikiour
