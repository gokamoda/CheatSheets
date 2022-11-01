# calendar関連


```JavaScript
function addEvents() {
  CALENDAR_ID = "<メアド>"
  const calendar = CalendarApp.getCalendarById(CALENDAR_ID)
  calendar.createEvent(title, start, end)  
}
```