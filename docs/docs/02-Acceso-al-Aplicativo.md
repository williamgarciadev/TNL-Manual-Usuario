# 2. Acceso al Aplicativo TNL

## Descripción General

El acceso al Sistema TNL se realiza mediante autenticación integrada con Office 365, garantizando seguridad y facilidad de uso para todos los usuarios corporativos. Este documento describe los requisitos, procedimientos y solución de problemas relacionados con el acceso al sistema.

---

## 2.1 Requisitos Previos

Antes de intentar acceder al Sistema TNL, el usuario debe verificar que cuenta con:

| Requisito | Descripción |
|-----------|------------|
| **Cuenta Office 365 Corporativa** | Dirección de correo electrónico institucional con dominio @bancocontactar.com |
| **Contraseña Vigente** | Clave de acceso activa asociada a la cuenta corporativa |
| **Navegador Compatible** | Chrome, Firefox, Safari o Edge (versiones recientes) |
| **Conexión a Internet** | Acceso a red corporativa, VPN o red externa autorizada |
| **Permisos de Sistema** | Perfil configurado correctamente por el administrador |
| **Autenticación 2FA (Opcional)** | Si está habilitada, tener acceso a dispositivo de verificación |

---

## 2.2 URL de Acceso

El Sistema TNL se encuentra disponible en los siguientes entornos:

### Ambiente de Producción
```
http://localhost:8080/TNLJavaSQLServer/com.contactar.login
```
**Uso:** Ambiente oficial para operaciones regulares

### Ambiente de Desarrollo  
```
http://172.19.19.40:8080/TNLJavaSQLServer/com.contactar.login
```
**Uso:** Ambiente para pruebas y validaciones

### Recomendación
Se sugiere almacenar la URL en los marcadores del navegador para facilitar accesos posteriores.

---

## 2.3 Pantalla de Inicio de Sesión

Cuando el usuario accede a la URL correspondiente, se presenta una interfaz con los siguientes componentes:

### Componentes Visuales

- **Logo de Banco Contactar** - Identificador visual del sistema
- - **Título:** "Acceso al Sistema TNL"
  - - **Botón de Inicio de Sesión con Office 365** - Opción recomendada (color naranja)
    - - **Opción de Acceso Local** - Reservada para administración técnica (texto pequeño)
      - - **Enlaces de Soporte** - Información de contacto e ayuda
       
        - ### Componentes Funcionales
       
        - La pantalla presenta dos modalidades de autenticación:
       
        - 1. **Office 365** (RECOMENDADO)
          2.    - Utilizados las credenciales corporativas
                -    - Mayor seguridad y sincronización automática
                     -    - Integración con servicios Microsoft
                      
                          - 2. **Local** (Reservado para Admin)
                            3.    - Solo para personal de tecnología
                                  -    - Requiere credenciales especiales
                                   
                                       - ---

                                       ## 2.4 Procedimiento de Autenticación - Office 365

                                       ### Paso 1: Acceso a la Plataforma

                                       El usuario realiza los siguientes pasos:

                                       1. Abre el navegador web
                                       2. 2. Ingresa la URL del Sistema TNL (producción o desarrollo)
                                          3. 3. Presiona la tecla Enter
                                             4. 4. Espera a que cargue la pantalla de inicio de sesión
                                               
                                                5. ### Paso 2: Selección de Opción de Autenticación
                                               
                                                6. El usuario:
                                               
                                                7. 1. Localiza el botón naranja denominado "INICIAR SESIÓN CON OFFICE 365"
                                                   2. 2. Hace clic en dicho botón
                                                      3. 3. El sistema redirecciona automáticamente al portal de Microsoft
                                                        
                                                         4. ### Paso 3: Ingreso de Credenciales Microsoft
                                                        
                                                         5. En la pantalla de Microsoft, el usuario:
                                                        
                                                         6. 1. **Ingresa Correo Corporativo:**
                                                            2.    - Formato: usuario@bancocontactar.com
                                                                  -    - Ejemplo: juan.garcia@bancocontactar.com
                                                                   
                                                                       - 2. **Presiona "Siguiente"**
                                                                        
                                                                         3. 3. **Ingresa Contraseña:**
                                                                            4.    - Utiliza la misma clave de Outlook o Teams
                                                                                  -    - La contraseña es sensible a mayúsculas y minúsculas
                                                                                   
                                                                                       - 4. **Presiona "Siguiente"** o "Iniciar Sesión"
                                                                                        
                                                                                         5. ### Paso 4: Autenticación de Dos Factores (Si está activa)
                                                                                        
                                                                                         6. Si la organización tiene configurada la autenticación de dos factores, el usuario recibirá:
                                                                                        
                                                                                         7. - **Opción 1:** Código SMS al celular registrado
                                                                                            - - **Opción 2:** Notificación en aplicación Microsoft Authenticator
                                                                                              - - **Opción 3:** Preguntas de seguridad predefinidas
                                                                                               
                                                                                                - El usuario:
                                                                                                - 1. Selecciona su método de verificación preferido
                                                                                                  2. 2. Completa la verificación según el método elegido
                                                                                                     3. 3. Confirma que es realmente él
                                                                                                       
                                                                                                        4. ### Paso 5: Autorización de Permisos
                                                                                                       
                                                                                                        5. Microsoft solicita permiso para que la aplicación TNL acceda a información básica de la cuenta:
                                                                                                       
                                                                                                        6. - Perfil
                                                                                                           - - Correo electrónico
                                                                                                             - - Información de sesión
                                                                                                              
                                                                                                               - El usuario:
                                                                                                               - 1. Revisa los permisos solicitados
                                                                                                                 2. 2. Selecciona "Aceptar" para continuar
                                                                                                                    3. 3. Espera a ser redireccionado a TNL
                                                                                                                      
                                                                                                                       4. ### Paso 6: Acceso Exitoso
                                                                                                                      
                                                                                                                       5. Tras completar la autenticación exitosa:
                                                                                                                      
                                                                                                                       6. - El navegador redirecciona automáticamente a TNL
                                                                                                                          - - Se carga la página de inicio (Bandeja de Novedades)
                                                                                                                            - - En la esquina superior derecha aparece el nombre del usuario
                                                                                                                              - - El correo electrónico se visualiza como confirmación de autenticación
                                                                                                                               
                                                                                                                                - **Tiempo esperado:** 3-10 segundos desde el inicio hasta acceso completo
                                                                                                                               
                                                                                                                                - ---
                                                                                                                                
                                                                                                                                ## 2.5 Validación del Acceso Exitoso
                                                                                                                                
                                                                                                                                El usuario puede confirmar que ha accedido correctamente al observar:
                                                                                                                                
                                                                                                                                ✅ **Pantalla de Inicio Cargada** - Se visualiza "Gestión de Novedades"
                                                                                                                                ✅ **Nombre de Usuario Visible** - Aparece en esquina superior derecha
                                                                                                                                ✅ **Menú Lateral Funcional** - Se pueden ver opciones del sistema
                                                                                                                                ✅ **URL Correcta** - Muestra `/com.contactar.tnl.wwtnlnovedad`
                                                                                                                                ✅ **Sin Mensajes de Error** - No hay alertas rojas de autenticación
                                                                                                                                
                                                                                                                                ---
                                                                                                                                
                                                                                                                                ## 2.6 Solución de Problemas de Acceso
                                                                                                                                
                                                                                                                                ### Problema: "Credenciales Inválidas"
                                                                                                                                
                                                                                                                                **Causa Probable:**
                                                                                                                                - Contraseña incorrecta
                                                                                                                                - - Nombre de usuario mal escrito
                                                                                                                                  - - Mayúsculas/minúsculas incorrectas
                                                                                                                                   
                                                                                                                                    - **Solución:**
                                                                                                                                    - 1. Verificar escritura del correo corporativo
                                                                                                                                      2. 2. Confirmar que CAPS LOCK no está activado
                                                                                                                                         3. 3. Intentar nuevamente con cuidado
                                                                                                                                            4. 4. Si persiste, usar "¿Olvidó su contraseña?" en Microsoft
                                                                                                                                              
                                                                                                                                               5. ### Problema: "Acceso Denegado"
                                                                                                                                              
                                                                                                                                               6. **Causa Probable:**
                                                                                                                                               7. - Usuario sin permisos en TNL
                                                                                                                                                  - - Cuenta no configurada correctamente
                                                                                                                                                    - - Permisos revocados recientemente
                                                                                                                                                     
                                                                                                                                                      - **Solución:**
                                                                                                                                                      - 1. Contactar a soporte.it@bancocontactar.com
                                                                                                                                                        2. 2. Proporcionar número de cédula y correo corporativo
                                                                                                                                                           3. 3. Solicitar que revisen permisos en el sistema
                                                                                                                                                              4. 4. Esperar confirmación de acceso
                                                                                                                                                                
                                                                                                                                                                 5. ### Problema: "Error 403 - Acceso Prohibido"
                                                                                                                                                                
                                                                                                                                                                 6. **Causa Probable:**
                                                                                                                                                                 7. - Usuario desactivado en sistema
                                                                                                                                                                    - - Licencia Office 365 expirada
                                                                                                                                                                      - - Permisos insuficientes
                                                                                                                                                                       
                                                                                                                                                                        - **Solución:**
                                                                                                                                                                        - 1. Verificar estado de cuenta en Office 365
                                                                                                                                                                          2. 2. Confirmar que licencia está activa
                                                                                                                                                                             3. 3. Contactar a administrador si persiste
                                                                                                                                                                               
                                                                                                                                                                                4. ### Problema: "No Recibo Código de 2FA"
                                                                                                                                                                               
                                                                                                                                                                                5. **Causa Probable:**
                                                                                                                                                                                6. - Número de teléfono no registrado
                                                                                                                                                                                   - - Servidor de SMS retrasado
                                                                                                                                                                                     - - Método de verificación inactivo
                                                                                                                                                                                      
                                                                                                                                                                                       - **Solución:**
                                                                                                                                                                                       - 1. Seleccionar método alternativo ("Usar aplicación")
                                                                                                                                                                                         2. 2. Usar Microsoft Authenticator si está disponible
                                                                                                                                                                                            3. 3. Contactar a TI si no puede verificarse
                                                                                                                                                                                              
                                                                                                                                                                                               4. ### Problema: "Tiempo de Sesión Agotado"
                                                                                                                                                                                              
                                                                                                                                                                                               5. **Causa Probable:**
                                                                                                                                                                                               6. - Inactividad prolongada
                                                                                                                                                                                                  - - Sesión expirada (máximo 8 horas)
                                                                                                                                                                                                    - - Cierre del navegador
                                                                                                                                                                                                     
                                                                                                                                                                                                      - **Solución:**
                                                                                                                                                                                                      - 1. Actualizar la página (F5)
                                                                                                                                                                                                        2. 2. Si redirige a login, ingrese credenciales de nuevo
                                                                                                                                                                                                           3. 3. No es necesario hacer clic en "Mantener sesión iniciada"
                                                                                                                                                                                                             
                                                                                                                                                                                                              4. ---
                                                                                                                                                                                                             
                                                                                                                                                                                                              5. ## 2.7 Mejores Prácticas de Seguridad
                                                                                                                                                                                                             
                                                                                                                                                                                                              6. ### Durante el Acceso
                                                                                                                                                                                                             
                                                                                                                                                                                                              7. - ✅ **Verificar URL** antes de ingresar credenciales
                                                                                                                                                                                                                 - - ✅ **Usar conexión segura** (HTTPS)
                                                                                                                                                                                                                   - - ✅ **No compartir credenciales** con colegas
                                                                                                                                                                                                                     - - ✅ **Usar contraseña única** diferente a otros sistemas
                                                                                                                                                                                                                       - - ✅ **Habilitar 2FA** si está disponible
                                                                                                                                                                                                                         - - ✅ **Usar navegador actualizado** con últimas actualizaciones
                                                                                                                                                                                                                          
                                                                                                                                                                                                                           - ### Después del Acceso
                                                                                                                                                                                                                          
                                                                                                                                                                                                                           - - ✅ **Cerrar sesión** al terminar de trabajar
                                                                                                                                                                                                                             - - ✅ **No dejar sesión abierta** en computadores compartidos
                                                                                                                                                                                                                               - - ✅ **Reportar accesos no autorizados** de inmediato
                                                                                                                                                                                                                                 - - ✅ **Cambiar contraseña regularmente**
                                                                                                                                                                                                                                   - - ✅ **No acceder desde redes públicas** sin VPN
                                                                                                                                                                                                                                    
                                                                                                                                                                                                                                     - ---
                                                                                                                                                                                                                                     
                                                                                                                                                                                                                                     ## 2.8 Cambio de Contraseña
                                                                                                                                                                                                                                     
                                                                                                                                                                                                                                     Si el usuario necesita cambiar su contraseña:
                                                                                                                                                                                                                                     
                                                                                                                                                                                                                                     1. Acceder a https://account.microsoft.com
                                                                                                                                                                                                                                     2. 2. Seleccionar "Seguridad" en el menú
                                                                                                                                                                                                                                        3. 3. Elegir "Cambiar contraseña"
                                                                                                                                                                                                                                           4. 4. Seguir el proceso de Microsoft
                                                                                                                                                                                                                                              5. 5. Esperar 30 minutos para sincronizar con TNL
                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                 6. ---
                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                 7. ## 2.9 Información de Soporte
                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                 8. Para problemas de acceso:
                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                 9. **Soporte Técnico (Plataforma y Accesos)**
                                                                                                                                                                                                                                                 10. - 📧 Email: soporte.it@bancocontactar.com
                                                                                                                                                                                                                                                     - - ☎️ Teléfono: Extensión 5555
                                                                                                                                                                                                                                                       - - ⏰ Horario: Lunes a Viernes, 8:00 AM - 5:00 PM
                                                                                                                                                                                                                                                         - - 🆘 Tiempo Respuesta: Máximo 4 horas
                                                                                                                                                                                                                                                          
                                                                                                                                                                                                                                                           - ---
                                                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                           ## 2.10 Próximos Pasos
                                                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                           Tras completar el acceso al Sistema TNL, el usuario:
                                                                                                                                                                                                                                                           
                                                                                                                                                                                                                                                           1. Se encontrará en la pantalla "Gestión de Novedades" (Bandeja)
                                                                                                                                                                                                                                                           2. 2. Podrá navegar a otros módulos desde el menú lateral
                                                                                                                                                                                                                                                              3. 3. Estará listo para registrar o consultar novedades
                                                                                                                                                                                                                                                                 4. 4. Podrá acceder a reportes y documentación
                                                                                                                                                                                                                                                                   
                                                                                                                                                                                                                                                                    5. Continúe con la sección **3. Pantalla de Inicio y Navegación** para comprender la interfaz del sistema.
                                                                                                                                                                                                                                                                   
                                                                                                                                                                                                                                                                    6. ---
                                                                                                                                                                                                                                                                    
                                                                                                                                                                                                                                                                    **Documento:** Sección 2 - Acceso al Aplicativo TNL
                                                                                                                                                                                                                                                                    **Versión:** 2.1 | **Fecha:** Febrero 2026
                                                                                                                                                                                                                                                                    **Clasificación:** Documento Interno - Banco Contactar
