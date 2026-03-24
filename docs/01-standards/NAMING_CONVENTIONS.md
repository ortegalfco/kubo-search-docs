# NAMING_CONVENTIONS

## 1. Purpose
Define consistent naming rules for all components of the Search & AI platform.

Consistent naming improves:
- readability
- maintainability
- onboarding
- scalability
- cross-client reuse

---

## 2. General Rules

### 2.1 Use lowercase for technical artifacts
Applies to:
- collections
- configsets
- fields
- folders

### 2.2 Use underscores (_)
Preferred format:
snake_case

### 2.3 Use uppercase for documentation files
Examples:
- SEARCH_PLATFORM_STANDARDS.md
- SCHEMA_PRODUCTS.md

---

## 3. Collection Naming
### 3.1 Recommended format

<company>_<platform>_<entity>

### Format
<company><platform><entity>

### Examples
- kubo_search_products
- kubo_search_rules
- kubo_search_signals

### Avoid
- products
- rules
- test
- collection1

---

## 4. Configset Naming

### Format
<collection_name>_config

### Examples
- kubo_search_products_config
- kubo_search_rules_config

---

## 5. Document ID Naming

### Format
<ENTITY><SOURCE><ID>

### Examples
- PRODUCT_COPPEL_12345
- RULE_GLOBAL_001

### Rules
- must be stable
- must not depend on text fields
- should allow traceability

---

## 6. Field Naming

### General rules
- lowercase
- descriptive
- stable
- functional

---

### Type suffix convention

| Suffix | Meaning |
|------|--------|
| _s | string exact |
| _ss | multi string |
| _txt_es | analyzed text |
| _b | boolean |
| _i | integer |
| _f | float |
| _dt | datetime |

---

### Examples

- brand_s
- category_ss
- title_txt_es
- price_f
- enabled_b
- updated_at_dt

---

## 7. Extended Attributes

Use namespace:
attr_<name>_<type>

### Examples
- attr_color_s
- attr_size_s
- attr_material_s

---

## 8. Important Note

Suffix naming:
- improves readability
- improves governance
- does NOT affect performance negatively

Performance issues come from:
- too many fields
- poor schema design
- uncontrolled dynamic fields

---

## 9. API Naming

Examples:
- /api/search
- /api/facets
- /api/rules

Avoid exposing Solr internals.

---

## 10. Anti-Patterns

- value, data, misc
- mixing naming styles
- UI-driven naming
- client-specific naming without standard
