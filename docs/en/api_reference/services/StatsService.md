# StatsService
StatsService retrieves the stats data of each campaign, ad group, ad, image and video.

#### WSDL
| environment | url |
|---|---|
| production  | https://location.im.yahooapis.jp/services/V201903/StatsService?wsdl |
| sandbox  | https://sandbox.im.yahooapis.jp/services/V201903/StatsService?wsdl |

#### Namespace
http://im.yahooapis.jp/V201903/Stats

#### Service Overview
StatsService retrieves the stats data of each campaign, ad group, ad, image and video.

#### Operation
Describes operations provided by StatsService.

+ [get](#get)

#### Object
[Stats](../data/Stats)

## get

### Request
Retrieves the stats information of each campaign, ad group, ad, image and video.

| Parameter | Requirement | Data Type | Description |
|---|---|---|---|
| selector | required | [StatsSelector](../data/Stats/StatsSelector.md) |Contains a set of criteria (parameters) for get method. |

##### Request Sample(Campaign Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <RequestHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:license>1111-1111-1111-1111</ns2:license>
      <ns2:apiAccountId>2222-2222-2222-2222</ns2:apiAccountId>
      <ns2:apiAccountPassword>password</ns2:apiAccountPassword>
    </RequestHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <get xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <selector>
        <accountId>11111</accountId>
        <campaignIds>22222</campaignIds>
        <statsPeriod>DEFINITE_VALUE_TWOWEEK</statsPeriod>
        <statsType>CAMPAIGN</statsType>
        <paging>
          <ns2:startIndex>1</ns2:startIndex>
          <ns2:numberResults>10</ns2:numberResults>
        </paging>
      </selector>
    </get>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
##### Request Sample(Ad group Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <RequestHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:license>1111-1111-1111-1111</ns2:license>
      <ns2:apiAccountId>2222-2222-2222-2222</ns2:apiAccountId>
      <ns2:apiAccountPassword>password</ns2:apiAccountPassword>
    </RequestHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <get xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <selector>
        <accountId>11111</accountId>
        <campaignIds>22222</campaignIds>
        <adGroupIds>33333</adGroupIds>
        <statsPeriod>DEFINITE_VALUE_TWOWEEK</statsPeriod>
        <statsType>ADGROUP</statsType>
        <paging>
          <ns2:startIndex>1</ns2:startIndex>
          <ns2:numberResults>10</ns2:numberResults>
        </paging>
      </selector>
    </get>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
##### Request Sample(Ad Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <RequestHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:license>1111-1111-1111-1111</ns2:license>
      <ns2:apiAccountId>2222-2222-2222-2222</ns2:apiAccountId>
      <ns2:apiAccountPassword>password</ns2:apiAccountPassword>
    </RequestHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <get xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <selector>
        <accountId>11111</accountId>
        <campaignIds>22222</campaignIds>
        <adGroupIds>33333</adGroupIds>
        <adIds>444444</adIds>
        <statsPeriod>DEFINITE_VALUE_TWOWEEK</statsPeriod>
        <statsType>AD</statsType>
        <paging>
          <ns2:startIndex>1</ns2:startIndex>
          <ns2:numberResults>10</ns2:numberResults>
        </paging>
      </selector>
    </get>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
##### Request Sample(Image Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <RequestHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:license>1111-1111-1111-1111</ns2:license>
      <ns2:apiAccountId>2222-2222-2222-2222</ns2:apiAccountId>
      <ns2:apiAccountPassword>password</ns2:apiAccountPassword>
    </RequestHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <get xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <selector>
        <accountId>11111</accountId>
        <mediaIds>22222</mediaIds>
        <statsPeriod>DEFINITE_VALUE_TWOWEEK</statsPeriod>
        <statsType>IMAGE</statsType>
        <paging>
          <ns2:startIndex>1</ns2:startIndex>
          <ns2:numberResults>10</ns2:numberResults>
        </paging>
      </selector>
    </get>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
##### Request Sample(Video Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <RequestHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:license>1111-1111-1111-1111</ns2:license>
      <ns2:apiAccountId>2222-2222-2222-2222</ns2:apiAccountId>
      <ns2:apiAccountPassword>password</ns2:apiAccountPassword>
    </RequestHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <get xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <selector>
        <accountId>11111</accountId>
        <mediaIds>22222</mediaIds>
        <statsPeriod>CUSTOM_DATE</statsPeriod>
        <statsPeriodCustomDate>
          <statsStartDate>20180101</statsStartDate>
          <statsEndDate>20190101</statsEndDate>
        </statsPeriodCustomDate>
        <statsType>VIDEO</statsType>
        <paging>
          <ns2:startIndex>1</ns2:startIndex>
          <ns2:numberResults>10</ns2:numberResults>
        </paging>
      </selector>
    </get>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
##### Request Sample(Video Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <RequestHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:license>1111-1111-1111-1111</ns2:license>
      <ns2:apiAccountId>2222-2222-2222-2222</ns2:apiAccountId>
      <ns2:apiAccountPassword>password</ns2:apiAccountPassword>
    </RequestHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <get xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <selector>
        <accountId>11111</accountId>
        <campaignIds>22222</campaignIds>
        <adGroupIds>33333</adGroupIds>
        <targetTypes>AD_SCHEDULE_TARGET</targetTypes>
        <statsPeriod>DEFINITE_VALUE_TWOWEEK</statsPeriod>
        <statsType>TARGET</statsType>
        <paging>
          <ns2:startIndex>1</ns2:startIndex>
          <ns2:numberResults>10</ns2:numberResults>
        </paging>
      </selector>
    </get>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

### Response
| Parameter | Data Type | Description |
|---|---|---|
| rval | [StatsPage](../data/Stats/StatsPage.md) | Contains the results (a list of all entities) for get method. |

##### Response Sample(Campaign Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <ResponseHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:service>Stats</ns2:service>
      <ns2:requestTime>1551686138900</ns2:requestTime>
      <ns2:timeTakenSeconds>0.2671</ns2:timeTakenSeconds>
    </ResponseHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <ns2:getResponse xmlns="http://im.yahooapis.jp/V201903" xmlns:ns2="http://im.yahooapis.jp/V201903/Stats">
      <ns2:rval>
        <totalNumEntries>1</totalNumEntries>
        <Page.Type>StatsPage</Page.Type>
        <ns2:period>
          <ns2:periodStartDate>
            <ns2:periodDate>20180216</ns2:periodDate>
          </ns2:periodStartDate>
          <ns2:periodEndDate>
            <ns2:periodDate>20180301</ns2:periodDate>
          </ns2:periodEndDate>
        </ns2:period>
        <ns2:values xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:type="ns2:CampaignStatsValues">
          <operationSucceeded>true</operationSucceeded>
          <ns2:accountId>1111</ns2:accountId>
          <ns2:statsPeriod>DEFINITE_VALUE_TWOWEEK</ns2:statsPeriod>
          <ns2:statsType>CAMPAIGN</ns2:statsType>
          <ns2:campaignId>22222</ns2:campaignId>
          <ns2:campaignName>Test Campaign</ns2:campaignName>
          <ns2:stats>
            <ns2:imps>4</ns2:imps>
            <ns2:clickRate>100.0</ns2:clickRate>
            <ns2:totalClickCost>4.23</ns2:totalClickCost>
            <ns2:clickCnt>4</ns2:clickCnt>
            <ns2:avgClickCost>0.2</ns2:avgClickCost>
            <ns2:conversions>19</ns2:conversions>
            <ns2:conversionRate>20.2</ns2:conversionRate>
            <ns2:cpa>21.2</ns2:cpa>
            <ns2:conversionValue>22</ns2:conversionValue>
            <ns2:valuePerConversions>23.3</ns2:valuePerConversions>
            <ns2:conversionsViaAdClick>100</ns2:conversionsViaAdClick>
            <ns2:conversionRateViaAdClick>100.1</ns2:conversionRateViaAdClick>
            <ns2:cpaViaAdClick>101</ns2:cpaViaAdClick>
            <ns2:conversionValueViaAdClick>102</ns2:conversionValueViaAdClick>
            <ns2:valuePerConversionsViaAdClick>103</ns2:valuePerConversionsViaAdClick>
            <ns2:allConversions>24</ns2:allConversions>
            <ns2:allConversionRate>25.0</ns2:allConversionRate>
            <ns2:allCpa>26.6</ns2:allCpa>
            <ns2:allConversionValue>27</ns2:allConversionValue>
            <ns2:valuePerAllConversions>28</ns2:valuePerAllConversions>
            <ns2:crossDeviceConversions>104</ns2:crossDeviceConversions>
            <ns2:avgDeliverRank>0.5</ns2:avgDeliverRank>
            <ns2:totalVimps>2</ns2:totalVimps>
            <ns2:vImps>2</ns2:vImps>
            <ns2:inViewClickCnt>2</ns2:inViewClickCnt>
            <ns2:inViewRate>100.0</ns2:inViewRate>
            <ns2:inViewClickRate>100.0</ns2:inViewClickRate>
            <ns2:paidVideoViews>4</ns2:paidVideoViews>
            <ns2:paidVideoViewRate>0.4</ns2:paidVideoViewRate>
            <ns2:averageCpv>0.5</ns2:averageCpv>
            <ns2:videoViews>2</ns2:videoViews>
            <ns2:videoViewsTo25>2</ns2:videoViewsTo25>
            <ns2:videoViewsTo50>2</ns2:videoViewsTo50>
            <ns2:videoViewsTo75>2</ns2:videoViewsTo75>
            <ns2:videoViewsTo95>2</ns2:videoViewsTo95>
            <ns2:videoViewsTo100>2</ns2:videoViewsTo100>
            <ns2:videoViewsTo3Sec>9</ns2:videoViewsTo3Sec>
            <ns2:averageRateVideoViewed>100.0</ns2:averageRateVideoViewed>
            <ns2:averageDurationVideoViewed>1.0</ns2:averageDurationVideoViewed>
            <ns2:convValuePerCost>1.1</ns2:convValuePerCost>
            <ns2:allConvValuePerCost>2.1</ns2:allConvValuePerCost>
            <ns2:convValueViaAdClickPerCost>3.1</ns2:convValueViaAdClickPerCost>
          </ns2:stats>
        </ns2:values>
      </ns2:rval>
    </ns2:getResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
##### Response Sample(Ad group Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <ResponseHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:service>Stats</ns2:service>
      <ns2:requestTime>1551686138951</ns2:requestTime>
      <ns2:timeTakenSeconds>0.2671</ns2:timeTakenSeconds>
    </ResponseHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <ns2:getResponse xmlns="http://im.yahooapis.jp/V201903" xmlns:ns2="http://im.yahooapis.jp/V201903/Stats">
      <ns2:rval>
        <totalNumEntries>1</totalNumEntries>
        <Page.Type>StatsPage</Page.Type>
        <ns2:period>
          <ns2:periodStartDate>
            <ns2:periodDate>20180216</ns2:periodDate>
          </ns2:periodStartDate>
          <ns2:periodEndDate>
            <ns2:periodDate>20180301</ns2:periodDate>
          </ns2:periodEndDate>
        </ns2:period>
        <ns2:values xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:type="ns2:AdGroupStatsValues">
          <operationSucceeded>true</operationSucceeded>
          <ns2:accountId>1111</ns2:accountId>
          <ns2:statsPeriod>DEFINITE_VALUE_TWOWEEK</ns2:statsPeriod>
          <ns2:statsType>ADGROUP</ns2:statsType>
          <ns2:campaignId>22222</ns2:campaignId>
          <ns2:campaignName>Test Campaign</ns2:campaignName>
          <ns2:adGroupId>33333</ns2:adGroupId>
          <ns2:adGroupName>Test AdGroup</ns2:adGroupName>
          <ns2:stats>
            <ns2:imps>4</ns2:imps>
            <ns2:clickRate>100.0</ns2:clickRate>
            <ns2:totalClickCost>4.23</ns2:totalClickCost>
            <ns2:clickCnt>4</ns2:clickCnt>
            <ns2:avgClickCost>0.2</ns2:avgClickCost>
            <ns2:conversions>19</ns2:conversions>
            <ns2:conversionRate>20.2</ns2:conversionRate>
            <ns2:cpa>21.2</ns2:cpa>
            <ns2:conversionValue>22</ns2:conversionValue>
            <ns2:valuePerConversions>23.3</ns2:valuePerConversions>
            <ns2:conversionsViaAdClick>100</ns2:conversionsViaAdClick>
            <ns2:conversionRateViaAdClick>100.1</ns2:conversionRateViaAdClick>
            <ns2:cpaViaAdClick>101</ns2:cpaViaAdClick>
            <ns2:conversionValueViaAdClick>102</ns2:conversionValueViaAdClick>
            <ns2:valuePerConversionsViaAdClick>103</ns2:valuePerConversionsViaAdClick>
            <ns2:allConversions>24</ns2:allConversions>
            <ns2:allConversionRate>25.0</ns2:allConversionRate>
            <ns2:allCpa>26.6</ns2:allCpa>
            <ns2:allConversionValue>27</ns2:allConversionValue>
            <ns2:valuePerAllConversions>28</ns2:valuePerAllConversions>
            <ns2:crossDeviceConversions>104</ns2:crossDeviceConversions>
            <ns2:avgDeliverRank>0.5</ns2:avgDeliverRank>
            <ns2:totalVimps>2</ns2:totalVimps>
            <ns2:vImps>2</ns2:vImps>
            <ns2:inViewClickCnt>2</ns2:inViewClickCnt>
            <ns2:inViewRate>100.0</ns2:inViewRate>
            <ns2:inViewClickRate>100.0</ns2:inViewClickRate>
            <ns2:paidVideoViews>4</ns2:paidVideoViews>
            <ns2:paidVideoViewRate>0.4</ns2:paidVideoViewRate>
            <ns2:averageCpv>0.5</ns2:averageCpv>
            <ns2:videoViews>2</ns2:videoViews>
            <ns2:videoViewsTo25>2</ns2:videoViewsTo25>
            <ns2:videoViewsTo50>2</ns2:videoViewsTo50>
            <ns2:videoViewsTo75>2</ns2:videoViewsTo75>
            <ns2:videoViewsTo95>2</ns2:videoViewsTo95>
            <ns2:videoViewsTo100>2</ns2:videoViewsTo100>
            <ns2:videoViewsTo3Sec>9</ns2:videoViewsTo3Sec>
            <ns2:averageRateVideoViewed>100.0</ns2:averageRateVideoViewed>
            <ns2:averageDurationVideoViewed>1.0</ns2:averageDurationVideoViewed>
            <ns2:convValuePerCost>1.1</ns2:convValuePerCost>
            <ns2:allConvValuePerCost>2.1</ns2:allConvValuePerCost>
            <ns2:convValueViaAdClickPerCost>3.1</ns2:convValueViaAdClickPerCost>
          </ns2:stats>
        </ns2:values>
      </ns2:rval>
    </ns2:getResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
##### Response Sample(Ad Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <ResponseHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:service>Stats</ns2:service>
      <ns2:requestTime>1551686138996</ns2:requestTime>
      <ns2:timeTakenSeconds>0.2671</ns2:timeTakenSeconds>
    </ResponseHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <ns2:getResponse xmlns="http://im.yahooapis.jp/V201903" xmlns:ns2="http://im.yahooapis.jp/V201903/Stats">
      <ns2:rval>
        <totalNumEntries>1</totalNumEntries>
        <Page.Type>StatsPage</Page.Type>
        <ns2:period>
          <ns2:periodStartDate>
            <ns2:periodDate>20180216</ns2:periodDate>
          </ns2:periodStartDate>
          <ns2:periodEndDate>
            <ns2:periodDate>20180301</ns2:periodDate>
          </ns2:periodEndDate>
        </ns2:period>
        <ns2:values xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:type="ns2:AdStatsValues">
          <operationSucceeded>true</operationSucceeded>
          <ns2:accountId>1111</ns2:accountId>
          <ns2:statsPeriod>DEFINITE_VALUE_TWOWEEK</ns2:statsPeriod>
          <ns2:statsType>AD</ns2:statsType>
          <ns2:campaignId>22222</ns2:campaignId>
          <ns2:campaignName>Test Campaign</ns2:campaignName>
          <ns2:adGroupId>33333</ns2:adGroupId>
          <ns2:adGroupName>Test AdGroup</ns2:adGroupName>
          <ns2:adId>44444</ns2:adId>
          <ns2:adName>Test Ad</ns2:adName>
          <ns2:stats>
            <ns2:imps>4</ns2:imps>
            <ns2:clickRate>100.0</ns2:clickRate>
            <ns2:totalClickCost>4.23</ns2:totalClickCost>
            <ns2:clickCnt>4</ns2:clickCnt>
            <ns2:avgClickCost>0.2</ns2:avgClickCost>
            <ns2:conversions>19</ns2:conversions>
            <ns2:conversionRate>20.2</ns2:conversionRate>
            <ns2:cpa>21.2</ns2:cpa>
            <ns2:conversionValue>22</ns2:conversionValue>
            <ns2:valuePerConversions>23.3</ns2:valuePerConversions>
            <ns2:conversionsViaAdClick>100</ns2:conversionsViaAdClick>
            <ns2:conversionRateViaAdClick>100.1</ns2:conversionRateViaAdClick>
            <ns2:cpaViaAdClick>101</ns2:cpaViaAdClick>
            <ns2:conversionValueViaAdClick>102</ns2:conversionValueViaAdClick>
            <ns2:valuePerConversionsViaAdClick>103</ns2:valuePerConversionsViaAdClick>
            <ns2:allConversions>24</ns2:allConversions>
            <ns2:allConversionRate>25.0</ns2:allConversionRate>
            <ns2:allCpa>26.6</ns2:allCpa>
            <ns2:allConversionValue>27</ns2:allConversionValue>
            <ns2:valuePerAllConversions>28</ns2:valuePerAllConversions>
            <ns2:crossDeviceConversions>104</ns2:crossDeviceConversions>
            <ns2:avgDeliverRank>0.5</ns2:avgDeliverRank>
            <ns2:totalVimps>2</ns2:totalVimps>
            <ns2:vImps>2</ns2:vImps>
            <ns2:inViewClickCnt>2</ns2:inViewClickCnt>
            <ns2:inViewRate>100.0</ns2:inViewRate>
            <ns2:inViewClickRate>100.0</ns2:inViewClickRate>
            <ns2:paidVideoViews>4</ns2:paidVideoViews>
            <ns2:paidVideoViewRate>0.4</ns2:paidVideoViewRate>
            <ns2:averageCpv>0.5</ns2:averageCpv>
            <ns2:videoViews>2</ns2:videoViews>
            <ns2:videoViewsTo25>2</ns2:videoViewsTo25>
            <ns2:videoViewsTo50>2</ns2:videoViewsTo50>
            <ns2:videoViewsTo75>2</ns2:videoViewsTo75>
            <ns2:videoViewsTo95>2</ns2:videoViewsTo95>
            <ns2:videoViewsTo100>2</ns2:videoViewsTo100>
            <ns2:videoViewsTo3Sec>9</ns2:videoViewsTo3Sec>
            <ns2:averageRateVideoViewed>100.0</ns2:averageRateVideoViewed>
            <ns2:averageDurationVideoViewed>1.0</ns2:averageDurationVideoViewed>
            <ns2:convValuePerCost>1.1</ns2:convValuePerCost>
            <ns2:allConvValuePerCost>2.1</ns2:allConvValuePerCost>
            <ns2:convValueViaAdClickPerCost>3.1</ns2:convValueViaAdClickPerCost>
          </ns2:stats>
        </ns2:values>
      </ns2:rval>
    </ns2:getResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
##### Response Sample(Image Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <ResponseHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:service>Stats</ns2:service>
      <ns2:requestTime>1551686139044</ns2:requestTime>
      <ns2:timeTakenSeconds>0.2671</ns2:timeTakenSeconds>
    </ResponseHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <ns2:getResponse xmlns="http://im.yahooapis.jp/V201903" xmlns:ns2="http://im.yahooapis.jp/V201903/Stats">
      <ns2:rval>
        <totalNumEntries>1</totalNumEntries>
        <Page.Type>StatsPage</Page.Type>
        <ns2:period>
          <ns2:periodStartDate>
            <ns2:periodDate>20180216</ns2:periodDate>
          </ns2:periodStartDate>
          <ns2:periodEndDate>
            <ns2:periodDate>20180301</ns2:periodDate>
          </ns2:periodEndDate>
        </ns2:period>
        <ns2:values xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:type="ns2:ImageStatsValues">
          <operationSucceeded>true</operationSucceeded>
          <ns2:accountId>1111</ns2:accountId>
          <ns2:statsPeriod>DEFINITE_VALUE_TWOWEEK</ns2:statsPeriod>
          <ns2:statsType>IMAGE</ns2:statsType>
          <ns2:mediaId>22222</ns2:mediaId>
          <ns2:mediaName>TestMedia.jpg</ns2:mediaName>
          <ns2:mediaTitle>Test Media</ns2:mediaTitle>
          <ns2:stats>
            <ns2:imps>4</ns2:imps>
            <ns2:clickRate>100.0</ns2:clickRate>
            <ns2:totalClickCost>4.23</ns2:totalClickCost>
            <ns2:clickCnt>4</ns2:clickCnt>
            <ns2:avgClickCost>0.2</ns2:avgClickCost>
            <ns2:conversions>19</ns2:conversions>
            <ns2:conversionRate>20.2</ns2:conversionRate>
            <ns2:cpa>21.2</ns2:cpa>
            <ns2:conversionValue>22</ns2:conversionValue>
            <ns2:valuePerConversions>23.3</ns2:valuePerConversions>
            <ns2:conversionsViaAdClick>100</ns2:conversionsViaAdClick>
            <ns2:conversionRateViaAdClick>100.1</ns2:conversionRateViaAdClick>
            <ns2:cpaViaAdClick>101</ns2:cpaViaAdClick>
            <ns2:conversionValueViaAdClick>102</ns2:conversionValueViaAdClick>
            <ns2:valuePerConversionsViaAdClick>103</ns2:valuePerConversionsViaAdClick>
            <ns2:allConversions>24</ns2:allConversions>
            <ns2:allConversionRate>25.0</ns2:allConversionRate>
            <ns2:allCpa>26.6</ns2:allCpa>
            <ns2:allConversionValue>27</ns2:allConversionValue>
            <ns2:valuePerAllConversions>28</ns2:valuePerAllConversions>
            <ns2:crossDeviceConversions>104</ns2:crossDeviceConversions>
            <ns2:avgDeliverRank>0.5</ns2:avgDeliverRank>
            <ns2:totalVimps>2</ns2:totalVimps>
            <ns2:vImps>2</ns2:vImps>
            <ns2:inViewClickCnt>2</ns2:inViewClickCnt>
            <ns2:inViewRate>100.0</ns2:inViewRate>
            <ns2:inViewClickRate>100.0</ns2:inViewClickRate>
            <ns2:paidVideoViews>4</ns2:paidVideoViews>
            <ns2:paidVideoViewRate>0.4</ns2:paidVideoViewRate>
            <ns2:averageCpv>0.5</ns2:averageCpv>
            <ns2:videoViews>2</ns2:videoViews>
            <ns2:videoViewsTo25>2</ns2:videoViewsTo25>
            <ns2:videoViewsTo50>2</ns2:videoViewsTo50>
            <ns2:videoViewsTo75>2</ns2:videoViewsTo75>
            <ns2:videoViewsTo95>2</ns2:videoViewsTo95>
            <ns2:videoViewsTo100>2</ns2:videoViewsTo100>
            <ns2:videoViewsTo3Sec>9</ns2:videoViewsTo3Sec>
            <ns2:averageRateVideoViewed>100.0</ns2:averageRateVideoViewed>
            <ns2:averageDurationVideoViewed>1.0</ns2:averageDurationVideoViewed>
            <ns2:convValuePerCost>1.1</ns2:convValuePerCost>
            <ns2:allConvValuePerCost>2.1</ns2:allConvValuePerCost>
            <ns2:convValueViaAdClickPerCost>3.1</ns2:convValueViaAdClickPerCost>
          </ns2:stats>
        </ns2:values>
      </ns2:rval>
    </ns2:getResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
##### Response Sample(Video Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <ResponseHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:service>Stats</ns2:service>
      <ns2:requestTime>1551686139094</ns2:requestTime>
      <ns2:timeTakenSeconds>0.2671</ns2:timeTakenSeconds>
    </ResponseHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <ns2:getResponse xmlns="http://im.yahooapis.jp/V201903" xmlns:ns2="http://im.yahooapis.jp/V201903/Stats">
      <ns2:rval>
        <totalNumEntries>1</totalNumEntries>
        <Page.Type>StatsPage</Page.Type>
        <ns2:period>
          <ns2:periodStartDate>
            <ns2:periodDate>20180101</ns2:periodDate>
            <ns2:periodTime>000000</ns2:periodTime>
          </ns2:periodStartDate>
          <ns2:periodEndDate>
            <ns2:periodDate>20190101</ns2:periodDate>
            <ns2:periodTime>000000</ns2:periodTime>
          </ns2:periodEndDate>
        </ns2:period>
        <ns2:values xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:type="ns2:VideoStatsValues">
          <operationSucceeded>true</operationSucceeded>
          <ns2:accountId>1111</ns2:accountId>
          <ns2:statsPeriod>CUSTOM_DATE</ns2:statsPeriod>
          <ns2:statsPeriodCustomDate>
            <ns2:statsStartDate>20180101</ns2:statsStartDate>
            <ns2:statsEndDate>20190101</ns2:statsEndDate>
          </ns2:statsPeriodCustomDate>
          <ns2:statsType>VIDEO</ns2:statsType>
          <ns2:mediaId>22222</ns2:mediaId>
          <ns2:videoName>test.mp4</ns2:videoName>
          <ns2:videoTitle>Test Video</ns2:videoTitle>
          <ns2:stats>
            <ns2:imps>4</ns2:imps>
            <ns2:clickRate>100.0</ns2:clickRate>
            <ns2:totalClickCost>4.23</ns2:totalClickCost>
            <ns2:clickCnt>4</ns2:clickCnt>
            <ns2:avgClickCost>0.2</ns2:avgClickCost>
            <ns2:conversions>19</ns2:conversions>
            <ns2:conversionRate>20.2</ns2:conversionRate>
            <ns2:cpa>21.2</ns2:cpa>
            <ns2:conversionValue>22</ns2:conversionValue>
            <ns2:valuePerConversions>23.3</ns2:valuePerConversions>
            <ns2:conversionsViaAdClick>100</ns2:conversionsViaAdClick>
            <ns2:conversionRateViaAdClick>100.1</ns2:conversionRateViaAdClick>
            <ns2:cpaViaAdClick>101</ns2:cpaViaAdClick>
            <ns2:conversionValueViaAdClick>102</ns2:conversionValueViaAdClick>
            <ns2:valuePerConversionsViaAdClick>103</ns2:valuePerConversionsViaAdClick>
            <ns2:allConversions>24</ns2:allConversions>
            <ns2:allConversionRate>25.0</ns2:allConversionRate>
            <ns2:allCpa>26.6</ns2:allCpa>
            <ns2:allConversionValue>27</ns2:allConversionValue>
            <ns2:valuePerAllConversions>28</ns2:valuePerAllConversions>
            <ns2:crossDeviceConversions>104</ns2:crossDeviceConversions>
            <ns2:avgDeliverRank>0.5</ns2:avgDeliverRank>
            <ns2:totalVimps>2</ns2:totalVimps>
            <ns2:vImps>2</ns2:vImps>
            <ns2:inViewClickCnt>2</ns2:inViewClickCnt>
            <ns2:inViewRate>100.0</ns2:inViewRate>
            <ns2:inViewClickRate>100.0</ns2:inViewClickRate>
            <ns2:paidVideoViews>4</ns2:paidVideoViews>
            <ns2:paidVideoViewRate>0.4</ns2:paidVideoViewRate>
            <ns2:averageCpv>0.5</ns2:averageCpv>
            <ns2:videoViews>2</ns2:videoViews>
            <ns2:videoViewsTo25>2</ns2:videoViewsTo25>
            <ns2:videoViewsTo50>2</ns2:videoViewsTo50>
            <ns2:videoViewsTo75>2</ns2:videoViewsTo75>
            <ns2:videoViewsTo95>2</ns2:videoViewsTo95>
            <ns2:videoViewsTo100>2</ns2:videoViewsTo100>
            <ns2:videoViewsTo3Sec>9</ns2:videoViewsTo3Sec>
            <ns2:averageRateVideoViewed>100.0</ns2:averageRateVideoViewed>
            <ns2:averageDurationVideoViewed>1.0</ns2:averageDurationVideoViewed>
            <ns2:convValuePerCost>1.1</ns2:convValuePerCost>
            <ns2:allConvValuePerCost>2.1</ns2:allConvValuePerCost>
            <ns2:convValueViaAdClickPerCost>3.1</ns2:convValueViaAdClickPerCost>
          </ns2:stats>
        </ns2:values>
      </ns2:rval>
    </ns2:getResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
##### Response Sample(Video Stats Information)
```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Header>
    <ResponseHeader xmlns="http://im.yahooapis.jp/V201903/Stats" xmlns:ns2="http://im.yahooapis.jp/V201903">
      <ns2:service>Stats</ns2:service>
      <ns2:requestTime>1551686139148</ns2:requestTime>
      <ns2:timeTakenSeconds>0.2671</ns2:timeTakenSeconds>
    </ResponseHeader>
  </SOAP-ENV:Header>
  <SOAP-ENV:Body>
    <ns2:getResponse xmlns="http://im.yahooapis.jp/V201903" xmlns:ns2="http://im.yahooapis.jp/V201903/Stats">
      <ns2:rval>
        <totalNumEntries>1</totalNumEntries>
        <Page.Type>StatsPage</Page.Type>
        <ns2:period>
          <ns2:periodStartDate>
            <ns2:periodDate>20180101</ns2:periodDate>
            <ns2:periodTime>000000</ns2:periodTime>
          </ns2:periodStartDate>
          <ns2:periodEndDate>
            <ns2:periodDate>20190101</ns2:periodDate>
            <ns2:periodTime>000000</ns2:periodTime>
          </ns2:periodEndDate>
        </ns2:period>
        <ns2:values xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:type="ns2:TargetStatsValues">
          <operationSucceeded>true</operationSucceeded>
          <ns2:accountId>1111</ns2:accountId>
          <ns2:statsPeriod>DEFINITE_VALUE_TWOWEEK</ns2:statsPeriod>
          <ns2:statsType>TARGET</ns2:statsType>
          <ns2:campaignId>22222</ns2:campaignId>
          <ns2:campaignName>Test Campaign</ns2:campaignName>
          <ns2:adGroupId>33333</ns2:adGroupId>
          <ns2:adGroupName>Test AdGroup</ns2:adGroupName>
          <ns2:target xsi:type="ns2:AdScheduleTarget">
            <ns2:type>AD_SCHEDULE_TARGET</ns2:type>
            <ns2:targetSetting>ACTIVE</ns2:targetSetting>
            <ns2:targetId>aa111111</ns2:targetId>
            <ns2:dayOfWeek>MONDAY</ns2:dayOfWeek>
            <ns2:startHour>13</ns2:startHour>
            <ns2:endHour>14</ns2:endHour>
          </ns2:target>
          <ns2:stats>
            <ns2:imps>4</ns2:imps>
            <ns2:clickRate>100.0</ns2:clickRate>
            <ns2:totalClickCost>4.23</ns2:totalClickCost>
            <ns2:clickCnt>4</ns2:clickCnt>
            <ns2:avgClickCost>0.2</ns2:avgClickCost>
            <ns2:conversions>19</ns2:conversions>
            <ns2:conversionRate>20.2</ns2:conversionRate>
            <ns2:cpa>21.2</ns2:cpa>
            <ns2:conversionValue>22</ns2:conversionValue>
            <ns2:valuePerConversions>23.3</ns2:valuePerConversions>
            <ns2:conversionsViaAdClick>100</ns2:conversionsViaAdClick>
            <ns2:conversionRateViaAdClick>100.1</ns2:conversionRateViaAdClick>
            <ns2:cpaViaAdClick>101</ns2:cpaViaAdClick>
            <ns2:conversionValueViaAdClick>102</ns2:conversionValueViaAdClick>
            <ns2:valuePerConversionsViaAdClick>103</ns2:valuePerConversionsViaAdClick>
            <ns2:allConversions>24</ns2:allConversions>
            <ns2:allConversionRate>25.0</ns2:allConversionRate>
            <ns2:allCpa>26.6</ns2:allCpa>
            <ns2:allConversionValue>27</ns2:allConversionValue>
            <ns2:valuePerAllConversions>28</ns2:valuePerAllConversions>
            <ns2:crossDeviceConversions>104</ns2:crossDeviceConversions>
            <ns2:avgDeliverRank>0.5</ns2:avgDeliverRank>
            <ns2:totalVimps>2</ns2:totalVimps>
            <ns2:vImps>2</ns2:vImps>
            <ns2:inViewClickCnt>2</ns2:inViewClickCnt>
            <ns2:inViewRate>100.0</ns2:inViewRate>
            <ns2:inViewClickRate>100.0</ns2:inViewClickRate>
            <ns2:paidVideoViews>4</ns2:paidVideoViews>
            <ns2:paidVideoViewRate>0.4</ns2:paidVideoViewRate>
            <ns2:averageCpv>0.5</ns2:averageCpv>
            <ns2:videoViews>2</ns2:videoViews>
            <ns2:videoViewsTo25>2</ns2:videoViewsTo25>
            <ns2:videoViewsTo50>2</ns2:videoViewsTo50>
            <ns2:videoViewsTo75>2</ns2:videoViewsTo75>
            <ns2:videoViewsTo95>2</ns2:videoViewsTo95>
            <ns2:videoViewsTo100>2</ns2:videoViewsTo100>
            <ns2:videoViewsTo3Sec>9</ns2:videoViewsTo3Sec>
            <ns2:averageRateVideoViewed>100.0</ns2:averageRateVideoViewed>
            <ns2:averageDurationVideoViewed>1.0</ns2:averageDurationVideoViewed>
            <ns2:convValuePerCost>1.1</ns2:convValuePerCost>
            <ns2:allConvValuePerCost>2.1</ns2:allConvValuePerCost>
            <ns2:convValueViaAdClickPerCost>3.1</ns2:convValueViaAdClickPerCost>
          </ns2:stats>
        </ns2:values>
      </ns2:rval>
    </ns2:getResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>
