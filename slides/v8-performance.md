##  v8 performance

> Just in case we don't hvae time to do deep dive:

The gist:

- V8 optimizes what it can
- Some constructs break optimization
- don't do those things


note:
  d8 - v8 shell
  install with brew install d8

  d8 --trace-opt <js file>
  d8 --trace-deopt <js file>

  not automatable right now. missing console/alert and other functions
  not well documented