# How to embed a p5.js sketch in a React page

### To run:

Clone this repo and then run the following commands in the terminal:
```
npm i
npm start
```
![](https://miro.medium.com/max/1400/1*wdMMfT2Zb4nbBlWI3bnRtw.png)

Making p5.js sketches is incredibly fun and is an amazing tool for creative coding. However, while p5.js themselves show how to embed a sketch in pure html, it’s not clear how to embed one in a React app since the <script> tag doesn’t work the same way in a React component. Here’s how I figured out to do it:

### Make a p5.js sketch
I use their [online editor](https://editor.p5js.org/) to develop and run mine. Put the sketch in a file in the same directory as index.html, I named the file sketch.js.

### Import p5.js
Add the following code in index.html within the <head> tags
  
```<script type=”text/javascript” src=”https://cdn.jsdelivr.net/npm/p5@1.3.1/lib/p5.min.js"></script>```

This directs React to the p5.js library it uses to run your sketch.
  
### Install ScriptTag
This library is what allows you to run your sketch as a script on the webpage. Run the following command in the terminal to install it:

```npm i react-script-tag```

In the React component you want to embed the sketch in, import ScriptTag with the following line

```import ScriptTag from ‘react-script-tag’;```

and then use the following line of code wherever you want in the component’s JSX

```<ScriptTag type=”text/javascript” src=”sketch.js” />```

Keep in mind that the file name of the sketch needs to match whatever you named it.

### That’s it!
With the last line of code, you can place the sketch where you want and it’ll appear in the React page! I have a full demo repo here if you want to see the code yourself.

If you found this helpful you can follow me on [Instagram](https://instagram.com/abhi.velaga) to keep up with my latest work.

*I’m currently an undergraduate at the University of Texas at Austin studying Computer Science and Studio Art. You can find more information about me and my work at my site — [abhi.work](https://abhi.work).*
