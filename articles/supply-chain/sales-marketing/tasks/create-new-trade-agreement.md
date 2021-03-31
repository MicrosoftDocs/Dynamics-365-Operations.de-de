---
title: Eine neue Handelsvereinbarung erstellen
description: Dieses Verfahren zeigt Ihnen an, wie eine Handelsvereinbarung erstellt, in der Sie einen Verkaufspreis der neuen Produktdimensionsgruppen erfassen, den Sie mit einem bestimmten Debitor aktualisiert haben.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c4ac436b57b6010a5d5b3759d2ccf1c4af95446
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208134"
---
# <a name="create-a-new-trade-agreement"></a>Eine neue Handelsvereinbarung erstellen

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt Ihnen an, wie eine Handelsvereinbarung erstellt, in der Sie einen Verkaufspreis der neuen Produktdimensionsgruppen erfassen, den Sie mit einem bestimmten Debitor aktualisiert haben. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen. Wenn Sie eigene Daten verwenden, bevor Sie dieses Handbuch starten, müssen Sie prüfen, ob ein Handelsvereinbarungserfassungsname vorhanden ist, in die standardmäßige Beziehung festgelegt ist „Preis- (Verkauf )“.


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Erstellen und buchen einer neuen Handelsvereinbarungs-Erfassung.
1. Wechseln Sie zu **Navigationsbereich > Module > Verrieb und Marketing > Preise und Rabatte > Handelsvereinbarungserfassungen**.
2. Klicken Sie auf **Neu**.
3. Klicken Sie im Feld **Name** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie im **Aktivitätsbereich** auf **Zeilen**.
6. Wählen Sie im Feld **Kontocode** die Option „Tabelle“ aus.
    
    In diesem Beispiel aktualisieren Sie den Preis für einen bestimmten Debitor, dem Durchschnitt Sie Tabelle auswählen muss. Wenn Sie den Listenpreis des Produkts aktualisierten, wählen Sie „Alle“ aus, damit der neue Preis für alle Debitoren gültig ist. Wenn Sie Preise unter verschiedenen Debitorensegmenten unterschieden, dann geben Sie Gruppe auswählen. Um Gruppe festzulegen, muss Debitorenpreisgruppen eingerichtet haben.  

7. Klicken Sie im Feld **Konto-Auswahl** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
9. Wählen Sie im Feld **Artikelcode** „Tabelle“ aus.
    
    Wenn Sie eine Handelsvereinbarung vom Typ „Preis (Verkauf)“ eingeben, müssen Sie nur „Tabelle“ im Feld **Artikelcode** auswählen. Dies ist, da ein Preis ein absoluter Wert ist und nicht gleiche für alle oder eine Gruppe Produkte werden kann.
    
10. Klicken Sie im Feld **Artikelrelation** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. In der Liste wählen Sie das Produkt aus, das Sie in die Vereinbarung aufnehmen wollen. Notieren Sie, an dem Produkt Sie ausgewählt haben.  
12. Geben Sie in das **Von**-Feld eine Minimalmenge ein.
    - Wenn der Debitor eine Mindestmenge bestellen muss, bevor er sich für den neuen Preis qualifiziert, dann können Sie diese Menge hier angeben.  
    - Geben Sie einen Wert im **Bis**-Feld ein, um die maximale Menge anzugeben, bis zu der der Preis der Vereinbarung nicht gültig ist. Wenn Sie Preise und Rabatte auf Grundlage mehrerer Mengennachlässe anbieten, dann geben Sie jeden Mengennachlass als Paar der minimalen und maximalen Menge in den **Von**- und **Bis**-Feldern an.
13. Geben Sie einen Preis in das Feld **Betrag in Währung** ein.
14. Geben Sie im Abschnitt **Details** im Feld **Von Datum** ein Datum ein, ab dem diese Vereinbarung gilt.
15. Klicken Sie auf **Speichern**.
16. Klicken Sie auf **Überprüfen**.
17. Klicken Sie auf **Ausgewählte Positionen überprüfen.**
18. Klicken Sie auf **OK**.
19. Klicken Sie auf **Buchen**.
20. Klicken Sie auf **OK**.

## <a name="view-trade-agreements-for-a-product"></a>Handelsvereinbarungen für ein Produkt anzeigen
1. Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.
2. Wählen Sie in der Liste suchen Sie und wählen Sie das Produkt aus, dessen Preis Sie derzeit aktualisiert haben.
3. Klicken Sie im **Aktivitätsbereich** auf **Verkaufen**.
4. Klicken Sie auf **Handelsvereinbarungen** anzeigen.
    
    Prüfen Sie die Details der Preishandelsvereinbarung, soeben erstellt haben.    

5. Schließen Sie die Seite.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="whitepaper"></a>Whitepaper
Laden Sie für weitere Informationen das folgende Whitepaper herunter (geschrieben zur Unterstützung von AX2012, gilt jedoch weiterhin für Dynamics 365 Supply Chain Management)
- [Handelsvereinbarungen](https://mbs.microsoft.com/files/public/CS/AX2012R3/TradeagreementsinAX.pdf)

### <a name="community-blogs"></a>Communityblogs
- [Verkaufspreise in Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]