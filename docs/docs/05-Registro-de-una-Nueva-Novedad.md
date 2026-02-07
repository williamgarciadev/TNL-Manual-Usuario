# 5. Registro de una Nueva Novedad

## Descripción General

El registro o creación de una nueva novedad en el Sistema TNL constituye el procedimiento fundamental mediante el cual los usuarios autorizados del sistema, principalmente colaboradores y administradores de recursos humanos, ingresan información sobre cambios o eventos laborales que afectan la condición del empleado. Esta funcionalidad proporciona un formulario estructurado y validado que captura todos los datos esenciales requeridos para procesar correctamente una novedad dentro del flujo de gestión del Sistema TNL de Banco Contactar.

## 5.1 Acceso al Formulario de Registro

### 5.1.1 Navegación desde la Pantalla de Inicio

**Descripción del Procedimiento:**

El acceso al formulario de creación de novedad se realiza desde la pantalla principal de Gestión de Novedades. El procedimiento es el siguiente:

**Pasos Detallados:**

1. El usuario debe estar autenticado en el Sistema TNL
2. 2. El usuario accede a la pantalla de "Gestión de Novedades" (pantalla inicial tras autenticación)
   3. 3. En la barra de herramientas, el usuario localiza el botón **AGREGAR** de color naranja
      4. 4. El usuario realiza un clic sobre el botón **AGREGAR**
         5. 5. El navegador carga la pantalla de formulario con el título "Crear Novedad"
            6. 6. El formulario aparece en blanco (excepto por el campo Cédula que puede estar pre-llenado)
              
               7. ### 5.1.2 Permisos Requeridos
              
               8. Para acceder al formulario de creación de novedad, el usuario debe contar con uno de los siguientes roles:
              
               9. - **Colaborador**: Puede crear novedades propias (limitado a su propia cédula)
                  - - **TnlNomina**: Puede crear novedades para cualquier empleado del sistema
                    - - **Administrador**: Acceso completo al formulario con todas las funcionalidades
                     
                      - **Nota:** Los usuarios sin los permisos adecuados verán el botón AGREGAR deshabilitado o no disponible.
                     
                      - ## 5.2 Estructura del Formulario
                     
                      - El formulario "Crear Novedad" está organizado en una secuencia lógica de campos que guía al usuario a través del proceso de captura de datos.
                     
                      - ### 5.2.1 Encabezado del Formulario
                     
                      - - **Título Visible**: "Crear Novedad" aparece en la parte superior izquierda en una tipografía clara y grande
                        - - **Identificación**: El formulario se identifica unívocamente como la pantalla de creación de nuevas novedades
                          - - **Consistencia**: El encabezado mantiene el mismo color de fondo naranja corporativo
                           
                            - ## 5.3 Campos del Formulario
                           
                            - A continuación se describe cada campo del formulario con sus características, tipos de datos y validaciones:
                           
                            - ### 5.3.1 Campo: Cédula
                           
                            - **Denominación:** Cédula
                           
                            - **Tipo de Campo:** Textbox de entrada de texto
                           
                            - **Descripción:**
                            - El campo Cédula captura el número de identificación del empleado para quien se registra la novedad. Este campo es fundamental ya que vincula la novedad a un empleado específico en el sistema.
                           
                            - **Características:**
                            - - Puede estar pre-llenado si se accede desde una búsqueda o registro específico
                              - - Generalmente contiene el identificador único del empleado
                                - - Ejemplo de valor: 1085266307
                                 
                                  - **Validación:**
                                  - - Formato: Numérico solamente (7-10 dígitos según estándar nacional)
                                    - - Requerido: Sí - debe completarse
                                      - - El sistema valida que la cédula corresponda a un empleado registrado
                                        - - Si la cédula no existe, se genera un error de validación
                                          - - Mensaje de error típico: "La cédula ingresada no existe en el sistema"
                                           
                                            - **Comportamiento:**
                                            - - Si el usuario intenta completar sin esta cédula, el sistema rechaza el envío
                                              - - Pueden ingresarse cédulas de empleados diferentes al usuario conectado (si tiene permisos)
                                                - - El campo no acepta espacios en blanco ni caracteres especiales
                                                 
                                                  - ### 5.3.2 Campo: Nombre
                                                 
                                                  - **Denominación:** Nombre
                                                 
                                                  - **Tipo de Campo:** Textbox de entrada de texto (solo lectura o automático)
                                                 
                                                  - **Descripción:**
                                                  - El campo Nombre muestra el nombre completo del empleado cuya cédula fue ingresada. Generalmente este campo se completa de forma automática desde la base de datos.
                                                 
                                                  - **Características:**
                                                  - - Normalmente es un campo de solo lectura (no editable)
                                                    - - Se auto-completa cuando se ingresa una cédula válida
                                                      - - Ejemplo: "BOTINA PAZOS BYRON ALFREDO"
                                                        - - Puede permanecer vacío si no hay empleado asociado a la cédula
                                                         
                                                          - **Validación:**
                                                          - - Validación: La información proviene de la base de datos maestra de empleados
                                                            - - Requerido: No - es informativo
                                                              - - No valida entrada del usuario (es solo lectura)
                                                               
                                                                - **Comportamiento:**
                                                                - - Al cambiar la cédula, el nombre se actualiza automáticamente
                                                                  - - Si la cédula no existe, el nombre permanece vacío
                                                                    - - Este campo ayuda a confirmar que se seleccionó al empleado correcto
                                                                     
                                                                      - ### 5.3.3 Campo: Fecha Inicio Novedad
                                                                     
                                                                      - **Denominación:** Fecha Inicio Novedad
                                                                     
                                                                      - **Tipo de Campo:** Textbox con selector de fecha (Date picker)
                                                                     
                                                                      - **Descripción:**
                                                                      - Este campo captura la fecha en que comienza el evento laboral registrado como novedad. Es fundamental para establecer la fecha de inicio del período afectado.
                                                                     
                                                                      - **Características:**
                                                                      - - Formato de entrada: DD/MM/YYYY (ejemplo: 06/02/2026)
                                                                        - - Incluye un botón auxiliar con ícono de calendario para seleccionar la fecha
                                                                          - - Permite entrada manual de la fecha o selección mediante calendario
                                                                            - - Campo obligatorio para la mayoría de tipos de novedad

                                                                            **Validación:**
                                                                            - Requerido: Sí - obligatorio
                                                                            - - Formato: DD/MM/YYYY
                                                                              - - Debe ser una fecha válida del calendario
                                                                                - - No acepta fechas futuras según muchos tipos de novedad
                                                                                  - - La fecha inicio no debe ser posterior a la fecha fin
                                                                                    - - Validación de fecha mínima: Normalmente permite fechas desde el inicio del año fiscal actual
                                                                                      - - Mensaje de error típico: "Ingrese una fecha válida en formato DD/MM/YYYY"
                                                                                        - - Mensaje de error típico: "La fecha inicio no puede ser mayor que la fecha fin"
                                                                                         
                                                                                          - **Comportamiento:**
                                                                                          - - Al hacer clic en el ícono de calendario, se abre un selector de fecha interactivo
                                                                                            - - El usuario puede escribir la fecha manualmente o seleccionarla del calendario
                                                                                              - - La fecha es vinculante para el período de la novedad
                                                                                                - - Se utiliza para calcular el número de días afectados
                                                                                                 
                                                                                                  - ### 5.3.4 Campo: Fecha Fin Novedad
                                                                                                 
                                                                                                  - **Denominación:** Fecha Fin Novedad
                                                                                                 
                                                                                                  - **Tipo de Campo:** Textbox con selector de fecha (Date picker)
                                                                                                 
                                                                                                  - **Descripción:**
                                                                                                  - Este campo captura la fecha en que termina el evento laboral registrado como novedad. Define el último día del período de afectación.
                                                                                                 
                                                                                                  - **Características:**
                                                                                                  - - Formato de entrada: DD/MM/YYYY (ejemplo: 13/02/2026)
                                                                                                    - - Incluye un botón auxiliar con ícono de calendario
                                                                                                      - - Permite entrada manual o selección mediante calendario
                                                                                                        - - Interdependencia con Fecha Inicio
                                                                                                         
                                                                                                          - **Validación:**
                                                                                                          - - Requerido: Sí - obligatorio
                                                                                                            - - Formato: DD/MM/YYYY
                                                                                                              - - Debe ser una fecha válida
                                                                                                                - - Debe ser mayor o igual a la Fecha Inicio Novedad
                                                                                                                  - - Validación de coherencia: La fecha fin siempre debe ser posterior o igual a la fecha inicio
                                                                                                                    - - Mensaje de error típico: "La fecha fin debe ser mayor o igual a la fecha inicio"
                                                                                                                      - - Rango típico: Generalmente no puede exceder 180 días desde la fecha inicio
                                                                                                                       
                                                                                                                        - **Comportamiento:**
                                                                                                                        - - Al cambiar la Fecha Inicio, la validación de Fecha Fin se recalcula
                                                                                                                          - - El período entre fechas determina la duración de la novedad
                                                                                                                            - - Crítico para cálculos de nómina y auditoría
                                                                                                                             
                                                                                                                              - ### 5.3.5 Campo: Tipo
                                                                                                                             
                                                                                                                              - **Denominación:** Tipo
                                                                                                                             
                                                                                                                              - **Tipo de Campo:** Combobox desplegable (Select)
                                                                                                                             
                                                                                                                              - **Descripción:**
                                                                                                                              - El campo Tipo especifica la categoría o clasificación de la novedad que se está registrando. Este campo determina el procesamiento específico que recibirá la novedad en el sistema.
                                                                                                                             
                                                                                                                              - **Características:**
                                                                                                                              - - Interfaz: Combobox desplegable con lista de opciones
                                                                                                                                - - Valor por defecto: "(Ninguno)" - opción no seleccionada
                                                                                                                                  - - Selección única: Solo se puede seleccionar un tipo a la vez
                                                                                                                                    - - Obligatorio: Debe seleccionarse un tipo específico (no "(Ninguno)")
                                                                                                                                     
                                                                                                                                      - **Opciones Disponibles:**
                                                                                                                                     
                                                                                                                                      - | Código | Tipo | Descripción |
                                                                                                                                      - |--------|------|-------------|
                                                                                                                                      - | (Ninguno) | Sin Especificar | Opción inicial - debe cambiarse |
                                                                                                                                      - | V | Vacaciones | Período de descanso remunerado del empleado |
                                                                                                                                      - | R | Licencias Remuneradas | Ausencia justificada con pago de salario |
                                                                                                                                      - | N | Licencias No Remuneradas | Ausencia justificada sin pago de salario |
                                                                                                                                      - | C | Suspención de Contrato | Interrupción temporal del contrato laboral |
                                                                                                                                      - | A | Ausencia No Justificada | Falta o inasistencia injustificada |
                                                                                                                                      - | I | Incapacidad | Ausencia por incapacidad médica o enfermedad |
                                                                                                                                      - | M | Licencia de Maternidad | Permiso remunerado por maternidad |
                                                                                                                                      - | P | Licencia de Paternidad | Permiso remunerado por paternidad |
                                                                                                                                     
                                                                                                                                      - **Validación:**
                                                                                                                                      - - Requerido: Sí - obligatorio
                                                                                                                                        - - Selección válida: No puede dejarse en "(Ninguno)"
                                                                                                                                          - - El sistema valida que el tipo seleccionado sea apropiado para el empleado
                                                                                                                                            - - Algunos tipos pueden tener restricciones según rol del usuario
                                                                                                                                              - - Mensaje de error: "Debe seleccionar un tipo de novedad"
                                                                                                                                               
                                                                                                                                                - **Comportamiento:**
                                                                                                                                                - - Al seleccionar un tipo, pueden habilitarse campos adicionales según el tipo
                                                                                                                                                  - - El tipo seleccionado determina el flujo de aprobación posterior
                                                                                                                                                    - - Distintos tipos pueden requerir documentación adicional (no en este formulario inicial)
                                                                                                                                                      - - El tipo afecta el cálculo de nómina y el tratamiento contable
                                                                                                                                                       
                                                                                                                                                        - ### 5.3.6 Campo: Observación Devolución
                                                                                                                                                       
                                                                                                                                                        - **Denominación:** Observación Devolución
                                                                                                                                                       
                                                                                                                                                        - **Tipo de Campo:** Textbox de texto larga (Textarea)
                                                                                                                                                       
                                                                                                                                                        - **Descripción:**
                                                                                                                                                        - Este campo permite al usuario (especialmente administradores) registrar observaciones, notas o comentarios sobre la novedad. Es particularmente útil cuando se devuelve una novedad rechazada para indicar las razones o recomendaciones.
                                                                                                                                                       
                                                                                                                                                        - **Características:**
                                                                                                                                                        - - Tipo: Área de texto multi-línea
                                                                                                                                                          - - Capacidad: Acepta texto largo con saltos de línea
                                                                                                                                                            - - Carácter optativo: No es obligatorio para crear la novedad
                                                                                                                                                              - - Uso principal: Documentación de devoluciones o rechazos
                                                                                                                                                                - - Ejemplo: "Se requiere documentación médica adicional" o "Falta aprobación del jefe inmediato"
                                                                                                                                                                 
                                                                                                                                                                  - **Validación:**
                                                                                                                                                                  - - Requerido: No - es opcional
                                                                                                                                                                    - - Longitud máxima: Generalmente 500-1000 caracteres
                                                                                                                                                                      - - Caracteres especiales: Se aceptan la mayoría de caracteres
                                                                                                                                                                        - - Validación: Sin validaciones especiales (puramente informativa)
                                                                                                                                                                         
                                                                                                                                                                          - **Comportamiento:**
                                                                                                                                                                          - - El campo aparece típicamente oculto o deshabilitado en el formulario de creación inicial
                                                                                                                                                                            - - Se habilita principalmente cuando se está rechazando o devolviendo una novedad
                                                                                                                                                                              - - Su contenido se registra en el historial de la novedad
                                                                                                                                                                                - - Es importante para auditoría y comunicación interna
                                                                                                                                                                                 
                                                                                                                                                                                  - ## 5.4 Procedimiento Paso a Paso para Crear una Novedad
                                                                                                                                                                                 
                                                                                                                                                                                  - A continuación se presenta un procedimiento detallado para completar y enviar el formulario de creación de novedad:
                                                                                                                                                                                 
                                                                                                                                                                                  - ### Paso 1: Verificar la Cédula del Empleado
                                                                                                                                                                                 
                                                                                                                                                                                  - 1. El usuario accede al formulario "Crear Novedad"
                                                                                                                                                                                  2. Examina el campo Cédula (que puede estar pre-llenado o vacío)
                                                                                                                                                                                  3. 3. Si la cédula es incorrecta, borra el contenido y escribe la cédula correcta
                                                                                                                                                                                     4. 4. Confirmación: Verifica que el campo Nombre se auto-complete con el nombre del empleado
                                                                                                                                                                                       
                                                                                                                                                                                        5. ### Paso 2: Ingresar la Fecha Inicio de la Novedad
                                                                                                                                                                                        6. 
                                                                                                                                                                                        1. El usuario localiza el campo "Fecha Inicio Novedad"
                                                                                                                                                                                        2. 2. Opción A - Entrada Manual:
                                                                                                                                                                                           3.    - Hace clic en el textbox y escribe la fecha en formato DD/MM/YYYY
                                                                                                                                                                                                 -    - Ejemplo: 06/02/2026
                                                                                                                                                                                                      - 3. Opción B - Selección con Calendario:
                                                                                                                                                                                                        4.    - Hace clic en el ícono de calendario azul
                                                                                                                                                                                                              -    - Se abre un selector de fecha interactivo
                                                                                                                                                                                                                   -    - Navega al mes y año deseado
                                                                                                                                                                                                                        -    - Selecciona el día haciendo clic en el número
                                                                                                                                                                                                                             -    - El formulario se actualiza con la fecha seleccionada
                                                                                                                                                                                                                                  - 4. El sistema valida el formato automáticamente
                                                                                                                                                                                                                                   
                                                                                                                                                                                                                                    5. ### Paso 3: Ingresar la Fecha Fin de la Novedad
                                                                                                                                                                                                                                   
                                                                                                                                                                                                                                    6. 1. El usuario localiza el campo "Fecha Fin Novedad"
                                                                                                                                                                                                                                       2. 2. Sigue el mismo proceso que en el Paso 2
                                                                                                                                                                                                                                          3. 3. Importante: Asegurarse de que Fecha Fin >= Fecha Inicio
                                                                                                                                                                                                                                          4. El sistema valida la relación entre fechas automáticamente
                                                                                                                                                                                                                                         
                                                                                                                                                                                                                                          5. ### Paso 4: Seleccionar el Tipo de Novedad
                                                                                                                                                                                                                                          
                                                                                                                                                                                                                                          1. El usuario localiza el combobox "Tipo"
                                                                                                                                                                                                                                          2. Hace clic en el combobox para abrir la lista desplegable
                                                                                                                                                                                                                                          3. Revisa las opciones disponibles:
                                                                                                                                                                                                                                          4.    - Vacaciones
                                                                                                                                                                                                                                                -    - Licencias remuneradas
                                                                                                                                                                                                                                                     -    - Licencias no remuneradas
                                                                                                                                                                                                                                                          -    - Suspención de contrato
                                                                                                                                                                                                                                                               -    - Ausencia no justificada
                                                                                                                                                                                                                                                                    -    - Incapacidad
                                                                                                                                                                                                                                                                         -    - Licencia de maternidad
                                                                                                                                                                                                                                                                              -    - Licencia de paternidad
                                                                                                                                                                                                                                                                                   - 4. Selecciona el tipo apropiado haciendo clic sobre la opción
                                                                                                                                                                                                                                                                                     5. 5. El combobox se actualiza mostrando la selección
                                                                                                                                                                                                                                                                                       
                                                                                                                                                                                                                                                                                        6. ### Paso 5: Completar Observaciones (Opcional)
                                                                                                                                                                                                                                                                                       
                                                                                                                                                                                                                                                                                        7. 1. Si es necesario, el usuario localiza el campo "Observación Devolución"
                                                                                                                                                                                                                                                                                           2. 2. Hace clic en el área de texto
                                                                                                                                                                                                                                                                                              3. 3. Escribe observaciones relevantes sobre la novedad
                                                                                                                                                                                                                                                                                                 4. 4. Ejemplo: Motivo del rechazo previo, documentación incluida, etc.
                                                                                                                                                                                                                                                                                                 5. Este paso es opcional en la creación inicial
                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                 6. ### Paso 6: Validación de Datos
                                                                                                                                                                                                                                                                                                 
                                                                                                                                                                                                                                                                                                 Antes de enviar, el usuario debe verificar:
                                                                                                                                                                                                                                                                                                 
                                                                                                                                                                                                                                                                                                 - ✓ La cédula es válida y corresponde al empleado correcto
                                                                                                                                                                                                                                                                                                 - - ✓ El nombre del empleado aparece correctamente
                                                                                                                                                                                                                                                                                                   - - ✓ La Fecha Inicio está en formato correcto (DD/MM/YYYY)
                                                                                                                                                                                                                                                                                                     - - ✓ La Fecha Fin está en formato correcto y es >= Fecha Inicio
                                                                                                                                                                                                                                                                                                       - - ✓ Se ha seleccionado un Tipo válido (no "(Ninguno)")
                                                                                                                                                                                                                                                                                                         - - ✓ Si hay observaciones, son claras y profesionales
                                                                                                                                                                                                                                                                                                          
                                                                                                                                                                                                                                                                                                           - ### Paso 7: Envío del Formulario
                                                                                                                                                                                                                                                                                                          
                                                                                                                                                                                                                                                                                                           - 1. El usuario localiza el botón **AGREGAR** en la parte inferior del formulario
                                                                                                                                                                                                                                                                                                             2. 2. Verifica que sea la acción deseada
                                                                                                                                                                                                                                                                                                                3. 3. Realiza un clic sobre el botón **AGREGAR**
                                                                                                                                                                                                                                                                                                                4. El sistema procesa el formulario
                                                                                                                                                                                                                                                                                                                5. 5. Si hay errores de validación, aparecen mensajes descriptivos
                                                                                                                                                                                                                                                                                                                   6. 6. Si el envío es exitoso, se redirige a una pantalla de confirmación o a la bandeja
                                                                                                                                                                                                                                                                                                                     
                                                                                                                                                                                                                                                                                                                      7. ### Paso 8: Retorno o Cancelación
                                                                                                                                                                                                                                                                                                                      
                                                                                                                                                                                                                                                                                                                      1. Si el usuario desea cancelar sin guardar:
                                                                                                                                                                                                                                                                                                                      2.    - Localiza el botón **VOLVER** en la parte inferior
                                                                                                                                                                                                                                                                                                                            -    - Realiza un clic sobre el botón
                                                                                                                                                                                                                                                                                                                               - Retorna a la pantalla de Gestión de Novedades sin guardar cambios
                                                                                                                                                                                                                                                                                                                               - 2. Los datos no guardados se pierden
                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                 3. ## 5.5 Validaciones y Manejo de Errores
                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                 4. ### 5.5.1 Errores Comunes y Soluciones
                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                 5. **Error 1: Cédula no válida**
                                                                                                                                                                                                                                                                                                                                 - **Síntoma**: Mensaje "La cédula ingresada no existe en el sistema"
                                                                                                                                                                                                                                                                                                                                 - - **Causa**: El número de cédula no corresponde a ningún empleado registrado
                                                                                                                                                                                                                                                                                                                                   - - **Solución**:
                                                                                                                                                                                                                                                                                                                                     -   1. Verificar que el número de cédula sea correcto
                                                                                                                                                                                                                                                                                                                                         2.   2. Revisar la cédula en el documento de identificación del empleado
                                                                                                                                                                                                                                                                                                                                              3.   3. Consultar con Recursos Humanos si la cédula aún no está registrada
                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                                   4. **Error 2: Formato de fecha inválido**
                                                                                                                                                                                                                                                                                                                                                   5. - **Síntoma**: Mensaje "Ingrese una fecha válida en formato DD/MM/YYYY"
                                                                                                                                                                                                                                                                                                                                                      - - **Causa**: La fecha ingresada no sigue el formato requerido
                                                                                                                                                                                                                                                                                                                                                        - - **Solución**:
                                                                                                                                                                                                                                                                                                                                                          -   1. Usar el calendario para seleccionar la fecha en lugar de escribirla manualmente
                                                                                                                                                                                                                                                                                                                                                              2.   2. Verificar que el separador sea "/" (barra diagonal)
                                                                                                                                                                                                                                                                                                                                                                   3.   3. Ejemplo correcto: 06/02/2026
                                                                                                                                                                                                                                                                                                                                                                        4.   4. Ejemplo incorrecto: 2026-02-06 o 6-2-26
                                                                                                                                                                                                                                                                                                                                                                          
                                                                                                                                                                                                                                                                                                                                                                             5. **Error 3: Fecha Inicio mayor que Fecha Fin**
                                                                                                                                                                                                                                                                                                                                                                             6. - **Síntoma**: Mensaje "La fecha fin debe ser mayor o igual a la fecha inicio"
                                                                                                                                                                                                                                                                                                                                                                                - - **Causa**: La Fecha Fin ingresada es anterior a la Fecha Inicio
                                                                                                                                                                                                                                                                                                                                                                                  - - **Solución**:
                                                                                                                                                                                                                                                                                                                                                                                    -   1. Revisar ambas fechas cuidadosamente
                                                                                                                                                                                                                                                                                                                                                                                        2.   2. Intercambiar los valores si están invertidos
                                                                                                                                                                                                                                                                                                                                                                                             3.   3. Verificar el período específico de la novedad
                                                                                                                                                                                                                                                                                                                                                                                               
                                                                                                                                                                                                                                                                                                                                                                                                  4. **Error 4: Tipo de Novedad no seleccionado**
                                                                                                                                                                                                                                                                                                                                                                                                  5. - **Síntoma**: Mensaje "Debe seleccionar un tipo de novedad"
                                                                                                                                                                                                                                                                                                                                                                                                     - - **Causa**: El campo Tipo permanece en "(Ninguno)"
                                                                                                                                                                                                                                                                                                                                                                                                       - - **Solución**:
                                                                                                                                                                                                                                                                                                                                                                                                         -   1. Hacer clic en el combobox "Tipo"
                                                                                                                                                                                                                                                                                                                                                                                                             2.   2. Seleccionar una opción específica de la lista
                                                                                                                                                                                                                                                                                                                                                                                                                  3.   3. Confirmar que se mostró la selección en el campo
                                                                                                                                                                                                                                                                                                                                                                                                                    
                                                                                                                                                                                                                                                                                                                                                                                                                       4. **Error 5: "Modo de transacción no válido"**
                                                                                                                                                                                                                                                                                                                                                                                                                       5. - **Síntoma**: Mensaje genérico "Modo de transacción no válido"
                                                                                                                                                                                                                                                                                                                                                                                                                          - - **Causa**: Problema de sesión o estado de la base de datos
                                                                                                                                                                                                                                                                                                                                                                                                                            - - **Solución**:
                                                                                                                                                                                                                                                                                                                                                                                                                              -   1. Recargar la página (F5)
                                                                                                                                                                                                                                                                                                                                                                                                                                  2.   2. Volver a llenar el formulario
                                                                                                                                                                                                                                                                                                                                                                                                                                       3.   3. Si persiste, contactar al equipo de soporte técnico
                                                                                                                                                                                                                                                                                                                                                                                                                                            4.   4. Puede indicar que el servidor está en mantenimiento
                                                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                                                                 5. ### 5.5.2 Validaciones Automáticas
                                                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                                                                 6. El sistema realiza automáticamente las siguientes validaciones:
                                                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                                                                 7. | Validación | Criterio | Mensaje de Error |
                                                                                                                                                                                                                                                                                                                                                                                                                                                 8. |------------|----------|-----------------|
                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Cédula | Existencia en BD | "La cédula no existe" |
| Fecha Inicio | Formato DD/MM/YYYY | "Formato inválido" |
                                                     
| Fecha Fin | Mayor que Inicio | "Fecha fin inválida" || Tipo | No "(Ninguno)" | "Seleccione tipo" |
| Rango de Fechas | Máximo 180 días | "Período demasiado largo" |
| Fechas Futuras | Según tipo de novedad | Puede rechazarse |

## 5.6 Ejemplos de Creación de Novedades

### Ejemplo 1: Registro de Vacaciones

**Datos a Ingresar:**
- Cédula: 1085266307
- - Nombre: BOTINA PAZOS BYRON ALFREDO (auto-completa)
  - - Fecha Inicio Novedad: 06/02/2026
    - - Fecha Fin Novedad: 13/02/2026
      - - Tipo: Vacaciones
        - - Observación: (vacío)
         
          - **Resultado Esperado:** La novedad se registra exitosamente con período de 8 días de vacaciones.
         
          - ### Ejemplo 2: Registro de Incapacidad
         
          - **Datos a Ingresar:**
          - - Cédula: 1234567890
            - - Nombre: (Se auto-completa con nombre del empleado)
              - - Fecha Inicio Novedad: 09/02/2026
                - - Fecha Fin Novedad: 18/02/2026
                  - - Tipo: Incapacidad
                    - - Observación: Incapacidad por procedimiento médico menor, documento EPS adjuntado
                     
                      - **Resultado Esperado:** La novedad se registra y queda en estado "Pendiente" para revisión médica.
                     
                      - ### Ejemplo 3: Registro de Licencia No Remunerada
                     
                      - **Datos a Ingresar:**
                      - - Cédula: 123456789
                        - - Nombre: (Se auto-completa)
                          - - Fecha Inicio Novedad: 20/02/2026
                            - - Fecha Fin Novedad: 20/02/2026
                              - - Tipo: Licencias no remuneradas
                                - - Observación: Asuntos personales - 1 día
                                 
                                  - **Resultado Esperado:** Se registra novedad de un día de licencia no remunerada.
                                 
                                  - ## 5.7 Flujo de Procesamiento Posterior
                                 
                                  - ### Estados de la Novedad Después del Registro
                                 
                                  - Una vez registrada la novedad, el sistema la coloca en uno de estos estados iniciales:
                                 
                                  - - **Pendiente**: Requiere aprobación del jefe inmediato o administrador
                                    - - **Pendiente SST**: Si requiere revisión de Salud y Seguridad en el Trabajo
                                      - - **Confirmar Nómina**: Si requiere confirmación de disponibilidad de saldo
                                        - - **Aprobado**: En casos donde se auto-aprueba según permisos
                                          - - **Devuelto**: Si hay validaciones automáticas que fallan
                                           
                                            - ### Acciones Posteriores
                                           
                                            - Después de crear la novedad, el usuario puede:
                                           
                                            - 1. Ver el registro en la "Gestión de Novedades"
                                              2. 2. Editar la novedad si aún está en estado "Pendiente" (según permisos)
                                                 3. 3. Revisar el estado de aprobación
                                                    4. 4. Recibir notificaciones de cambios de estado
                                                       5. 5. Ver la novedad en reportes y auditoría
                                                         
                                                          6. ## 5.8 Consideraciones de Seguridad y Auditoría
                                                         
                                                          7. ### Seguridad
                                                         
                                                          8. - **Registro de Acceso**: Todas las creaciones de novedades se registran con usuario, fecha y hora
                                                             - - **Validación de Permisos**: El sistema valida que el usuario tenga autorización para crear novedades
                                                               - - **Integridad de Datos**: Los datos se validan antes de insertarse en la base de datos
                                                                 - - **Prevención de Duplicados**: El sistema detecta novedades duplicadas o conflictivas
                                                                  
                                                                   - ### Auditoría
                                                                  
                                                                   - - **Historial Completo**: Se mantiene un registro de todos los cambios a la novedad
                                                                     - - **Trazabilidad**: Es posible rastrear quién creó, modificó y aprobó cada novedad
                                                                       - - **Cambios de Estado**: Cada transición de estado se documenta
                                                                         - - **Modificaciones de Datos**: Las correcciones a datos se registran con marca de tiempo
                                                                          
                                                                           - ## 5.9 Solución de Problemas Avanzados
                                                                          
                                                                           - ### El formulario no carga
                                                                          
                                                                           - **Causa Posible**: Problemas de conexión o sesión expirada
                                                                          
                                                                           - **Solución**:
                                                                           - 1. Recargar la página completamente (Ctrl+Shift+R)
                                                                             2. 2. Verificar que la sesión esté activa
                                                                                3. 3. Si la sesión expiró, volver a autenticarse
                                                                                   4. 4. Intentar nuevamente
                                                                                     
                                                                                      5. ### Los datos no se guardan
                                                                                     
                                                                                      6. **Causa Posible**: Error en el servidor o base de datos
                                                                                     
                                                                                      7. **Solución**:
                                                                                      8. 1. Verificar que no hay errores en la consola (F12)
                                                                                         2. 2. Reintent el envío después de algunos segundos
                                                                                            3. 3. Consultar el estado del servidor con el equipo de IT
                                                                                               4. 4. Contactar a soporte si el problema persiste
                                                                                                 
                                                                                                  5. ### El calendario no funciona
                                                                                                 
                                                                                                  6. **Causa Posible**: JavaScript deshabilitado o problema de navegador
                                                                                                 
                                                                                                  7. **Solución**:
                                                                                                  8. 1. Verificar que JavaScript está habilitado en el navegador
                                                                                                     2. 2. Actualizar a la versión más reciente del navegador
                                                                                                        3. 3. Intentar con un navegador diferente
                                                                                                           4. 4. Escribir manualmente la fecha en formato DD/MM/YYYY
                                                                                                           
                                                                                                           ### El tipo de novedad no aparece en la lista
                                                                                                           
                                                                                                           **Causa Posible**: Restricciones de rol o permisos insuficientes
                                                                                                           
                                                                                                           **Solución**:
                                                                                                           1. Verificar el rol asignado al usuario
                                                                                                           2. 2. Contactar al administrador para incrementar permisos
                                                                                                              3. 3. Verificar si el tipo está disponible para el contexto específico
                                                                                                                 4. 4. Revisar políticas de RH que pueden restringir ciertos tipos
                                                                                                                   
                                                                                                                    5. ## 5.10 Buenas Prácticas para Registro de Novedades
                                                                                                                   
                                                                                                                    6. ### Antes de Registrar
                                                                                                                   
                                                                                                                    7. - Verificar que el empleado realmente debe ser registrado en la novedad
                                                                                                                       - - Confirmar que las fechas son correctas en el calendario laboral
                                                                                                                         - - Asegurar que se dispone de toda la documentación requerida
                                                                                                                           - - Revisar políticas internas sobre límites de novedades por período
                                                                                                                            
                                                                                                                             - ### Durante el Registro
                                                                                                                            
                                                                                                                             - - Completar todos los campos obligatorios
                                                                                                                               - - Usar las fechas exactas (no aproximadas)
                                                                                                                                 - - Seleccionar el tipo que mejor describa la novedad
                                                                                                                                   - - Ser preciso en observaciones si las hay
                                                                                                                                    
                                                                                                                                     - ### Después del Registro
                                                                                                                                    
                                                                                                                                     - - Imprimir o descargar confirmación si está disponible
                                                                                                                                       - - Verificar que la novedad aparece en la bandeja
                                                                                                                                       - Revisar el estado regularmente
                                                                                                                                       - - Responder a notificaciones o solicitudes de información adicional
                                                                                                                                        
                                                                                                                                         - ## 5.11 Información de Soporte
                                                                                                                                        
                                                                                                                                         - Para asistencia técnica relacionada con la creación de novedades:
                                                                                                                                        
                                                                                                                                         - | Tipo de Consulta | Contacto | Horario |
                                                                                                                                         - |-----------------|----------|--------|
                                                                                                                                         - | **Problemas Técnicos del Formulario** | sistemas@bancocontactar.com | Lunes-Viernes 8:00-18:00 |
                                                                                                                                         - | **Validaciones o Rechazos** | rrhh@bancocontactar.com | Lunes-Viernes 8:00-17:00 |
                                                                                                                                         - | **Errores de Base de Datos** | dba@bancocontactar.com | Lunes-Viernes 8:00-18:00 |
                                                                                                                                         - | **Emergencias (Fuera de Horario)** | soporte-24h@bancocontactar.com | 24/7 |
                                                                                                                                         - | **Capacitación en Procesos** | capacitacion@bancocontactar.com | Lunes-Viernes 9:00-16:00 |
                                                                                                                                        
                                                                                                                                         - ## 5.12 Próximos Pasos
                                                                                                                                        
                                                                                                                                         - Después de registrar una novedad exitosamente, el usuario puede:
                                                                                                                                        
                                                                                                                                         - 1. **Consultar Estado**: Verificar el estado de la novedad en la Gestión de Novedades
                                                                                                                                           2. 2. **Registrar Otra Novedad**: Volver a AGREGAR para registrar otro evento
                                                                                                                                              3. 3. **Ver Reportes**: Acceder a reportes consolidados de novedades registradas
                                                                                                                                                 4. 4. **Editar Información**: Si la novedad está en estado editable, hacer cambios
                                                                                                                                                    5. 5. **Consultar Auditoría**: Revisar el historial y cambios de la novedad
                                                                                                                                                       6. 6. **Contactar Apoyo**: Si hay problemas, comunicarse con el equipo de soporte
