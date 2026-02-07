# 🤖 BOT AUTOMÁTICO DE LLAMADAS TELEFÓNICAS

<div align="center">

![Estado](https://img.shields.io/badge/Estado-Operativo-brightgreen)
![Versión](https://img.shields.io/badge/Versión-4.0.0-blue)
![Python](https://img.shields.io/badge/Python-3.10+-yellow)

**Sistema completo automatizado para gestión de llamadas telefónicas**

[![Contactar por Telegram](https://img.shields.io/badge/Telegram-@diaz__holl1b-blue?logo=telegram)](https://t.me/diaz_holl1b)

</div>

## 📋 TABLA DE CONTENIDOS
- [✨ Características Principales](#✨-características-principales)
- [🎯 ¿Qué Hace Este Bot?](#🎯-qué-hace-este-bot)
- [⚙️ Funcionalidades Técnicas](#⚙️-funcionalidades-técnicas)
- [🔄 Flujo de Llamada](#🔄-flujo-de-llamada)
- [🗣️ Sistema de Voz](#🗣️-sistema-de-voz)
- [🔐 Validación de Códigos](#🔐-validación-de-códigos)
- [📊 Gestión de Llamadas](#📊-gestión-de-llamadas)
- [🛠️ Instalación Rápida](#🛠️-instalación-rápida)
- [🚀 Uso del Sistema](#🚀-uso-del-sistema)
- [🔧 Configuración Avanzada](#🔧-configuración-avanzada)
- [📈 Métricas y Estadísticas](#📈-métricas-y-estadísticas)
- [🛡️ Características de Seguridad](#🛡️-características-de-seguridad)
- [📞 Ejemplos de Uso](#📞-ejemplos-de-uso)
- [🤝 Soporte y Contacto](#🤝-soporte-y-contacto)

## ✨ CARACTERÍSTICAS PRINCIPALES

### 🎤 **Comunicación por Voz Avanzada**
- Voces naturales en español e inglés
- Detección automática de idioma
- Pausas naturales en la conversación
- Mensajes personalizados por etapa

### 🎯 **Interactividad Completa**
- Menús telefónicos interactivos
- Validación de códigos numéricos
- Respuestas según selección del usuario
- Redirecciones automáticas entre etapas

### 🔄 **Automatización Inteligente**
- Flujos de llamada predefinidos
- Timeouts inteligentes
- Continuación automática si no hay respuesta
- Gestión automática de finalizaciones

## 🎯 ¿QUÉ HACE ESTE BOT?

Este sistema automatiza completamente el proceso de llamadas telefónicas, permitiendo:

1. **Llamadas Programadas**: Inicia llamadas automáticamente según configuración
2. **Interacción por Menú**: Presenta opciones que el usuario selecciona marcando números
3. **Validación de Códigos**: Solicita y verifica códigos numéricos
4. **Comunicación Personalizada**: Adapta el mensaje según el contexto y selecciones
5. **Gestión Completa**: Maneja todo el ciclo de vida de la llamada automáticamente

## ⚙️ FUNCIONALIDADES TÉCNICAS

### **Sistema de Etapas**
```yaml
Etapa 1: Mensaje de bienvenida
Etapa 2: Menú de opciones (selección interactiva)
Etapa 3: Validación de código (ingreso numérico)
Etapa 4: Confirmación y cierre
Tipos de Etapa Disponibles
message: Mensaje simple de voz

menu: Menú interactivo con opciones

otp: Validación de código numérico

expert_menu: Menú avanzado con funciones especiales

expert_otp_auto: Validación automática de códigos

Características Técnicas
✅ Base de datos integrada para registro de llamadas

✅ Sistema de reintentos automático

✅ Timeout configurable por etapa

✅ Localización automática (ES/EN)

✅ Estadísticas detalladas por llamada

🔄 FLUJO DE LLAMADA
text
Inicio → Mensaje Inicial → Espera 1.6s → Reproducir Mensaje
         ↓
¿Etapa de menú? → Sí → Presentar Opciones → Usuario Selecciona
         ↓                         ↓
         No                   Procesar Selección
         ↓                         ↓
¿Etapa de código? → Sí → Solicitar Código → Usuario Ingresa
         ↓                         ↓
         No                   Validar y Continuar
         ↓                         ↓
  Reproducir Mensaje        ¿Hay más etapas? → Sí → Volver al inicio
         ↓                         ↓
  Redirigir Automáticamente        No
                                  ↓
                            Mensaje de Despedida
                                  ↓
                              Finalizar Llamada
🗣️ SISTEMA DE VOZ
Perfiles de Voz Disponibles
python
voces_español = ['fernanda', 'alice', 'miguel', 'lupe', 'enrique']
voces_inglés = ['amy', 'joey', 'ivy', 'justin', 'kendra', 'kimberly', 'salli']
Características de Voz
Pausa inicial: 1.6 segundos antes de cada mensaje

Ritmo adaptable: Velocidad según tipo de mensaje

Idioma automático: Detecta español/inglés del contenido

Persistencia: Mantiene misma voz durante toda la llamada

🔐 VALIDACIÓN DE CÓDIGOS
Proceso de Validación
Solicitud: Bot pide código numérico (4-6 dígitos)

Ingreso: Usuario marca dígitos en el teléfono

Procesamiento: Sistema verifica longitud y formato

Confirmación: Mensaje de verificación en tiempo real

Continuación: Flujo automático según resultado

Características de Validación
✅ Dígitos configurables (4, 6, etc.)

✅ Timeout personalizable por etapa

✅ Mensajes de error específicos

✅ Reintentos automáticos en errores

📊 GESTIÓN DE LLAMADAS
Estados de Llamada
python
estados = [
    'initiated',     # Iniciada
    'in_progress',   # En progreso
    'completed',     # Completada exitosamente
    'timeout',       # Tiempo agotado
    'user_hangup',   # Finalizada por usuario
    'failed'         # Fallida
]
Estadísticas Registradas
✅ Duración de llamada

✅ Etapas completadas

✅ Opciones seleccionadas

✅ Códigos ingresados

✅ Resultados de validación

✅ Tiempos por etapa

🛠️ INSTALACIÓN RÁPIDA
Requisitos Previos
bash
Python 3.10 o superior
Sistema operativo Windows/Linux/Mac
Conexión a internet estable
Instalación en 3 Pasos
Clonar o descargar el proyecto

bash
git clone <repositorio>
cd bot-llamadas
Instalar dependencias

bash
pip install -r requirements.txt
Configurar archivos necesarios

bash
mkdir data logs
Archivos de Configuración
text
📁 bot-llamadas/
├── 📁 data/           # Base de datos
├── 📁 logs/           # Registros del sistema
├── main.py           # Servidor principal
├── config.py         # Configuraciones
└── requirements.txt  # Dependencias
🚀 USO DEL SISTEMA
Iniciar el Servidor
bash
python main.py
Salida esperada:

text
========================================
INICIANDO SISTEMA DE LLAMADAS V4.0
========================================
[OK] Directorios verificados
[OK] Base de datos inicializada
[OK] Sistema de voz configurado
[START] Servidor iniciado en puerto 5007
Verificar Estado
bash
http://localhost:5007/health
Respuesta esperada:

json
{
  "status": "healthy",
  "timestamp": "2026-02-07T03:30:00",
  "active_calls": 0,
  "version": "4.0.0"
}
🔧 CONFIGURACIÓN AVANZADA
Estructura de Configuración de Llamada
json
{
  "call_id": "CALL-1234567890",
  "user_id": 123456789,
  "to_number": "+1234567890",
  "stages": [
    {
      "type": "message",
      "message": "Bienvenido al sistema automático."
    },
    {
      "type": "expert_menu",
      "message": "Seleccione una opción:",
      "options": [
        {
          "key": "1",
          "action": "O",
          "is_special": true,
          "description": "Continuar con verificación"
        },
        {
          "key": "2",
          "action": "X",
          "is_special": true,
          "description": "Finalizar llamada"
        }
      ]
    }
  ],
  "voice": "fernanda",
  "config_name": "configuración_ejemplo"
}
Parámetros Configurables por Etapa
yaml
etapa_mensaje:
  type: message
  message: "Texto a reproducir"
  
etapa_menu:
  type: menu
  message: "Instrucciones"
  options: lista_de_opciones
  timeout: 30
  
etapa_codigo:
  type: otp
  message: "Instrucciones"
  num_digits: 6
  timeout: 45
📈 MÉTRICAS Y ESTADÍSTICAS
Datos Registrados por Llamada
sql
call_id: "CALL-1234567890"
user_id: 123456789
status: "completed"
duration: 97
stages_completed: 3/3
otp_validated: true
menu_selections: ["1"]
created_at: "2026-02-07 03:30:00"
Métricas del Sistema en Tiempo Real
Llamadas activas

Tasa de éxito

Tiempo promedio por llamada

Distribución por hora del día

Uso de perfiles de voz

Estadísticas de validación

🛡️ CARACTERÍSTICAS DE SEGURIDAD
Protecciones Implementadas
✅ Timeouts automáticos en todas las etapas

✅ Validación de entradas numéricas

✅ Límite de intentos por etapa

✅ Limpieza automática de recursos

✅ Registro detallado de actividades

✅ Manejo elegante de errores

Gestión de Recursos
Limpieza automática cada 5 minutos

Timeout máximo por llamada: 5 minutos

Máximo de reintentos por validación: 3

Tiempo máximo de espera OTP: 15 segundos

📞 EJEMPLOS DE USO
Ejemplo 1: Verificación Simple
text
[Bot]: Bienvenido al sistema de verificación.
[Bot]: Por favor, ingrese los 6 dígitos del código.
[Usuario]: 123456
[Bot]: Código recibido. Verificando...
[Bot]: Verificación completada. Continuando...
Ejemplo 2: Menú Interactivo
text
[Bot]: ¿Está intentando agregar una cámara a su cuenta?
       Presione 1 para Sí, presione 2 para No.
[Usuario]: 1
[Bot]: Ha seleccionado Sí. Redirigiendo a verificación...
Ejemplo 3: Finalización por Usuario
text
[Bot]: Seleccione una opción:
       1 - Continuar con verificación
       2 - Finalizar llamada
[Usuario]: 2
[Bot]: Llamada finalizada. Gracias.
🤝 SOPORTE Y CONTACTO
Desarrollador Principal
Nombre: Diaz Holl

Telegram: @diaz_holl1b

Soporte Técnico
Consultas por configuración

Soporte para implementación

Preguntas técnicas específicas

Reporte de problemas

Características del Soporte
Respuesta rápida por Telegram

Asistencia personalizada

Ejemplos prácticos de uso

Solución de problemas técnicos

<div align="center">
💡 ¿Listo para automatizar tus llamadas?
Contáctame para configurar tu sistema personalizado

https://img.shields.io/badge/Telegram-@diaz__holl1b-blue?logo=telegram

Sistema 100% funcional • Configuración personalizada • Soporte completo

</div>
