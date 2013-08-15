Conzole
=======

Conzole is a debug panel built in javascript that wraps javascript native console object methods and functionality in a panel displayed inside the page.
Include it once and see it the same every time you open up the page, in every browser, on mobile etc.

It also adds some unique functions as the &ldquo;watching&rdquo; list. It let you watch variables as many browsers debug console does. But setting up the watches via javascript is much easier, can be conditional and you don't have to do it every time you launch the browser.

Usage
---
Include the script just after the <span class="pre">&lt;body&gt;</span> open tag:
```html
</head>
<body>
    <script type="text/javascript" src="conzole.js"></script>
    <!-- rest of body content -->
```

Panel managment
---
Drag left edge to resize panel.</p>
Press bound keys to accomplish the following tasks (active when focus is not isnide a input item).
Keyboard bindings:
--'z' toggle panel;
--'c' clear panel content;
--'u' toggle panel active/paused;
--'t' show alternate timings (current time/time elapsed from previous message)
    
Otherwise call specific methods via javascript:
```javascript
conzole.open()
conzole.close()
conzole.toggle()
conzole.setWidth(parseInt(Math.random()*1000))
```
Basic
---
Notice the javascript native "console" is called. </p>
```javascript
console.log('a log')
console.info('an info')
console.warn('a warn')
console.error('an error')
```
Timers
---
Notice the javascript native "console" is called.
```javascript
console.time('timer1')
console.timeEnd('timer1')

console.time('timer2')
console.timeEnd('timer2')
```
Watch
---
Update of the values must be explicitly called every time. Autoupdate has been intentionally not implemented.
```javascript
conzole.watching.foo=Math.random()
conzole.watching.foo=null
delete conzole.watching.foo
```
