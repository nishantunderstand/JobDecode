
APIResponse 

status
httpStatus
message
msID : Microservice Identifier / Request ID / Trace ID
data

BuilderDesignPattern

GenericResponseWrapper

Factory + Builder Hybrid Design Pattern

APIResponse
APIResponseFactory
	success
	failure
	error
	You can merge them as well.


Payload 
	Header
	Body

APIResponse  : Generic
PageApiResponse : Generic (Backward Compatibility)
ApiPageableResponse : List	
