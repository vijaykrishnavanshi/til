## Tools to benchmark APIs Performance

Tools:
 
* **wrk** - Wrk is a tool that is very similar   to the traditional Apache Benchmark (which was first designed as a benchmark for the Apache server). Compared with JMeter, both wrk and ab are radically different beasts:
	* Everything is configured and executed through a command line tool
	* Few but powerful settings, only the essential to generate HTTP load
	* High performance

* **vegeta** - Vegeta is an open-source command line tool but one that takes a different approach than all the previous ones we’ve seen before. It focuses on making it easy to achieve and sustain a target rate of requests per second. It’s meant to test how a service behaves at X requests per second. This is extremely useful when you have actual data or an estimation of what your peak traffic will be and you want to validate that your API will be able to keep up with it.
