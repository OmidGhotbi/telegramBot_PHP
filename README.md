# telegramBot_PHP
PHP class for telegram bots working on webhooks

##Использование
```php
include("botClass.php");
$bot = new Bot($token); //$token - токен выданный BotFather

$message = $bot->incomingText();
```

##Методы
####setWebhook
```php
$bot->setWebHook([handler-url]);
```

Для того, чтобы бот мог реагировать на действия собеседника необходимо повесить на него хук. Ссылка должна вести на домен с валидным SSL сертификатом. Этот метод нужно использовать один раз, в самом начале. Чтобы убрать хук, достаточно вместо ссылки указать пустую строку.

*Выводит на экран результат установки хука*

###incomingText
```php
$bot->incomingText();
```

*Получает входящий текст целиком*

###getMethod
```php
$bot->getMethod();
```

Получение метода (т.е. команды, начинающийся с "/").

*Получает входящую команду: например "/help test" вернёт "help"*

###getMethodText
```php
$bot->getMethodText();
```

Получение текста метода (т.е. атрибута команды).

*Получает атрибут входящей команды: например "/help test" вернёт "test"*
