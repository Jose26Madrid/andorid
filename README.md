# Desarrollo de Aplicaciones Android: Pagos, Emuladores y Proyectos Base

## Descripción
Este proyecto detalla la creación de aplicaciones Android con Kotlin, integrando el sistema de pagos de Google Play Billing, la creación de emuladores, el uso de plantillas de proyectos base en Android Studio y la implementación de un proyecto inicial "Hola Mundo".

## Tecnologías utilizadas
- Kotlin
- Android Studio
- Google Play Billing Library

## Instalación y configuración de Android Studio
1. Descargar Android Studio desde [developer.android.com/studio](https://developer.android.com/studio).
2. Instalar Android Studio y seguir los pasos del asistente de instalación.
3. Instalar el SDK de Android y configurar el AVD (Android Virtual Device) Manager.
4. Configurar la emulación de dispositivos para probar las aplicaciones.

## Flujo de integración de pagos
1. Crear productos y suscripciones en Google Play Console.
2. Integrar Google Play Billing Library en la app.
3. Consultar productos disponibles mediante BillingClient.
4. Iniciar flujos de compra.
5. Gestionar suscripciones y confirmar pagos.
6. (Opcional) Validar recibos de compra desde servidor usando la API de Google Play Developer.

## Gestionar pagos web (información relacionada)
Para ventas de productos físicos o servicios externos dentro de apps Android, se permite usar Stripe o PayPal.
- Integración mediante SDKs o WebView según el caso.
- Se debe cumplir HTTPS y normas de seguridad.

## Creación de Proyectos en Android Studio
1. Abrir Android Studio y seleccionar **New Project**.
2. Elegir una plantilla de proyecto según necesidad:
   - **Empty Activity**: para proyectos básicos.
   - **Basic Activity**: incluye navegación y acciones comunes.
   - **Bottom Navigation Activity**: para apps con menú inferior.
   - **Navigation Drawer Activity**: para apps con menú lateral.
   - **Login Activity**: para aplicaciones que requieran autenticación.
3. Configurar el lenguaje (Kotlin recomendado) y el SDK mínimo.
4. Utilizar el editor visual (Design) y el editor de código (Code) para desarrollar la app.

## Proyecto "Hola Mundo"

### Estructura del Proyecto
```
app/
 └── src/
     └── main/
         ├── java/
         │    └── com.tuempresa.holamundoapp/
         │         └── MainActivity.kt
         ├── res/
         │    └── layout/
         │         └── activity_main.xml
         └── AndroidManifest.xml
```

### Código de la actividad principal (MainActivity.kt)
```kotlin
package com.tuempresa.holamundoapp

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.widget.TextView

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val texto = findViewById<TextView>(R.id.textoHola)
        texto.text = "¡Hola Mundo desde Kotlin!"
    }
}
```

### Diseño de la interfaz (activity_main.xml)
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout 
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    android:orientation="vertical">

    <TextView
        android:id="@+id/textoHola"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Texto inicial"
        android:textSize="24sp"/>
</LinearLayout>
```

### Imagen del proyecto en Android Studio

![Vista de Android Studio](sandbox:/mnt/data/A_digital_screenshot_of_Android_Studio_IDE_capture.png)

## Emulador de Android
- Instalado y gestionado desde Android Studio.
- Creación de dispositivos virtuales con AVD Manager.
- Permite simular diferentes modelos, condiciones de red, batería, GPS, etc.

## Seguridad
- Gestionar correctamente estados de la compra.
- Validar los eventos recibidos para evitar fraudes.
- Cumplir políticas de Google Play.

## Testing
- Uso de cuentas de prueba de Google Play.
- Simulación de compras de prueba.
- Emulación de dispositivos Android de diferentes modelos y versiones.

## Documentación adicional
- [Google Play Billing Library](https://developer.android.com/google/play/billing)
- [Guía de integración de pagos en Android](https://developer.android.com/google/play/billing/integrate)
- [Guía para crear proyectos en Android Studio](https://developer.android.com/studio/projects/create-project)

### MIT License
### Copyright (c) 2025 Jose Magariño
### See LICENSE file for more details.
