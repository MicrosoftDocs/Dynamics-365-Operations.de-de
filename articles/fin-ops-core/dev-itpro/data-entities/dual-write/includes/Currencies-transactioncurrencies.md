## <a name="currencies-to-transactioncurrencies"></a>Währungen zu transactioncurrencies

Diese Vorlage synchronisiert Daten zwischen Finance and Operations-Apps und Common Data Service.

Quellfilter: ((CURRENCYCODE != "999"))

Finance and Operations-Feld | Zuordnungstyp | Anderes Dynamics 365-Feld | Standardwert
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
nichts | >> | exchangerate | 1
