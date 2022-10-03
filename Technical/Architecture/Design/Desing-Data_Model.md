# Technical | Architecture | Design | Data model

TODO: Show and explain data model (database/dto) that your project is going to use/implement.

## Class diagram example

``` mermaid
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }
```

[Link to examples](https://github.com/mermaid-js/mermaid/blob/develop/docs/classDiagram.md)

## Requirement Diagram:

``` mermaid
    requirementDiagram

    requirement test_req {
    id: 1
    text: the test text.
    risk: high
    verifymethod: test
    }

    element test_entity {
    type: simulation
    }

    test_entity - satisfies -> test_req
```

[Link to examples](https://github.com/mermaid-js/mermaid/blob/develop/docs/requirementDiagram.md)

## Entity Relationship diagram example:

``` mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

[Link to examples](https://github.com/mermaid-js/mermaid/blob/develop/docs/entityRelationshipDiagram.md)

