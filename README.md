![Logo de GammaTech School](./assets/Logo_Yellow.png)

# Ejercicio React Forms

Para practicar todo lo que hemos visto hasta ahora, tanto los estados como los formularios, vamos a implementar una herramienta de registro y gestión de usuarios, muy similar a la que podríamos encontrar en una aplicación real.

### Introducción
Nuestra aplicación de React debe ser capaz de hacer 3 cosas:
1. Registrar usuarios y guardar su información.
2. Buscar usuarios en función de uno o varios parámetros (nombre, email...).
3. Gestionar la eliminación del usuario deseado.

Para ello, vamos a necesitar todo lo que hemos aprendido hasta ahora: `useState`, `useEffect` y la gestión de formularios.

La aplicación tendrá, como mínimo, los siguientes componentes:

### Componente `App` 
El componente principal de la aplicación, de donde colgarán el resto de componentes.

### Componente `UserForm`
El formulario a rellenar por el usuario. Constará de los siguientes campos:
- nombre
- email
- edad
- teléfono
- género: `radio` con las siguientes opciones:
	- masculino
	- femenino
	- no binario
	- otros / prefiero no decirlo
- tipo de cuenta: `select` con las siguientes opciones excluyentes:
	- básica
	- premium
	- business
- acepto recibir publicidad por email: `checkbox`

Todos los campos tendrán sus `label` correspondientes y correctamente ligadas a sus `inputs`.
Para que la información persista en la aplicación, considera guardar la lista de usuarios en `LocalStorage`, además de en un estado.

### Componente `SearchUser`
Un formulario para buscar usuarios por `email`. Cuando se envía debe renderizar en la `UserList` la lista con usuarios que tengan dicho email. Si no hay ninguna coincidencia, se deberá renderizar toda la lista de usuarios existentes.
Como opción, puedes añadir un botón de `Clear` que limpie la búsqueda y renderice todos los usuarios.

### Componente `UserList`
El componente que renderizará la lista de usuarios registrados con la información guardada de cada uno.
Si se ha buscado por `email`, mostrará los usuarios que tengan dicho email. Si no se ha buscado nada, mostrará **todos** los usuarios.

### Componente `UserCard`
Cada uno de los usuarios renderizados por `UserList`.