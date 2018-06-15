# Returned results {#concept_skk_h5b_b2b .concept}

After the API service is called, data is returned in a unified format.

-   The returned HTTP status code 2xx indicates a successful call,
-   and the status code 4xx or 5xx indicates a failed call.

For a successful call, the returned data is in XML or JSON format. An external system can set the format of returned data by setting an input parameter in the request. The default format is XML.

This document lists the examples of returned results in easy-to-view formats. The actual returned results have no line breaks, indentation, or other layouts.

## Successful results {#section_mrw_cwb_b2b .section}

-   XML format

    ```
    <? xml version="1.0" encoding="UTF-8"? > 
    <!—Result root node-->
    <API name+Response>
        <!—Returned request tag-->
        <RequestId>4C467B38-3910-447D-87BC-AC049166F216</RequestId>
        <!—Returned results-->
    </API name+Response>
    ```

-   JSON format

    ```
    {
        "RequestId": "4C467B38-3910-447D-87BC-AC049166F216"
        /* Returned results */
    }
    ```


## Error results {#section_eb1_kn4_c2b .section}

If an error is reported in an API call, no result data is returned. The caller can locate the cause of an error based on the error code corresponding to each interface and the public error codes.

When an error occurs in a call, an HTTP status code 4xx or 5xx is returned for the HTTP request. The returned message body contains the specific error code and error message. The message body also contains the globally unique RequestId and the requested HostId.

If the cause of error cannot be identified at the caller, contact Alibaba Cloud customer service and provide the HostId and RequestId to help us to solve the problem as soon as possible.

-   XML format

    ```
    <? xml version="1.0" encoding="UTF-8"? >
    <Error>
        <RequestId>8906582E-6722-409A-A6C4-0E7863B733A5</RequestId>
        <HostId>domain-intl.aliyuncs.com</HostId>
        <Code>DomainNotExist</Code>
        <Message>The domain name does not exist.</Message>
    </Error>
    ```

-   JSON format

    ```
    {
        "RequestId": "8906582E-6722-409A-A6C4-0E7863B733A5",
        "HostId": "domain-intl.aliyuncs.com",
        "Code": "DomainNotExist",
        "Message": "The domain name does not exist."
    }
    ```


