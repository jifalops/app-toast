[![Published on Vaadin  Directory](https://img.shields.io/badge/Vaadin%20Directory-published-00b4f0.svg)](https://vaadin.com/directory/component/jifalopsapp-toast)
[![Stars on vaadin.com/directory](https://img.shields.io/vaadin-directory/star/jifalopsapp-toast.svg)](https://vaadin.com/directory/component/jifalopsapp-toast)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/jifalops/app-toast)

# app-toast
A swipeable, actionable, and themable paper-toast.

## Installation
```
bower i -S app-toast        # Polymer 2.0 hybrid (1.x compatible)
bower i -S app-toast#0.2.3  # Polymer 1.x based
```

## Usage
* Drop `app-toast` in and call the `show()` method.
* Use [app-toasts](https://www.webcomponents.org/element/jifalops/app-toasts)
  for preset themes.

## Demo
<!--
```
<custom-element-demo height="300">
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="app-toast.html">
    <custom-style>
      <style is="custom-style">
        app-toast.styled {
          --app-toast: {
            color: red;
            background-color: #888;
          };
          --app-toast-button: {
            color: blue;
          };
          --app-toast-main-icon: {
            color: green;
          };
          --app-toast-main-icon-stroke-color: orange;
          --app-toast-cancel-icon: {
            color: purple;
          };
        }
      </style>
    </custom-style>
    <next-code-block></next-code-block>
    <script>
      var toast = document.getElementById('toast');
      var icon = document.getElementById('icon');
      var text = document.getElementById('text');
      var duration = document.getElementById('duration');
      var actionText = document.getElementById('actionText');
      var showCancel = document.getElementById('showCancel');
      var disableSwipe = document.getElementById('disableSwipe');
      var fitBottom = document.getElementById('fitBottom');
      var styled = document.getElementById('styled');
      var feedback = document.getElementById('feedback');
      function showToast() {
        var tmp = icon.options[icon.selectedIndex].text;
        toast.icon = tmp == 'No icon' ? '' : tmp;
        toast.text = text.value;
        toast.duration = Number(duration.value);
        toast.actionText = actionText.value;
        toast.showCancel = showCancel.checked;
        toast.disableSwipe = disableSwipe.checked;
        toast.fitBottom = fitBottom.checked;
        toast.onAction = function() { feedback.innerText = "onAction()"; };
        toast.onCancel = function() { feedback.innerText = "onCancel()"; };
        if (styled.checked) toast.classList.add('styled');
        else toast.classList.remove('styled');
        toast.show();
      }
    </script>
  </template>
</custom-element-demo>
```
-->

```html
<app-toast id="toast"></app-toast>
<select id="icon">
  <option>No icon</option>
  <option selected>check-circle</option>
  <option>check</option>
  <option>check-box</option>
  <option>info</option>
  <option>info-outline</option>
  <option>warning</option>
  <option>error</option>
  <option>error-outline</option>
</select><br/>
<input id="text" placeholder="text" value="text"/><br/>
<input id="duration" placeholder="duration (ms)" value="3000"/><br/>
<input id="actionText" placeholder="action button text" value="action"/><br/>
<label><input id="showCancel" type="checkbox"/>Show cancel</label><br/>
<label><input id="disableSwipe" type="checkbox"/>Disable swipe</label><br/>
<label><input id="fitBottom" type="checkbox"/>Fit to bottom</label><br/>
<label><input id="styled" type="checkbox"/>Styled</label><br/>
<button onclick="showToast()">Show</button>&nbsp;
<button onclick="toast.close()">Close</button><br/>
Last Event: <span id="feedback"></span>
```

Full demo:
[webcomponents.org](https://www.webcomponents.org/element/jifalops/app-toast/demo/demo/index.html)
| [github](https://jifalops.github.io/app-toast/components/app-toast/demo/).

API: [webcomponents.org](https://www.webcomponents.org/element/jifalops/app-toast/app-toast)

## Contributing

1. Fork it on Github.
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## License

[MIT](https://opensource.org/licenses/MIT)
