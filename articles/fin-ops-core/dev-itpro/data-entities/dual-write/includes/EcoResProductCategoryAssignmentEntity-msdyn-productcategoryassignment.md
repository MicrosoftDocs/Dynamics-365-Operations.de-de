## <a name="product-category-assignments-to-msdyn_productcategoryassignments"></a>Produktkategoriezuweisungen zu productcategoryassignments

Diese Vorlage synchronisiert Daten zwischen Finance and Operations-Apps und Common Data Service.

Finance and Operations-Feld | Zuordnungstyp | Anderes Dynamics 365-Feld | Standardwert
---|---|---|---
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber | 
PRODUCTCATEGORYNAME | = | msdyn_productcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_productcategory.msdyn_hierarchy.msdyn_name | 
PRODUCTNUMBER | >> | msdyn_name | 
