# Sistema de Registro de Libros - Biblioteca (Normalización 3FN)

## Descripción del Proyecto
Diseño e implementación de una base de datos relacional para un sistema de biblioteca, normalizada hasta la **Tercera Forma Normal (3FN)** para garantizar la eficiencia, eliminar redundancias y mantener la integridad referencial.

## Estructura de la Base de Datos (3FN)
La base de datos está compuesta por tres tablas principales relacionadas mediante el modelo **1:N (Uno a Muchos)**:

1. **Autores:** Almacena la información única de los autores.
   - `id_autor` (PK)
   - `nombre_autor`
2. **Editores:** Almacena la información de las editoriales.
   - `id_editor` (PK)
   - `nombre_editor`
3. **Libros (Entidad Central):** Contiene los registros de los libros y se conecta a los autores y editores mediante claves foráneas.
   - `id_libros` (PK)
   - `titulo_libro`
   - `id_autor` (FK)
   - `id_editor` (FK)

## Relaciones Principales
- **Un autor escribe muchos libros:** Relación 1:N desde la tabla `autores` hacia `libros`.
- **Muchos libros pertenecen a un editor:** Relación 1:N desde la tabla `editores` hacia `libros`.

## Diagrama EER
![alt text](image-1.png)