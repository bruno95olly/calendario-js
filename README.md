# 📅 calendario-js 

[![FullCalendar](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAYAAACqaXHeAAAAAXNSR0IArs4c6QAAAsBJREFUeAHtW8FqFEEQrers4sUf2ERBEN2D0at39TM8GKN7j4fsQRKJEDAezH2TGEE/Q/yImCAhEQSTzSeIZnfK6tnFTWanxhoh0lPbDQPdVW9m672q7ukdZhC4Ndq7TwFogbtNIHLeZrYhJsxtHwDXT9ZmNzAlT0nHLOEiYuhaDoGeFWFs+2jBEcBN2yQL2TWd+TlfxJ/XO9sLXhH5oS8KoBDJNCRWgOn0KsjFClCIZBoSK8B0ehXkYgUoRDINqYnsEHoO3ArQpXfHr28cibjAHTOLB1cAfswlCMtAMMYXG4s7/IdwvCHCi+7anZfjnmpapts7y0Swko1eXgNquJ0FV3os8BEF6K7e/l5pwpngJT6iAJnzzQ6jAGZTqyQWK0AplFlYrACzqVUSixWgFMosLFaA2dQqicUKUAplFhYrwGxqlcRiBSiFMguLFWA2tUpiY4+Jlef9VxgR4fzX/hNIaJ5fb7s1+HHaA4dbW9enNhEx98m2Jsjgp0DrGzUeH/Y/UkIdZnmXgC4PDu6zzfs8RkM2DxO0AD7zp6f9D/wi17284FMb+3q/+u89VsQUOIIWIC37IvJDYlwR91NsAVHJFbQAgzkvhZ6xp+tDxqYYhi3AnwVPwaQUdnS9wAUYBXpRvcAF4FudupXBji4atgB8nx+F+pdeGeyZSwUtgN/kAOKnM/HmdxmTYvO9hdagBfA7vHp96mGhCEzeY/51Nxj8VrhzDU94k/PgorbCwQvg63eY3Q3u+uNce3tuVH4Q9BQoT6f8GVGA8prZOiNWgJTP6eefr0q+KtolPnIF9GiuikTFmAU+4m2Qn74szbR3E6zVt49Wm8fihQN3pG+K4s9HCSRLeaGKb4rmgS3aHO8y/Le0k9mYu18D+EPiiW37LACuTyp93mK/cf4TcuCvqHkqfJmI6eCnfMrVtbqvZjd/Ayj3u2zl1YldAAAAAElFTkSuQmCC)](https://fullcalendar.io/)

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

