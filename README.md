# Taller: Modelado NoSQL Documental con MongoDB para una Pizzería

### 1. Investigación

**- ¿Qué es una base de datos NoSQL?**

    Una base de datos NoSQL (Not Only SQL) es un tipo de base de datos que no utiliza el modelo relacional tradicional basado en tablas y filas, sino que emplea modelos de datos más flexibles como documentos, pares clave-valor, grafos o columnas.

    Estas bases de datos están diseñadas para manejar grandes volúmenes de datos no estructurados o semi-estructurados, y son ideales cuando se necesita escalabilidad horizontal, alta disponibilidad y rendimiento en aplicaciones distribuidas.

**- ¿Qué es MongoDB?**

    MongoDB es una base de datos NoSQL orientada a documentos, desarrollada para manejar grandes volúmenes de datos de forma flexible, escalable y eficiente. A diferencia de las bases de datos relacionales que almacenan datos en tablas, MongoDB almacena la información en documentos BSON (una extensión de JSON).

    CARACTERISTICAS PRINCIPALES:

    📄 Documentos: Los datos se almacenan en documentos similares a JSON ({ clave: valor }), lo que permite estructuras complejas y anidadas.

    🔄 Sin esquema fijo: No necesitas definir una estructura rígida, lo que facilita cambios rápidos en los datos.

    🚀 Escalable horizontalmente: Soporta particionamiento automático de datos entre múltiples servidores (sharding).

    🔍 Consultas flexibles: Permite realizar búsquedas, filtros y agregaciones complejas.

    🧩 Compatible con múltiples lenguajes: Tiene drivers para JavaScript, Python, Java, C#, entre otros.

    EJEMPLO:
            {
            "nombre": "Max",
            "especie": "Perro",
            "edad": 5,
            "vacunas": ["rabia", "moquillo"],
            "propietario": {
                "nombre": "Ana",
                "telefono": "3124567890"
            }
            }

**- ¿Qué diferencia hay entre una base de datos relacional (como MySQL) y una base de datos documental como MongoDB?**

**- ¿Qué son documentos y colecciones en MongoDB?*

---

### 2. Diseño de propuesta

- Imaginen y propongan **qué colecciones tendrían**.
- ¿Qué información tendría un documento de pedido? ¿Y un producto?
- ¿Qué iría dentro del documento y qué se referenciaría?
- ¿Qué campos serían listas, objetos u otros documentos incrustados?

---

### 3. Documentos JSON

- Un producto (ej. pizza con ingredientes)
- Un combo
- Un pedido con un cliente y varios productos (algunos personalizados)

---

### 4. Reflexión

- ¿Qué fue lo más difícil de imaginar sin tablas?
- ¿Qué les gustó del enfoque con documentos?
- ¿Qué dudas les surgieron al pensar en este nuevo tipo de base de datos?



