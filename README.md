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

##Extend/Inheritance

This is one of the most useful features of Sass. Using @extend lets you share a set of CSS properties from one selector to another. 
It helps keep your Sass very DRY.





