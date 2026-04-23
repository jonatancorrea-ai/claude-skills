|   |   |
|---|---|
| name | responder-emails-gmail |
| description | Redacta borradores de respuesta en Gmail con el estilo del usuario cuando este quiere contestar un correo concreto. Se activa cuando el usuario pide responder, contestar o redactar una respuesta para un email específico de su Gmail conectado (por asunto, remitente o contexto) y quiere dejar el correo listo como borrador sin enviarlo todavía. |

Estas son instrucciones para ayudar al usuario a **responder correos de Gmail** dejando borradores listos con su propio estilo de comunicación, sin enviar nada automáticamente.

La skill se centra en:
- Entender bien el correo original.
- Redactar una respuesta clara, cercana y profesional.
- Crear un borrador en Gmail (si hay integración) o devolver el texto listo para copiar y pegar.

---

RESPONDER EMAILS EN GMAIL CON MI ESTILO
=======================================

### QUÉ HACE ESTA SKILL

Esta skill ayuda a responder correos de Gmail dejando borradores preparados con el estilo del usuario.  
Se usa cuando el usuario indica que quiere responder un email concreto de su Gmail (por ejemplo: menciona remitente, asunto, fecha o resume el contenido) y pide que le prepares la respuesta para revisarla y enviarla manualmente después.

---

CUÁNDO DEBES ACTIVARLA
=======================

Claude debe usar esta skill cuando el usuario:

- Diga que quiere **responder, contestar o redactar** un correo que está en su Gmail.  
- Dé pistas sobre un correo específico: remitente, asunto, fecha aproximada o un resumen claro del mensaje.  
- Pida algo como:  
  - “Déjame el borrador listo”.  
  - “Prepárame la respuesta”.  
  - “Solo quiero revisar y enviar”.

Si el usuario solo está pidiendo que mejores un texto suelto (no menciona Gmail ni un correo real), esta skill **no** es necesaria.

---

INSTRUCCIONES PARA CLAUDE
=========================

IDENTIFICAR EL CORREO CORRECTO
------------------------------

1. Usa la información que te dé el usuario (remitente, asunto, fecha, resumen del contenido…) para localizar el correo adecuado en Gmail usando los conectores o herramientas disponibles.  
2. Si hay varias coincidencias y no está claro cuál es, pide una **aclaración corta** antes de continuar.  
3. Una vez identificado el correo, léelo completo para entender:  
   - Qué pide la otra persona.  
   - Qué contexto o historial hay en el hilo (si lo hay).  
   - Qué espera el usuario que tú respondas.

ESTILO DE ESCRITURA
-------------------

Cuando redactes la respuesta:

- Tono cercano, claro y profesional.  
- Nada de tecnicismos innecesarios.  
- Frases sencillas y fáciles de leer.  
- Respuestas cortas y al grano, sin relleno.  
- Prioriza que la otra persona entienda rápido qué tiene que hacer o cuál es el siguiente paso.

No escribas como un texto genérico de IA; escribe como si fueras la propia persona usuaria.

REDACTAR LA RESPUESTA
---------------------

1. Responde de forma amable, directa y alineada con la intención del usuario.  
2. Si el correo es de trabajo o negocio, prioriza:  
   - Claridad en la propuesta o respuesta.  
   - Próximo paso concreto (qué debe pasar después).  
   - Información clave que la otra persona necesita.  
3. Si falta información para responder bien:  
   - Incluye en el borrador **una o dos preguntas claras** para obtener esos datos.  
4. Evita explicar cosas técnicas dentro del correo; escribe como si fuera el propio usuario hablando con la otra persona.

CREAR EL BORRADOR EN GMAIL (SIN ENVIAR)
---------------------------------------

1. Usa la integración o conector de Gmail para crear un **borrador de respuesta** en el hilo correcto.  
2. No envíes nunca el correo. Tu tarea termina cuando:  
   - El borrador está creado en Gmail.  
   - El usuario puede entrar, revisar y enviarlo manualmente.  
3. Respeta el hilo original (responder sobre el mismo email, no crear uno nuevo salvo que el usuario lo pida explícitamente).

---

QUÉ DEVOLVER EN EL CHAT
=======================

Cada vez que ejecutes esta skill, tu respuesta en el chat debe seguir este formato:

1. **Resumen breve del correo encontrado:**  
   - Remitente.  
   - Asunto.  

2. **Confirmación explícita de la acción:**  
   - Indica que has creado un borrador en Gmail y que no se ha enviado.  
   - Si no hay integración con Gmail, aclara que el texto está listo para copiar y pegar en Gmail manualmente.

3. **Texto completo del borrador de respuesta**, listo para revisar, copiar y pegar.

Ejemplo de estructura de salida (solo como guía):

- “He encontrado un correo de [NOMBRE] con el asunto ‘[ASUNTO]’.”  
- “He preparado un borrador de respuesta sin enviarlo todavía.”  
- “Este es el texto del borrador:”  
  (aquí va el correo completo listo para enviar).

---

SEGURIDAD Y LÍMITES
====================

- Si no tienes permiso para acceder a Gmail o a ese correo concreto, explícalo de forma clara.  
- Ofrece como alternativa redactar la respuesta a partir del texto que el usuario pegue en el chat.  
- Nunca digas que has **enviado** un correo; tu rol es solo preparar borradores y texto listo para revisión.
