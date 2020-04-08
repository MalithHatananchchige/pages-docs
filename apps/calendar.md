# Calendar

Pages calendar plugin is exclusive only on pages and is not a third party plugin. The horizontal scrolling helps it to fit easily on to small screens and user experience is seamless across all platforms. It supports many features including **multiple languages and timezones**

## How to Setup

### **Dependencies**

```markup
<script src="assets/plugins/interactjs/interact.min.js" type="text/javascript"></script>
<script src="assets/plugins/moment/moment-with-locales.min.js"></script>
```

### **Pages Calendar Lib**

```markup
<script src="pages/js/pages.calendar.min.js"></script>
```

### **HTML Source**

Inlcude the following HTML source to your file, you can remove the compontents you do not need to have

```markup
<div id="myCalendar" class="full-height"></div>
```

### **Initialize Pages Calendar**

To initialize pages calendar with default setting use the following code

```javascript
$('#myCalendar').pagescalendar();
```

### **Calendar Settings and Callbacks**

```javascript
 $('body').pagescalendar({
    ui: {
        //Year Selector
        year: {
            visible: true,
            format: 'YYYY',
            startYear: '2000',
            endYear: moment().add(10, 'year').format('YYYY'),
            eventBubble: true
        },
        //Month Selector
        month: {
            visible: true,
            format: 'MMM',
            eventBubble: true
        },
        dateHeader: {
            format: 'MMMM YYYY, D dddd',
            visible: true,
        },
        //Mini Week Day Selector
        week: {
            day: {
                format: 'D'
            },
            header: {
                format: 'dd'
            },
            eventBubble: true,
            startOfTheWeek: '0',
            endOfTheWeek:'6'
        },
        //Week view Grid Options
        grid: {
            dateFormat: 'D dddd',
            timeFormat: 'h A',
            eventBubble: true,
            scrollToFirstEvent:false,
            scrollToAnimationSpeed:300,
            scrollToGap:20
        }
    },
    eventObj: {
        editable: true
    },
    view:'week',
    now: null,
    locale: 'en',
    //Event display time format
    timeFormat: 'h:mm a',
    minTime:0,
    maxTime:24,
    dateFormat: 'MMMM Do YYYY',
    slotDuration: '30', //In Mins : supports 15, 30 and 60
    events: [],
    eventOverlap: false,
    weekends:true,
    disableDates:[],
    //Event CallBacks
    onViewRenderComplete: function() {},
    onEventDblClick: function() {},
    onEventClick: function(event) {},
    onEventRender: function() {},
    onEventDragComplete: function(event) {},
    onEventResizeComplete: function(event) {},
    onTimeSlotDblClick: function(timeSlot) {},
    onDateChange:function(range){}
})
```

**Sample JSON Event Object**

```javascript
[
    {
        "title": "Call Dave",
        "class": "bg-success-lighter",
        "start": "2014-10-07T06:00:00",
        "end": "2014-10-07T08:00:24",
        "other": {}
    },
    {
        "title": "Meeting Roundup",
        "class": "bg-success-lighter",
        "start": "2014-11-07T06:00:00"
    },
    {
        "title": "Double click Any where",
        "class": "bg-complete-lighter",
        "start": "2014-11-07T01:00:00",
        "end": "2014-11-07T02:00:00",
        "other": {
            "note": "test"
        }
    }
]
```

## **Public Methods**

```javascript
$('#my_calendar_elment').pagescalendar('rebuild');
```

Rebuild your calendar  


```javascript
$('#my_calendar_elment').pagescalendar('today');
```

Set date to current date  


```javascript
$('#my_calendar_elment').pagescalendar('next');
```

Next Month  


```javascript
$('#my_calendar_elment').pagescalendar('prev');
```

Previous Month  


```javascript
$('#my_calendar_elment').pagescalendar('setDate',value);
```

Parse in the date string to set a date to the calendar, it will accept any standard date formate  


```javascript
$('body').pagescalendar('getDate',formate);
```

You can get the current date of the calendar and also pass in the required date formate to get the the desire formate output   
  
**example :** `$('#my_calendar_elment').pagescalendar('getDate','dd/mm/yyyy');`   
It will accept any date formate string   


```javascript
$('#my_calendar_elment').pagescalendar('render');
```

To render the calendar  


```javascript
$('#my_calendar_elment').pagescalendar('setLocale','fr');
```

Change langues  


```javascript
$('#my_calendar_elment').pagescalendar('reloadEvent');
```

Reload and draw events for the particular view.  


```javascript
$('#my_calendar_elment').pagescalendar('addEvent',eventObject);
```

Adding an event to the calendar using the even object varriable, demostrated in demos/assets/js/calendar.js  


```javascript
$('#my_calendar_elment').pagescalendar('addEvent',eventArray);
```

Add a batch of events at once.  


```javascript
$('#my_calendar_elment').pagescalendar('removeEvent',index);
```

Removing an event also demonstrated in : demos/assets/js/calendar.js  


```javascript
$('#my_calendar_elment').pagescalendar('removeAllEvents');
```

This method will remove all events in your array  


```javascript
$('#my_calendar_elment').pagescalendar('updateEvent',eventObject);
```

Editing an event to the calendar using the even object variable, demonstrated in `demos/assets/js/calendar.js`  


```javascript
$('#my_calendar_elment').pagescalendar('getEvents',option);
```

Will get you all the events in your calendar array  


```javascript
$('#my_calendar_elment').pagescalendar('view',option);
```

You can set the view / You can change your view to : "month" & " week"  


```javascript
$('#my_calendar_elment').pagescalendar('getView');
```

Display the view type that is currently loaded : "month" or " week"  


```javascript
$('#my_calendar_elment').pagescalendar('getDateRangeInView');
```

Will display start and end date of the current view  


```javascript
$('#my_calendar_elment').pagescalendar('getDateRangeInView');
```

Will display start and end date of the current view  


```javascript
$('#my_calendar_elment').pagescalendar('setState',state);
```

You can set state mannually when you need to, there are two states "loading" and "loaded", This will help you to show a progressbar for lazy event fetching  


```javascript
$('#my_calendar_elment').pagescalendar('error',msg);
```

You can display an error message on your calendar by passing in a string  


```javascript
$('#my_calendar_elment').pagescalendar('scrollToFirstEvent')
```

Scroll to the first even on week and day view   
**Settings**  


```javascript
grid: {
    dateFormat: 'D dddd',
    timeFormat: 'h A',
    eventBubble: true,
    scrollToFirstEvent:false,
    scrollToAnimationSpeed:300,
    scrollToGap:20
}
```

## **Callbacks**

You can see a list of call back demonstrated in `demo/assets/calendar.js` file

`onViewRenderComplete()`

On Render Complete  


`onEventDblClick()`

Event Double Click  


`onEventClick(event)`

Event click call back returns the clicked event details into an array, you can `console.log(event)` to see all event attributes  


`onEventRender()`

After Events are rendered to the view  


`onEventDragComplete()`

After user drag event is completed  


`onEventResizeComplete()`

After user resize event is completed  


`onTimeSlotDblClick(timeSlot)`

Double click time slot on the grid, returns the date and time of the particular timeslot  


`onDateChange(range)`

When ever the calendar's date is change, this call back will return a range, i.e: range.start and range.end both are dates  
  


## **Supported Languages**

Use the language code and set it to `locale`

| LANGUAGE | CODE |
| :--- | :--- |
| Afrikaans | af |
| Albanian | sq |
| Armenian | hy-am |
| Azerbaijani | az |
| Bahasa Indonesia | id |
| Bahasa Malayu | ms-my |
| Basque | eu |
| Belarusian | be |
| Bengali | bn |
| Bosnian | bs |
| Breton | br |
| Bulgarian | bg |
| Catalan | ca |
| Chinese | zh-cn |
| Chinese \(Traditional\) | zh-tw |
| Chuvash | cv |
| Croatian | hr |
| Czech | cs |
| Danish | da |
| Dutch | nl |
| English | en |
| English \(Australia\) | en-au |
| English \(Canada\) | en-ca |
| English \(England\) | en-gb |
| Esperanto | eo |
| Estonian | et |
| Farose | fo |
| Finnish | fi |
| French | fr |
| French \(Canada\) | fr-ca |
| Galician | gl |
| Georgian | ka |
| German | de |
| German \(Austria\) | de-at |
| Greek | el |
| Hebrew | he |
| Hungarian | hu |
| Icelandic | is |
| Italian | it |
| Japanese | ja |
| Khmer \(Cambodia\) | km |
| Korean | ko |
| Latvian | lv |
| Lithuanian | lt |
| Luxembourgish | lb |
| Macedonian | mk |
| Malayalam | ml |
| Norwegian | nb |
| Norwegian Nynorsk | nn |
| Polish | pl |
| Portuguese | pt |
| Portuguese \(Brazil\) | pt-br |
| Romanian | ro |
| Russian | ru |
| Serbian | sr |
| Serbian Cyrillic | sr-cyrl |
| Slovak | sk |
| Slovenian | sl |
| Spanish | es |
| Swedish | sv |
| Tagalog \(Filipino\) | tl-ph |
| Tamaziɣt | tzm |
| Tamaziɣt Latin | tzm-latn |
| Tamil | ta |
| Thai | th |
| Turkish | tr |
| Ukrainian | uk |
| Uzbek | uz |
| Vietnamese | vi |
| Welsh | cy |

For help and bug report please contact support@revox.io  


