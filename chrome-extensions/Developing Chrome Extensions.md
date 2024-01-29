<p><a target="_blank" href="https://app.eraser.io/workspace/YZcxjIfmFRHyEmWyogm3" id="edit-in-eraser-github-link"><img alt="Edit in Eraser" src="https://firebasestorage.googleapis.com/v0/b/second-petal-295822.appspot.com/o/images%2Fgithub%2FOpen%20in%20Eraser.svg?alt=media&amp;token=968381c8-a7e7-472a-8ed6-4a6626da5501"></a></p>

```
В Chrome расширениях данные передаются и хранятся с помощью нескольких методов и API. 

## Передача сообщений

Передача сообщений является основным способом обмена данными между различными компонентами расширения, такими как фоновые скрипты, скрипты содержимого и всплывающие скрипты[8]. Это можно сделать с помощью методов `chrome.runtime.sendMessage` и `chrome.runtime.connect`[2][5]. 

Пример кода для отправки сообщения:

```javascript
chrome.runtime.sendMessage({greeting: "hello"}, function(response) {
  console.log(response.farewell);
});
```

Пример кода для прослушивания сообщений:

```javascript
chrome.runtime.onMessage.addListener(
  function(request, sender, sendResponse) {
    if (request.greeting === "hello")
      sendResponse({farewell: "goodbye"});
  });
```

## Хранение данных

API `chrome.storage` предоставляет способ сохранения пользовательских данных и состояния, специфичных для расширения[3]. Это асинхронный API с операциями массового чтения и записи. Данные сохраняются даже если пользователь очищает кэш и историю просмотров. 

Пример кода для сохранения данных:

```javascript
chrome.storage.sync.set({key: "value"}, function() {
  console.log('Value is set to ' + "value");
});
```

Пример кода для чтения данных:

```javascript
chrome.storage.sync.get(['key'], function(result) {
  console.log('Value currently is ' + result.key);
});
```

## Взаимодействие с веб-страницами

Расширения Chrome также могут взаимодействовать с веб-страницами. Они могут получать и отвечать на сообщения от других веб-страниц, но не могут отправлять сообщения на веб-страницы. Для отправки сообщений с веб-страницы в расширение, в файле `manifest.json` расширения необходимо указать, с какими веб-сайтами вы хотите общаться, используя ключ "externally_connectable"[2][11].

Важно отметить, что при работе с данными в расширениях Chrome необходимо учитывать вопросы безопасности. Например, при передаче сообщений ваши скрипты должны быть осторожны, чтобы не стать жертвой межсайтового скриптинга[5]. Кроме того, при хранении данных, таких как API-токены, важно использовать безопасные методы хранения[12].

Citations:
[1] https://dl.acm.org/doi/abs/10.1145/3460120.3484745
[2] https://developer.chrome.com/docs/extensions/develop/concepts/messaging
[3] https://developer.chrome.com/docs/extensions/reference/api/storage
[4] https://chrome.google.com/webstore/detail/flowcontrol/gjgnnpogleklcieniomjfmoiklekedcm
[5] https://developer.chrome.com/docs/extensions/mv2/messaging
[6] https://developer.chrome.com/docs/extensions/develop/concepts/storage-and-cookies
[7] https://developer.chrome.com/docs/extensions/develop
[8] https://www.linkedin.com/pulse/message-passing-chrome-extension-lakebrains-technologies
[9] https://stackoverflow.com/questions/5364062/how-can-i-save-information-locally-in-my-chrome-extension
[10] https://blog.taboola.com/optimising-chrome-extensions-part-2/
[11] https://stackoverflow.com/questions/11431337/sending-message-to-chrome-extension-from-a-web-page
[12] https://www.reddit.com/r/javascript/comments/8txe2q/how_to_securely_store_an_api_token_in_a_chrome/?rdt=37495
[13] https://chrome.google.com/webstore/detail/eadashboardhelper/dgkfkmoaonlhfajkpfjcdiioigckfhgl
[14] https://www.reddit.com/r/chrome_extensions/comments/148b3la/message_passing_not_working_with_the_sidepanel/?rdt=35719
[15] https://davidwalsh.name/chrome-extension-storage
[16] https://cloud.google.com/dataflow/docs/reference/sql/streaming-extensions
[17] https://www.freecodecamp.org/news/chrome-extension-message-passing-essentials/
[18] https://github.com/topics/chrome-storage-api
[19] https://github.com/Aurore54F/DoubleX
[20] http://www.dre.vanderbilt.edu/~schmidt/android/android-4.0/external/chromium/chrome/common/extensions/docs/messaging.html
[21] https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/API/storage
[22] https://cloud.google.com/dataflow
[23] https://www.youtube.com/watch?v=kA3ICP_ciEQ
[24] https://developers.google.com/privacy-sandbox/3pcd/storage-partitioning
```
```

```
# 
1. Abstact Q/A flow 


# 



<!--- Eraser file: https://app.eraser.io/workspace/YZcxjIfmFRHyEmWyogm3 --->