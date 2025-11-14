# Librerías Java para Facturación Electrónica (Ecuador) — Java 8

Este repositorio únicamente almacena una colección de librerías Java (archivos JAR) que ya no se encuentran disponibles en los repositorios públicos de Maven. Estas librerías facilitan el desarrollo de aplicaciones o backends para la facturación electrónica en Ecuador (SRI) y están destinadas a proyectos que usan Java 8.

IMPORTANTE: este repositorio NO contiene el código fuente de la plataforma del SRI ni pretende ser una implementación oficial. Solo centraliza binarios necesarios para construir/ejecutar soluciones legadas o integraciones que dependen de artefactos no disponibles en Maven Central.

Contenido
- JARs binarios útiles para la facturación electrónica en Ecuador (Ecuador SRI).
- Instrucciones para instalar las librerías en tu repositorio Maven local o en un repositorio privado.

Requisitos
- Java 8 (JDK 8). Estas librerías fueron compiladas para ser compatibles con Java 8 y no se garantiza su funcionamiento con versiones mayores sin pruebas adicionales.
- Maven (u otro gestor que consuma repositorios Maven).

Cómo usar estas librerías
1. Copia los JAR necesarios desde la carpeta `libs/` (o el directorio donde estén almacenados) a tu proyecto, o instálalos en tu repositorio Maven local.

Ejemplo (instalar en el repositorio Maven local):
```bash
mvn install:install-file \
  -Dfile=libs/nombre-libreria.jar \
  -DgroupId=com.example.ec \
  -DartifactId=nombre-libreria \
  -Dversion=1.0.0 \
  -Dpackaging=jar
```

Repite el comando por cada JAR, cambiando `file`, `groupId`, `artifactId` y `version` según corresponda.

Ejemplo de dependencia en `pom.xml`:
```xml
<dependency>
  <groupId>com.example.ec</groupId>
  <artifactId>nombre-libreria</artifactId>
  <version>1.0.0</version>
</dependency>
```

Alternativa: subir los JARs a un repositorio privado (Nexus, Artifactory) y consumirlos desde allí usando las coordenadas Maven apropiadas.

Lista sugerida de información por cada JAR
- Nombre del archivo: `nombre-libreria.jar`
- groupId / artifactId / version (sugeridos)
- Descripción breve (qué funcionalidad aporta)
- Requisitos (por ejemplo: dependencias externas, versión mínima de Java)

Responsabilidades y advertencias
- Estas librerías pueden contener dependencias no publicadas: realiza pruebas de integración completas.
- No se garantiza soporte oficial. Úsalas bajo tu responsabilidad y revisa licencias antes del uso en producción.
- Si consideras que alguna librería puede ser publicada en un repositorio público o que se requiere actualizar, abre un issue o contacta al mantenedor.

Recursos útiles
- Documentación SRI (Facturación Electrónica Ecuador): https://www.sri.gob.ec (ver sección de facturación electrónica)
- Guías y esquemas XML/WS provistos por el SRI (para integración y validación)

Contribuciones
- Si tienes JARs adicionales que deberían estar aquí, por favor crea un issue describiendo el artefacto, su origen y la licencia. No subas archivos binarios en issues; súbelos en PR o contacta al/los mantenedor(es) para coordinar.

Licencia
- Cada JAR mantiene su propia licencia. Revisa la licencia de cada artefacto antes de redistribuirlo. Este repositorio actúa solo como almacén, no como autor ni propietario de las librerías.

Contacto
- Mantenedor: byrone593 (ver perfil de GitHub para contacto).

Versiones y mantenimiento
- Fecha de creación/actualización: consulta el historial de commits para ver cuándo se añadieron o actualizaron librerías.
- Objetivo: preservar acceso a artefactos necesarios para proyectos legados de facturación electrónica en Ecuador con Java 8.
