## <a name="product-categories-to-msdyn_productcategories"></a>Produktkategorien zu msdyn_productcategories

Diese Vorlage synchronisiert Daten zwischen Finance and Operations-Apps und Common Data Service.

Finance and Operations-Feld | Zuordnungstyp | Anderes Dynamics 365-Feld | Standardwert
---|---|---|---
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_hierarchy.msdyn_name | 
ISCATEGORYINHERITINGPARENTPRODUCTATTRIBUTES | >< | msdyn_isinheritingparentproductattributes | 
PROJECTCATEGORYNAME | = | msdyn_projectcategoryname | 
ISTANGIBLEPRODUCT | >< | msdyn_istangibleproduct | 
ISCATEGORYINHERITINGPARENTCATEGORYATTRIBUTES | >< | msdyn_isinheritingparentcategoryattributes | 
CATEGORYCODE | = | msdyn_code | 
CATEGORYDESCRIPTION | = | msdyn_description | 
CATEGORYKEYWORDS | = | msdyn_keywords | 
CATEGORYNAME | = | msdyn_name | 
FRIENDLYCATEGORYNAME | = | msdyn_friendlycategoryname | 
PARENTPRODUCTCATEGORYNAME | = | msdyn_parentproductcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | >> | msdyn_parentproductcategory.msdyn_hierarchy.msdyn_name | 
