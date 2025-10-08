# 📄 Football League XML Dataset

Este proyecto contiene una representación en **XML** de varios clubes de fútbol ingleses, junto con un archivo **DTD** que define la estructura y validación del documento XML.  
Su propósito es mostrar cómo se puede usar **Document Type Definition (DTD)** para garantizar la consistencia y validez de los datos estructurados en XML.

---

## 🗂️ Archivos incluidos

### 1. `football_league.xml`
Este archivo contiene los datos principales de varios clubes de fútbol.  
Cada club está descrito mediante una serie de elementos que incluyen información general y logros.

#### 🧩 Estructura del XML

```xml
<!DOCTYPE clubs SYSTEM "football_league.dtd">
<clubs>
    <club>
        <name>Chelsea FC</name>
        <year_of_foundation>1905</year_of_foundation>
        <Last_trophie>Club World Cup 2025</Last_trophie>
        <best_player>Cole Palmer</best_player>
        <legend>Frank Lampard</legend>
        <total_trophies>35</total_trophies>
    </club>
    ...
</clubs>
```

#### 📘 Elementos incluidos
- `<clubs>`: Elemento raíz que agrupa todos los clubes.  
- `<club>`: Representa un club individual.  
  - `<name>`: Nombre del club.  
  - `<year_of_foundation>`: Año de fundación.  
  - `<Last_trophie>`: Último trofeo ganado.  
  - `<best_player>`: Mejor jugador actual.  
  - `<legend>`: Jugador legendario del club.  
  - `<total_trophies>`: Número total de trofeos ganados.  

---

### 2. `football_league.dtd`
Este archivo define las **reglas estructurales** y los tipos de elementos que deben aparecer en el XML.  
Garantiza que todos los documentos sigan el mismo formato y que contengan los elementos obligatorios.

#### 📐 Ejemplo de contenido esperado del DTD

```dtd
<!ELEMENT clubs (club+)>
<!ELEMENT club (name, year_of_foundation, Last_trophie, best_player, legend, total_trophies)>
<!ELEMENT name (#PCDATA)>
<!ELEMENT year_of_foundation (#PCDATA)>
<!ELEMENT Last_trophie (#PCDATA)>
<!ELEMENT best_player (#PCDATA)>
<!ELEMENT legend (#PCDATA)>
<!ELEMENT total_trophies (#PCDATA)>
```

---

## ✅ Validación del XML

Para verificar que el archivo `football_league.xml` cumple con la definición del DTD:

### 💻 En la terminal (Linux/Mac)
```bash
xmllint --noout --valid football_league.xml
```

### 🪟 En Windows (con PowerShell)
```bash
msxml6 football_league.xml
```

---

## 🏟️ Ejemplo de salida esperada
Cuando el XML es válido, no se mostrará ningún error:
```
football_league.xml validates
```

---

## 🧠 Objetivo educativo

Este proyecto sirve para:
- Comprender cómo estructurar datos jerárquicos en XML.  
- Aprender a usar DTD para definir esquemas de validación.  
- Representar información de forma portable y estandarizada.

---

## 📅 Última actualización
Octubre de 2025
