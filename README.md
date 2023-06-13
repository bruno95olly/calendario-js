# 📅 calendario-js 

[📅 FullCalendar](https://fullcalendar.io/)

Repositório feito com o objetivo de entender como funciona a biblioteca FullCalendar.
##

# Estilizações necessárias:

~~~html
<!-- Importando o estilo do FullCalendar para a aparência do calendário -->
<link rel="stylesheet" href="./styles/fullcalendar.min.css" />
<!-- Importando o estilo do tema "Materia" do Bootstrap para personalização -->
<link rel="stylesheet" href="./styles/bootstrap.min.css" />
<!-- Importando o estilo dos ícones do FontAwesome -->
<link rel="stylesheet" href="./styles/fontawesome.css" />
~~~

# Scripts necessários:
~~~html
<!-- Importando a dependência moment.js para manipulação de datas e horários pelo FullCalendar -->
<script src="./js/moment.js"></script>
<!-- Importando a dependência jQuery para uso do FullCalendar -->
<script src="./js/jquery.js"></script>
<!-- Importando a biblioteca FullCalendar.js para gerar o calendário -->
<script src="./js/fullcalendar/fullcalendar.js" type="text/javascript"></script>
<!-- Importando o arquivo locale.js para alterar o idioma utilizado do calendário -->
<script src="./js/locale.js" type="text/javascript"></script>
~~~

# HTML necessário:
~~~html
<!-- A div contém id para que seja possível referenciá-la no javascript -->
<div id="calendar"></div>
~~~

# Script para manipular calendário:
~~~javascript
$(document).ready(function() {
  $('#calendar').fullCalendar({
    themeSystem: 'bootstrap4',
    defaultView: 'month',
    displayEventTime: false,
    nowIndicator: true, 
    slotLabelInterval: "01:00:00",
    timeFormat: 'H(:mm)',
    slotLabelFormat:"HH:mm",
    header: {
      left: 'month,agendaWeek, listWeek',
      center: 'title',
      right: 'today prev,next'
    },
    navLinks: true,
    allDaySlot: true,   
    events: [
      {
        title: 'Evento 1',
        start: '2023-06-01'
      },
      {
        title: 'Evento 2',
        start: '2023-06-05',
        end: '2023-06-08'
      },
      {
        title: 'Evento 2-1',
        start: '2023-06-05',
      },
      {
        title: 'Evento 2-2',
        start: '2023-06-05',
        end: '2023-06-07'
      },
      {
        title: 'Evento 2-3',
        start: '2023-06-05',
        end: '2023-06-07'
      },
      {
        title: 'Evento 3',
        start: '2023-06-09T12:30:00',
        end: '2023-06-10T12:30:00'
      }
    ],
    eventColor: '#000',
  });
});
~~~

