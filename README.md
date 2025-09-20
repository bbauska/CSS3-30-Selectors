<h1>The 30 CSS Selectors You Must Memorize</h1>
https://css3-selectors.bauska.org/#toc-txlk-x

<p>So you learned the base id, class, and descendant selectors—and then called it a day? If so, you’re missing out on an enormous level of flexibility. You owe it to yourself to commit these advanced CSS selectors to memory.</p>

<p>Jump to a particular CSS selector from the list:</p>

1. &ast; &nbsp;&nbsp;				6. X + Y
2. #X	 &nbsp;&nbsp;				7. X > Y
3. .X	&nbsp;&nbsp;				8. x ~ Y
4. X	&nbsp;&nbsp;				9. X[title]
5. X Y	&nbsp;&nbsp;				10. X[href="foo"]

<h2>Basic Selectors</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>1. &ast;</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<pre>
* {
 margin: 0;
 padding: 0;
}
</pre>

<p>Let’s knock the obvious ones out, for the beginners, before we move on to the more advanced selectors.</p>

The star symbol will target every single element on the page. Many developers will use this trick to zero out the margins and padding. While this is certainly fine for quick tests, I’d advise you never to use this in production code. It adds too much weight on the browser, and is unnecessary.

<h2>* Selector</h2>

<p> My paragraph here. </p>

<ol>
  <li> List Item</li>
  <li> List Item</li>
</ol>

<ul>
  <li> List Item</li>
  <li> List Item</li>
</ul>  

css:
* { 
  border: 1px dotted black; 
}

Output: https://codepen.io/tutsplus/pen/XWdOOjE

<p>The &ast; can also be used with child selectors.</p>
<pre>
#container * {
 border: 1px solid black;
}
</pre>

<p>This will target every single element that is a child of the #container div. Again, try not to use this technique very much, if ever.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>2. #X</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<pre>
#container {
   width: 960px;
   margin: auto;
}
</pre>
Prefixing the hash symbol to a selector allows us to target by id. This is easily the most common usage; however, be cautious when using id selectors.

<blockquote>
Ask yourself: “do I absolutely need to apply an id to this element in order to target it?”
</blockquote>
id selectors are rigid and don’t allow for reuse. If possible, first try to use a tag name, one of the more semantic HTML elements, or even a pseudo-class.

html:
<h2>#X Selector</h2>

<div id="id-selector">
   <p> My paragraph here. </p>
   <ol>
      <li> List Item</li>
      <li> List Item</li>
   </ol>

   <ul>
      <li> List Item</li>
      <li> List Item</li>
   </ul>   
</div>
css:
<pre>
#id-selector {
  border: 1px dotted black; 
}
</pre>
Output: https://codepen.io/tutsplus/pen/OJdwgxG



