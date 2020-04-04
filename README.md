# project-starter-docs
This docs contains the simple way to start simple project.

# Laravel Typescript React
package.json
```
{
    ...
    "devDependencies": {
        ...
        "@babel/preset-react": "^7.9.4",
        "@types/react": "^16.9.0",
        "@types/react-dom": "^16.9.0",
        "react": "^16.13.1",
        "react-dom": "^16.13.1",
        "ts-loader": "^6.2.2",
        "typescript": "~3.7.2",
    }
}
```
resources/js/app.js -> app.tsx
```js
/**
 * First we will load all of this project's JavaScript dependencies.
 */
require('./bootstrap');

import React from 'react'
import ReactDOM from 'react-dom'
import App from './components/App'

/**
 * Next, we will create a fresh javascript application instance and attach it to DOM
 */
if (document.getElementById('app')) {
    ReactDOM.render(<App />, document.getElementById('app'))
}
```
resources/js/components/App.tsx
```js
import React from 'react'
import Button from './Button'

export default function App() {
    return (
        <div>
            Typescript React App
        </div>
    )
}
```
webpack.mix.js
```js
mix.ts('resources/js/app.tsx', 'public/js')
   .sass('resources/sass/app.scss', 'public/css');
```
views/welcome.blade.php
```html
<div id="app"></div>
<script src="/js/app.js"></script>
```
After that just run the following command.
```
npm install
npm run watch-poll
```
