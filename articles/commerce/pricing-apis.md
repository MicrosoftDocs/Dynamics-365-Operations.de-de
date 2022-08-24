---
title: Commerce-Preis-APIs
description: In diesem Artikel werden verschiedene Preis-APIs beschrieben, die von Microsoft Dynamics 365 Commerce Preis-Engine bereitgestellt werden.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294117"
---
# <a name="commerce-pricing-apis"></a>Commerce-Preis-APIs

[!include [banner](../includes/banner.md)]

In diesem Artikel werden verschiedene Preis-APIs beschrieben, die von Microsoft Dynamics 365 Commerce Preis-Engine bereitgestellt werden.

Die Dynamics 365 Commerce Pricing Engine bietet die folgenden Retail Server-APIs, die von externen Anwendungen genutzt werden können, um verschiedene Preisszenarien zu unterstützen:

- **GetActivePrices** – Diese API erhält den berechneten Preis eines Produkts, einschließlich einfacher Rabatte.
- **CalculateSalesDocument** – Diese API berechnet Preise und Rabatte für Produkte in bestimmten Mengen, wenn sie zusammen gekauft werden.
- **GetAvailableAktionen** – Diese API erhält anwendbare Rabatte für Produkte im Warenkorb. 
- **AddCoupons** – Diese API fügt Coupons zu einem Warenkorb hinzu.
- **RemoveCoupons** – Diese API entfernt Coupons aus einem Warenkorb.

Weitere Informationen zur Verwendung von Retail Server-APIs in externen Anwendungen finden Sie unter [Verwenden Sie Retail-Server-APIs in externen Anwendungen](dev-itpro/consume-retail-server-api.md).

## <a name="getactiveprices"></a>GetActivePrices

Die API *GetActivePrices* wurde in der Commerce-Version 10.0.4 eingeführt. Diese API erhält den berechneten Preis eines Produkts, einschließlich einfacher Rabatte. Sie berechnet keine Rabatte für mehrere Zeilen und geht davon aus, dass jedes Produkt in einer API-Anforderung eine Menge von 1 hat. Diese API kann auch eine Liste von Produkten als Eingabe verwenden und den Preis einzelner Produkte in großen Mengen abfragen.

Die API *GetActivePrices* unterstützt die Commerce-Rollen **Angestellter**, **Kunde**, **Anonym** und **Anwendung**.

Der Hauptanwendungsfall für die API *GetActivePrices* ist die Produktdetailseite (PDP), auf der Einzelhändler den besten Preis für ein Produkt präsentieren möchten, einschließlich wirksamer Rabatte.

Die folgende Tabelle zeigt die Eingabeparameter für die API *GetActivePrices*.

| Name                                    | Untername | Typ | Erforderlich/Optional | Description |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | Erforderlich | |
|                                         | ChannelId | lang | Erforderlich | |
|                                         | CatalogId | lang | Erforderlich | |
| productIds                              | | IEnumerable\<long\> | Erforderlich | Die Liste der Produkte, für die Preise berechnet werden sollen. |
| activeDate                              | | DateTimeOffset | Erforderlich | Das Datum, an dem die Preise berechnet werden. |
| customerId                              | | Zeichenfolge | Optional | Die Debitorenkontonummer. |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | Optional | Die Zugehörigkeit und Treuestufen. |
|                                         | AffiliationId | lang | Erforderlich | Die Zugehörigkeitskennung. |
|                                         | LoyaltyTierId | lang | Optional | Die Treuestufekennung. |
| includeSimpleDiscountsInContextualPrice | | bool | Optional | Stellen Sie diesen Parameter auf **true**, um einfache Rabatte in die Preiskalkulation einzubeziehen. Der Standardwert ist **Falsch**. |
| includeVariantPriceRange                | | bool | Optional | Stellen Sie diesen Parameter auf **true**, um die Mindest- und Höchstpreise aller Varianten für ein Hauptprodukt zu erhalten. Der Standardwert ist **Falsch**. |
| includeAttainablePricesAndDiscounts     | | bool | Optional | Stellen Sie diesen Parameter auf **true**, um erreichbare Preise und Rabatte zu erhalten. Der Standardwert ist **Falsch**. |

**Beispiel für Anforderungstext**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Beispielantworttext**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

Die API *CalculateSalesDocument* wurde in der Commerce-Version 10.0.25 eingeführt. Diese API berechnet Preise und Rabatte für Produkte in bestimmten Mengen, wenn sie zusammen in einer Bestellung gekauft werden. Die Preiskalkulation der *CalculateSalesDocument*-API berücksichtigt sowohl Rabatte für einzelne Zeilen als auch Rabatte für mehrere Zeilen.

Der Hauptanwendungsfall für die *CalculateSalesDocument* API ist die Preisberechnung in Szenarien, in denen der vollständige Warenkorbkontext nicht bestehen bleibt (z. B. Verkaufsangebote). Auch Szenarien im Point of Sale (POS) und Commerce E-Commerce können von diesem Anwendungsfall profitieren. Ein niedrigerer Gesamtpreis, wenn Artikel im Warenkorb als Set berechnet werden (z. B. bei Einzelpaketen, verknüpften oder empfohlenen Produkten oder Produkten, die bereits in den Warenkorb gelegt wurden) kann Kunden davon überzeugen, Produkte in den Warenkorb zu legen.

Das Datenmodell sowohl für die Anfrage als auch für die Antwort der *CalculateSalesDocument* API ist **Einkaufskorb**. Im Kontext dieser API wird jedoch das Datenmodell **SalesDocument** benannt. Da die meisten Eigenschaften optional sind und nur wenige die Preisberechnung beeinflussen, werden in der folgenden Tabelle nur preisbezogene Felder angezeigt. Wir empfehlen, keine anderen Felder in die API-Anforderung einzubeziehen.

Der Geltungsbereich der *CalculateSalesDocument* API ist nur die Berechnung von Preisen und Rabatten. Steuern und Abgaben werden nicht inkludiert.

Die folgende Tabelle zeigt die Eingabeparameter innerhalb des benannten Objekts **salesDocument**.

| Name             | Untername | Typ | Erforderlich/Optional | Description |
|------------------|----------|------|-------------------|-------------|
| ID               | | Zeichenfolge | Erforderlich | Die Kennung des Verkaufsbelegs. |
| CartLines        | | IList\<CartLine\> | Optional | Die Liste der Positionen, für die Preise und Rabatte berechnet werden sollen. |
|                  | Produktkennung | lang | Erforderlich im Rahmen von CartLine | Die Produktdatensatzkennung. |
|                  | ItemId | Zeichenfolge | Optional | Der Artikelbezeichner. Wenn ein Wert angegeben wird, muss er mit dem Wert von **ProductId** Parameter übereinstimmen. |
|                  | InventoryDimensionId | Zeichenfolge | Optional | Der Bestandsdimensionsbezeichner. Wenn ein Wert angegeben wird, muss die Kombination der Werte **ItemId** und **InventoryDimensionId** mit dem Wert von **ProductId** übereinstimmen. |
|                  | Menge | decimal | Erforderlich im Rahmen von CartLine | Die Menge des Produkts. |
|                  | UnitOfMeasureSymbol | Zeichenfolge | Optional | Die Einheit des Produkts. Wenn kein Wert angegeben wird, verwendet die API standardmäßig die Verkaufseinheit des Produkts. |
| CustomerId       | | Zeichenfolge | Optional | Die Debitorenkontonummer. |
| LoyaltyCardId    | | Zeichenfolge | Optional | Die Treuekartenkennung. Jedes Kundenkonto, das mit der Treuekarte verknüpft ist, muss dem Wert des **CustomerId** Parameters (sofern vorhanden) entsprechen. Die Treuekarte wird nicht berücksichtigt, wenn sie nicht gefunden wird oder ihr Status **Gesperrt** ist. |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | Optional | Zugehörigkeits- und Treuestufenpositionen. Wenn **CustomerId** und/oder **LoyaltyCardId** bereitgestellt werden, werden die entsprechenden Positionen der Zugehörigkeits-Treuestufe mit den Positionen zusammengeführt, die in **AffiliationLines** bereitgestellt werden. |
|                  | AffiliationId | lang | Erforderlich im Rahmen von AffiliationLoyaltyTier | Die Zugehörigkeitsdatensatzkennung. |
|                  | LoyaltyTierId | lang | Erforderlich im Rahmen von AffiliationLoyaltyTier | Die Treuestufedatensatzkennung. |
|                  | AffiliationTypeValue | int | Erforderlich im Rahmen von AffiliationLoyaltyTier | Ein Wert, der angibt, ob die Zugehörigkeitsposition vom Typ **Allgemein** (**0**) oder **Zugehörigkeit** (**1**) ist. Wenn dieser Parameter auf **0** eingestellt ist, übernimmt die API den Wert **AffiliationId** als Bezeichner und ignoriert den Wert **LoyaltyTierId**. Wenn dieser Parameter auf **1** eingestellt ist, übernimmt die API den Wert **LoyaltyTierId** als Bezeichner und ignoriert den Wert **AffiliationId**. |
|                  | ReasonCodeLines | Kollektion\<ReasonCodeLine\> | Erforderlich im Rahmen von AffiliationLoyaltyTier | Ursachencodepositionen. Dieser Parameter hat keinen Einfluss auf die Preiskalkulation, wird aber als Teil des Elements **AffiliationLoyaltyTier** benötigt. |
|                  | CustomerId | Zeichenfolge | Erforderlich im Rahmen von AffiliationLoyaltyTier | Die Debitorenkontonummer. |
| Gutscheine          | | IList\<Coupon\> | Optional | Gutscheine, die nicht anwendbar sind (inaktiv, abgelaufen oder nicht gefunden), werden bei der Preisberechnung nicht berücksichtigt. |
|                  | Code | Zeichenfolge | Erforderlich im Rahmen von Coupon | Der Couponcode. |
|                  | CodeId | Zeichenfolge | Optional | Der Couponcodebezeichner. Wenn ein Wert angegeben wird, muss er mit dem Wert des **Code** Parameters übereinstimmen. |
|                  | DiscountOfferId | Zeichenfolge | Optional | Der Rabattbezeichner. Wenn ein Wert angegeben wird, muss er mit dem Wert des **Code** Parameters übereinstimmen. |

**Beispiel für Anforderungstext**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Das gesamte Warenkorbobjekt wird als Antworttext zurückgegeben. Um Preise und Rabatte zu überprüfen, sollten Sie sich auf die Felder in der folgenden Tabelle konzentrieren.

| Name           | Untername | Typ | Description |
|----------------|----------|------|--------------|
| NetPrice       | | decimal | Der Nettopreis des gesamten Verkaufsbelegs vor Abzug der Rabatte. |
| DiscountAmount | | decimal | Der Gesamtrabattbetrag des gesamten Verkaufsbelegs. |
| Gesamtbetrag    | | decimal | Der Gesamtbetrag des gesamten Verkaufsbelegs. |
| CartLines      | | IList\<CartLine\> | Berechnete Zeilen, die Preis- und Rabattdetails enthalten. |
|                | Preis | decimal | Der Einheitspreis des Produkts. |
|                | NetPrice | decimal | Der Nettopreis für die Position vor Abzug der Rabatte (= *Preis* &times; *Menge*). |
|                | DiscountAmount | decimal | Der Rabattbetrag. |
|                | Gesamtbetrag | decimal | Das endgültige Gesamtpreisergebnis der Position. |
|                | PriceLines | IList\<PriceLine\> | Preisdetails, einschließlich der Quelle des Preises (Basispreis, Preisanpassung oder Handelsvereinbarung) und des Betrags. |
|                | DiscountLines | IList\<DiscountLine\> | Rabattdetails. |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

Bei einem Einkaufskorb mit mehreren Positionen gibt die Api *GetAvailablePromotions* alle anwendbaren Rabatte für die Warenkorbpositionen zurück. 

Der Hauptanwendungsfall für die *GetAvailablePromotions* API ist die Warenkorbseite, auf der Einzelhändler angewendete Rabatte oder verfügbare Coupons für den aktuellen Warenkorb präsentieren möchten.

Die folgende Tabelle zeigt die Eingabeparameter für die API *GetAvailablePromotions*.

| Name        | Typ | Erforderlich/Optional | Description |
|-------------|------|-------------------|-------------|
| Schlüssel         | Zeichenfolge | Erforderlich | Die Einkaufskorbkennung. |
| cartLineIds | IEnumerable\<string\> | Optional | Legen Sie diesen Parameter fest, um Rabatte nur für ausgewählte Warenkorbpositionen zurückzugeben. |

**Beispielantworttext**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

Die Api *AddCoupons* unterstützt das Hinzufügen einer Liste von Gutscheinen zu einem Einkaufskorb. Es gibt das Einkaufskorbelement zurück, nachdem die Gutscheine hinzugefügt wurden.

Die folgende Tabelle zeigt die Eingabeparameter für die API *AddCoupons*.

| Name                 | Typ | Erforderlich/Optional | Description |
|----------------------|------|-------------------|-------------|
| Schlüssel                  | Zeichenfolge | Erforderlich | Die Einkaufskorbkennung. |
| couponCodes          | IEnumerable\<string\> | Erforderlich | Die Gutscheincodes, die dem Warenkorb hinzugefügt werden sollen. |
| isLegacyDiscountCode | bool | Optional | Stellen Sie diesen Parameter auf **true** um anzuzeigen, dass es sich bei dem Gutschein um einen alten Rabattcode handelt. Der Standardwert ist **Falsch**. |

## <a name="removecoupons"></a>RemoveCoupons

Die API *RemoveCoupons* unterstützt das Entfernen einer Liste von Gutscheinen aus einem Einkaufskorb. Es gibt das Einkaufskorbelement zurück, nachdem die Gutscheine entfernt wurden.

Die folgende Tabelle zeigt die Eingabeparameter für die API *RemoveCoupons*.

| Name        | Typ | Erforderlich/Optional | Description |
|-------------|------|-------------------|-------------|
| Schlüssel         | Zeichenfolge | Erforderlich | Die Einkaufskorbkennung. |
| couponCodes | IEnumerable\<string\> | Erforderlich | Die Gutscheincodes, die aus dem Warenkorb entfernt werden sollen. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
