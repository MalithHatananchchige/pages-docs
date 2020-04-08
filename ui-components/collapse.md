# Collapse

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { pgCardModule} from './@pages/components/card/card.module';
@NgModule({
  imports: [pgCardModule,...]
})
export class AppModule(){}
```

## How to use 

{% tabs %}
{% tab title="HTML" %}
```markup
<pg-collapseset>
    <pg-collapse [pgTitle]="'Collapsible Group Item'">
    Click headers to expand/collapse content that is broken into logical sections, much like tabs. Optionally, toggle sections open/closed on mouseover.
    </pg-collapse>
    <pg-collapse [pgTitle]="'Typography Variables'">
    <h1 class="light">
        go explore the <span class="semi-bold">world</span>
    </h1>
    <h4>
        small things in life matters the most
    </h4>
    <h2>
        Big Heading <span class="semi-bold">Body</span>,
        <i>Variations</i>
    </h2>
    <h4>
        <span class="semi-bold">Open Me</span>, Light , <span class=
        "semi-bold">Bold</span>, <i>Everything</i>
    </h4>
    <p>
        is the art and technique of arranging type in order to make language visible. The arrangement of type involves the selection of typefaces, point size, line length, leading (line spacing), adjusting the spaces between groups of letters (tracking)
    </p>
    <p>
        and adjusting the Case space between pairs of letters (kerning). Type design is a closely related craft, which some consider distinct and others a part of typography
    </p>
    </pg-collapse>
    <pg-collapse [pgTitle]="'Easy Edit'">
    Click headers to expand/collapse content that is broken into logical sections, much like tabs. Optionally, toggle sections open/closed on mouseover.
    </pg-collapse>
</pg-collapseset>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
  constructor() { }

  ngOnInit() {
  }
  isLoading:boolean=false;
  errorMessage:boolean=false;
  message:string = "Something went terribly wrong. Just keep calm and carry on!";
  
  sampleRefresh(){
    this.isLoading = true;
    this.errorMessage = false;
    setTimeout(()=>{
          this.isLoading = false;
          this.errorMessage = true;
    },3000);
  }
```
{% endtab %}
{% endtabs %}

## API

| Property | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| Title | Set title to a collapse component | string | null |



