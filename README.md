
# Dialogflow Fulfillment: Node.js Weather RU

## Установка Dialogflow и Fulfillment
Выберите **только один** из вариантов ниже.

### Вариант 1: Добавить в Dialogflow (Рекомендуется)
Для того что-бы создать этого агента по нашему шаблону:

<a href="https://console.dialogflow.com/api-client/oneclick?templateUrl=https://oneclickgithub.appspot.com/dialogflow/fulfillment-weather-nodejs&agentName=WeatherSample" target="blank">
  <img src="https://dialogflow.com/images/deploy.png">
</a>

1. Получите  ключ WWO Local Weather REST API в https://developer.worldweatheronline.com/api/
2. Замените <ENTER_WWO_API_KEY_HERE> своим WWO API ключом в 20-ой строке: `functions/index.js`
3. Выберите **Deploy**.
4. В Dialogflow Console > **Settings** ⚙ > выберите **Google Cloud** в разделе Project ID. В Google Cloud Platform > **menu** ☰ > **Enable Billing**.

### Вариант 2: Firebase CLI
1. Создайте [Dialogflow Agent](https://console.dialogflow.com/)
2. `git clone https://github.com/themurka/dialogflow-weather-ru-nodejs.git`
3. В консоли Dialogflow под **Settings** ⚙ > [Restore from Zip](https://dialogflow.com/docs/agents#export_and_import) используй `weather-agent.zip` в данной директории.
4. Получи ключ WWO Local Weather REST API в https://developer.worldweatheronline.com/api/
5. Замените <ENTER_WWO_API_KEY_HERE> на свой WWO API ключ на 20 строке:`functions/index.js`
6. `cd`перейдите в `functions`
7. Запустите `npm install`
8. Установите Firebase CLI с помощью `npm install -g firebase-tools`
9. Авторизуйтесь в своём Google Account с помощью `firebase login`
10. Добавьте свой проект в образец с помощью `firebase use [project ID]`
      + В Dialogflow console под **Settings** ⚙ > **General** tab > скопируйте **Project ID**.
11. Запустите `firebase deploy --only functions:dialogflowFulfillmentLibAdvancedSample`
12. После успешной загрузки, посетите **Project Console** ссылка > **Functions** > **Dashboard**
      + Скопируйте ссылку под столбцом событий.
      + Пример: `https://us-central1-<PROJECTID>.cloudfunctions.net/<FUNCTIONNAME>`
13. Вернитесь Dialogflow Console > **Fulfullment** > **Enable** Webhook.
14. Вставьте URL-адрес из столбца событий консоли Firebase в **URL** поле > **Save**.
15. В Dialogflow Console > **Settings** ⚙ > выберите **Google Cloud** ссылка в Project ID раздел. В Google Cloud Platform > **menu** ☰ > **Enable Billing**.

Для Fulfillment Webhook [JSON Requests & Responses](https://github.com/dialogflow/fulfillment-webhook-json).

## References & Issues
+ Остались вопросы? Добро пожаловать в [StackOverflow](https://stackoverflow.com/questions/tagged/dialogflow) или [Dialogflow Developer Community](https://plus.google.com/communities/103318168784860581977).
+ Если нашли баг, пожалуйста отпишите в [Github](https://github.com/dialogflow/dialogflow-fulfillment-nodejs/issues).
+ Dialogflow [Documentation](https://docs.dialogflow.com).
+ Dialogflow [Classes Reference Doc](https://github.com/dialogflow/dialogflow-fulfillment-nodejs/tree/master/docs).
+ Дополнительная информация [billing](https://dialogflow.com/docs/concepts/google-projects-faq).

## Make Contributions
Пожалуйста, прочитайте и следуйте инструкциям в CONTRIBUTING.md.

## License
Почитайте LICENSE.md.
