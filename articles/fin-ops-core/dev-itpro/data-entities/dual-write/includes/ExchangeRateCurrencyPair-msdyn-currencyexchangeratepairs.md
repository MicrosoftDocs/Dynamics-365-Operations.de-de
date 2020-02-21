## <a name="exchange-rate-currency-pair-to-msdyn_currencyexchangeratepairs"></a>Währungspaar für Wechselkurs zu msdyn_currencyexchangeratepairs

Diese Vorlage synchronisiert Daten zwischen Finance and Operations-Apps und Common Data Service.

Finance and Operations-Feld | Zuordnungstyp | Anderes Dynamics 365-Feld | Standardwert
---|---|---|---
EXCHANGERATEDISPLAYFACTOR | >< | msdyn_displayfactor | 
EXCHANGERATETYPENAME | = | msdyn_currencyexchangeratetypeid.msdyn_name | 
FROMCURRENCYCODE | = | msdyn_fromtransactioncurrencyid.isocurrencycode | 
TOCURRENCYCODE | = | msdyn_totransactioncurrencyid.isocurrencycode | 
