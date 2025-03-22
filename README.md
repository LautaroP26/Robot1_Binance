# 🚀 LautaroP_EX1 - Automatización con RocketBot (v2.0)

## 📌 Descripción
Este proyecto es un bot desarrollado en RocketBot que automatiza la extracción de datos de la plataforma **Binance**. El bot navega por la web, obtiene información sobre criptomonedas y la guarda en un archivo de Excel para su posterior análisis.

![Flujo del bot](https://via.placeholder.com/800x400.png?text=Diagrama+de+Flujo)

---

## 🔄 Flujo de Ejecución
1. **Inicialización**
   - Se establece un contador en 1 para controlar el número de iteraciones y evitar errores en ejecuciones repetitivas.
2. **Apertura de Binance**
   - Se abre el navegador con la URL de Binance.
   - Se verifica que la página se haya cargado correctamente mediante una espera activa sobre un objeto de la web.
3. **Carga de Archivo Excel**
   - Se abre un archivo de Excel (`Binance.xlsx`) para almacenar los datos extraídos.
   - Es importante modificar la variable `archi` para que contenga la ruta correcta del archivo en el sistema del usuario.
4. **Extracción de Datos**
   - Se extraen los nombres y valores de distintas criptomonedas de Binance utilizando `XPath`.
   - Se escriben en el archivo Excel en una fila correspondiente al contador, asegurando que los datos no se sobrescriban.
   - Se registra el timestamp exacto de la extracción para mayor precisión, dado que los valores cambian constantemente.
5. **Guardado y Cierre**
   - Se guardan los cambios en el archivo.
   - Se cierra el archivo Excel para evitar bloqueos o errores de acceso en futuras ejecuciones.

---

## 📦 Módulos Utilizados
- `AdvancedExcel` (versión: 34.37.21 → Última: 34.39.28)
  - Manejo de archivos Excel.
- `webpro` (versión: 12.3.2 → Última: 12.9.5)
  - Extracción de datos de la web mediante XPath.

---

## 📁 Variables Importantes
| Nombre   | Descripción                          | Valor Inicial |
|----------|--------------------------------------|--------------|
| `cont`   | Contador de iteraciones             | 5            |
| `archi`  | Ruta del archivo Excel              | `C:/Users/lauta/OneDrive/Escritorio/Binance.xlsx` |
| `nom`    | Nombre de la criptomoneda extraída  | XRP          |
| `val`    | Valor de la criptomoneda extraída   | 2.20 $       |
| `tiempo` | Timestamp de la extracción          | `2025-03-11 19:12:59` |

---

## 🚀 Cómo Ejecutar el Bot
1. Asegúrate de tener RocketBot instalado y configurado.
2. Carga el proyecto en RocketBot.
3. Antes de ejecutar, verifica que la variable `archi` apunte al archivo correcto de Excel.
4. Ejecuta el bot y verifica que los datos se guarden correctamente en el archivo Excel.
5. Revisa la hoja de cálculo después de la ejecución para comprobar la correcta extracción de los datos.

---

## 📌 Notas Adicionales
- El bot no verifica la existencia del archivo de Excel antes de abrirlo. Es importante asegurarse de que el archivo esté creado y accesible.
- Si el archivo Excel no se abre correctamente, se mostrará una alerta.
- Se recomienda mantener actualizados los módulos `AdvancedExcel` y `webpro`.
- El proceso de extracción funciona con un bucle `while`, que se ejecuta hasta que el contador llegue a 5. Este valor puede modificarse para extraer más datos si es necesario.
- Dado que los valores de las criptomonedas cambian cada segundo, el uso del timestamp en la extracción mejora la precisión de los datos almacenados.

---

## 📜 Créditos
Desarrollado por **LautaroP** como parte del curso de **BotSolution**.
