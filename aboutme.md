---
layout: page
title: NWiMLDS
subtitle: Nairobi women in machine learning and Data science
use-site-title: true
---
 <link rel="stylesheet" href="/fullcalendar.0/packages/core/main.css" />
  <link rel="stylesheet" href="/fullcalendar.0/packages/daygrid/main.css" />
  <link rel="stylesheet" href="/fullcalendar.0/packages/list/main.css" />
	  
  <script src="/fullcalendar.0/packages/core/main.js"></script>
  <script src="/fullcalendar.0/packages/interaction/main.js"></script>
  <script src="/fullcalendar.0/packages/daygrid/main.js"></script>
  <script src="/fullcalendar.0/packages/list/main.js"></script>
  <script src="/fullcalendar.0/packages/google-calendar/main.js"></script>

  <script>
  
  document.addEventListener('DOMContentLoaded', function() {
    var calendarEl = document.getElementById('calendar');
    var calendar = new FullCalendar.Calendar(calendarEl, {
      plugins: ['interaction', 'dayGrid', 'list', 'googleCalendar' ],
      header: {
        left: ',prev,next,today',
        center: 'title',
        right: 'dayGridMonth,dayGridDay'
      },
      displayEventTime: false, // don't show the time column in list view
      // THIS KEY WON'T WORK IN PRODUCTION!!!
      // To make your own Google API key, follow the directions here:
      // http://fullcalendar.io/docs/google_calendar/
      googleCalendarApiKey: 'AIzaSyD6O2e49eZW0XzgQzcrPr751qtBldszdiU',
      // google calendar API
      events: 'pa6cmu4i96qud9lo6faah4id94@group.calendar.google.com',
      eventClick: function(arg) {
        // opens events in a popup window
        window.open(arg.event.url, 'google-calendar-event', 'width=700,height=600');
        arg.jsEvent.preventDefault() // don't navigate in main tab
      },
      loading: function(bool) {
        document.getElementById('loading').style.display =
          bool ? 'block' : 'none';
      }
    });
    calendar.render();
  });
</script>

<style>
    body {
      margin: 40px 10px;
      padding: 0;
      font-family: Arial, Helvetica Neue, Helvetica, sans-serif;
      font-size: 14px;
    }
  
    #calendar {
      max-width: 900px;
      margin: 0 auto;
    }
  
  </style>
  
 <p>Calendar </p>
	    
<div id='loading'>loading...</div>
	<div id='calendar'></div>
