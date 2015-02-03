jTinder v.1.0.0
-------------------------
Created: 2014-05-26
By: Dominik Weber
Licensed under GPL Version 2.

jTinder is a javascript library that makes rating people, products, images very easy and fast. It is optimized for mobile touch device but has also a desktop fallback.

jTinder Example
-------------------------
http://x5c.de/jtinder/

jTinder Installation
-------------------------

Add the css file before the HEAD tag:
```
<link rel="stylesheet" type="text/css" href="css/jTinder.css">
```

Add the following before the BODY tag in your html file:
```
<!-- jQuery lib -->
<script type="text/javascript" src="js/jquery.min.js"></script>

<!-- transform2d lib -->
<script type="text/javascript" src="js/jquery.transform2d.js"></script>

<!-- jTinder lib -->
<script type="text/javascript" src="js/jquery.jTinder.js"></script>

<!-- jTinder initialization script -->
<script>$("#tinderslide").jTinder();</script>
```

Add this HTML code in your body for the jTinder content:
```
<div id="tinderslide">
    <ul>
        <li class="pane1"><div class="img"></div><div>Miami Beach</div><div class="like"></div><div class="dislike"></div></li>
        <li class="pane2"><div class="img"></div><div>San Francisco</div><div class="like"></div><div class="dislike"></div></li>
        <li class="pane3"><div class="img"></div><div>Chicago</div><div class="like"></div><div class="dislike"></div></li>
        <li class="pane4"><div class="img"></div><div>New York</div><div class="like"></div><div class="dislike"></div></li>
        <li class="pane5"><div class="img"></div><div>Beach</div><div class="like"></div><div class="dislike"></div></li>
    </ul>
</div>
```
Change the CSS (jTinder.css) for your images.



jTinder Options
-------------------------

onDislike (Optional) - Default value: null - Callback function, if a user dislikes a item. Parameter assigned: The current li item.

onLike (Optional) - Default value: null - Callback function if a user likes a item. Parameter assigned: The current li item.

animationRevertSpeed (Optional) - Default value: 200 - Speed in milliseconds the item reverts back to the init state.

animationSpeed (Optional) - Default value: 400 - Speed in milliseconds the item go away on like/dislike.

threshold (Optional) - Default value: 1 - The value the item must slide before a like/dislike accepted. A good value is 1-5.

likeSelector (Optional) - Default value: .like - CSS selector of a like image in the pane.

dislikeSelector (Optional) - Default value: .dislike - CSS selector of a like image in the pane.


jTinder Methods
-------------------------

like - Trigger like for the current item.

dislike - Trigger dislike for the current item.


Example Calls:
```
$("#tinderslide").jTinder('like');

$("#tinderslide").jTinder('dislike');
```

jTinder Option Usage Example
-------------------------
```
$("#tinderslide").jTinder({
    onDislike: function (item) {
        alert('Dislike image ' + (item.index()+1));
    },
    onLike: function (item) {
        alert('Like image ' + (item.index()+1));
    },
	animationRevertSpeed: 200,
	animationSpeed: 400,
	threshold: 1,
	likeSelector: '.like',
	dislikeSelector: '.dislike'
});
```
