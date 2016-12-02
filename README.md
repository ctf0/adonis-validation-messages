# adonis-validation-messages
custom validation msgs instead of the default `{{validation}} validation failed on {{field}}`

## Usage (until its added to core)

```js
const Helpers = use('Helpers')

let data = request.all();
let rules = {
    // ...
};

const fs = require('fs');
const file = Helpers.resourcesPath('locales/en/validation.json')
const messages = JSON.parse(fs.readFileSync(file, 'utf8'));

const validation = yield Validator.validateAll(data, rules, messages);

```
