# WAFL Documentation

Latest version: `v0.1.0`

## What is WAFL?

**WAFL (Wider Attribute Formatting Language)** is an indentation-based configuration format with expressions, imports, schemas, and tags. The docs below describe the language itself.

**Example:**

```
@schema:
  App:
    name: string
    version: string
    port: int
    debug?: bool
    theme:
      primary: string
      secondary: string
    features: list<string>

app<App>:
  name: "WAFL Demo"
  version: "1.0.0"
  port = $ENV.PORT || 3000
  debug = $ENV.NODE_ENV === "dev"
  theme:
    primary = !rgb(255, 200, 80)
    secondary: "#111"
  features:
    - login
    - analytics
    - if $ENV.NODE_ENV === "dev": monitoring
```

## Table of contents

**[Getting Started]**
- [Introduction](https://github.com/wafl-lang/wafl-website/docs/v0.1.0/getting-started/introduction.mdx) (High-level overview of the WAFL format and concepts)
 
**[Specs]**
- [Structure](https://github.com/wafl-lang/wafl-website/blob/master/docs/v0.1.0/specs/structure.mdx) (Document scaffolding: headers, directives, indentation, and keys)
- [Values](https://github.com/wafl-lang/wafl-website/blob/master/docs/v0.1.0/specs/values.mdx) (Supported scalar types and how to write them)
- [Collections](https://github.com/wafl-lang/wafl-website/blob/master/docs/v0.1.0/specs/collections.mdx) (Objects, lists, and conditional list items)
- [Expressions](https://github.com/wafl-lang/wafl-website/blob/master/docs/v0.1.0/specs/expressions.mdx) (Evaluated values and environment variable access)
- [Tags](https://github.com/wafl-lang/wafl-website/blob/master/docs/v0.1.0/specs/tags.mdx) (Tagged values and built-in tag behaviors)
- [Directives](https://github.com/wafl-lang/wafl-website/blob/master/docs/v0.1.0/specs/directives.mdx) (Imports, schemas, and evaluation directives)
- [Validation](https://github.com/wafl-lang/wafl-website/blob/master/docs/v0.1.0/specs/validation.mdx) (Type annotations, schemas, and validation rules)
- [Examples](https://github.com/wafl-lang/wafl-website/blob/master/docs/v0.1.0/specs/examples.mdx) (Complete WAFL file showing structure, tags, imports, and validation together)

**[Versions]**
- [v0.1.0 (latest)](https://github.com/wafl-lang/wafl-website/tree/v0.1.0)
