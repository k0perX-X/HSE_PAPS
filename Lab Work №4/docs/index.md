# Core API

## Access

## [Methods]{#__Methods}

\[ Jump to [Models](#__Models) \]

### Table of Contents

::: method-summary
:::

#### [ActiveBlankets](#ActiveBlankets)

-   [`get /ActiveBlankets`](#activeBlanketsGet)
-   [`delete /ActiveBlankets/{id}`](#activeBlanketsIdDelete)
-   [`get /ActiveBlankets/{id}`](#activeBlanketsIdGet)
-   [`put /ActiveBlankets/{id}`](#activeBlanketsIdPut)
-   [`post /ActiveBlankets`](#activeBlanketsPost)

#### [Clients](#Clients)

-   [`get /Clients`](#clientsGet)
-   [`delete /Clients/{id}`](#clientsIdDelete)
-   [`get /Clients/{id}`](#clientsIdGet)
-   [`put /Clients/{id}`](#clientsIdPut)
-   [`post /Clients`](#clientsPost)

#### [Example](#Example)

-   [`get /Example/{id}`](#exampleIdGet)
-   [`get /Example`](#getWeatherForecast)

#### [Map](#Map)

-   [`get /Map`](#getAllVendingMachneInformation)

# [ActiveBlankets]{#ActiveBlankets}

::: method
[]{#activeBlanketsGet}

::: method-path
[Up](#__Methods){.up}

``` get
get /ActiveBlankets
```
:::

::: method-summary
Получить полный список пледов в аренде ([activeBlanketsGet]{.nickname})
:::

::: method-notes
:::

### Return type {#return-type .field-label}

::: return-type
array\[[ActiveBlanket](#ActiveBlanket)\]
:::

### Example data {#example-data .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
[ {
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
  "paymentTariff" : {
    "price" : 0.8008281904610115,
    "name" : "name",
    "description" : "description",
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
  }
}, {
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
  "paymentTariff" : {
    "price" : 0.8008281904610115,
    "name" : "name",
    "description" : "description",
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
  }
} ]
```

### Produces {#produces .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses .field-label}

#### 200 {#section .field-label}

Данные о всех пледах

#### 500 {#section-1 .field-label}

Ошибка базы данных [](#)
:::

------------------------------------------------------------------------

::: method
[]{#activeBlanketsIdDelete}

::: method-path
[Up](#__Methods){.up}

``` delete
delete /ActiveBlankets/{id}
```
:::

::: method-summary
Удалить активный плед ([activeBlanketsIdDelete]{.nickname})
:::

::: method-notes
:::

### Path parameters {#path-parameters .field-label}

::: field-items
::: param
id (required)
:::

::: param-desc
[Path Parameter]{.param-type} --- GUID пледа format: uuid
:::
:::

### Return type {#return-type-1 .field-label}

::: return-type
[ActiveBlanket](#ActiveBlanket)
:::

### Example data {#example-data-1 .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
{
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
  "paymentTariff" : {
    "price" : 0.8008281904610115,
    "name" : "name",
    "description" : "description",
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
  }
}
```

### Produces {#produces-1 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-1 .field-label}

#### 200 {#section-2 .field-label}

Данные о пледе удалены [ActiveBlanket](#ActiveBlanket)

#### 404 {#section-3 .field-label}

Не найден плед [ProblemDetails](#ProblemDetails)

#### 500 {#section-4 .field-label}

Ошибка базы данных [](#)
:::

------------------------------------------------------------------------

::: method
[]{#activeBlanketsIdGet}

::: method-path
[Up](#__Methods){.up}

``` get
get /ActiveBlankets/{id}
```
:::

::: method-summary
Получить конкретный плед по ID ([activeBlanketsIdGet]{.nickname})
:::

::: method-notes
:::

### Path parameters {#path-parameters-1 .field-label}

::: field-items
::: param
id (required)
:::

::: param-desc
[Path Parameter]{.param-type} --- GUID пледа format: uuid
:::
:::

### Return type {#return-type-2 .field-label}

::: return-type
[ActiveBlanket](#ActiveBlanket)
:::

### Example data {#example-data-2 .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
{
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
  "paymentTariff" : {
    "price" : 0.8008281904610115,
    "name" : "name",
    "description" : "description",
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
  }
}
```

### Produces {#produces-2 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-2 .field-label}

#### 200 {#section-5 .field-label}

Данные о конкретном пледе [ActiveBlanket](#ActiveBlanket)

#### 500 {#section-6 .field-label}

Ошибка базы данных [](#)
:::

------------------------------------------------------------------------

::: method
[]{#activeBlanketsIdPut}

::: method-path
[Up](#__Methods){.up}

``` put
put /ActiveBlankets/{id}
```
:::

::: method-summary
Изменить данные о активном пледе ([activeBlanketsIdPut]{.nickname})
:::

::: method-notes
:::

### Path parameters {#path-parameters-2 .field-label}

::: field-items
::: param
id (required)
:::

::: param-desc
[Path Parameter]{.param-type} --- GUID пледа format: uuid
:::
:::

### Consumes {#consumes .field-label}

This API call consumes the following media types via the
[Content-Type]{.header} request header:

-   `application/json`
-   `text/json`
-   `application/*+json`

### Request body {#request-body .field-label}

::: field-items
::: param
body [ActiveBlanket](#ActiveBlanket) (optional)
:::

::: param-desc
[Body Parameter]{.param-type} --- Полное представление активного пледа
:::
:::

### Produces {#produces-3 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-3 .field-label}

#### 204 {#section-7 .field-label}

Данные о пледе изменены [](#)

#### 400 {#section-8 .field-label}

GUID не совпадают [ProblemDetails](#ProblemDetails)

#### 404 {#section-9 .field-label}

Не найден плед [ProblemDetails](#ProblemDetails)

#### 500 {#section-10 .field-label}

Ошибка базы данных [](#)
:::

------------------------------------------------------------------------

::: method
[]{#activeBlanketsPost}

::: method-path
[Up](#__Methods){.up}

``` post
post /ActiveBlankets
```
:::

::: method-summary
Создать новый активный плед ([activeBlanketsPost]{.nickname})
:::

::: method-notes
:::

### Consumes {#consumes-1 .field-label}

This API call consumes the following media types via the
[Content-Type]{.header} request header:

-   `application/json`
-   `text/json`
-   `application/*+json`

### Request body {#request-body-1 .field-label}

::: field-items
::: param
body [ActiveBlanket](#ActiveBlanket) (optional)
:::

::: param-desc
[Body Parameter]{.param-type} --- Полное представление активного пледа
:::
:::

### Return type {#return-type-3 .field-label}

::: return-type
[ActiveBlanket](#ActiveBlanket)
:::

### Example data {#example-data-3 .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
{
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
  "paymentTariff" : {
    "price" : 0.8008281904610115,
    "name" : "name",
    "description" : "description",
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
  }
}
```

### Produces {#produces-4 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-4 .field-label}

#### 200 {#section-11 .field-label}

Данные сохранены [ActiveBlanket](#ActiveBlanket)

#### 500 {#section-12 .field-label}

Ошибка базы данных [](#)
:::

------------------------------------------------------------------------

# [Clients]{#Clients}

::: method
[]{#clientsGet}

::: method-path
[Up](#__Methods){.up}

``` get
get /Clients
```
:::

::: method-summary
Получить полный список клиентов ([clientsGet]{.nickname})
:::

::: method-notes
:::

### Return type {#return-type-4 .field-label}

::: return-type
array\[[Client](#Client)\]
:::

### Example data {#example-data-4 .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
[ {
  "phoneNumber" : 0,
  "activeBlankets" : [ {
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
    "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
    "paymentTariff" : {
      "price" : 0.8008281904610115,
      "name" : "name",
      "description" : "description",
      "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
    }
  }, {
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
    "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
    "paymentTariff" : {
      "price" : 0.8008281904610115,
      "name" : "name",
      "description" : "description",
      "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
    }
  } ],
  "dateOfRegistration" : "2000-01-23T04:56:07.000+00:00",
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "email" : "email"
}, {
  "phoneNumber" : 0,
  "activeBlankets" : [ {
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
    "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
    "paymentTariff" : {
      "price" : 0.8008281904610115,
      "name" : "name",
      "description" : "description",
      "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
    }
  }, {
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
    "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
    "paymentTariff" : {
      "price" : 0.8008281904610115,
      "name" : "name",
      "description" : "description",
      "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
    }
  } ],
  "dateOfRegistration" : "2000-01-23T04:56:07.000+00:00",
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "email" : "email"
} ]
```

### Produces {#produces-5 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-5 .field-label}

#### 200 {#section-13 .field-label}

Данные о всех клиентах

#### 500 {#section-14 .field-label}

Ошибка базы данных [](#)
:::

------------------------------------------------------------------------

::: method
[]{#clientsIdDelete}

::: method-path
[Up](#__Methods){.up}

``` delete
delete /Clients/{id}
```
:::

::: method-summary
Удалить клиента ([clientsIdDelete]{.nickname})
:::

::: method-notes
:::

### Path parameters {#path-parameters-3 .field-label}

::: field-items
::: param
id (required)
:::

::: param-desc
[Path Parameter]{.param-type} --- GUID клиента format: uuid
:::
:::

### Return type {#return-type-5 .field-label}

::: return-type
[Client](#Client)
:::

### Example data {#example-data-5 .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
{
  "phoneNumber" : 0,
  "activeBlankets" : [ {
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
    "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
    "paymentTariff" : {
      "price" : 0.8008281904610115,
      "name" : "name",
      "description" : "description",
      "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
    }
  }, {
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
    "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
    "paymentTariff" : {
      "price" : 0.8008281904610115,
      "name" : "name",
      "description" : "description",
      "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
    }
  } ],
  "dateOfRegistration" : "2000-01-23T04:56:07.000+00:00",
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "email" : "email"
}
```

### Produces {#produces-6 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-6 .field-label}

#### 200 {#section-15 .field-label}

Данные о кллиенте удалены [Client](#Client)

#### 404 {#section-16 .field-label}

Не найден клиент [ProblemDetails](#ProblemDetails)

#### 500 {#section-17 .field-label}

Ошибка базы данных [](#)
:::

------------------------------------------------------------------------

::: method
[]{#clientsIdGet}

::: method-path
[Up](#__Methods){.up}

``` get
get /Clients/{id}
```
:::

::: method-summary
Получить конкретного клиента по ID ([clientsIdGet]{.nickname})
:::

::: method-notes
:::

### Path parameters {#path-parameters-4 .field-label}

::: field-items
::: param
id (required)
:::

::: param-desc
[Path Parameter]{.param-type} --- GUID клиента format: uuid
:::
:::

### Return type {#return-type-6 .field-label}

::: return-type
[Client](#Client)
:::

### Example data {#example-data-6 .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
{
  "phoneNumber" : 0,
  "activeBlankets" : [ {
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
    "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
    "paymentTariff" : {
      "price" : 0.8008281904610115,
      "name" : "name",
      "description" : "description",
      "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
    }
  }, {
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
    "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
    "paymentTariff" : {
      "price" : 0.8008281904610115,
      "name" : "name",
      "description" : "description",
      "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
    }
  } ],
  "dateOfRegistration" : "2000-01-23T04:56:07.000+00:00",
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "email" : "email"
}
```

### Produces {#produces-7 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-7 .field-label}

#### 200 {#section-18 .field-label}

Данные о конкретном клиенте [Client](#Client)

#### 500 {#section-19 .field-label}

Ошибка базы данных [](#)
:::

------------------------------------------------------------------------

::: method
[]{#clientsIdPut}

::: method-path
[Up](#__Methods){.up}

``` put
put /Clients/{id}
```
:::

::: method-summary
Изменить данные о клиенте ([clientsIdPut]{.nickname})
:::

::: method-notes
:::

### Path parameters {#path-parameters-5 .field-label}

::: field-items
::: param
id (required)
:::

::: param-desc
[Path Parameter]{.param-type} --- GUID клиента format: uuid
:::
:::

### Consumes {#consumes-2 .field-label}

This API call consumes the following media types via the
[Content-Type]{.header} request header:

-   `application/json`
-   `text/json`
-   `application/*+json`

### Request body {#request-body-2 .field-label}

::: field-items
::: param
body [Client](#Client) (optional)
:::

::: param-desc
[Body Parameter]{.param-type} --- Полное представление клиента
:::
:::

### Produces {#produces-8 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-8 .field-label}

#### 204 {#section-20 .field-label}

Данные о клиенте изменены [](#)

#### 400 {#section-21 .field-label}

GUID не совпадают [ProblemDetails](#ProblemDetails)

#### 404 {#section-22 .field-label}

Не найден клиент [ProblemDetails](#ProblemDetails)

#### 500 {#section-23 .field-label}

Ошибка базы данных [](#)
:::

------------------------------------------------------------------------

::: method
[]{#clientsPost}

::: method-path
[Up](#__Methods){.up}

``` post
post /Clients
```
:::

::: method-summary
Создать нового клиента ([clientsPost]{.nickname})
:::

::: method-notes
:::

### Consumes {#consumes-3 .field-label}

This API call consumes the following media types via the
[Content-Type]{.header} request header:

-   `application/json`
-   `text/json`
-   `application/*+json`

### Request body {#request-body-3 .field-label}

::: field-items
::: param
body [Client](#Client) (optional)
:::

::: param-desc
[Body Parameter]{.param-type} --- Полное представление клиента
:::
:::

### Return type {#return-type-7 .field-label}

::: return-type
[Client](#Client)
:::

### Example data {#example-data-7 .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
{
  "phoneNumber" : 0,
  "activeBlankets" : [ {
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
    "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
    "paymentTariff" : {
      "price" : 0.8008281904610115,
      "name" : "name",
      "description" : "description",
      "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
    }
  }, {
    "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
    "dataOfIssue" : "2000-01-23T04:56:07.000+00:00",
    "paymentTariff" : {
      "price" : 0.8008281904610115,
      "name" : "name",
      "description" : "description",
      "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91"
    }
  } ],
  "dateOfRegistration" : "2000-01-23T04:56:07.000+00:00",
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "email" : "email"
}
```

### Produces {#produces-9 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-9 .field-label}

#### 200 {#section-24 .field-label}

Данные сохранены [Client](#Client)

#### 500 {#section-25 .field-label}

Ошибка базы данных [](#)
:::

------------------------------------------------------------------------

# [Example]{#Example}

::: method
[]{#exampleIdGet}

::: method-path
[Up](#__Methods){.up}

``` get
get /Example/{id}
```
:::

::: method-summary
Retrieves a specific product by unique id ([exampleIdGet]{.nickname})
:::

::: method-notes
Awesomeness!
:::

### Path parameters {#path-parameters-6 .field-label}

::: field-items
::: param
id (required)
:::

::: param-desc
[Path Parameter]{.param-type} --- The product id format: int32
:::
:::

### Return type {#return-type-8 .field-label}

::: return-type
[Product](#Product)
:::

### Example data {#example-data-8 .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
{
  "sizes" : [ "Small", "Medium", "Large" ],
  "availableStock" : 10,
  "name" : "Men's basketball shoes"
}
```

### Produces {#produces-10 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-10 .field-label}

#### 200 {#section-26 .field-label}

Product retrieved [Product](#Product)

#### 404 {#section-27 .field-label}

Product not found [ProblemDetails](#ProblemDetails)

#### 500 {#section-28 .field-label}

Oops! Can\'t lookup your product right now [](#)
:::

------------------------------------------------------------------------

::: method
[]{#getWeatherForecast}

::: method-path
[Up](#__Methods){.up}

``` get
get /Example
```
:::

::: method-summary
Рандомайзер погоды ([getWeatherForecast]{.nickname})
:::

::: method-notes
:::

### Query parameters {#query-parameters .field-label}

::: field-items
::: param
id (optional)
:::

::: param-desc
[Query Parameter]{.param-type} --- Рандомный параметр format: int32
:::
:::

### Return type {#return-type-9 .field-label}

::: return-type
array\[[WeatherForecast](#WeatherForecast)\]
:::

### Example data {#example-data-9 .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
[ {
  "date" : {
    "dayOfWeek" : 5,
    "month" : 6,
    "year" : 0,
    "dayOfYear" : 5,
    "dayNumber" : 2,
    "day" : 1
  },
  "summary" : "summary",
  "temperatureC" : 7,
  "temperatureF" : 9
}, {
  "date" : {
    "dayOfWeek" : 5,
    "month" : 6,
    "year" : 0,
    "dayOfYear" : 5,
    "dayNumber" : 2,
    "day" : 1
  },
  "summary" : "summary",
  "temperatureC" : 7,
  "temperatureF" : 9
} ]
```

### Produces {#produces-11 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-11 .field-label}

#### 200 {#section-29 .field-label}

Success
:::

------------------------------------------------------------------------

# [Map]{#Map}

::: method
[]{#getAllVendingMachneInformation}

::: method-path
[Up](#__Methods){.up}

``` get
get /Map
```
:::

::: method-summary
Выдать полный список всех доступных автоматов
([getAllVendingMachneInformation]{.nickname})
:::

::: method-notes
:::

### Return type {#return-type-10 .field-label}

::: return-type
array\[[VendingMachine](#VendingMachine)\]
:::

### Example data {#example-data-10 .field-label}

::: example-data-content-type
Content-Type: application/json
:::

``` example
[ {
  "numberOfEmptyCells" : 6,
  "address" : "address",
  "numberOfCellsWBlankets" : 0,
  "latitude" : 5.962133916683182,
  "description" : "description",
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "longitude" : 1.4658129805029452
}, {
  "numberOfEmptyCells" : 6,
  "address" : "address",
  "numberOfCellsWBlankets" : 0,
  "latitude" : 5.962133916683182,
  "description" : "description",
  "id" : "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
  "longitude" : 1.4658129805029452
} ]
```

### Produces {#produces-12 .field-label}

This API call produces the following media types according to the
[Accept]{.header} request header; the media type will be conveyed by the
[Content-Type]{.header} response header.

-   `text/plain`
-   `application/json`
-   `text/json`

### Responses {#responses-12 .field-label}

#### 200 {#section-30 .field-label}

Success
:::

------------------------------------------------------------------------

## [Models]{#__Models}

\[ Jump to [Methods](#__Methods) \]

### Table of Contents

1.  [`ActiveBlanket`](#ActiveBlanket)
2.  [`Client`](#Client)
3.  [`DateOnly`](#DateOnly)
4.  [`DayOfWeek`](#DayOfWeek)
5.  [`PaymentTariff`](#PaymentTariff)
6.  [`ProblemDetails`](#ProblemDetails)
7.  [`Product`](#Product)
8.  [`VendingMachine`](#VendingMachine)
9.  [`WeatherForecast`](#WeatherForecast)

::: model
### [`ActiveBlanket`]{#ActiveBlanket} [Up](#__Models){.up}

::: model-description
Плед взятый в данный момент в аренду
:::

::: field-items
::: param
id (optional)
:::

::: param-desc
[[UUID](#UUID)]{.param-type} GUID активного пледа format: uuid
:::

::: param
dataOfIssue (optional)
:::

::: param-desc
[[Date](#DateTime)]{.param-type} ДатаВремя выдачи format: date-time
:::

::: param
paymentTariff (optional)
:::

::: param-desc
[[PaymentTariff](#PaymentTariff)]{.param-type}
:::
:::
:::

::: model
### [`Client`]{#Client} [Up](#__Models){.up}

::: model-description
Аккаунт клиента
:::

::: field-items
::: param
id (optional)
:::

::: param-desc
[[UUID](#UUID)]{.param-type} GUID клиента format: uuid
:::

::: param
phoneNumber (optional)
:::

::: param-desc
[[Long](#long)]{.param-type} Номер телефона клиента format: int64
:::

::: param
email (optional)
:::

::: param-desc
[[String](#string)]{.param-type} E-mail
:::

::: param
dateOfRegistration (optional)
:::

::: param-desc
[[Date](#DateTime)]{.param-type} Дата регистрации format: date-time
:::

::: param
activeBlankets (optional)
:::

::: param-desc
[[array\[ActiveBlanket\]](#ActiveBlanket)]{.param-type} Пледы
находящиеся в аренде
:::
:::
:::

::: model
### [`DateOnly`]{#DateOnly} [Up](#__Models){.up}

::: field-items
::: param
year (optional)
:::

::: param-desc
[[Integer](#integer)]{.param-type} format: int32
:::

::: param
month (optional)
:::

::: param-desc
[[Integer](#integer)]{.param-type} format: int32
:::

::: param
day (optional)
:::

::: param-desc
[[Integer](#integer)]{.param-type} format: int32
:::

::: param
dayOfWeek (optional)
:::

::: param-desc
[[DayOfWeek](#DayOfWeek)]{.param-type}
:::

::: param
dayOfYear (optional)
:::

::: param-desc
[[Integer](#integer)]{.param-type} format: int32
:::

::: param
dayNumber (optional)
:::

::: param-desc
[[Integer](#integer)]{.param-type} format: int32
:::
:::
:::

::: model
### [`DayOfWeek`]{#DayOfWeek} [Up](#__Models){.up}

::: field-items
:::
:::

::: model
### [`PaymentTariff`]{#PaymentTariff} [Up](#__Models){.up}

::: field-items
::: param
id (optional)
:::

::: param-desc
[[UUID](#UUID)]{.param-type} format: uuid
:::

::: param
name (optional)
:::

::: param-desc
[[String](#string)]{.param-type}
:::

::: param
description (optional)
:::

::: param-desc
[[String](#string)]{.param-type}
:::

::: param
price (optional)
:::

::: param-desc
[[Double](#double)]{.param-type} format: double
:::
:::
:::

::: model
### [`ProblemDetails`]{#ProblemDetails} [Up](#__Models){.up}

::: field-items
:::
:::

::: model
### [`Product`]{#Product} [Up](#__Models){.up}

::: field-items
::: param
name (optional)
:::

::: param-desc
[[String](#string)]{.param-type} The name of the product
:::

::: param-desc
[example: Men\'s basketball shoes]{.param-type}
:::

::: param
availableStock (optional)
:::

::: param-desc
[[Integer](#integer)]{.param-type} Quantity left in stock format: int32
:::

::: param-desc
[example: 10]{.param-type}
:::

::: param
sizes (optional)
:::

::: param-desc
[[array\[String\]](#string)]{.param-type} The sizes the product is
available in
:::

::: param-desc
[example: \[\"Small\",\"Medium\",\"Large\"\]]{.param-type}
:::
:::
:::

::: model
### [`VendingMachine`]{#VendingMachine} [Up](#__Models){.up}

::: field-items
::: param
id (optional)
:::

::: param-desc
[[UUID](#UUID)]{.param-type} GUID аппарата format: uuid
:::

::: param
numberOfCellsWBlankets (optional)
:::

::: param-desc
[[Integer](#integer)]{.param-type} Количество пледов готовых к выдаче
format: int32
:::

::: param
numberOfEmptyCells (optional)
:::

::: param-desc
[[Integer](#integer)]{.param-type} Количество ячеек для возврата format:
int32
:::

::: param
longitude (optional)
:::

::: param-desc
[[Double](#double)]{.param-type} Долгота format: double
:::

::: param
latitude (optional)
:::

::: param-desc
[[Double](#double)]{.param-type} Широта format: double
:::

::: param
description (optional)
:::

::: param-desc
[[String](#string)]{.param-type} Полное описание местоположения автомата
:::

::: param
address (optional)
:::

::: param-desc
[[String](#string)]{.param-type} Краткое описание местоположения
:::
:::
:::

::: model
### [`WeatherForecast`]{#WeatherForecast} [Up](#__Models){.up}

::: field-items
::: param
date (optional)
:::

::: param-desc
[[DateOnly](#DateOnly)]{.param-type}
:::

::: param
temperatureC (optional)
:::

::: param-desc
[[Integer](#integer)]{.param-type} format: int32
:::

::: param
temperatureF (optional)
:::

::: param-desc
[[Integer](#integer)]{.param-type} format: int32
:::

::: param
summary (optional)
:::

::: param-desc
[[String](#string)]{.param-type}
:::
:::
:::
