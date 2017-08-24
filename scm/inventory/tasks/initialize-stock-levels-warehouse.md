--- 
title: Bestandswerte im Lagerort initialisieren
description: "Dieses Verfahren zeigt Ihnen, wie der verfügbare Lagerbestand manuell mithilfe einer Lagerverlagerungserfassung aktualisiert wird."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 953125ae6e9d669bd13a3344c9f679747af6ff93
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# Bestandswerte im Lagerort initialisieren

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


