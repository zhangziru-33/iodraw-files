```mermaid
%% {init: {'theme': 'base', 'themeVariables': {'background': '#ffffff'}}}%%
erDiagram

    Company ||--o{ "Companies Involved" : "1对多（通过Company Name关联）"
    Company ||--o{ "PV Product" : "1对多（通过Company字段关联）"
    Company ||--o{ "Contact" : "1对多（通过Company Name关联）"
    
    "Market Project" ||--o{ "Companies Involved" : "1对多（通过Market Project字段关联）"
    "Market Project" ||--o{ "Contact Involved" : "1对多（通过Market Project字段关联）"
    "Market Project" ||--o{ "MP Product" : "1对多（通过Market Project字段关联）"

    "MP Product" }|--|| "PV Product" : "多对1（通过PV Product字段关联）"
    Contact ||--o{ "Contact Involved" : "1对多（通过Contact关联）"
    Contact ||--o{ "Company" : "1对多（通过Primary Contact关联）"

```