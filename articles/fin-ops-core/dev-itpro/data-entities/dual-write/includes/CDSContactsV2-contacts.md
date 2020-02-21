## <a name="cds-contacts-v2-to-contacts"></a>CDS-Kontakte V2 zu Kontakten

Diese Vorlage synchronisiert Daten zwischen Finance and Operations-Apps und Common Data Service.

Quellfilter: (AssociatedContactType = 1)

Umgekehrter Quellfilter: msdyn_contactforvendor eq true und msdyn_sellable eq false und msdyn_contactpersonid ne ''

Finance and Operations-Feld | Zuordnungstyp | Anderes Dynamics 365-Feld | Standardwert
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | nichts | Lieferant
FIRSTNAME | = | firstname | 
MIDDLENAME | = | middlename | 
LASTNAME | = | lastname | 
ASSOCIATEDCONTACTNUMBER | = | msdyn_vendorcontactid.msdyn_vendoraccountnumber | 
PRIMARYADDRESSCITY | = | address1_city | 
PRIMARYADDRESSCOUNTRYREGIONID | = | address1_country | 
PRIMARYADDRESSCOUNTYID | = | address1_county | 
PRIMARYFAXNUMBER | = | fax | 
PRIMARYADDRESSSTATEID | = | address1_stateorprovince | 
PRIMARYADDRESSSTREET | = | address1_line1 | 
PRIMARYADDRESSZIPCODE | = | address1_postalcode | 
PRIMARYPHONENUMBER | = | telephone1 | 
PRIMARYEMAILADDRESS | = | emailaddress1 | 
EMPLOYMENTDEPARTMENT | = | department | 
NOTES | = | description | 
GENDER | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | spousesname | 
nichts | >> | msdyn_contactforvendor | True
CONTACTPERSONID | = | msdyn_contactpersonid | 
