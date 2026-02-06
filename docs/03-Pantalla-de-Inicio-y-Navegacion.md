# 3. Pantalla de Inicio y Navegación

## Descripción General

La pantalla de inicio representa el punto de acceso principal a las funcionalidades del Sistema TNL tras la autenticación exitosa. Esta pantalla, denominada formalmente como "Gestión de Novedades" o "Bandeja Principal", constituye el centro de operaciones donde el usuario interactúa con las funciones principales de gestión de cambios laborales (novedades). La interfaz ha sido diseñada siguiendo principios de usabilidad para facilitar la navegación eficiente y el acceso a las herramientas necesarias según el rol del usuario dentro del sistema.

## 3.1 Componentes de la Interfaz Principal

La interfaz del Sistema TNL se organiza en tres bloques funcionales principales que estructuran la experiencia del usuario:

### A. Encabezado (Header)

El encabezado superior de la aplicación contiene los siguientes elementos:

| Elemento | Descripción | Función |
|----------|-------------|---------|
| **Logotipo Institucional** | Banco Contactar (esquina superior izquierda) | Identifica la institución propietaria de la aplicación |
| **Información del Usuario** | Nombre de usuario (ej: "Administrator") | Muestra la identidad del usuario actualmente autenticado en el sistema |
| **Fecha del Sistema** | Formato DD/MM/YYYY (ej: 06/02/2026) | Indica la fecha actual según la configuración del servidor |
| **Opción Finalizar Sesión** | Enlace en color azul (esquina superior derecha) | Permite al usuario cerrar su sesión de trabajo de forma segura |

El encabezado permanece visible en todas las pantallas de la aplicación y facilita la identificación rápida del usuario conectado y la fecha de operación.

### B. Navegación (Menú Lateral)

El sistema implementa un menú de navegación colapsable ubicado en el lado izquierdo de la pantalla. Las características de este componente son:

| Característica | Detalles |
|----------------|---------|
| **Tipo de Navegación** | Menú lateral collapsable (se puede expandir/contraer) |
| **Ubicación** | Lado izquierdo de la interfaz principal |
| **Color de Fondo** | Naranja intenso (marca corporativa Banco Contactar) |
| **Iconografía** | Incluye íconos para cada opción de navegación |
| **Responsividad** | El menú se puede contraer para ampliar el espacio de contenido |
| **Control** | Botón de expansión/contracción (flecha) en la parte inferior izquierda |

#### Opciones Principales del Menú

El menú lateral proporciona acceso a las siguientes funcionalidades según el rol del usuario:

- **Gestión de Novedades**: Acceso a la bandeja principal de novedades
- - **Crear Nueva Novedad**: Opción para registrar una nueva novedad en el sistema
  - - **Reportes**: Acceso a informes y consultas de novedades
    - - **Configuración**: Acceso a opciones de configuración disponibles según permisos
      - - **Sincronización de Directorio**: Gestión de sincronización con Active Directory (para administradores)
       
        - ### C. Área de Contenido Principal
       
        - El área central de la pantalla muestra el contenido dinámico según la sección seleccionada. En la pantalla de inicio, esta área presenta:
       
        - #### 3.1.1 Título de la Sección
       
        - En la parte superior izquierda del área de contenido, aparece el título "Gestión de Novedades" en una tipografía clara y legible, indicando la funcionalidad actual disponible para el usuario.
       
        - #### 3.1.2 Barra de Herramientas de Acción
       
        - Inmediatamente bajo el título se encuentra una barra de herramientas que contiene:
       
        - | Elemento | Tipo | Descripción |
        - |----------|------|-------------|
        - | **Botón AGREGAR** | Botón de acción | Permite crear una nueva novedad en el sistema; color naranja corporativo para visibilidad |
        - | **Campo de Búsqueda por Cédula** | Textbox con ícono de búsqueda | Permite filtrar novedades por número de identificación del empleado |
        - | **Filtro de Estado** | Combobox desplegable | Permite filtrar las novedades mostradas por su estado actual |
       
        - #### 3.1.3 Tabla de Novedades
       
        - La tabla constituye el elemento central de la pantalla y contiene la lista de novedades registradas. Las columnas incluidas son:
       
        - | Columna | Contenido | Tipo de Dato |
        - |---------|-----------|--------------|
        - | **Cédula** | Número de identificación del empleado | Identificador (enlace activo) |
        - | **Tipo** | Categoría de la novedad (Incapacidad, Vacaciones, etc.) | Texto descriptivo |
        - | **Fecha Inicio Novedad** | Fecha de inicio del evento laboral | Formato DD/MM/YYYY |
        - | **Fecha Fin Novedad** | Fecha de terminación del evento laboral | Formato DD/MM/YYYY |
        | **Estado** | Estado actual de procesamiento de la novedad | Categorizado (Aprobado, Pendiente, Devuelto, etc.) |
| **Nombre** | Nombre completo del empleado | Texto |
| **Cargo** | Posición del empleado dentro de la institución | Texto |
| **Oficina** | Ubicación administrativa del empleado | Texto |
| **EPS** | Entidad de Salud asignada al empleado | Texto |
| **Ícono de Acciones** | Menú contextual de operaciones | Ícono (i) |

#### 3.1.4 Características de la Tabla

- **Paginación**: La tabla implementa paginación (Pág. 1 de 1) para manejar listados largos
- - **Ordenamiento**: Las columnas son ordenables haciendo clic en los encabezados
  - - **Interactividad**: El número de cédula funciona como enlace activo para acceder a detalles
    - - **Filas Alternadas**: Color de fondo alternado para facilitar la lectura
     
      - ## 3.2 Contexto de Rol de Usuario
     
      - Las funcionalidades disponibles en la pantalla de inicio varían según el rol asignado al usuario:
     
      - ### Rol TnlNomina (Administrador de Novedades)
     
      - Los usuarios con rol TnlNomina tienen acceso a:
     
      - - **Visualización Completa**: Pueden ver todas las novedades registradas en el sistema
        - - **Gestión de Estados**: Pueden aprobar, devolver o rechazar novedades según el flujo de proceso
          - - **Reportes**: Acceso a reportes consolidados de novedades
            - - **Búsqueda y Filtrado**: Capacidad para buscar y filtrar novedades por múltiples criterios
              - - **Acciones en Registro**: Pueden realizar operaciones sobre registros específicos a través del menú contextual
               
                - ### Rol Colaborador (Empleado)
               
                - Los usuarios colaboradores pueden:
               
                - - **Ver Sus Novedades**: Visualizar únicamente las novedades propias
                  - - **Crear Novedades**: Registrar nuevas novedades mediante el botón AGREGAR
                    - - **Consultar Estado**: Verificar el estado actual de sus solicitudes de novedades
                     
                      - ## 3.3 Navegación Entre Pantallas
                     
                      - ### Desde la Pantalla de Inicio
                     
                      - El usuario puede acceder a diferentes secciones del sistema:
                     
                      - #### 3.3.1 Creación de Nueva Novedad
                     
                      - **Acción**: Hacer clic en el botón **AGREGAR**
                     
                      - **Resultado**: El sistema navega a la pantalla de formulario para crear una nueva novedad, donde se capturan los detalles del evento laboral.
                     
                      - **Pasos**:
                      - 1. El usuario identifica el botón AGREGAR en la barra de herramientas
                        2. 2. Realiza un clic sobre el botón
                           3. 3. El navegador carga la pantalla de creación de novedad
                              4. 4. Se despliega un formulario con campos para completar
                                
                                 5. #### 3.3.2 Consulta de Detalles de Novedad
                                
                                 6. **Acción**: Hacer clic en el número de cédula del empleado en la tabla
                                
                                 7. **Resultado**: El sistema abre la pantalla de detalles de la novedad, permitiendo ver información completa y realizar acciones según permisos.
                                
                                 8. **Pasos**:
                                 9. 1. El usuario localiza el número de cédula en la primera columna de la tabla
                                    2. 2. Realiza un clic sobre el número (que aparece subrayado y en color naranja)
                                       3. 3. Se carga la página de gestión de la novedad específica
                                          4. 4. Se presentan detalles completos y opciones de acción
                                            
                                             5. #### 3.3.3 Aplicación de Filtros
                                            
                                             6. **Búsqueda por Cédula**:
                                             7. 1. El usuario localiza el campo de búsqueda "Cédula" en la barra de herramientas
                                                2. 2. Ingresa el número de identificación del empleado deseado
                                                   3. 3. Realiza clic en el ícono de búsqueda o presiona Enter
                                                      4. 4. La tabla se actualiza mostrando solo las novedades del empleado especificado
                                                        
                                                         5. **Filtrado por Estado**:
                                                         6. 1. El usuario localiza el combobox desplegable "(Ninguno)" en la barra de herramientas
                                                            2. 2. Hace clic en el desplegable para revelar las opciones disponibles
                                                               3. 3. Selecciona el estado deseado de la lista (Pendiente, Aprobado, Devuelto, Anulado, etc.)
                                                                  4. 4. La tabla se actualiza automáticamente mostrando solo novedades en ese estado
                                                                    
                                                                     5. #### 3.3.4 Cerrar Sesión
                                                                    
                                                                     6. **Acción**: Hacer clic en el enlace **Finalizar Sesión** en el encabezado
                                                                    
                                                                     7. **Resultado**: El usuario es desconectado del sistema y retornado a la pantalla de autenticación.
                                                                    
                                                                     8. **Pasos**:
                                                                     9. 1. El usuario localiza el enlace "Finalizar Sesión" en la esquina superior derecha
                                                                        2. 2. Realiza un clic sobre el enlace
                                                                           3. 3. El sistema destruye la sesión de usuario
                                                                              4. 4. Se redirige a la pantalla de "Acceso al Sistema"
                                                                                
                                                                                 5. ## 3.4 Elementos Interactivos y Comportamiento
                                                                                
                                                                                 6. ### Comportamiento del Menú Lateral
                                                                                
                                                                                 7. - **Estado Expandido**: El menú muestra íconos y etiquetas de texto para cada opción
                                                                                    - - **Estado Contraído**: El menú muestra solo los íconos, reduciendo el espacio utilizado
                                                                                      - - **Transición**: La contracción y expansión es suave (animada) para mejorar la experiencia
                                                                                        - - **Persistencia**: El estado del menú (expandido o contraído) se mantiene durante la sesión
                                                                                         
                                                                                          - ### Interactividad de la Tabla
                                                                                         
                                                                                          - - **Cambio de Color al Pasar el Ratón**: Las filas cambian de color cuando el cursor pasa sobre ellas (hover)
                                                                                            - - **Ícono de Información**: Al final de cada fila existe un ícono "(i)" que proporciona acceso a operaciones adicionales
                                                                                              - - **Enlaces Activos**: Los números de cédula son enlaces que naveganen a detalles de la novedad
                                                                                               
                                                                                                - ### Comportamiento del Formulario de Filtrado
                                                                                               
                                                                                                - - **Filtro en Tiempo Real**: Los cambios en los campos de búsqueda y filtrado actualizan la tabla sin necesidad de hacer clic en un botón explícito
                                                                                                  - - **Acumulación de Filtros**: El usuario puede combinar búsqueda por cédula y filtro por estado simultáneamente
                                                                                                    - - **Limpiar Filtros**: Dejar los campos en blanco o seleccionar "(Ninguno)" restaura la visualización de todas las novedades
                                                                                                     
                                                                                                      - ## 3.5 Validaciones y Restricciones
                                                                                                     
                                                                                                      - ### Búsqueda por Cédula
                                                                                                     
                                                                                                      - - **Formato**: Se acepta entrada numérica única
                                                                                                        - - **Validación**: El sistema verifica que la cédula ingresada corresponda a un empleado registrado
                                                                                                          - - **Resultado Vacío**: Si no hay coincidencias, la tabla se muestra vacía y se puede visualizar un mensaje informativo
                                                                                                            - - **Longitud**: Generalmente acepta cédulas de 7 a 10 dígitos según el formato nacional
                                                                                                             
                                                                                                              - ### Combobox de Estado
                                                                                                             
                                                                                                              - - **Opciones Válidas**: Pendiente, Devuelto, Aprobado, Pendiente SST, Confirmar Nómina, Suspendido, Anulado, Transcrito, Reconocido, (Ninguno)
                                                                                                                - - **Valor por Defecto**: "(Ninguno)" - no aplica filtro
                                                                                                                  - - **Selección Única**: Solo se puede seleccionar un estado a la vez
                                                                                                                    - - **Actualización de Tabla**: La actualización ocurre de forma automática
                                                                                                                     
                                                                                                                      - ## 3.6 Indicadores Visuales de Estado
                                                                                                                     
                                                                                                                      - La tabla utiliza códigos de color y etiquetas de texto para indicar el estado de cada novedad:
                                                                                                                     
                                                                                                                      - | Estado | Significado | Color (si aplica) |
                                                                                                                      - |--------|-------------|-------------------|
                                                                                                                      - | **Aprobado** | La novedad ha sido aprobada y procesada | Verde (generalmente) |
                                                                                                                      - | **Pendiente** | La novedad está en espera de aprobación | Amarillo/Naranja (generalmente) |
                                                                                                                      - | **Devuelto** | La novedad fue rechazada y requiere corrección | Rojo (generalmente) |
                                                                                                                      - | **Pendiente SST** | Requiere revisión por parte del área SST (Salud y Seguridad en el Trabajo) | Específico |
                                                                                                                      - | **Confirmar Nómina** | Requiere confirmación por parte del área de Nómina | Específico |
                                                                                                                      - | **Suspendido** | La novedad ha sido suspendida temporalmente | Gris |
                                                                                                                      - | **Anulado** | La novedad ha sido cancelada definitivamente | Gris oscuro |
                                                                                                                      - | **Transcrito** | La novedad ha sido procesada y transcrita | Verde oscuro |
                                                                                                                      - | **Reconocido** | La novedad ha sido oficialmente reconocida | Verde |
                                                                                                                     
                                                                                                                      - ## 3.7 Prácticas Recomendadas para Navegación
                                                                                                                     
                                                                                                                      - ### Para Búsquedas Efectivas
                                                                                                                     
                                                                                                                      - - El usuario debe ingresar cédulas completas para resultados precisos
                                                                                                                        - - Se recomienda limpiar búsquedas anteriores antes de realizar nuevas consultas
                                                                                                                          - - El uso combinado de filtro por cédula y estado acelera la localización de registros
                                                                                                                           
                                                                                                                            - ### Para Eficiencia Operativa
                                                                                                                           
                                                                                                                            - - La navegación mediante clic en cédulas es más rápida que el uso de filtros para acceso a novedades específicas
                                                                                                                              - - El filtro por estado es útil para identificar novedades que requieren acción inmediata (Pendiente, Devuelto)
                                                                                                                                - - Se recomienda revisar regularmente el estado "Pendiente SST" para asegurar cumplimiento normativo
                                                                                                                                 
                                                                                                                                  - ### Para Gestión de Sesiones
                                                                                                                                 
                                                                                                                                  - - Siempre utilizar "Finalizar Sesión" en lugar de cerrar la ventana del navegador directamente
                                                                                                                                    - - Este procedimiento asegura que la sesión se destruya correctamente en el servidor
                                                                                                                                      - - Previene problemas de autenticación en inicios de sesión posteriores
                                                                                                                                       
                                                                                                                                        - ## 3.8 Acceso a Funcionalidades Secundarias
                                                                                                                                       
                                                                                                                                        - ### Menú Contextual de Filas
                                                                                                                                       
                                                                                                                                        - El ícono "(i)" al final de cada fila en la tabla abre un menú contextual con opciones como:
                                                                                                                                        
                                                                                                                                        - **Ver Detalles**: Accede a la información completa de la novedad
                                                                                                                                        - - **Editar**: Permite modificar la novedad (según permisos)
                                                                                                                                          - - **Eliminar**: Permite remover la novedad (según permisos y estado)
                                                                                                                                            - - **Aprobar/Rechazar**: Opciones de gestión disponibles según el rol y estado actual
                                                                                                                                              - - **Descargar**: Permite exportar la información en formato PDF o Excel (si está disponible)
                                                                                                                                               
                                                                                                                                                - ## 3.9 Integración con Otras Secciones
                                                                                                                                               
                                                                                                                                                - La pantalla de inicio se conecta con las siguientes secciones del sistema:
                                                                                                                                               
                                                                                                                                                - | Sección | Acceso Desde | Descripción |
                                                                                                                                                - |---------|-------------|-------------|
                                                                                                                                                - | **Crear Nueva Novedad (Sección 4)** | Botón AGREGAR | Formulario completo para captura de datos |
                                                                                                                                                - | **Detalles de Novedad** | Clic en cédula | Pantalla de gestión individual de novedades |
                                                                                                                                                - | **Reportes (Sección 8)** | Menú lateral | Información consolidada y análisis |
                                                                                                                                                - | **Configuración** | Menú lateral | Ajustes de usuario y preferencias |
                                                                                                                                                - | **Autenticación (Sección 2)** | Finalizar Sesión | Retorno a la pantalla de acceso |
                                                                                                                                               
                                                                                                                                                - ## 3.10 Solución de Problemas Comunes
                                                                                                                                               
                                                                                                                                                - ### La tabla no muestra resultados
                                                                                                                                               
                                                                                                                                                - **Causa Posible**: Se han aplicado filtros que no generan coincidencias
                                                                                                                                               
                                                                                                                                                - **Solución**:
                                                                                                                                                - 1. Limpiar el campo de búsqueda de cédula
                                                                                                                                                  2. 2. Cambiar el combobox de estado a "(Ninguno)"
                                                                                                                                                     3. 3. Presionar Enter o esperar a que se actualice la tabla automáticamente
                                                                                                                                                       
                                                                                                                                                        4. ### El menú lateral no aparece
                                                                                                                                                       
                                                                                                                                                        5. **Causa Posible**: El menú está colapsado
                                                                                                                                                       
                                                                                                                                                        6. **Solución**:
                                                                                                                                                        7. 1. Localizar el botón de expansión/contracción (flecha) en la parte inferior izquierda
                                                                                                                                                           2. 2. Hacer clic en el botón para expandir el menú
                                                                                                                                                              3. 3. El menú debe aparecer con las opciones de navegación
                                                                                                                                                                
                                                                                                                                                                 4. ### No se puede hacer clic en el botón AGREGAR
                                                                                                                                                                
                                                                                                                                                                 5. **Causa Posible**: Permisos insuficientes o carga de página incompleta
                                                                                                                                                                
                                                                                                                                                                 6. **Solución**:
                                                                                                                                                                 7. 1. Recargar la página (F5 o Ctrl+R)
                                                                                                                                                                    2. 2. Verificar que la sesión esté activa
                                                                                                                                                                       3. 3. Consultar con el administrador si el problema persiste
                                                                                                                                                                         
                                                                                                                                                                          4. ### El filtro por estado no actualiza la tabla
                                                                                                                                                                         
                                                                                                                                                                          5. **Causa Posible**: Problemas de actualización de JavaScript en el navegador
                                                                                                                                                                         
                                                                                                                                                                          6. **Solución**:
                                                                                                                                                                          7. 1. Limpiar el caché del navegador
                                                                                                                                                                             2. 2. Recargar la página completamente (Ctrl+Shift+R)
                                                                                                                                                                                3. 3. Probar con navegador diferente si el problema persiste
                                                                                                                                                                                  
                                                                                                                                                                                   4. ## 3.11 Información de Soporte
                                                                                                                                                                                  
                                                                                                                                                                                   5. Para asistencia técnica relacionada con la navegación y funcionalidades de la pantalla de inicio:
                                                                                                                                                                                  
                                                                                                                                                                                   6. | Tipo de Problema | Contacto | Horario |
                                                                                                                                                                                   7. |-----------------|----------|--------|
                                                                                                                                                                                   8. | **Problemas de Navegación** | help-desk@bancocontactar.com | Lunes a Viernes, 8:00 AM - 5:00 PM |
                                                                                                                                                                                   9. | **Acceso a Funcionalidades** | sistemas@bancocontactar.com | Lunes a Viernes, 8:00 AM - 6:00 PM |
                                                                                                                                                                                   10. | **Errores de Sistema** | soporte-tnl@bancocontactar.com | 24/7 (urgencias) |
                                                                                                                                                                                   11. | **Consultas Administrativas** | administrador-tnl@bancocontactar.com | Lunes a Viernes, 9:00 AM - 4:00 PM |
                                                                                                                                                                                  
                                                                                                                                                                                   12. ## 3.12 Próximos Pasos
                                                                                                                                                                                  
                                                                                                                                                                                   13. Una vez el usuario comprenda la estructura y navegación de la pantalla de inicio, puede proceder a:
                                                                                                                                                                                  
                                                                                                                                                                                   14. 1. **Crear una Nueva Novedad**: Utilizando el botón AGREGAR (Sección 4)
                                                                                                                                                                                       2. 2. **Consultar Novedades Existentes**: Haciendo clic en números de cédula en la tabla
                                                                                                                                                                                          3. 3. **Aplicar Filtros Avanzados**: Utilizando combinaciones de búsqueda y estado
                                                                                                                                                                                             4. 4. **Acceder a Reportes**: Mediante el menú lateral para análisis consolidados
                                                                                                                                                                                                5. 5. **Gestionar Configuración**: Ajustando preferencias personales del usuario
