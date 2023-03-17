"""
#ADD TASK WEB DEVELOPERS TOOLS CONSOLE

fetch('/tasks', {
   method: 'POST',
   headers: {
      'Content-Type': 'application/json'
   },
   body: JSON.stringify({title: 'Tarea 1', description: 'Descripción de la tarea 1'})
}).then(response => {
   console.log(response);
}).catch(error => {
   console.error(error);
});

#ADD TASK LINUX CONSOLE:

curl -X POST -H "Content-Type: application/json" -d '{"title": "Tarea 1", "description": "Descripción de la tarea 1"}' http://localhost:5000/tasks | jq


#PRINT TASKS WEB DEVELOPERS TOOLS CONSOLE

fetch('/tasks').then(response => {
    console.log(response);
}).catch(error => {
    console.error(error);
});

#PRINT TASK LINUX CONSOLE:

curl http://localhost:5000/tasks | jq


#EDIT TASK WEB DEVELOPERS TOOLS CONSOLE

fetch('/tasks/1', {
    method: 'PUT',
    headers: {
        'Content-Type': 'application/json'
    },
    body: JSON.stringify({
        title: 'Nuevo título',
        description: 'Nueva descripción'
    })
}).then(response => {
    console.log(response);
}).catch(error => {
    console.error(error);
});

#EDIT TASK LINUX CONSOLE:

curl -X PUT -H "Content-Type: application/json" -d '{"title": "Nuevo título", "description": "Nueva descripción"}' http://localhost:5000/tasks/1

#DELETE TASK WEB DEVELOPERS TOOLS CONSOLE

fetch('/tasks/1', {
    method: 'DELETE'
}).then(response => {
    console.log(response);
}).catch(error => {
    console.error(error);
});

#DELETE TASK LINUX CONSOLE:

curl -X DELETE http://localhost:5000/tasks/1

"""