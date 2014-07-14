##  Managing the Loop

- process.nextTick() <!-- .element: class="fragment" data-fragment-index="1" -->
- setTimeout() <!-- .element: class="fragment" data-fragment-index="2" -->
- foo.emit() <!-- .element: class="fragment" data-fragment-index="3" -->



note:

  process.nextTick()
  - special queue outside of the event queue. executed first before event stack FIFO

  setTimeout(n)
  - executes at the end of the event loop after at least n time has passed

  foo.emit() <- JS
  - sets a state that is acted upon by subsequent items in the stack
