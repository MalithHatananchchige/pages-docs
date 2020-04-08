---
description: >-
  Charts are powered by nvd3 and echarts please refer there guid for further
  documentation
---

# Charts

{% embed url="https://ecomfe.github.io/echarts-doc/public/en/option.html" %}

## Importing

First import it to your app module or any submodule as you wish

```typescript
import { NgxEchartsModule } from 'ngx-echarts';
import { NvD3Module } from 'ngx-nvd3';
@NgModule({
  imports: [NvD3Module,NgxEchartsModule,...]
})
export class AppModule(){}
```

## How to use 

{% tabs %}
{% tab title="HTML" %}
```markup
<div echarts [options]="optionsLineStack" [initOpts]="initOptionsLineStack" class="demo-chart"></div>
```
{% endtab %}

{% tab title="Typescript" %}
```typescript
    initOptionsLineStack = {
      renderer: 'svg',
      width: 460,
      height: 300
    };
  
    optionsLineStack = {
      tooltip : {
        trigger: 'axis',
        backgroundColor:'#fff',
        padding:10,
        textStyle:{
            color:pg.getColor('master'),
            fontSize:12,
            fontFamily:"Arial",
        },
        axisPointer:{
          type:"line",
          lineStyle:{
              opacity:0.6
          }
        },
        extraCssText:"box-shadow: 0 0 6px rgba(0,0,0,.1);"
      },
      grid: {
          left: '3%',
          right: '4%',
          bottom: '3%',
          containLabel: true
      },
      xAxis : [
          {
              type : 'category',
              boundaryGap : false,
              data : [10, 10, 25, 29, 20, 22, 20, 22],
                          axisLine:{
                  show:false
              },
              axisTick:{
                  show:false
              },
              axisLabel:{
                  show:false
              }
          }
      ],
      yAxis : [
          {
              type : 'value',
              axisLine:{
                  show:false
              },
              axisLabel:{
                  show:false
              },
              axisTick:{
                  show:false
              },
              splitLine:{
                  show:false
              },
              backgroundColor:"#fff"
          }
      ],
      series : [
          {
              name:'Visitors',
              type:'line',
              stack: '',
              areaStyle: {
                opacity:0.4
              },
              data:[10, 10, 25, 29, 20, 22, 20, 22],
              clipOverflow:'start',
              itemStyle:{
                color:pg.getColor('warning')
              },
              lineStyle:{
                width:0
              }
          },
          {
              name:'New Visitors',
              type:'line',
              stack: '',
              areaStyle: {
                opacity:0.4
              },
              data:[0, 10, 8, 20, 15, 10, 15, 5],
              clipOverflow:'start',
              itemStyle:{
                color:pg.getColor('danger')
              },
              lineStyle:{
                width:0
              }
          }
      ]
    } 
```
{% endtab %}
{% endtabs %}

