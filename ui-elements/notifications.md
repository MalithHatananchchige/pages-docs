# Notifications

Use Pages Notification plugin that has been custom-made to suit overall theme, to add unique notifications of various styles

Show a sliding bar from top or bottom that fits the screen width

```markup
<script>
$(document).ready(function() {
    // Apply the plugin to the body 
   $('body').pgNotification(options).show();
});
</script>
```

## **Options**

| `NAME` | `TYPE` | `DEFAULT` | `DESCRIPTION` |
| :--- | :--- | :--- | :--- |
| style | string | 'simple' | Sets the style of the notification. Styles available are 'bar', 'flip', 'circle', 'simple' |
| message | string | null | Message to be displayed inside the notification. |
| position | string | 'top-right' | Where to place the notification. Positions available are:topbottomtop-righttop-leftbottom-rightbottom-leftNote: Use 'top' and 'bottom' only for positioning 'bar' notification |
| type | string | 'info' | Sets the type of the notification - 'info', 'warning', 'success', 'danger'.Changing the type will change the background color and font color of the notification |
| showClose | boolean | true | Show/Hide the close button |
| timeout | number | 4000 | Decides for how long the notification should be visible on the screen in miliseconds. Setting timeout `0` will keep notification forever. |
| onShown | function | null | Callback function fired after the notification is shown |
| onClose | function | null | Callback function fired after the notification is closed |
| title | string | null | Only available for style 'circle'. Sets the title of the notification |
| thumbnail | string | null | Only available for style 'circle'. Shows a thumbnail image together with the messageAny `img` can be passed. The following structure is recommended`<img width="40" height="40" style="display: inline-block;" src="assets/img/profiles/avatar2x.jpg" data-src="assets/img/profiles/avatar.jpg" data-src-retina="assets/img/profiles/avatar2x.jpg" alt="">` |

