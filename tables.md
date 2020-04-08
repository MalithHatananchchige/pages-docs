# Tables / Datatables

Tables and Datatables are powered by the famous ngx-datatable plugin. Please refer there documentation for more details. [https://github.com/swimlane/ngx-datatable](https://github.com/swimlane/ngx-datatable)

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { NgxDatatableModule } from '@swimlane/ngx-datatable';
@NgModule({
  imports: [NgxDatatableModule,...]
})
export class AppModule(){}
```

## How to use 

Simple table example. 

{% hint style="info" %}
More examples can be found in `angular/src/app/tables/advance` and  `angular/src/app/tables/simple` pages
{% endhint %}

{% tabs %}
{% tab title="HTML" %}
```markup
<ngx-datatable
class='table table-hover'
[rows]="basic_table_data"
[columnMode]="'force'"
[headerHeight]="43"
[footerHeight]="50"
[rowHeight]="'auto'"
[limit]="5"
[selected]="selected"
[selectionType]="'checkbox'"
(activate)="onActivate($event)"
(select)='onSelect($event)'>
<ngx-datatable-column [width]="30" [sortable]="false" [canAutoResize]="false" [draggable]="false" [resizeable]="false" cellClass="d-flex align-items-center">
    <ng-template ngx-datatable-header-template let-value="value" let-allRowsSelected="allRowsSelected" let-selectFn="selectFn">
        <button class="btn btn-link"><i class="pg pg-trash"></i>
        </button>
    </ng-template>
    <ng-template ngx-datatable-cell-template let-rowIndex="rowIndex" let-row="row" let-value="value" let-isSelected="isSelected" let-onCheckboxChangeFn="onCheckboxChangeFn">
    <div class="checkbox d-flex align-items-center">
        <input type="checkbox" value="1" id="checkbox_1{{rowIndex}}"  [checked]="isSelected" (change)="onCheckboxChangeFn($event)">
        <label for="checkbox_1{{rowIndex}}"></label>
    </div>
    </ng-template>
</ngx-datatable-column>
<ngx-datatable-column name="Title" cellClass="d-flex align-items-center"></ngx-datatable-column>
<ngx-datatable-column name="Place" cellClass="d-flex align-items-center">
    <ng-template let-row="row" let-value="value" ngx-datatable-cell-template>
        <a href="javascript:;" *ngFor="let value of row.places" class="btn btn-tag">{{value}}</a>
    </ng-template>
</ngx-datatable-column>
<ngx-datatable-column name="Activities" cellClass="d-flex align-items-center"></ngx-datatable-column>
<ngx-datatable-column name="Status" cellClass="d-flex align-items-center"></ngx-datatable-column>
<ngx-datatable-column name="Last Update" cellClass="d-flex align-items-center"></ngx-datatable-column>
</ngx-datatable>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
import { Component, OnInit,ViewChild } from '@angular/core';

@Component({
  selector: 'app-basic',
  templateUrl: './basic.component.html',
  styleUrls: ['./basic.component.scss']
})
export class BasicComponent implements OnInit {

  basic_table_data;
  
  constructor() {
    this.fetch((data) => {
      this.basic_table_data = data;
    });
   }

  ngOnInit() {
  }

  fetch(cb) {
    const req = new XMLHttpRequest();
    req.open('GET', `assets/data/table.json`);

    req.onload = () => {
      cb(JSON.parse(req.response));
    };

    req.send();
  }

}

```
{% endtab %}
{% endtabs %}

