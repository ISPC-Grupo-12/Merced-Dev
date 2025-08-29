# Proyecto Merced-Dev

Repositorio de la materia: Sistema de Gestión de Contenidos del equipo Merced Dev<br>

## Propósito:

Merced nace con el objetivo de transformar la experiencia de compra de indumentaria, llevando la propuesta de una tienda física tradicional a una plataforma digital moderna y accesible. Su propósito central es romper las barreras geográficas y económicas, ofreciendo moda actual de calidad a un público global. A través de su sitio web, Merced busca consolidarse como una marca que combina accesibilidad, estilo y proyección internacional, brindando a cada cliente la posibilidad de acceder a productos únicos sin importar su ubicación.

## Utilidades:

- **Exhibición global de productos**: la plataforma permite mostrar de forma atractiva y ordenada el catálogo completo de prendas, potenciando la visibilidad de la marca.<br>

- **Filtros y organización de búsqueda**: los usuarios pueden navegar con mayor facilidad entre productos gracias a menús y opciones de filtrado, mejorando la experiencia de compra.<br>

- **Carrito de compras y métodos de pago**: el sistema integra diferentes alternativas de pago, garantizando flexibilidad y comodidad para cada cliente.<br>

- **Atención al cliente directa**: se incluye contacto inmediato con los vendedores mediante WhatsApp o correo electrónico, resolviendo dudas y generando confianza.<br>

- **Envíos internacionales**: Merced amplía el alcance de sus productos más allá de las fronteras locales, ofreciendo envíos accesibles y seguros a distintos países.<br>


----
----

# Instalación de WordPress con XAMPP

Guía paso a paso para instalar **WordPress** en un entorno local usando **XAMPP**.  
El cual usaremos para desarrollar y probar antes de subir nuestro proyecto a un servidor real.

---

## 📑 Requisitos previos
- Tener instalado [XAMPP](https://www.apachefriends.org/es/index.html).
- Conocimientos básicos de carpetas en Windows.
- Un navegador web actualizado (Chrome, Firefox, Edge, etc.).

---

## Pasos de instalación

### 1. Instalar XAMPP
1. Descargá e instalá **XAMPP** desde su [página oficial](https://www.apachefriends.org/es/index.html).  
2. Abrí el panel de control de XAMPP.  
3. Iniciá los siguientes servicios: Apache y MySQL.


### 2. Crear la base de datos
1. Entrá a: (http://localhost/phpmyadmin).
2. Creá una nueva base de datos, para nosotros sería: **merced**
3. No es necesario crear tablas (WordPress lo hará automáticamente).


### 3. Descargar y descomprimir WordPress
1. Descargamos la última versión desde: (https://wordpress.org/download/).
2. Descomprimir el archivo en:
C:\xampp\htdocs\
3. Renombrá la carpeta, en nuestro caso, a:
C:\xampp\htdocs\merced
4. Accedé luego a:(http://localhost/merced).


### 4. Configurar `wp-config.php`
1. Dentro de la carpeta de WordPress, renombrá:
*wp-config-sample.php → wp-config.php*
2. Abrí el archivo `wp-config.php` y editá:

```php
define('DB_NAME', 'merced');    // Nombre de la base de datos
define('DB_USER', 'root');      // Usuario (por defecto en XAMPP)
define('DB_PASSWORD', '');      // Contraseña (vacía por defecto en XAMPP)
define('DB_HOST', 'localhost'); // Normalmente "localhost" o "Localhost:3307" si se tuvo que cambiar de
```

3. Guardá los cambios.


### 5.Instalación desde el navegador
1. Abrír el navegador en:
(http://localhost/merced)
2. Completar los campos:  
- *Título del sitio*  
- *Usuario administrador*  
- *Contraseña*
- *Correo electrónico*
3. Hacer clic en
**Instalar WordPress**


### 6. Iniciar sesión
1. Acceder a:
(http://localhost/merced/wp-admin)
2. Usá el usuario y contraseña creados en la instalación.


### 7. Ajustes generales
1. Entrá en: Ajustes → Generales
2. Configurá:  
*Nombre del sitio*  
*Idioma*  
*Zona horaria*  
*Formato de fecha y hora*


### 8. Configurar enlaces permanentes
1. Ir a Ajustes → Enlaces permanentes  
2. Seleccionar *Nombre de la entrada*
3. Las URLs quedarán así:  
(**http://localhost/merced/ejemplo-de-entrada/**)

---

## Cómo usar WordPress

*Una vez instalado, podemos utilizarlo para crear y administrar nuestro sitio sin necesidad de programar. Para tener una guía sencilla pero detallada de lo que ofrece **WordPress**, a continuación dejamos las principales secciones que tiene.*

### 1. 📝 Entradas (Posts)
- Crear nuevas publicaciones: **Entradas → Añadir nueva**  
- Editar, publicar o programar publicaciones  
- Asignar categorías y etiquetas para organizar contenido

### 2. 📄 Páginas (Pages)
- Crear páginas estáticas como “Inicio”, “Contacto” o “Nosotros”  
- **Páginas → Añadir nueva**

### 3. 🖼 Medios (Media)
- Subir imágenes, videos y archivos: **Medios → Biblioteca → Añadir nuevo**  
- Insertar medios en entradas y páginas

### 4. 🎨 Apariencia (Appearance)
- Cambiar tema o plantilla: **Apariencia → Temas**  
- Personalizar colores, menús, widgets y diseño general: **Apariencia → Personalizar**

### 5. 🔌 Plugins
- Añadir funcionalidades extra: **Plugins → Añadir nuevo**  
- Activar, desactivar o eliminar plugins según lo necesites
- Algunos que podrían servir son *Contact Form 7* o *Flamingo*, por ejemplo.

### 6. 👥 Usuarios
- Administrar usuarios y roles: **Usuarios → Añadir nuevo**  
- Asignar permisos (Administrador, Editor, Autor, Colaborador, Suscriptor)
