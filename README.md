# MiParqueo App: snapshot de vistas

## Identificacion

- Repositorio: https://github.com/probandoel44/app-mi-parqueo-vista-main
- Rama revisada: `main`
- Commit base revisado: `c5ac91970a32cf13238ec11b788e97b6aecc91dc`
- Los archivos están dentro de `app-mi-parqueo-vista-main/`.
- Es una copia de interfaz relacionada con MiParqueo, no el repositorio canónico integrado. La referencia canónica recomendada es https://github.com/probandoel44/Desarrollar-software-a-partir-de-la-integraci-n-de-sus-m-dulos-componentes.

## Propósito y límites

La copia contiene páginas estáticas en `src/main/resources/static` y plantillas HTML en `src/main/resources/templates`, además de `pom.xml`. El árbol revisado no contiene controladores Java ni configuración de base de datos. Varias vistas muestran datos de ejemplo y expresiones Thymeleaf, por lo que su presentación completa requiere un backend compatible.

No se debe reportar este repositorio como aplicación integrada ni como despliegue. Los enlaces `/ocupacion`, `/movimientos`, `/alertas`, `/pagos`, `/ubicacion-vehiculos` y `/fidelizacion` necesitan rutas de servidor que no están implementadas en esta copia.

## Entradas, salidas e interfaces observadas

| Vista/entrada | Datos observables | Salida/efecto observado |
| --- | --- | --- |
| `static/login.html` | Campos de texto de usuario y contraseña. | JavaScript local redirige a `dashboard.html` cuando coincide su condición de demostración; en caso contrario muestra una alerta. No autentica contra servidor ni crea una sesión. |
| `templates/ocupacion.html` | No tiene formulario de reserva en el contenido revisado. | Muestra valores de ejemplo y cuadrícula visual; no consulta por sí sola el estado de la base de datos. |
| `templates/movimientos.html` | No se observan formularios de alta/consulta en el archivo revisado. | Tabla con filas de muestra; no persiste movimientos por sí sola. |
| Otras plantillas (`alertas`, `pagos`, `fidelizacion`, `ubicacion-vehiculos`) | Revisar campos en cada plantilla antes de definir contrato. | Plantillas UI; no se verificó un controlador que suministre datos. |

El inicio de sesión contiene una condición de credenciales local en JavaScript. No es un control de seguridad y no debe reutilizarse como autenticación de producción.

## Evidencia SENA

| Elemento | Evidencia actual | Estado |
| --- | --- | --- |
| Informe de requerimientos y componente formativo | No localizados en esta copia. | Pendiente; solicitar documentos oficiales. |
| Acta de aprobación | No localizada. | Pendiente; no inferir aprobación. |
| Control de versiones | Repositorio público, rama `main`, commit base indicado arriba. | Disponible; registrar commit del README después de publicarlo. |
| Módulos funcionales | La copia provee vistas, pero no se verificó un backend en el árbol revisado. | Parcial/pendiente de integración con el backend canónico. |
| Ejecutable | El `pom.xml` es de un proyecto Maven, pero no se verificó una aplicación completa compilable ni un JAR. | Pendiente; no declarar un JAR existente. |
| URL desplegada | No se encontró una URL de despliegue. | Pendiente. Las rutas `/...` son paths relativos, no URLs de despliegue. |
| Pruebas | No se revisó una suite ni un reporte para este snapshot. | No verificadas. |
| Servidor/base de datos | El POM declara dependencias web/JPA y MySQL, pero no se halló configuración de datasource en los recursos observados. | Pendiente de integración/configuración. |
| Manual técnico | Esta guía documenta los límites de la copia. | Parcial; requiere contrato del backend que la integre. |

## Ambiente y uso

No se verificó un servidor ejecutable en esta copia. Para usar las vistas como parte de MiParqueo, intégralas con el proyecto Spring Boot canónico y confirma las rutas y datos que el backend suministra. No se asigna un comando de inicio como validado ni se inventa una URL pública.

## Pendientes

1. Confirmar si esta copia debe conservarse como antecedente de interfaz.
2. Relacionar cada vista con los controladores/rutas del repositorio integrado.
3. Retirar o sustituir la autenticación demostrativa local por sesión y permisos del backend antes de un despliegue.
4. Ejecutar pruebas de renderizado e integración con el backend y documentar el resultado real.
5. Adjuntar requerimientos, aprobación, configuración de ambientes y URL desplegada si existen.