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

This is because the `import` statement is executed before the actual statement.

So build result is below code 

```js
import $ from 'jquery'
import 'summernote/dist/lang/summernote-ko-KR';   // not working 
window.jQuery = $ 
```

# Use jquery-globals  

You don't need webpack.ProviderPlugin anymore.

```js
import 'jquery-globals'
import 'summernote/dist/lang/summernote-ko-KR'; 
```


