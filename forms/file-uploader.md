---
description: Pages Drag and Drop File Uploader
---

# File Uploader

pg-upload is a fork of [NG-ZORRO](https://github.com/NG-ZORRO/ng-zorro-antd) implementation of Dropzone Initial credits go to the author

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgUploadModule } from '../@pages/components/upload/upload.module';
@NgModule({
  imports: [pgUploadModule,...]
})
export class AppModule(){}
```

## How to use 

Basic Select with Search

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-upload
    Type="drag"
    [Multiple]="true"
    [Limit]="2"
    Action="https://jsonplaceholder.typicode.com/posts/"
    (Change)="handleChange($event)"
    extraClass="dropzone"
    progressType="circle"
    >
    <div class="d-flex flex-column align-items-center">
    <h4 class="semi-bold no-margin">Drop files to Upload</h4>
    <p>or click here</p>
    </div>
</pg-upload>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
 //Fileupload HandleChange 

 handleChange(event){ }
```
{% endtab %}
{% endtabs %}

## API

{% hint style="info" %}
The server upload interface implementation can refer to [jQuery-File-Upload](https://github.com/blueimp/jQuery-File-Upload/wiki) .
{% endhint %}

| parameter | Instructions | Types of | Defaults |
| :--- | :--- | :--- | :--- |
| Accept | Accepted upload file types, see [input accept Attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-accept) | string | no |
| Action | Required parameters, uploaded address | string | no |
| BeforeUpload | Before uploading files hooks, parameters for the uploaded files, if returned to`false`stop uploading. Note: **IE9** does not support this method. Note: Be sure what `=>`the definition of treatment. | \(file, fileList\) =&gt; `boolean | Observable<boolean>` | no |
| CustomRequest | By overriding the default upload behavior, you can customize your own upload implementation. Note: Be sure what `=>`the definition of treatment. | \(item\) =&gt; `Subscription` | no |
| Data | Upload the required parameters or return upload methods. Note: Be sure what`=>`the definition of treatment. | Object \| \(\(file: UploadFile\) =&gt; Object\) | no |
| Disabled | Is it disabled | boolean | false |
| FileList | File list, two-way binding | UploadFile\[\] | no |
| Limit | Limit the maximum number of single uploads, `Multiple`valid when opened;`0`unlimited | number | 0 |
| FileType | Limit the file type, for example:`image/png,image/jpeg,image/gif,image/bmp` | string | no |
| Filter | Custom filter | UploadFilter\[\] | no |
| Headers | Set upload request header, above IE10 | object | no |
| ListType | Upload list of built-in styles, support three basic styles `text`,`picture`and`picture-card` | string | 'text' |
| Multiple | Whether to support multiple-choice files, `IE10+`support. After opening, hold down ctrl to select multiple files. | boolean | false |
| Name | File parameter names sent to the background | string | 'file' |
| ShowUploadList | Whether to display the list, can be set as an object for individually setting showPreviewIcon and showRemoveIcon | Boolean or { showPreviewIcon?: boolean, showRemoveIcon?: boolean } | true |
| ShowButton | Whether to display the upload button | boolean | true |
| WithCredentials | Whether to carry a cookie when uploading a request | boolean | false |
| Preview | Clickback when clicking on a file link or preview icon. Note: Be sure what `=>`the definition of treatment. | \(file: UploadFile\) =&gt; void | no |
| Remove | Click on the callback when the file is removed. If the return value is false, it will not be removed. Support for returning Observable&lt;boolean&gt; objects. Note: Be sure what `=>`the definition of treatment. | \(file: UploadFile\) =&gt; boolean \| Observable&lt;boolean&gt; | no |
| \(Change\) | Callback when upload file status changes | EventEmitter |  |

