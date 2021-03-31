---
title: Debitoren-Fälligkeitsinformationen einrichten und generieren
description: Dieses Handbuch unterstützt Sie dabei, eine Zahlungsfristdefinition sowie Dauerdebitorensalden einzurichten und Salden in der Liste "Saldorückblick" und auf der Seite "Inkasso" anzuzeigen.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b21fe217aacd11821ff8d5cf7c7682b2181e36c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220082"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Debitoren-Fälligkeitsinformationen einrichten und generieren

[!include [banner](../../includes/banner.md)]

Dieses Handbuch unterstützt Sie dabei, eine Zahlungsfristdefinition sowie Dauerdebitorensalden einzurichten und Salden in der Liste "Saldorückblick" und auf der Seite "Inkasso" anzuzeigen. Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.


## <a name="create-an-aging-period-definition"></a>Eine Zahlungsfristdefinition erstellen
1. Wechseln Sie zu **Navigationsbereich > Module > Kredit und Inkasso > Einstellungen > Zahlungsfristdefinitionen**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Zahlungsfristdefinition** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Klicken Sie auf **Unten hinzufügen**, um eine neue Zahlungsfrist einzufügen.
6. Geben Sie im Feld **Periode** die Beschreibung ein, die in Fälligkeitsberichten angezeigt werden soll.
7. Geben Sie im Feld **Einheit** eine Zahl ein.
8. Wählen Sie im Feld **Intervall** eine Option aus. Die Sachkontoperiode passt die Periode an Ihren Sachkontokalender an. Tag, Woche, Monat, Quartal und Jahre definieren die Größe des Intervalls nach Datumstyp. Bei "Unbegrenzt" werden alle Buchungen vor oder nach der vorherigen Periode ausgewählt, je nachdem, ob sie die erste oder letzte Periode ist.  
9. Wählen Sie im Feld **Fälligkeitsindikator** eine Option aus.
10. Wählen Sie die Periode oben im Raster aus. Aktualisieren Sie die Beschreibung, um die älteste Periode in der Zahlungsfristdefinition zu beschreiben
11. Geben Sie im Feld **Periode** die neue Beschreibung der Zahlungsfrist ein.
12. Schließen Sie die Seite.

## <a name="age-the-balances"></a>Die Salden nach Fälligkeit anzeigen
1. Wechseln Sie zu **Kredit und Inkasso > Periodische Aufgaben > Fällige Debitorensalden**.
2. Wählen Sie im Feld **Zahlungsfristdefinition** die Zahlungsfristdefinition aus, die Sie selbst erstellt haben.
    + Sie können eine aktive Momentaufnahme für jede Zahlungsfristdefinition haben.  
    + Alle Debitoren werden standardmäßig verarbeitet. Sie können diese Auswahl verwenden, um einen einzelnen Inkassopool von Debitoren zu berechnen.  
    + Wählen Sie das Datum aus der Transaktion aus, das Sie für die Fälligkeit verwenden.  
    + Wählen Sie ein "per"-Datum für die Fälligkeit aus. Der Standardwert ist Heute, aber, wenn Sie dieses Feld zu "Ausgewähltes Datum" ändern, können Sie das Datum auswählen, das sie möchten. Verwenden Sie für die Stapelverarbeitung das "Heutige Datum".  
3. Erweitern Sie den Bereich **Unternehmen**. Sie können die Unternehmen auswählen, die in die Momentaufnahme eingeschlossen werden. Das aktuelle Unternehmen wird standardmäßig ausgewählt.
4. Klicken Sie auf **OK,** um die Momentaufnahme zu verarbeiten. Es wird einige Zeit dauern. Warten Sie deshalb, bis der Schieberegler ausgeblendet wird und überprüfen Sie das Nachrichtencenter nach einer Nachricht.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Die Salden auf der Liste "Saldenrückblick" und auf der Seite "Inkasso" anzeigen
1. Wechseln Sie zu **Kredit und Inkasso > Inkassi > Saldenrückblick**. Auf der Listenseite werden die Salden für den Debitor angezeigt. Das Fälligkeitssymbol zeigt die Zahlungsfrist für die älteste Transaktion an.  
2. Wählen Sie einen Debitor mit einem Saldo aus.
3. Erweitern Sie den Infoboxbereich **Fälligkeit**, um den Saldenrückblick anzuzeigen. Die Zahlungsfristdefinition für die Infobox ist der standardmäßigen Zahlungsfristdefinition entnommen, die in den Parametern angegeben ist. Sie können sie mithilfe des Menüs "Mahnen" ändern.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]