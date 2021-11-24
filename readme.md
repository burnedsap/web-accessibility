Create a tree digram for the webpage before you start coding it. This pseudo-code will help you structure your content before you start writing your code. As they say, measure twice, cut once. Use as many semantic HTML elements as you can. This will not only help you structure your website better, but also make it easily accessible to screen-readers and other accessibility technologies. See all the relevant semantic tags here: [MDN HTML Elements Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) You'll be surprised at how many tags exist-so many useful ones!


Try translating the following html structure into real HTML code, then try making your own pseudo-code.

```html
html
  ->head
  ->body
    ->header
      ->h1
        ->"Critical Computation Portfolio"
    ->nav
      ->ul
        ->li
          ->a
            ->Project 1
        ->li
          ->a
            ->Project 2
        ->li
          ->a
            ->Project 3
        ->li
          ->a
            ->Project 4
        ->li
          ->a
            ->Project 1
    ->main
        ->h2
          ->"Introduction"
        ->p
          ->"For this week's assignment I'm making a..."
        ->img
          ->alt
        ->iframe
          ->describe/alt
        ->h2
          ->"Process"
        ->p
          ->"I used multiple functions..."
          ->em/mark
            ->"This function was the most...."
        ->figure
          ->img
            ->alt
          ->figcaption
            ->"Initial ideation sketches"
        ->h2
          ->"Learnings"
        ->p
          ->"I've finally figure out functions...."
        ->img
          ->alt
    ->footer
      ->address
        ->a
          ->"email@mail.com" 
```

Designing for accessibility isn't a 'layer' you add to your website after designing it for able-bodied users–treat it as a design principle from the very beginning. It makes for cleaner, easier to read websites which are also much easier to code and debug. Remember, it's much easier to build in accessibility features from the ground up rather than retrofitting them later.

After writing out the basic structure of the webpage, head over to the style.css page to style the page. Remember, when using native HTML semantic tags, you just don't need to prepend tags with a '.' or '#'. Just write the tag and style away.
 
To test your website, use ChromeVox, Voiceover, or the appropriate screen reader technology for your device to experience your web page in order to spot any issues, or improve the experience to make it just as smooth for able-bodied users

#### Things to look out for!

1. The intended order and hierarchy of your webpage should be the same visually as well as through a screen-reader
2. Is it easy for users to browse through the content and be aware of the overall structure of your webpage so that they may get to the content they want to quickly? Enable the Rotor using VO Button+U to view the overall structure of your website
3. Use skip-links to give the option for screen reader users to quickly navigate the main content 

```html
<a href="#mysketch" class="skip-link">Skip to my p5js sketch</a>
<section id="mysketch">

//your sketch comes here

</section>
```

Read more about this here: [WebAIM Skip Navigation Links](https://webaim.org/techniques/skipnav/)

4. When using hamburger menus or other elements which aren't immediately visible on-screen, you might find that the focus ring might disappear onto those hidden elements, which could be confusing when using a screen-reader. You can fix this by setting the visibility:none in the CSS when it is not visible, so that the focus ring doesn't select it.
 

When adding images, videos, p5js sketches, and other visual content to your webpage, think about the experience from the perspective of someone using a screen reader to viewing the page. What would they see? What is the best possible solution for them? Images have alt text, videos have audio+captions, and iframes (which holds p5js sketches, embeds and more) can also be assigned an alt text. p5js also has a describe function which dynamically changes the alt text based on whats happening on the canvas. Although these options are tried and tested, and designed for accessibility, always think of the alternate methods if they provide better solutions.

The goal is not to complete a check list, rather it's to ensure that the experience of viewing a web page is not just as accessible (the minimum requirement) but more importantly, enjoyable for everyone.

 Think of the colours used on your web page–would people with different kinds of colour vision deficiency be able to access visual content on screen? Are the fonts used easily readable and legible? It might not be easy at first, but there's plenty of tools available to help find the blind spots in your design and development. Safari, Firefox, and Chrome have in-built accessibility audits/tools to help you find gaps. They are never going to be 100% accurate, and will definitely not give you qualitative feedback on the experience–but they will help you design better. Testing is the only way to find all the issues. 

This is no different from designing and creating responsive websites. The effort that is put into making sure websites look consistent and function as intended across screen sizes is no more important than make sure it's accessible to everyone.

#### Good design is accessible.



Bruce Lawson, co-editor ofthe HTML 5.3 spec
> "built-in beats bolt-on. Bigly."
