## We will be following BEM naming convention
### BEM divides class names into three parts: Block, Element, and Modifier.   
### Block (B):   
The block represents a high-level component or module in your application or webpage. It is a stand-alone entity that has its own independent meaning and functionality.
Block names are written in lowercase and should be hyphen-separated (kebab case).   
_css Example: .button, .header, .menu_     
_module.css Example: .button, .header, .menu_    
### Element (E):       
Elements are parts or components within a block that don't make sense or function independently outside of the block. They are dependent on the block.
Element names are written with two underscores (__) followed by a lowercase name and should be within the context of a block.   
_css Example: .button__icon, .header__logo, .menu__item_      
_module.css Example: .buttonIcon, .headerLogo, .menuItem_      
### Modifier (M):   
Modifiers are used to change the appearance or behavior of blocks or elements. They allow you to create variations of blocks or elements without creating entirely new class names.
Modifier names are written with two hyphens (--) followed by a lowercase name.   
_css Example: .button--large, .header--dark, .menu__item--active_   
_module.css Example: .button_large, .header_dark, .menuItem_active_   


### Example Code
``` css
<div class="menu">
  <a class="menuItem" href="#">Home</a>
  <a class="menu__item menu__item--active" href="#">About</a>
</div>
```
``` module.css
<div className=classes.menu>
  <a class=classes.menuItem href="#">Home</a>
  <a class={`${classes.menuItem} ${classes.menuItem_active}`} href="#">About</a>
</div>
```


## Define global CSS variables, also known as CSS custom properties 
`:root` is used to define global CSS variables inside a CSS block. These variables are prefixed with two dashes (--), which is the convention for naming CSS custom properties.  
Once these global variables are defined, you can use them throughout your CSS by referencing the variable name enclosed in `var()`    

### Example Code
```
/*index.css*/
:root {
  --main-bg-color: #f2f2f2;
  --text-color: #333;
  --primary-color: #007bff;
  --secondary-color: #6c757d;
}
```
```
/*componentx.css*/
body {
  background-color: var(--main-bg-color);
  color: var(--text-color);
}
.button {
  background-color: var(--primary-color);
  color: white;
}
.secondary-button {
  background-color: var(--secondary-color);
  color: white;
}
```

## what to include in index.css file
* `\*{}`  ->for css reset/normalization rule (applies on all html elements and page properties)
* `body, h1, p, a` -> Define global typography styles ie Set fonts, line heights, and text colors.
* `:root{}` -> for declaring css custom variables 
* `.btn, .img, .icon` ->  Resuable component styles
* `@media (max-width: xxx)` ->global media queries common for all components.



