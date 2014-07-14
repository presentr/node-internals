##  Handling more requests with concurrency


![](http://assets.markhuge.com/images/presentations/multiple-requests.png)



note:
  - concurrency defers slow tasks and tries to execute non dependent tasks during the io wait time
  - concurrency does not make slow io faster, it just tries to make use of idle time
  - concurrent tasks do not literally run at the same time in a single thread
  - concurrency and parallelism are not opposites, they're just different and can be used together 