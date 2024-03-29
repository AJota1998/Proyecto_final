# Nombre de la web

cofraNews

# Eslogan

Información cofrade a tu manera

# Objetivo

Realizar una página web donde los usuarios cofrades puedan estar informados de las noticias que suceden en cualquier colectivo 
de la Semana Santa.
Estos colectivos pueden ser hermandades, bandas de música, organismos oficiales, etc. Y estarán agrupados en "espacios" según 
su lugar de procedencia, con el objetivo de que el usuario pueda seguir a tantos "espacios" como quiera para informase de una 
manera organizada. 

# Funcionalidades

    USUARIO ADMINISTRADOR:
        - Registrarse y loguearse
        - Crear, editar y eliminar colectivos
        - Crear, editar y eliminar usuarios generales
        - Crear, editar y eliminar espacios
        - Adherir y eliminar colectivos dentro de los espacios
        - Consultar algún gráfico estadístico de la página

    USUARIO COLECTIVO:
        - Registrarse y loguearse
        - Editar sus datos de pefil
        - Adherirse y salirse de un espacio creado o crear uno para que se adhieran los demás colectivos similares
        - Establecer un contenido de noticias, mensajes, fotos y videos solo para usuarios premium 
        - Establecer un contenido de noticias, mensajes, fotos y videos para el resto de los usuarios
        - Crear, editar y eliminar una página de información general sobre el colectivo dentro de su perfil 
        - Eliminar su cuenta y todos sus datos

    USUARIO GENERAL: 
        - Registrarse y loguearse
        - Editar sus datos de perfil 
        - Crear cero o varios espacios personalizados con los colectivos que el desee, aunque pertenezcan a tipos de colectivos distintos
        - Buscar con filtros a los colectivos que desee, bien para ver su perfil, consultar su página de información o adherirlos a sus espacios creados
        - Seguir a los espacios que ya estén creados
        - Consultar los espacios a los que está siguiendo
        - Consumir el contenido premium que los colectivos publican en los espacios que está suscrito
        - Suscribirse al contenido premium de tantos espacios como desee
        - Interactuar mediante "me gusta", "no me gusta" sobre el contenido que publiquen los colectivos, y si es suscriptor del espacio poder comentar en todas las publicaciones
        - Consultar sus estadísticas
        - Eliminar su cuenta y todos sus datos

# Modelos 

USUARIOS
    - ID_usuario
    - Nombre completo
    - Nombre de usuario (@4-12 caracteres)
    - Correo electrónico
    - Contraseña
    - Imagen de perfil
    - Rol (Administrador, General)
    - Espacios FK [espacio1, e23, e34]

COLECTIVOS
    - ID_colectivo
    - Nombre de colectivo
    - Correo 
    - Contraseña
    - Tipo (Asociación cofrade, Hermandad de vísperas, Hermandad de penitencia, Hermandad de gloria, Agrupación musical (AM), Cornetas y tambores (CCTT),  
            Banda de música (BM), Órgano oficial, Órgano católico)
    - Provincia
    - Localidad
    - Imagen de perfil
    - Información
        - Nombre del colectivo
        - Año de fundación
        - Descripción del colectivo

ESPACIOS
    - ID_espacio
    - Nombre
    - Colectivos FK [colectivo1, c2, c67, c78]
    - Descripción del espacio 
    - Campo Privado / publico (Como mejora para agrandar funcionalidades)
    
PUBLICACIONES
    - ID_publicación
    - ID_colectivo FK
    - Tipo (Noticia, mensaje, foto, video)
    - Contenido
    - Pie (opcional)
    - Fecha de publicación

# Stack tecnológico

Back: 
    - NodeJs
    - Express

BBDD:
    - MongoDB

Front: 
    - JS
    - HTML, CSS, Boostrap
    - Angular

Despliegues: 
    - GithubPages
    - Railway

