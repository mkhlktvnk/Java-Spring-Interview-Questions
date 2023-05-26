# WireMock

## Что такое WireMock и для чего он используется?
WireMock - это библиотека для создания стабов HTTP-серверов в Java-приложениях. Она используется для имитации внешних сервисов или API, чтобы эмулировать различные сценарии и проверить взаимодействие приложения с внешними системами.

## Что представляет собой WireMockServer?
WireMockServer представляет собой класс в библиотеке WireMock, который предоставляет функциональность для запуска и управления фейковым HTTP-сервером. Он позволяет создавать и настраивать фейковые эндпоинты, устанавливать ожидаемые запросы и ответы, а также запускать и останавливать сервер. WireMockServer позволяет эмулировать внешние сервисы или API в тестовых сценариях и проверять взаимодействие приложения с ними.

## Каким образом WireMock обрабатывает запросы и отвечает на них?
WireMock обрабатывает запросы, сравнивая их с заранее определенными ожидаемыми запросами. Если полученный запрос соответствует ожидаемому, WireMock возвращает заранее определенный ответ. В противном случае, если запрос не соответствует ни одному ожидаемому, WireMock может возвращать стандартный ответ, например, с кодом ошибки или пустым телом.

## Как создать стаб-сервер с использованием WireMock?
Для создания стаб-сервера с использованием WireMock в Java необходимо выполнить следующие шаги:

1. Создать экземпляр WireMockServer:

```java
WireMockServer wireMockServer = new WireMockServer();
```

2. Настроить ожидаемые запросы и ответы:

```java
WireMock.configureFor("localhost", 8080); // Настройка хоста и порта
WireMock.stubFor(
    WireMock.get(WireMock.urlEqualTo("/api/users"))
        .willReturn(WireMock.aResponse()
            .withStatus(200)
            .withHeader("Content-Type", "application/json")
            .withBody("{\"id\": 1, \"name\": \"John\"}"))
);
```

3. Запустить сервер:

```java
wireMockServer.start();
```

4. Остановить сервер после завершения тестов:

```java
wireMockServer.stop();
```

## Как можно задать ожидаемый HTTP-запрос для WireMock и какие параметры могут быть проверены?

1. Метод запроса (`GET`, `POST`, `PUT`, и т.д.) и его путь:
```java
WireMock.get(WireMock.urlEqualTo("/api/users"))
```

2. Заголовки запроса:
```java
WireMock.get(WireMock.urlEqualTo("/api/users"))
    .withHeader("Content-Type", WireMock.equalTo("application/json"))
```

3. Параметры запроса:
```java
WireMock.get(WireMock.urlPathEqualTo("/api/users"))
    .withQueryParam("page", WireMock.equalTo("1"))
```

4. Тело запроса:
```java
WireMock.post(WireMock.urlEqualTo("/api/users"))
    .withRequestBody(WireMock.equalToJson("{\"name\": \"John\"}"))
```

## Какие методы API WireMock могут быть использованы для определения ожидаемого ответа от сервера?

1. Установка статуса ответа:
```java
WireMock.aResponse().withStatus(200)
```

2. Установка заголовков ответа:
```java
WireMock.aResponse().withHeader("Content-Type", "application/json")
```

3. Установка тела ответа:
```java
WireMock.aResponse().withBody("{\"id\": 1, \"name\": \"John\"}")
```

4. Установка задержки ответа:
```java
WireMock.aResponse().withFixedDelay(2000)
```

5. Установка файла в качестве тела ответа:
```java
WireMock.aResponse().withBodyFile("response.json")
```

## Какие возможности есть для настройки динамических ответов от WireMock, например, генерация случайных данных или использование переменных?
WireMock предлагает несколько возможностей для настройки динамических ответов:

1. Генерация случайных данных: WireMock позволяет генерировать случайные данные в ответе, такие как случайные числа, строки или UUID. Это может быть полезно при тестировании сценариев, где требуется разнообразие данных.

2. Использование переменных: WireMock позволяет использовать переменные в ожидаемых запросах и ответах. Это позволяет создавать более гибкие и параметризованные сценарии тестирования. Например, можно использовать переменные для динамического формирования URL или заголовков.

3. Вычисления на основе запроса: WireMock позволяет выполнять вычисления или логику на основе полученного запроса и использовать их для формирования ответа. Например, можно использовать значения из запроса для генерации динамического тела ответа.

Пример использования генерации случайных данных:
```java
WireMock.stubFor(
    WireMock.get(WireMock.urlEqualTo("/api/users"))
        .willReturn(WireMock.aResponse()
            .withStatus(200)
            .withBody("{\"id\": \"${randomValue}\"}"))
);
```

Пример использования переменных:
```java
WireMock.stubFor(
    WireMock.get(WireMock.urlEqualTo("/api/users/${userId}"))
        .willReturn(WireMock.aResponse()
            .withStatus(200)
            .withBody("{\"id\": \"${userId}\", \"name\": \"John\"}"))
);
```

## Как можно настроить WireMock для выполнения проверок наличия запросов и их параметров?

1. Проверка наличия запросов: WireMock позволяет проверять, был ли выполнен ожидаемый запрос или нет. Если запрос не был выполнен, это может указывать на непредвиденное взаимодействие или ошибку в тестовом сценарии.

```java
WireMock.verify(WireMock.getRequestedFor(WireMock.urlEqualTo("/api/users")));
```

2. Проверка параметров запроса: WireMock позволяет проверять значения параметров запроса, таких как пути, заголовки или параметры URL. Это полезно для убеждения в правильности передаваемых данных.

```java
WireMock.verify(WireMock.getRequestedFor(WireMock.urlEqualTo("/api/users"))
    .withQueryParam("page", WireMock.equalTo("1")));
```
