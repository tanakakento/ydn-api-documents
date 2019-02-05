# FeedDataService
FeedDataService provides functions to get URL for upload item list(tsv file format), to get upload status.

#### WSDL
| environment | url |
|---|---|
| production  | https://location.im.yahooapis.jp/services/V201806/FeedDataService?wsdl |
| sandbox  | https://sandbox.im.yahooapis.jp/services/V201806/FeedDataService?wsdl |

#### Namespace
http://im.yahooapis.jp/V201806/FeedData

#### Overview
Use this service to get URL for upload item list(tsv file format), to get upload status.

#### Operation
Describes the operation which provides by FeedDataService.

+ [getUploadUrl](#getuploadurl)
+ [getUploadStatus](#getuploadstatus)

#### Object
[FeedData](../data/FeedData)

## getUploadUrl
Returns URL for upload item list.

#### Request
| Parameter | Requirement | Data Type | Description |
|---|---|---|---|
| accountId | Req | xsd:long | Account ID. |
| itemListUploadType | Req |  [ItemListUploadType](../data/FeedData/ItemListUploadType.md)| Type of item list upload. |
| feedHolderId | Req |  xsd:long| FeedHolder ID. |

##### Request Sample
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <RequestHeader xmlns="http://im.yahooapis.jp/V201806/FeedData" xmlns:ns2="http://im.yahooapis.jp/V201806">
      <ns2:license>1111-1111-1111-1111</ns2:license>
      <ns2:apiAccountId>2222-2222-2222-2222</ns2:apiAccountId>
      <ns2:apiAccountPassword>password</ns2:apiAccountPassword>
    </RequestHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <getUploadUrl xmlns="http://im.yahooapis.jp/V201806/FeedData">
      <accountId>1111</accountId>
      <itemListUploadType>UPDATE_ALL</itemListUploadType>
      <feedHolderId>222</feedHolderId>
    </getUploadUrl>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

#### Response
| Field | Data Type | Description |
|---|---|---|
| rval | [UploadUrlValue](../data/FeedData/UploadUrlValue.md) | Temporary URL for upload. |

##### Response Sample
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <ResponseHeader xmlns="http://im.yahooapis.jp/V201806/FeedData" xmlns:ns2="http://im.yahooapis.jp/V201806">
      <ns2:service>FeedData</ns2:service>
      <ns2:requestTime>1531887805443</ns2:requestTime>
      <ns2:timeTakenSeconds>0.2671</ns2:timeTakenSeconds>
    </ResponseHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <getUploadUrlResponse xmlns="http://im.yahooapis.jp/V201806/FeedData" xmlns:ns2="http://im.yahooapis.jp/V201806">
      <rval>
        <accountId>1111</accountId>
        <itemListUploadType>UPDATE_ALL</itemListUploadType>
        <feedHolderId>2222</feedHolderId>
        <uploadUrl>https://colo01.im.yahooapis.jp/feedUpload/V201806/upload/KSwRXZuvEOH06e29wJuflTf9ZqYb.wn6ftbC_7stbaa6eF0TYw5HTZW8bwmNkway59_Nw62ExfIIFj2XPjXwNoDhtCRLjEVrbvtxIgxjxTpBmNqe0vItGSU-</uploadUrl>
      </rval>
    </getUploadUrlResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

## getUploadStatus
Returns status of uploaded item list.

#### Request
| Parameter | Requirement | Data Type | Description |
|---|---|---|---|
| selector | Req | [FeedDataSelector](../data/FeedData/FeedDataSelector.md) | Acquisition condition of upload status. |

##### Request Sample
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <RequestHeader xmlns="http://im.yahooapis.jp/V201806/FeedData" xmlns:ns2="http://im.yahooapis.jp/V201806">
      <ns2:license>1111-1111-1111-1111</ns2:license>
      <ns2:apiAccountId>2222-2222-2222-2222</ns2:apiAccountId>
      <ns2:apiAccountPassword>password</ns2:apiAccountPassword>
    </RequestHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <getUploadStatus xmlns="http://im.yahooapis.jp/V201806/FeedData" xmlns:ns2="http://im.yahooapis.jp/V201806">
      <selector>
        <accountId>1111</accountId>
        <feedHolderIds>222</feedHolderIds>
        <feedHolderIds>333</feedHolderIds>
        <feedHolderIds>444</feedHolderIds>
        <feedHolderIds>555</feedHolderIds>
        <feedHolderIds>666</feedHolderIds>
        <itemListUploadIds>777</itemListUploadIds>
        <uploadStatuses>COMPLETED</uploadStatuses>
        <uploadStatuses>SYSTEM_ERROR</uploadStatuses>
        <uploadStatuses>FILE_FORMAT_ERROR</uploadStatuses>
        <uploadStatuses>UPLOADED</uploadStatuses>
        <dateRange>
          <startDate>20160101</startDate>
          <endDate>20170101</endDate>
        </dateRange>
        <paging>
          <ns2:startIndex>1</ns2:startIndex>
          <ns2:numberResults>10</ns2:numberResults>
        </paging>
      </selector>
    </getUploadStatus>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

#### Response
| Field | Data Type | Description |
|---|---|---|
| rval | [FeedDataPage](../data/FeedData/FeedDataPage.md) | Registration result. |

##### Response Sample
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <ResponseHeader xmlns="http://im.yahooapis.jp/V201806/FeedData" xmlns:ns2="http://im.yahooapis.jp/V201806">
      <ns2:service>FeedData</ns2:service>
      <ns2:requestTime>1531887804443</ns2:requestTime>
      <ns2:timeTakenSeconds>0.2671</ns2:timeTakenSeconds>
    </ResponseHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <ns2:getUploadStatusResponse xmlns="http://im.yahooapis.jp/V201806" xmlns:ns2="http://im.yahooapis.jp/V201806/FeedData">
      <ns2:rval>
        <totalNumEntries>1</totalNumEntries>
        <Page.Type>FeedDataPage</Page.Type>
        <ns2:values>
          <operationSucceeded>true</operationSucceeded>
          <ns2:feedData>
            <ns2:accountId>1111</ns2:accountId>
            <ns2:feedHolderId>2222</ns2:feedHolderId>
            <ns2:itemListUploadId>777</ns2:itemListUploadId>
            <ns2:itemListUploadType>UPDATE_ALL</ns2:itemListUploadType>
            <ns2:itemListUploadStatus>UPLOADED</ns2:itemListUploadStatus>
            <ns2:uploadDate>20180313143813</ns2:uploadDate>
            <ns2:errorCount>2</ns2:errorCount>
            <ns2:errorListDownloadUrl>https://colo01.im.yahooapis.jp/feedUpload/V201806/downloadErrorFile/gaChTAqlEOFLfOACISiRi2A1Cq_K3zZUXT95bA2X08mrAkckbvq4e79qoNiyq34QaHNTG_0dfevjoURTzf6dGnqGXQkEPgQp4gGsl59Z</ns2:errorListDownloadUrl>
          </ns2:feedData>
        </ns2:values>
      </ns2:rval>
    </ns2:getUploadStatusResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
