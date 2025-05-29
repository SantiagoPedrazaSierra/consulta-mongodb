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

**- Un producto (ej. pizza con ingredientes)**

    Productos = [
        {"id": 1,
        "nombre": "Pizza de pollo",
        "categoria":["pizza"],
        "ingredientes": ["pollo", "champiñon"],
        "precio": 6000,
        "elaborado": true,
        "disponible": true},

        {"id": 2,
        "nombre": "Panzerotti de carne",
        "categoria":["panzerotti"],
        "ingredientes": ["carne", "jamon"],
        "precio": 8000,
        "elaborado": true,
        "disponible": true},

        {"id": 3,
        "nombre": "Agua",
        "categoria":["bebida"],
        "ingredientes": [],
        "precio": 2000,
        "elaborado": false,
        "disponible": true},
    ]

**- Un combo**

    Combos = {
        "1": {"Nombre": "Familiar", 
            "descripcion": "Alcanza para 6 personas", 
            "precio": 68000},

        "2": {"Nombre": "Pareja", 
            "descripcion": "Alcanza para 2 personas", 
            "precio": 46000},

        "3": {"Nombre": "Solitario", 
            "descripcion": "Alcanza para 1 persona", 
            "precio": 32000},
    } 

**- Un pedido con un cliente y varios productos (algunos personalizados)**

    Pedidos = [
        {"id": 1,
        "nombre": "Juan Mariño",
        "modalidadPedido":["recoger"],
        "metodoPago": ["efectivo"],
        "precio": 95000,
        "producto": {"Familiar", "Agua"},
        "adicionales": ["tocineta"]},

        {"id": 2,
        "nombre": "Nicolas Espitia",
        "modalidadPedido":["mesa"],
        "metodoPago": ["credito"],
        "precio": 21000,
        "producto": {"Pizza de pollo", "Agua"},
        "adicionales": ["extra queso", "cebolla"]},

        {"id": 3,
        "nombre": "Santiago Pedraza",
        "modalidadPedido":["mesa"],
        "metodoPago": ["debito"],
        "precio": 64000,
        "producto": {"Panzerotti de carne", "Agua"},
        "adicionales": ["maiz"]}
    ]

---

### 4. Reflexión

**- ¿Qué fue lo más difícil de imaginar sin tablas?**

**- ¿Qué les gustó del enfoque con documentos?**

**- ¿Qué dudas les surgieron al pensar en este nuevo tipo de base de datos?**

    Una de las dudas más persistentes durante la realización del taller fue entender cómo se maneja la relación entre datos en NoSQL, especialmente porque venimos de trabajar con bases de datos relacionales donde las tablas intermedias son fundamentales para conectar información. Nos resultó complicado imaginar cómo unir todos los datos en una sola colección de documentos, ya que estábamos acostumbrados a utilizar llaves foráneas y relaciones explícitas para estructurar la información.







