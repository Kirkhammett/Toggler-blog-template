# Toggler-blog-template
Example template for a blog site. Easy to customize, compiled with Bourbon, a mixin library for Sass. Blog design inspired by a 
college assignment for creating user interfaces. The examle page scales down in respect to the container transitions and scaling prompted 
by the toggling of the side menu. All transitions that occur are done using css only, save for the ones that are intrinsic to bootstrap/fontawesome. The sidebar toggle uses no JavaScript, strictly css
by taking advantage of the label/checkbox relationship.
</br>
Markup example: 
</br>
```html
<!--checkbox id is styled in the css to be hidden, it will react as active once the brand 
in the navbar i.e. the label is clicked -->
<input type="checkbox" id="sidebartoggler" name="" value="">
<!--label is bound the aforementioned checkbox and will trigger the css change to transition the sidebar-->
<label for="sidebartoggler" class="toggle"><span class="brand1">to</span><span class="brando">GG</span><span class="brand1">ler</span></label>
```
</br>
Css example:
</br>
```css
/*set checkbox with display none to allocate no space for it in the DOM*/
#sidebartoggler {
  display: none; }
  /*For a better visual representation of the sidebar, it shouldn't be scaled down in size with the rest
  of the container*/
  #sidebartoggler:checked + .page-wrap .sidebar {
    left: 0%; }
  /*Transitionn the page wrapper and containter 150 to the left to avoid overlapping on smaller screens
  and enable smooth transition. Wrapper will be scaled down to 0.89% relative of its normal size 
  without hindering the readibility of the content, making for a nice looking and fluid effect.
  */
  #sidebartoggler:checked + .page-wrap .container-fluid {
    margin-left: 150px !important;
    -webkit-transition: all 0.15s ease-out 0s;
    -moz-transition: all 0.15s ease-out 0s;
    transition: all 0.15s ease-out 0s;
    -webkit-transform: scale(0.890);
    -moz-transform: scale(0.890,0.890);
    -ms-transform: scale(0.890);
    -o-transform: scale(0.890);
    transform: scale(0.890);
	transform-origin: center 20%;	}
  #sidebartoggler:checked + .page-wrap .page-content {
    -webkit-transition: all 0.15s ease-out 0s;
    -moz-transition: all 0.15s ease-out 0s;
    transition: all 0.15s ease-out 0s;
    -webkit-transform: scale(0.890,);
    -moz-transform: scale(0.890,0.890);
    -ms-transform: scale(0.890);
    -o-transform: scale(0.890);
    transform: scale(0.890);
    box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.2);	}
```

Example mockup:
============
<h4>Desktop size:<br /></h4>
![alt tag](https://github.com/Kirkhammett/Toggler-blog-template/blob/master/mockup/normalSize.png)
</br>

<h4>Desktop size toggled, container size is scaled down to 0.89%: <br /></h4>
![alt tag](https://github.com/Kirkhammett/Toggler-blog-template/blob/master/mockup/normalSize-toggled.png)
</br>

<ul>
<h4>Phone size: <br /></h4>
![alt tag](https://github.com/Kirkhammett/Toggler-blog-template/blob/master/mockup/phoneSize.png)
</br>

<h4>Phone size with sidemenu toggled, container is additionally scaled but maintains flow: <br /></h4>
![alt tag](https://github.com/Kirkhammett/Toggler-blog-template/blob/master/mockup/mobileSize-Toggled.png)
</br>

<h4>Phone size with one layer of dropdown: <br /></h4>
![alt tag](https://github.com/Kirkhammett/Toggler-blog-template/blob/master/mockup/phoneSize-Dropdown.png)
</br>

<h4>Phone size with double layer dropdown menu: <br /></h4>
![alt tag](https://github.com/Kirkhammett/Toggler-blog-template/blob/master/mockup/phoneSize-double-dropdown.png)
</br>

