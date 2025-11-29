# Introduccio Git GitHub Avançat mdBook
Pera alumnes de Entorns de Desenvolupament per practicar Git i GitHub

-----

## 🚀 Instalación de `mdBook`

Primero, necesitas tener **Rust** y su gestor de paquetes **Cargo** instalados en tu sistema. 
Si no los tienes, puedes encontrarlos en la página oficial de [Rust](https://www.rust-lang.org/tools/install).

Una vez que tengas Cargo, puedes instalar `mdBook` ejecutando el siguiente comando en tu terminal:

```bash
cargo install mdbook
```
-----

## 🛠️ Creación de un Nuevo Libro

Para iniciar un nuevo proyecto de `mdBook`, navega hasta el directorio donde quieres crear el libro y usa el comando `init`:

```bash
mdbook init nombre-de-mi-libro
```

Esto creará una nueva carpeta llamada `nombre-de-mi-libro` con la siguiente estructura básica:

```
nombre-de-mi-libro/
├── book/
├── src/
│   ├── chapter_1.md
│   └── SUMMARY.md
└── book.toml
```

  * **`book.toml`**: El archivo de configuración principal de tu libro.
  * **`src/`**: Contiene todos los archivos fuente de Markdown de tu libro.
  * **`src/SUMMARY.md`**: Define la estructura, el orden y los títulos de los capítulos. **Este es el archivo más importante para la navegación.**
  * **`book/`**: Es el directorio donde se generará el libro estático (HTML, etc.).

-----

## 📝 Edición del Contenido y Estructura

### 1\. **Definir la Estructura en `SUMMARY.md`**

Abre el archivo `src/SUMMARY.md` y edita la lista con el formato de enlaces de Markdown. Los títulos de los enlaces se usarán como nombres en el índice, y las rutas apuntarán a los archivos Markdown correspondientes.

**Ejemplo de `src/SUMMARY.md`:**

```markdown
# Summary

[Introducción](README.md)

# Parte I: Conceptos Básicos

* [Primer Capítulo](capitulo_1.md)
* [Segundo Capítulo](capitulo_2.md)
    * [Subsección A](subseseccion_a.md)
* [Tercer Capítulo](capitulo_3.md)
```

**Nota:** El archivo `README.md` se usa por defecto para la página de inicio.

### 2\. **Crear los Archivos Markdown**

Crea los archivos Markdown mencionados en `SUMMARY.md` dentro de la carpeta `src/`. Por ejemplo, si definiste `capitulo_1.md`, debes crearlo en `src/capitulo_1.md` y escribir tu contenido en él.

````markdown
# Primer Capítulo

Este es el contenido de mi primer capítulo.
Puedes usar **negritas**, *cursivas* y bloques de código:

```rust
fn main() {
    println!("¡Hola, mdBook!");
}
````

````

---

## 🖥️ Previsualización del Libro

Mientras editas, es muy útil previsualizar los cambios en tiempo real.

1.  Navega al directorio raíz de tu proyecto (`cd nombre-de-mi-libro`).
2.  Ejecuta el comando `serve`:

```bash
mdbook serve
````

Esto iniciará un servidor web local y abrirá automáticamente tu navegador. El servidor **recargará la página** cada vez que guardes un archivo en el directorio `src/`.

-----

## 🏗️ Construcción Final del Libro

Una vez que estés satisfecho con el contenido, puedes generar la versión estática final de tu libro.

1.  Asegúrate de estar en el directorio raíz del proyecto.
2.  Ejecuta el comando `build`:

<!-- end list -->

```bash
mdbook build
```

Esto generará los archivos HTML, CSS y JavaScript necesarios en el directorio **`book/`**. Puedes subir el contenido de esta carpeta a cualquier servidor web para publicar tu libro.

-----

¿Te gustaría que te mostrara cómo modificar el archivo de configuración `book.toml` para personalizar el título y el idioma de tu libro?
