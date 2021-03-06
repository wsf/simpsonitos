<img title="mcb-logo" src="http://s11.postimg.org/dwjiobp4j/simpsonitos.gif" width="800px" alt="meteor-coffee-boilerplate logo"/>
# Simpsonitos: Juego Trivia

Un juego de tipo trivia, preguntas y respuestas acerca de Los Simpsons. Hecho completamente con [Meteor](http://meteor.com/).

## Instalación

No se necesita ninguna otra dependencia, solo Meteor.

Antes de correr el juego, necesitas crear una App en [Facebook Developers](https://developers.facebook.com/apps/). Luego agregar el **ID** y el **SECRET** al `settings.json`.

```bash
# Clonar el proyecto.
$ git clone https://github.com/juanifioren/simpsonitos.git
$ cd simpsonitos/

# Cargar las preguntas.
$ mongoimport --port 3001 --db meteor --collection questions < ./questions.json

# Correr el juego.
$ meteor run --settings settings.json
```

## Preguntas y Respuestas

Si bien no hay muchas preguntas (pueden repetirse a lo largo del juego), es fácil agregar más. Solo ten en cuenta el siguiente formato. Se agregan al archivo `questions.json`.

```json
{ "_id": "", "difficulty": 0, "text": "", "answers": [ { "number": 1, "text": "" }, { "number": 2, "text": "" }, { "number": 3, "text": "" }, { "number": 4, "text": "" } ], "correctAnswer": 1 }

```
