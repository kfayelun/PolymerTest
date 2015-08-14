# PolymerTest
Simplified project to test styling in Polymer.

Just disregard the header-menu element, I was having an issue in there too but figured it out now. 
Kept it as it gives me the main container where the side-drawer lives.

Relevant parts for this issue: 
/*
app-theme.html
  side-drawer {
    --side-drawer-container-left-theme: {
      background: blue;
    };
  }

side-drawer.html
  .drawer-container-left {
      background: red;
      position: absolute;
      left: 0;
      display: block;
      
      /*uncomment this and see that it breaks*/
      /*@apply(--side-drawer-container-left-theme);*/

  }
*/

So. We want to have a lot of the styling in one place; in the app-theme.html.
Looking at the starter kits, theres a :root with some styling, and then theres ids like #drawerToolbar, and then elements like 
paper-material, and lots more. I have made a couple custom elements, but am not able to style them the same way. 
If you have a look at the app-theme.html in this project, I also have a root, and then I'm trying to make a custom theme for my 
custom element side-drawer, but it does not change the color. I really tried doing this just as in the polycast episode.

Also, trying to do this, breaks the other styling as the class that gets appended within the <template> of side-drawer (drawer-container-left and -right), 
isnt added to the element anymore. Or at least it's not showing up as a class if you inspect the element in Chrome.
This might be cus of a syntax error etc. but I'm not seeing any errors. 

Sorry for the ugly colors, just trying to make it obvious. Hope this clears it up. 

Thanks so much, 
Kristi
