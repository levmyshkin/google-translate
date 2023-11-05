# Google Translate service

It's a Drupal library for getting translation from Node.js service.
It depends on iamtraction/google-translate npm package:
https://www.npmjs.com/package/@iamtraction/google-translate
https://github.com/iamtraction/google-translate

## Installation and run Node.js service

Run these commands:
```
npm install
npm start
```

## Usage

See Translator.postman_collection.json with POST request:
http://localhost:8000

Langcodes must be ISO-639 codes:
https://cloud.google.com/translate/docs/languages

with x-www-form-urlencoded data:
translateText: Hello
translateFrom: en
translateTo: ru

## Run node.js service in background

You can run translation node.js service in background or even on
system start up:
```
npm install pm2@latest -g
yarn global add pm2
pm2 start index.js
```

More info about PM2:
https://pm2.keymetrics.io/

### Saving the app list to be restored at reboot.

Once you have started all desired apps, save the app list,
so it will respawn after reboot:
```
pm2 save
```
