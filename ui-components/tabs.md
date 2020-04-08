# Tabs

pg-tabs is a fork of [NG-ZORRO](https://github.com/NG-ZORRO/ng-zorro-antd) implementation of Tabs Initial credits go to the author.

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgTabsModule } from '../@pages/components/tabs/tabs.module';
@NgModule({
  imports: [pgTabsModule,...]
})
export class AppModule(){}
```

## How to use 

### Basic Tabs

Base on Bootstrap tabs, Pages Angular tab components come with different styles, orientation and animations

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-tabset tabAnimation="slide-left" Type="simple" ShowPagination="true">
    <pg-tab>
    <ng-template #TabHeading>
        Hello World
    </ng-template>
    <div class="row column-seperation">
        <div class="col-lg-6">
            <h3>
            <span class="semi-bold">Sometimes</span> Small things in life means the most
            </h3>
        </div>
        <div class="col-lg-6">
            <h3 class="semi-bold">great tabs</h3>
            <p>Native boostrap tabs customized to Pages look and feel, simply changing class name you can change color as well as its animations</p>
        </div>
        </div>
    </pg-tab>
    <pg-tab>
    <ng-template #TabHeading>
        Hello Two
    </ng-template>
    <div class="row">
        <div class="col-lg-12">
            <h3>“ Nothing is
            <span class="semi-bold">impossible</span>, the word itself says 'I'm
            <span class="semi-bold">possible</span>'! ”
            </h3>
            <p>A style represents visual customizations on top of a layout. By editing a style, you can use Squarespace's visual interface to customize your...</p>
            <br>
            <p class="pull-right">
            <button type="button" class="btn btn-default btn-cons">White</button>
            <button type="button" class="btn btn-success btn-cons">Success</button>
            </p>
        </div>
    </div>
    </pg-tab>
    <pg-tab>
        <ng-template #TabHeading>
            Hello Three
        </ng-template>
        <div class="row">
            <div class="col-lg-12">
            <h3>Follow us &amp; get updated!</h3>
            <p>Instantly connect to what's most important to you. Follow your friends, experts, favorite celebrities, and breaking news.</p>
            <br>
            </div>
        </div>
    </pg-tab>
</pg-tabset>
```
{% endtab %}
{% endtabs %}

### Orientations

You can change the "TabPosition" parameter to left or right

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-tabset tabAnimation="slide-left" Type="simple" TabPosition="left" extraTabClass="bg-white">
    <pg-tab>
    <ng-template #TabHeading>
        Hello World
    </ng-template>
    <div class="row column-seperation">
        <div class="col-lg-6">
            <h3>
            <span class="semi-bold">Sometimes</span> Small things in life means the most
            </h3>
        </div>
        <div class="col-lg-6">
            <h3 class="semi-bold">great tabs</h3>
            <p>Native boostrap tabs customized to Pages look and feel, simply changing class name you can change color as well as its animations</p>
        </div>
        </div>
    </pg-tab>
    <pg-tab>
    <ng-template #TabHeading>
        Hello Two
    </ng-template>
    <div class="row">
        <div class="col-lg-12">
            <h3>“ Nothing is
            <span class="semi-bold">impossible</span>, the word itself says 'I'm
            <span class="semi-bold">possible</span>'! ”
            </h3>
            <p>A style represents visual customizations on top of a layout. By editing a style, you can use Squarespace's visual interface to customize your...</p>
            <br>
            <p class="pull-right">
            <button type="button" class="btn btn-default btn-cons">White</button>
            <button type="button" class="btn btn-success btn-cons">Success</button>
            </p>
        </div>
    </div>
    </pg-tab>
</pg-tabset>
```
{% endtab %}
{% endtabs %}

### Different Styles

#### Triangle Tabs

```markup
<pg-tabset tabAnimation="slide-left" Type="linetriangle" extraTabContentClass="bg-white">
    <pg-tab>
        <ng-template #TabHeading>
        Hello World
        </ng-template>
        <div class="row column-seperation">
            <div class="col-lg-6">
            <h3>
                <span class="semi-bold">Sometimes</span> Small things in life means the most
            </h3>
            </div>
            <div class="col-lg-6">
            <h3 class="semi-bold">great tabs</h3>
            <p>Native boostrap tabs customized to Pages look and feel, simply changing class name you can change color as well as its animations</p>
            </div>
        </div>
    </pg-tab>
    <pg-tab>
        <ng-template #TabHeading>
            Hello Two
        </ng-template>
        <div class="row">
            <div class="col-lg-12">
            <h3>“ Nothing is
                <span class="semi-bold">impossible</span>, the word itself says 'I'm
                <span class="semi-bold">possible</span>'! ”
            </h3>
            <p>A style represents visual customizations on top of a layout. By editing a style, you can use Squarespace's visual interface to customize your...</p>
            <br>
            <p class="pull-right">
                <button type="button" class="btn btn-default btn-cons">White</button>
                <button type="button" class="btn btn-success btn-cons">Success</button>
            </p>
            </div>
        </div>
    </pg-tab>
    <pg-tab>
        <ng-template #TabHeading>
            Hello Three
        </ng-template>
        <div class="row">
            <div class="col-lg-12">
                <h3>Follow us &amp; get updated!</h3>
                <p>Instantly connect to what's most important to you. Follow your friends, experts, favorite celebrities, and breaking news.</p>
                <br>
            </div>
            </div>
        </pg-tab>
</pg-tabset>
```

#### Fill In Tabs

```markup
<pg-tabset tabAnimation="slide-left" Type="fillup" extraTabContentClass="bg-white">
    <pg-tab>
    <ng-template #TabHeading>
        <span>Hello World</span>
    </ng-template>
    <div class="row column-seperation">
        <div class="col-lg-6">
            <h3>
            <span class="semi-bold">Sometimes</span> Small things in life means the most
            </h3>
        </div>
        <div class="col-lg-6">
            <h3 class="semi-bold">great tabs</h3>
            <p>Native boostrap tabs customized to Pages look and feel, simply changing class name you can change color as well as its animations</p>
        </div>
        </div>
    </pg-tab>
    <pg-tab>
    <ng-template #TabHeading>
        <span>Hello Two</span>
    </ng-template>
    <div class="row">
        <div class="col-lg-12">
            <h3>“ Nothing is
            <span class="semi-bold">impossible</span>, the word itself says 'I'm
            <span class="semi-bold">possible</span>'! ”
            </h3>
            <p>A style represents visual customizations on top of a layout. By editing a style, you can use Squarespace's visual interface to customize your...</p>
            <br>
            <p class="pull-right">
            <button type="button" class="btn btn-default btn-cons">White</button>
            <button type="button" class="btn btn-success btn-cons">Success</button>
            </p>
        </div>
        </div>
    </pg-tab>
    <pg-tab>
        <ng-template #TabHeading>
        <span>Hello Three</span>
        </ng-template>
        <div class="row">
            <div class="col-lg-12">
            <h3>Follow us &amp; get updated!</h3>
            <p>Instantly connect to what's most important to you. Follow your friends, experts, favorite celebrities, and breaking news.</p>
            <br>
            </div>
        </div>
    </pg-tab>
</pg-tabset>
```

## API

| Property | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| tabAnimation | Animation type. Only supports "slide-left" | string | null |
| Type | Style Type - "fillup" , "linetriangle", "simple" | string | null |
| TabPosition | Orientation - "left" , "right" | string | null |
| extraTabClass | Add extra class for tabs wrapper | string | null |

