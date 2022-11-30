# Animated Vector Graphics
Everyone likes SVGs. They're compact and infinitely scalable. Did you know, that you can animate them and even make them interactive, using a JavaScript library called GSAP? Well, you can, and it's easy. The code can even be written inside the SVG-file itself.

Simply create the svg in inkscape, illustrator, or other vector-drawing software. Open the file in a text-editor and add your code.

Check out the examples. Only gifs are shown, along with a snippet of the code. Download them, open in a browser, and check out the real results.

Note: only tested with Chrome.

---
## A starry night
![Starry Night](gifs/night.gif)
```html
<!-- GSAP -->
<script type="text/javascript" xlink:href="https://cdnjs.cloudflare.com/ajax/libs/gsap/2.0.1/TweenMax.min.js"/>

<!-- Custom animation -->
<script type="text/javascript">
  function anim() {
    var master = new TimelineMax({repeat:-1});
    master.add(waves(), 0).add(clouds(), 0).add(moon(), 0).add(stars(), 0);
    master.timeScale(1.6);
    master.running = true;

    var light = {
      mask  : document.getElementById('light_mask'),
      cone  : document.getElementById('light_cone'),
      torch : document.getElementById('torch'),
      isOn  : false
    };

// More code...
```

---
## A tree, waving in the wind
![Waving Tree](gifs/tree.gif)
```html
<!-- GSAP  -->
<script type="text/javascript" xlink:href="https://cdnjs.cloudflare.com/ajax/libs/gsap/2.0.1/TweenMax.min.js"/>

<!-- Custom animation -->
<script type="text/javascript">
  function anim() {
    const branch_1 = document.getElementById('branch_1');
    const branch_2 = document.getElementById('branch_2');
    const branch_3 = document.getElementById('branch_3');
    const front_leaves_2 = document.getElementById('front_leaves');

    var tl = new TimelineMax({repeat:1, yoyo:true});

    tl
      .to(branch_3, 3, {rotation:-2, transformOrigin:'0% 100%', ease:Power1.easeInOut}, 0)
      .to(branch_1, 3, {rotation:-1, transformOrigin:'100% 100%', ease:Power1.easeInOut}, 0)
      .to(branch_2, 3, {rotation:-1, transformOrigin:'50% 100%', ease:Power1.easeInOut}, 0)
      .to(front_leaves_2, 3, {rotation:-1, x:-2, transformOrigin:'50% 50%', ease:Power1.easeInOut}, 0)
  }
</script>
```

Open the raw files to check out the full code.
