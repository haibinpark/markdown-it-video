# markdown-it-video-ext

> markdown-it plugin for embedding hosted videos.

## Usage

#### Enable plugin


```js
npm install markdown-it-video-ext@0.4.0 --save
```

```js
var md = require('markdown-it')({
  html: true,
  linkify: true,
  typography: true
}).use(require('markdown-it-video')); // <-- this use(package_name) is required
```

#### Example

##### youtube  

This only works in the inline style.

```md
@[youtube](dQw4w9WgXcQ)
```

is interpreted as

```html
<p><iframe id="ytplayer" type="text/html" width="640" height="390"
  src="http://www.youtube.com/embed/dQw4w9WgXcQ"
  frameborder="0"/></p>
```

Alternately, you could use a number of different YouTube URL formats rather than just the video id.

```md
@[youtube](http://www.youtube.com/embed/dQw4w9WgXcQ)
@[youtube](https://www.youtube.com/watch?v=dQw4w9WgXcQ&feature=feedrec_centerforopenscience_index)
@[youtube](http://www.youtube.com/user/IngridMichaelsonVEVO#p/a/u/1/QdK8U-VIH_o)
@[youtube](http://www.youtube.com/v/dQw4w9WgXcQ?fs=1&amp;hl=en_US&amp;rel=0)
@[youtube](http://www.youtube.com/watch?v=dQw4w9WgXcQ#t=0m10s)
@[youtube](http://www.youtube.com/embed/dQw4w9WgXcQ?rel=0)
@[youtube](http://www.youtube.com/watch?v=dQw4w9WgXcQ)
@[youtube](http://youtu.be/dQw4w9WgXcQ)
```

##### youku  

This only works in the inline style.


```md
@[youku](http://v.youku.com/v_show/id_XMTQ4MTk1MjQ4MA==.html?from=s1.8-1-1.1)
```  

is interpreted as

```html
<p><iframe height=498 width=510 
    src="http://player.youku.com/embed/XMTQ4MTk1MjQ4MA==" 
    frameborder=0 allowfullscreen></iframe></p>
```


## Currently supported services
 * YouTube
 * youku
 * vimeo