# ARDF JSON Format version 1.1b

The ARDF JSON format is a lightweight way to exchange ARDF (Radio Orienteering) competition data in web apps, APIs and small tools.

Current version: **ARDF JSON is in develop. It can be changed!**

The exact structure and allowed values are defined in the JSON Schema.

## Open categories

A category that accepts competitors of any gender may set `category_open` to
`true`. Keep the required Boolean `category_gender` for compatibility with
existing readers. When `category_open` is true, either Boolean value is valid
and the category imposes no gender restriction. If the flag is absent or
false, interpret `category_gender` as before. The flag describes the category
and does not change an individual competitor’s registered gender.

For example, a mixed Practice course can use this category object:

```json
{
  "category_name": "Long",
  "category_gender": true,
  "category_open": true
}
```

## Schema & examples in this repository

In this repository you will find:

- **JSON Schema for ARDF JSON**  
  Defines all properties, data types, enums and time formats.

- **Example JSON files**  
  Demonstrating a complete event document plus smaller race, results and startlist fragments.
  `ardf_schema_example.json` is the full document example for the schema. The other example
  files show reusable fragments that can be embedded in or derived from a full ARDF JSON
  document.
