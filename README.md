
Vision Statement: STA se especializa en la recolección, procesamiento y distribución de imágenes médicas anonimizadas para entrenar modelos de inteligencia artificial en el sector salud. Su enfoque es la escalabilidad, seguridad y cumplimiento regulatorio en múltiples regiones.

# Lenguaje Ubicuo

Conceptos Clave

  - Imagen Médica: Archivo visual que representa un estudio clínico (Rayos X, Tomografía, Resonancia, Mamografía, Ultrasonido, etc.).
  - Metadatos: Información asociada a una imagen médica, como modalidad, región anatómica, atributos de imagen y diagnóstico asociado.
  - Anonimización: Proceso de eliminación o transformación de información sensible en imágenes médicas para cumplir con regulaciones de privacidad (HIPAA, GDPR).
  - Paciente Pseudonimizado: Identificador único que permite rastrear datos de un mismo paciente sin revelar su identidad real.
  - Centro de Salud: Institución proveedora de imágenes médicas (hospital, clínica, laboratorio, institución gubernamental de salud).
  - Cliente: Empresa, investigador o individuo que consume los datos procesados (desarrollador de IA, centro de investigación, institución reguladora, etc.).
  - Pipeline de Procesamiento: Flujo automatizado de ingestión, anonimización, etiquetado y estructuración de imágenes médicas.
  - Historial Clínico Pseudonimizado: Conjunto de datos longitudinales anonimizados de un mismo paciente a través del tiempo.
  - Región Anatómica: Parte del cuerpo asociada a una imagen médica, como cabeza, tórax, abdomen, musculoesquelético o pélvico.
  - Modalidad de Imagen: Tipo de estudio diagnóstico, como Rayos X, Tomografía Computarizada (CT), Resonancia Magnética (MRI), Ultrasonido (US), entre otros.
  - Condición Médica: Diagnóstico o sospecha clínica asociada a una imagen médica, como neumonía, fracturas, tumores o infecciones.
  - Plataforma de Datos: Interfaz que permite a los clientes acceder, filtrar y descargar imágenes médicas anonimizadas y sus metadatos asociados.
  - Normativa de Protección de Datos: Reglas y regulaciones que rigen la privacidad y el uso de datos médicos, como HIPAA (EE.UU.), GDPR (Europa) y LGPD (Brasil).
  - Multi-Tenancy: Arquitectura que permite gestionar datos segmentados de múltiples clientes y regiones de manera segura e independiente.

Este proyecto se centra en definir el **lenguaje ubicuo** y establecer **contextos acotados** para el proyecto **SaludTech de los Alpes**. Los siguientes puntos han sido documentados:

1. **Documentación de dominios y subdominios**
2. **Creación del lenguaje ubicuo**
3. **Definición de contextos acotados y sus relaciones**

## Estructura del Proyecto

```
Lenguaje-obicuo/
├── src/
│   ├── main/
│   │   ├── cml/
│   │   |   |── 1. dominios-subdominios/
│   │   |   |   |── 1. domains-subdomains-v1.cml (Punto 1)
│   │   |   |── 3. contextos-acotados/ (Punto 3)
│   │   |   |   |── as-is.cml
│   │   |   |   |── to-be.cml
...
```

## 1. Documentación de dominios y subdominios

Los dominios y subdominios se pueden encontrar en la ruta:  
`src/main/cml/dominios-subdominios/1. domains-subdomains-v1.cml`

![image](https://github.com/user-attachments/assets/97f71ad9-fc96-4cf2-a354-6028ebc86ff5)

## 2. Creación del lenguaje ubicuo

El lenguaje ubicuo fue desarrollado en Miro, utilizando la técnica Top-Down, con Event Storming y una vista Big Picture

![image](https://github.com/user-attachments/assets/2c4aae14-a396-40ba-9842-1fb86b925b75)

![image](https://github.com/user-attachments/assets/de3957b5-69dd-4fea-ae78-62437cea57db)


## 3. Definición de contextos acotados y sus relaciones

Las imágenes pueden generarse en las siguientes rutas:

- `src/main/cml/3. contextos-acotados/as-is.cml`
- ![as-is_ContextMap](https://github.com/user-attachments/assets/f5fd5b42-83a3-4d06-808a-78e0a935bb74)
- `src/main/cml/3. contextos-acotados/to-be.cml`
- ![to-be_ContextMap](https://github.com/user-attachments/assets/a8a928c5-25df-422b-8187-5e3ccafbfa17)

### Detalles de Archivos Importantes

- **.gitpod.Dockerfile:**
  - Basado en la imagen `gitpod/workspace-full`.
  - Instala **Graphviz** para la generación de gráficos.
  - Configura Java 11 (versión 11.0.12-tem) utilizando SDKMAN.

- **.gitpod.yml:**
  - Define tareas de inicialización:
    - Da permisos de ejecución a `gradlew` y ejecuta `./gradlew build`.
  - Configura la imagen de Gitpod para usar el Dockerfile personalizado.
  - Incluye extensiones de VS Code necesarias para trabajar con Context Mapper, PlantUML, Java y AsciiDoc.

- **src/main/cml:**
  - Contiene los archivos `.cml` que documentan los dominios, subdominios y contextos acotados.
    - `1. dominios-subdominios/domains-subdomains-v1.cml`
    - `3. contextos-acotados/as-is.cml`
    - `3. contextos-acotados/to-be.cml`

## Instrucciones para Abrir el Repositorio en Gitpod

1. Asegúrate de tener una cuenta en [Gitpod](https://www.gitpod.io/).
2. Clona este repositorio o simplemente abrelo directamente en Gitpod:

   ```bash
   https://gitpod.io/#<URL_DEL_REPOSITORIO>
   ```

3. Gitpod se encargará de:
   - Construir el proyecto automáticamente.
   - Instalar las dependencias necesarias.
   - Configurar el entorno de desarrollo con las extensiones requeridas.

4. Abre los archivos `.cml` dentro del directorio `src/main/cml` para comenzar a trabajar con Context Mapper.

Si hay errores de permisos al abrir Gitpod, puedes hacer un **fork** del repositorio y agregar la URL del nuevo repo después del `#`.  

Ejemplo:  
`https://gitpod.io/#https://github.com/Rabbits-4/lenguaje-ubicuo`


<a href="https://gitpod.io/#https://github.com/Rabbits-4/lenguaje-obicuo" style="padding: 10px;">
    <img src="https://gitpod.io/button/open-in-gitpod.svg" width="150" alt="Push" align="center">
</a>

---

Para cualquier duda, consulta la documentación oficial de [Context Mapper](https://contextmapper.org/).
