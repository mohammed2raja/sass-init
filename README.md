# sass-init

## Variables

${variable-name} : {value}

## Nexting

nav{

 color: red,

 ul{
 
  background-color: blue;
  
  li{
  
    display: block;
    
  }
  
 }
  
}

## Partials

You can create partial Sass files that contain little snippets of CSS that you can include in other Sass files. This is a great way to modularize your CSS and help keep things easier to maintain. A partial is simply a Sass file named with a leading underscore

_partial.scss

Sass partials are used with the @import directive.

## Mixins

Mixins let you to group of CSS declaration that let you reuse throughout your site. 

You can even pass in values to make your mixin more flexible.

A good use of a mixin is for vendor prefixes. Here's an example for transform.


@mixin transform($property) {

  -webkit-transform: $property;
  
      -ms-transform: $property;
      
          transform: $property;
          
}

.box { @include transform(rotate(30deg)); }

## Extend/Inheritance

This is one of the most useful features of Sass. Using @extend lets you share a set of CSS properties from one selector to another. 
It helps keep your Sass very DRY.

.dialog-button {

  box-sizing: border-box;
  
  color: #ffffff;
  
  box-shadow: 0 1px 1px 0 rgba(0, 0, 0, 0.12);
  
  padding: 12px 40px;
  
  cursor: pointer;
  
}


.confirm {

  @extend .dialog-button;
  
  background-color: #87bae1;
  
  float: left;
  
}


.cancel {

  @extend .dialog-button;
  
  background-color: #e4749e;
  
  float: right;
  
}

## Functions http://sass-lang.com/documentation/Sass/Script/Functions.html

Sass offers a long list of built-in functions. 

They serve all kinds of purposes including string manipulation, color related operations, and some handy math methods such as random() and round().

To exhibit one of the more simple Sass functions, we will create a quick snippet that utilizes darken($color, $amount) to make an on-hover effect.

$awesome-blue: #2196F3;

a {

  padding: 10px 15px;
  
  background-color: $awesome-blue;
  
}


a:hover {

  background-color: darken($awesome-blue,10%);
  
}



## Map

In SassScript, maps are key-value pairs. Their syntax is slightly different from a list: They must be comma-separated, and the entire map must be wrapped in parentheses:

$red-map: (light: #e57373, medium: #f44336, dark: #b71c1c);

p {

   color: map-get($red-map, light);
   
}







