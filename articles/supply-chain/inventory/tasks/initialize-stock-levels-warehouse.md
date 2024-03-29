---
title: Bestandswerte im Lagerort initialisieren
description: Dieses Verfahren zeigt Ihnen, wie der verfügbare Lagerbestand manuell mithilfe einer Lagerverlagerungserfassung aktualisiert wird.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 264dabf9c1c10c3d2cee3e0c942abbfa249f21f5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565878"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Bestandswerte im Lagerort initialisieren

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt Ihnen, wie der verfügbare Lagerbestand manuell mithilfe einer Lagerverlagerungserfassung aktualisiert wird. (Es ist auch möglich den verfügbaren Lagerbestand zu aktualisieren, indem Sie Buchungen in Datenentitäten importieren.) Sie können dieses Handbuch im Demodatenunternehmen USMF ausführen, in dem alle Voraussetzungen wie Erfassungen, Artikeleinstellungen, Buchungsprofile und Konten verfügbar sind. Das Handbuch schlägt bestimmte Werte für den Artikel und die Dimensionen vor, die verwendet werden. Wenn Sie einen anderen Artikel auswählen, müssen Sie ggf. Werte für verschiedene Dimensionen eingeben.

1. Wechseln Sie zu Lagerverwaltung > Journaleinträge > Artikel > Bewegung.
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Wählen Sie IMov.
    * Es empfiehlt sich, verschiedene Erfassungsvorlagen für verschiedene Geschäftszwecke zu verwenden.  
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Geben Sie im Feld "Gegenkonto" den Wert "140200" an.
    * Hierbei handelt es sich um das in Erfassungspositionen als Standardkonto verwendete Gegenkonto. Es ist möglich, die Standardeinstellung zu überschreiben, um verschiedene Gegenkontos pro Position zuzuweisen.  
7. Klicken Sie auf "OK".
8. Klicken Sie auf "Neu".
9. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
10. Artikel A0001 auswählen.
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
12. Klicken Sie auf die Registerkarte "Lagerungsdimension".
13. Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
14. Wählen Sie Standort 1.
15. Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
16. Wählen Sie Lagerort 13.
17. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
18. Klicken Sie im Feld "Lagerplatz" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
19. Wählen Sie Lagerplatz 13.
20. Geben Sie im Feld "Menge" eine Zahl ein.
21. Klicken Sie auf "Speichern".
22. Klicken Sie auf "Buchen".
23. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Alle Buchungsfehler in eine neue Erfassung übertragen".
    * Wenn Sie diese Option aktivieren, werden alle Positionen, die nicht gebucht werden können, in eine neue Erfassung kopiert. Sie können die Informationen im Protokoll verwenden, um Probleme zu korrigieren und anschließend die Positionen erneut zu buchen.  
24. Klicken Sie auf "OK".
25. Schließen Sie die Seite.
26. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]