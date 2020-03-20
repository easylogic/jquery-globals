# jquery-globals

jquery helper library to using in esm module 

# install 

```
npm install jquery @easylogic/jquery-globals
```


# not woking in webpack 

```js
new webpack.ProvidePlugin({
    $: "jquery",
    jQuery: "jquery",
    "window.jQuery": "jquery"
})  
```

```js
import $ from 'jquery'
window.jQuery = $ 
import 'summernote/dist/lang/summernote-ko-KR'; 
```

# Use jquery-globals  

You don't need webpack.ProviderPlugin anymore.

```js
import 'jquery-globals'
import 'summernote/dist/lang/summernote-ko-KR'; 
```


