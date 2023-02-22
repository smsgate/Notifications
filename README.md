# Содержание

* [Входящее сообщение от абонента Viber](https://github.com/smsgate/Notifications/blob/master/README.md#)

# Входящее сообщение от абонента Viber

На ваш URL будет отправлено JSON запрос.
Заголовки отправляемых данных должны содержать:
```
Content-Type: application/json; charset=utf-8
```
Кодировка JSON документов UTF-8.

# Пример JSON запроса:
```{
  "message_id": "123456",
  "channel": "viber",
  "timestamp": "2023-01-01 09:00:00",
  "recipient_response": {
    "recipient": {
      "phone": 79001234567
    },
    "from": "TEST",
    "content": {
      "type": "text",
      "text": "Ответ на сообщение"
    }
  }
}```

Где:
* **message_id** – Идентификатор сообщения в системе.;
* **channel** – Канал отправки. Всегда "viber";
* **timestamp** – Время входящего сообщения, по часовому поясу +0 (GMT);
* **recipient_response**
	* **recipient**
	    * **phone** – Номер телефона абонента, от которого поступило входящее сообщение;
	* **from** – Имя отправителя которому отвечает абонент;
	* **content**
	    * **type** – Тип входящего сообщения. "text" - текстовое сообщение;
	    * **text** – Текст входящего сообщения.
