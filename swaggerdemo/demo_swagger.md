---
Title: Test For Jeallyn's Swagger REST API reference
---

# Jeallyn's Test for Swagger API reference


## <a id="Swagger"> </a> Swagger


[!code-REST-i[test.op.swagger](test.op.swagger.json)]


## <a id="Code_table"> </a>Code table


<!-- BEGINSECTION class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar" -->
```cs-i
var outlookClient = await CreateOutlookClientAsync("Calendar");
var events = await outlookClient.Me.Events
  .Take(10)
  .ExecuteAsync();
 
foreach(var calendarEvent in events.CurrentPage)
{
  System.Diagnostics.Debug.WriteLine("Event '{0}'.", calendarEvent.Subject);
}
 
```
```javascript-i
outlookClient.me.events.getEvents().fetch().then(function (result) {
    result.currentPage.forEach(function (event) {
console.log('Event "' + event.subject + '"')
    });
}, function(error) {
    console.log(error);
});
```
<!-- ENDSECTION -->
