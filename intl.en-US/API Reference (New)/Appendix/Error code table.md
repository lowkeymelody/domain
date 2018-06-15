# Error code table {#concept_yy1_rsp_b2b .concept}

## Client errors {#section_rsg_s4q_b2b .section}

|Error code|Description|HTTP status code|Semantics|
|:---------|:----------|:---------------|:--------|
|MissingParameter|The input parameter “parameter name” that is mandatory for processing this request is not supplied.|400|The parameter is missing.|
|InvalidParameter|The specified value of parameter “parameter name” is not valid.|400|The parameter value is invalid.|
|UnsupportedOperation|The specified action is not supported.|400|The interface is invalid.|
|NoSuchVersion|The specified version does not exist.|400| The version is invalid.|
|Throttling|Request was denied due to request throttling.|400|The operation is rejected by the traffic control system.|
|InvalidAccessKeyId.NotFound|The Access Key ID provided does not exist in our records.|400|The AccessKey is invalid.|
|Forbidden|User not authorized to operate on the specified resource.|403|The operation is not permitted.|
|Forbidden.RiskControl|This operation is forbidden by Aliyun Risk Control system.|403|The operation is forbidden by the risk control system.|
|SignatureDoesNotMatch|The signature we calculated does not match the one you provided. Please refer to the API reference about authentication for details.|403| The signature is invalid.|
|Forbidden.UserVerification|Your user account is not verified by Aliyun.|403|Real-name verification is missing.|

## Server errors {#section_o5d_1pq_b2b .section}

|Error code|Description| HTTP status code|Semantic|
|:---------|:----------|:----------------|:-------|
|InternalError|The request processing has failed due to some unknown error, exception or failure.|500|The server cannot process the request.|
|ServiceUnavailable|The request has failed due to a temporary failure of the server.|503|The server cannot process the request currently.|

