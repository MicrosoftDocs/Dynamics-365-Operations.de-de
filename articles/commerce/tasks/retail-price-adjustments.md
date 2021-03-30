---
title: " Einzelhandelspreisregulierungen"
description: Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung einer Handelspreisregulierung.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbd2f818930424313e1d76aea4a257efa7c7b3be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232784"
---
# <a name="retail-price-adjustments"></a> Einzelhandelspreisregulierungen

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung einer Handelspreisregulierung. Eine Preisregulierung kann den Verkaufspreis eines Artikels direkt festlegen oder den Basisverkaufspreis oder Handelsvereinbarungsverkaufspreis ändern. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Klicken Sie auf Verwaltung von Preisen und Rabatten.
2. Klicken Sie auf die Preisregulierungsregisterkarte.
3. Klicken Sie auf "Neu".
    * Von hier aus können Sie alle am häufigsten verwendeten Preis- und Rabattregeln erstellen, einschließlich Rabatte, Preisregulierungen, Handelsvereinbarungserfassungen und Kategoriepreiskalkulationsregeln.  
4. Klicken Sie auf "Preisregulierung".
5. Geben Sie im Feld "Name" einen Wert ein.
6. Erweitern Sie den Abschnitt "Positionen".
7. Klicken Sie auf Hinzufügen.
    * In vorliegenden Beispiel geben Sie "81126" im Produkt-Feld ein. Geben Sie anschließend "10,0" im Feld "Rabattprozentsatz" ein.  
    * Eine Rabattprozentsatz-Typpreisregulierung reduziert einen Basisverkaufspreis oder Handelsvereinbarungsverkaufspreis.  
8. Klicken Sie auf Hinzufügen.
    * In vorliegenden Beispiel geben Sie "81125" im Produkt-Feld ein. Anschließend wählen Sie "Skontobetrag" im Feld "Rabattmethode" aus.    Schließlich geben Sie "5,0" im Skontobetrag-Feld ein.  
    * Ein Skontobetrag-Rabatttyp ist ein Betrag, der von einem Basispreis oder von einem Handelsvereinbarungs-Preis abgezogen wird.  
9. Klicken Sie auf "Preisgruppen".
    * Wählen Sie im Feld "Preisgruppe" die Option "RP-Houston" aus.  
    * Dieses ordnet die Preisregulierung dem Houston-Shop zu.  
10. Klicken Sie auf "Speichern".
11. Schließen Sie die Seite.
12. Wählen Sie im Feld "Status" die Option "Aktiviert" aus.
13. Klicken Sie auf "Speichern".
14. Schließen Sie die Seite.
15. Aktualisieren Sie die Seite.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]