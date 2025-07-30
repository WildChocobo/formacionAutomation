# formacionAutomation

Repositorio para nuestra práctica de automation con [Playwright](https://playwright.dev/).

## Descripción

Este proyecto contiene ejemplos y ejercicios de automatización de pruebas usando Playwright. Incluye pruebas automatizadas para aplicaciones web y ejemplos básicos para aprender a usar Playwright en distintos navegadores.

## Estructura del proyecto

- `tests/`: Pruebas automatizadas principales.
- `tests-examples/`: Ejemplos adicionales de pruebas.
- `playwright.config.js`: Configuración de Playwright.
- `.github/workflows/playwright.yml`: Integración continua para ejecutar pruebas en GitHub Actions.

## Cómo iniciar un nuevo proyecto con Playwright

1. **Instalar Node.js**  
   Descarga e instala [Node.js](https://nodejs.org/).

2. **Crear una carpeta para tu proyecto**  
   ```sh
   mkdir mi-proyecto-playwright
   cd mi-proyecto-playwright
   ```

3. **Inicializar npm**  
   ```sh
   npm init -y
   ```

4. **Instalar Playwright**  
   ```sh
   npm install -D @playwright/test
   npx playwright install
   ```

5. **Crear tu primer test**  
   Crea una carpeta `tests` y un archivo `example.spec.js`:
   ```js
   // tests/example.spec.js
   const { test, expect } = require('@playwright/test');

   test('mi primer test', async ({ page }) => {
     await page.goto('https://playwright.dev/');
     await expect(page).toHaveTitle(/Playwright/);
   });
   ```

6. **Ejecutar las pruebas**  
   ```sh
   npx playwright test
   ```

7. **Ver el reporte de resultados**  
   Después de ejecutar las pruebas, abre el reporte HTML:
   ```sh
   npx playwright show-report
   ```

## Documentación

- [Documentación oficial de Playwright](https://playwright.dev/docs/intro)
- [Ejemplos en este repositorio](./tests/example.spec.js)

---

¡Listo para automatizar tus pruebas!
