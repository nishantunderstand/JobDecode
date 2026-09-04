Logging , Monitoring , Distributed Tracing 
  
Three Pillars of Observability
Logs  
Metrics   
Traces
  
W3C Trace Context.

  
Logs    → What happened?
Metrics → How much/how often?
Traces  → Where did the request go?
  
Learn this by an example :
  
What happened?
Payment failed for order 123
How much / how often?
Payment API latency = 2.5 sec
Error rate = 5%
  
Where did the request go and where did it spend time?
Gateway
   ↓ 100ms
Order
   ↓ 200ms
Payment
   ↓ 2.2 sec ← bottleneck
Inventory
   ↓ 100ms
  

Trace vs Span
Trace ID
Span ID
  
Trace = Whole Journey
Span  = Individual Step
  
Distributed Tracing vs Logging
Logging  vs Metrics vs Tracing 
  
Open Telemetry
  
Can tracing work asynchronously?
  
W3C Trace Context : World Wide Web Consortium Trace Context
  
W3C Headers
1. traceparent
2. tracestate
  
traceparent 4 Parts
3. TraceID
4. ParentID
5. Version
6. Trace Flag
  
Trace Flag
00 → not sampled
01 → sampled
  
Trace flags are not HTTP status codes.