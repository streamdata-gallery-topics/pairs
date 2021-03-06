swagger: "2.0"
x-collection-name: nFusion Solutions
x-complete: 1
info:
  title: nFusion Solutions Market Data API v1
  description: nfusion-solutions-provides-rest-and-streaming-apis-that-deliver-enterprisegrade-financial-data--data-sets-include-realtime-and-historical-pricing-for-spot-prices-of-precious-metals-such-as-gold-silver-platinum-and-palladium-exchange-rates-for-major-currency-pairs-exchange-rates-for-crypto-currencies-such-as-btc-eth-and-ltc--all-api-access-requires-authentication--in-order-to-be-issued-access-credentials-you-must-first-enter-into-a-service-agreement-with-nfusion-solutions-and-acquire-a-commercial-license--for-information-on-how-to-obtain-a-licence-contact-salesnfusionsolutions-com-
  contact:
    name: nFusion Solutions
    url: https://nfusionsolutions.com/contact
    email: support@nfusionsolutions.com
  version: 1.0.0
host: api.nfusionsolutions.biz
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v{version}/Currencies/summary/supported:
    get:
      summary: Get list of currency pairs supported by the Summary endpoint
      description: "Only the currency pairs in the direction noted can be used with
        the Summary endpoint.\r\nFor example: USD/CAD is not the same as CAD/USD"
      operationId: ApiV{versionCurrenciesSummarySupportedGet
      x-api-path-slug: apivversioncurrenciessummarysupported-get
      parameters:
      - in: query
        name: format
        description: to override content negotiation specify a value of json or xml
      - in: query
        name: token
        description: auth token
      - in: path
        name: version
        description: The requested API version
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Currency
      - Pairs
      - Supported
      - By
      - Summary
      - Endpoint
  /api/v{version}/Currencies/history/supported:
    get:
      summary: Get list of currency pairs supported by the history endpoint
      description: "Only the currency pairs in the direction noted can be used with
        the history endpoint.\r\nFor example: USD/CAD is not the same as CAD/USD"
      operationId: ApiV{versionCurrenciesHistorySupportedGet
      x-api-path-slug: apivversioncurrencieshistorysupported-get
      parameters:
      - in: query
        name: format
        description: to override content negotiation specify a value of json or xml
      - in: query
        name: token
        description: auth token
      - in: path
        name: version
        description: The requested API version
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Currency
      - Pairs
      - Supported
      - By
      - History
      - Endpoint
  /api/v{version}/Currencies/rate:
    get:
      summary: Get latest mid rate for requested currency pairs
      description: Get latest mid rate for requested currency pairs.
      operationId: ApiV{versionCurrenciesRateGet
      x-api-path-slug: apivversioncurrenciesrate-get
      parameters:
      - in: query
        name: format
        description: to override content negotiation specify a value of json or xml
      - in: query
        name: pairs
        description: comma separated list of currency pairs
      - in: query
        name: token
        description: auth token
      - in: path
        name: version
        description: The requested API version
      responses:
        200:
          description: OK
      tags:
      - Latest
      - Mid
      - Raterequested
      - Currency
      - Pairs
  /api/v{version}/Currencies/summary:
    get:
      summary: Get latest Summary for requested currency pairs
      description: Current and daily summary information combined into a single quote
      operationId: ApiV{versionCurrenciesSummaryGet
      x-api-path-slug: apivversioncurrenciessummary-get
      parameters:
      - in: query
        name: format
        description: to override content negotiation specify a value of json or xml
      - in: query
        name: pairs
        description: comma separated list of currency pairs
      - in: query
        name: token
        description: auth token
      - in: path
        name: version
        description: The requested API version
      responses:
        200:
          description: OK
      tags:
      - Latest
      - Summaryrequested
      - Currency
      - Pairs
  /api/v{version}/Currencies/history:
    get:
      summary: Get historical prices for requested currency pairs
      description: "Historical OHLC data for the specified period and interval size\r\n\r\nThe
        combination of the interval parameter and start and end dates can result in
        results\r\nbeing truncated to conform to result size limits. See comments
        on interval parameter for details on valid interval values."
      operationId: ApiV{versionCurrenciesHistoryGet
      x-api-path-slug: apivversioncurrencieshistory-get
      parameters:
      - in: query
        name: end
        description: end date of time period
      - in: query
        name: format
        description: to override content negotiation specify a value of json or xml
      - in: query
        name: interval
        description: aggregation interval
      - in: query
        name: pairs
        description: comma separated list of currency pairs
      - in: query
        name: start
        description: start date of time period
      - in: query
        name: token
        description: auth token
      - in: path
        name: version
        description: The requested API version
      responses:
        200:
          description: OK
      tags:
      - Historical
      - Pricesrequested
      - Currency
      - Pairs