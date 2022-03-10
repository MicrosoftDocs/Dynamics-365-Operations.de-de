---
title: Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben
description: In diesem Thema wird beschrieben, wie das Rechnungsbuch verwendet wird, um Rechnungen zu erstellen.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc8e8ec224208990563e7c0f5d354bb13bb45fbcd35821e7f980b6cfb2c5a379
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777263"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie das Rechnungsbuch verwendet wird, um Rechnungen zu erstellen. Nehmen Sie anschließend den Rechnungspool, um die Rechnung mit einer Bestellung abzugleichen und die Ausgaben auf der Kreditorenrechnungsseite abzuschließen.


## <a name="create-a-purchase-order"></a>Eine Bestellung erstellen
1. Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Bestellungen > Bestellungen**.
2. Klicken Sie auf **Neu** , um eine neue Bestellung zu erstellen.
3. Wählen Sie im Feld **Kreditorenkonto** einen Lieferant aus der Dropdownliste, um eine Option auszuwählen. Wählen Sie z. B. Händler **1001** aus.
4. Wählen Sie **OK**.
5. Wählen Sie im Feld **Artikelnummer** die Services-Artikelnummer aus der Dropdown-Liste aus. Wählen Sie z. B. **S0001** aus. Der Nettobetrag ist 75,00.  Der ist der Betrag, den wir auf der Rechnung erwarten.  
6. Wählen Sie im Aktivitätsbereich **Einkauf** aus.
7. Wählen Sie **Bestätigen** aus.

## <a name="create-and-post-and-invoice"></a>Erstellen und buchen und fakturieren
1. Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Rechnungen > Rechnungserfassung**.
2. Wählen Sie **Neu** aus.
3. Öffnen Sie die Suche, um den Namen des Rechnungsregisters auswählen, das Sie verwenden möchten.
4. Wählen Sie den Namen des Rechnungsregisters aus, den Sie benutzen möchten.
5. Klicken Sie auf **Positionen**, um das Register zu öffnen und Ausgabenpositionen einzugeben.
6. Wählen Sie in der Suche einen Händler aus. Wählen Sie z. B. Händler **1001** aus.
7. Geben Sie im Feld **Rechnung** die Rechnungsnummer ein.
8. Geben Sie im Feld **Beschreibung** einen Wert ein.
9. Geben Sie im Feld **Kredit** eine Zahl ein.
10. Öffnen Sie im Feld **Bestellung** die Dropdownliste, um die Bestellung auszuwählen, die Sie eben erstellt haben.
11. Markieren Sie im Feld **Genehmigt von** einen Genehmiger in der Dropdownliste und klicken Sie **Auswählen**, um diesen auszuwählen.
12. Wählen Sie **Buchen** aus.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Öffnen einer Rechnung aus dem Pool und Abgleichen mit einer Bestellung, um den Rechnungsprozess abzuschließen
1. Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Rechnungen > Rechnungspool**.
2. Klicken Sie auf **Bestellung**, um eine Kreditorenrechnung aus der Rechnung im Pool zu erstellen.
3. Wählen Sie die Rechnung aus, die Sie prüfen möchten.
4. Klicken Sie auf **Abgleichstatus**, um den Abgleich abzuschließen.
5. Wählen Sie im Aktivitätsbereich **Optionen** aus.
6. Wählen Sie **Ansicht wechseln** aus.
7. Wählen SIe **Rasteransicht** aus.
8. Wählen Sie **Buchen** aus.
9. Schließt das Formular.
10. Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Kreditoren > Kreditoren**.
11. Wählen Sie den Händler aus, der auf der Bestellung war. Wählen Sie z. B. Händler **1001** aus.
12. Wählen Sie im Aktivitätsbereich **Kreditoren** aus.
13. Wählen Sie **Buchungen** aus.
14. Wählen Sie die Rechnung aus, die Sie erstellt haben. Die Rechnungsbuchabgrenzung wurde storniert und auf das entsprechende Ausgabenkonto gebucht.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]