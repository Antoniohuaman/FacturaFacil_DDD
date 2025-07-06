# FacturaFacil\_DDD

**PROYECTO FACTURA FÁCIL DDD**

Sistema de gestión de ventas y facturación electrónica desarrollado siguiendo principios de **Domain-Driven Design** (DDD) y **Arquitectura Limpia**.

---

## 📋 Contenido del Repositorio

* `.vscode/`
  Configuración de tareas y depuración para VS Code.

* `build/`
  Scripts y pipelines de compilación (vacío por defecto).

* `docs/`
  Documentación y diagramas.

* `src/`
  Código fuente organizado en **Bounded Contexts**:

  * `ControlCajaBC/`
    Gestión de apertura, cierre y movimientos de caja.
  * `CatalogoArticulosBC/`
    Administración de catálogo de productos y servicios.
  * `GestionClientesBC/`
    Módulo de gestión de clientes y contactos.
  * `ListaPreciosBC/`
    Manejo de listas de precios según cliente, canal y campañas.
  * `Integration/`
    Handlers y orquestadores de eventos entre contextos.
  * `SharedKernel/`
    Objetos y utilidades comunes a todos los BCs.

* `tests/`
  Proyectos de pruebas (**unitarias** e **integración**) para cada BC y pruebas **End-to-End**.

* `.gitignore`
  Reglas para excluir binarios, artefactos y configuraciones locales.

* `FacturaFacil_DDD.sln`
  Solución de Visual Studio / .NET que agrupa todos los proyectos.

---

## ⚙️ Requisitos

* [.NET 9.0 SDK](https://dotnet.microsoft.com/download)
* [Visual Studio Code](https://code.visualstudio.com/) con la extensión C# instalada.

---

## 🚀 Primeros Pasos

1. **Clonar el repositorio**

   ```bash
   git clone https://github.com/Antoniohuaman/FacturaFacil_DDD.git
   cd FacturaFacil_DDD
   ```

2. **Restaurar paquetes y compilar**

   ```bash
   dotnet restore
   # O usa VS Code: Ctrl+Shift+B ➔ "build"
   ```

3. **Ejecutar tests**

   ```bash
   dotnet test
   ```

4. **Depurar en VS Code**

   * Abre la paleta (Ctrl+Shift+P) y selecciona **Run and Debug**.
   * Elige la configuración **.NET Core Launch (Console App)**.
   * Presiona **F5**.

---

## 🏗 Estructura DDD

Cada Bounded Context (`BC`) sigue la siguiente organización interna:

```
<BCName>/
 ├── Adapters/
 │   ├── Input/Controllers
 │   └── Output/Persistence
 ├── Application/
 │   ├── Interfaces
 │   └── UseCases
 ├── Domain/
 │   ├── Aggregates
 │   ├── Entities
 │   ├── Events
 │   └── ValueObjects
 └── Infrastructure/
     ├── EFCore
     └── ExternalServices
```

---

## 📖 Contribuciones

1. Crea una rama con el nombre de tu feature o fix:

   ```bash
   git checkout -b feature/nombre-descriptivo
   ```
2. Realiza tus cambios y **commit** con mensajes claros:

   ```bash
   git commit -m "Describe brevemente lo que haces"
   ```
3. Sube tu rama y abre un **Pull Request**.

---

## ⚖️ Licencia

Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo `LICENSE` para más detalles.
