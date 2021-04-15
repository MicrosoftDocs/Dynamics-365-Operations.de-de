---
title: " Treueprogramme definieren"
description: Im folgenden Verfahren sehen Sie, wie ein Treueprogramm mit zwei Treuestufen eingerichtet wird.
author: jashanno
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8013ffc0727fddd7acde58e75182ee9f3165c09d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796825"
---
# <a name="define-loyalty-programs"></a> Treueprogramme definieren

[!include [banner](../includes/banner.md)]

Im folgenden Verfahren sehen Sie, wie ein Treueprogramm mit zwei Treuestufen eingerichtet wird. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Gehen Sie zu Retail and Commerce > .. > Treueprogramme.
2. Klicken Sie auf Neu.
3. Geben Sie im Feld "Name" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie auf "Position hinzufügen".
6. Geben Sie im Feld "Ebene" eine Zahl ein.
7. Geben Sie im Feld "Stufe" einen Namen für die Treuestufe ein.
8. Geben Sie im Feld "Beschreibung" einen Wert ein.
9. Klicken Sie im Feld "Datumsintervall" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Dieses Datumsintervall sollte sich auf die Zukunft erstrecken. Wenn beispielsweise das Datumsintervall, das für Goldstufenebene ausgewählt ist, ein Jahr beträgt, kann jeder Debitor, der sich für die Goldstufenebene qualifiziert, die Belohnungen in Anspruch nehmen, die der Goldstufenebene für ein Jahr zugewiesen sind. Wenn der Debitor sich erneut für die Goldstufenebene qualifiziert, während er sich in dieser Stufe befindet, wird das Datum, an dem seine Stufe abläuft, um ein Jahr verlängert, beginnend an dem Datum, an dem er sich erneut qualifiziert.  
10. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
11. Klicken Sie auf "Position hinzufügen".
12. Geben Sie im Feld "Ebene" eine Zahl ein.
13. Geben Sie im Feld "Stufe" einen Namen für die Treuestufe ein.
14. Geben Sie im Feld "Beschreibung" einen Wert ein.
15. Klicken Sie im Feld "Datumsintervall" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
16. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
17. Klicken Sie auf "Speichern".
18. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Ebenenregeln definieren die Belohnungspunkt-Mindestanzahl, die in einer Zeitperiode erworben werden muss, um sich für die Ebene zu qualifizieren.  
19. Schalten Sie die Erweiterung des Abschnitts "Stufenregeln" ein/aus.
20. Klicken Sie auf "Neu".
    * Für eine Stufe können mehrere Stufenregeln verwendet werden. So können Sie beispielsweise drei verschiedene Kriterien haben, um eine Stufe zu erwerben; durch die Ausgabe von 500 EUR in einem Monat, durch die Ausgabe von 1000 EUR in einem Jahr und nach 20 Buchungen in einem Jahr. Zu diesem Zweck müssen Sie drei Stufenregeln erstellen.  
21. Klicken Sie im Feld "Belohnungspunkt" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Dies muss ein nicht-einlösbarer Treuebelohnungspunkt sein.  
22. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
23. Geben Sie im Feld "Niedrigste vergebene Punktanzahl" eine Zahl ein.
    * Wenn sich alle Debitoren für die niedrigste Treuestufe qualifizieren können, indem sie einfach am Programm teilnehmen, geben Sie 0 (Null) ein.  
24. Klicken Sie im Feld "Beurteilungsdatumsintervall" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Dieses Datumsintervall sollte sich auf die Vergangenheit erstrecken. Nur Punkte, die für dieses Datumsintervall erworben wurden, werden für das Erreichen des mindestens ausgegebenen Punktwerts gezählt.  
25. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
26. Klicken Sie auf "Speichern".
27. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
28. Klicken Sie auf Neu.
29. Klicken Sie im Feld "Belohnungspunkt" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
30. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
31. Geben Sie im Feld "Niedrigste vergebene Punktanzahl" eine Zahl ein.
32. Klicken Sie im Feld "Beurteilungsdatumsintervall" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Dieses Datumsintervall sollte sich auf die Vergangenheit erstrecken.  
33. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
34. Klicken Sie auf "Speichern".
35. Klicken Sie auf "Preisgruppen".
    * Wenn Debitoren mit Kundentreue Rabatte erhalten sollen. Sie müssen eine oder mehrere Preisgruppen dem Treueprogramm zuweisen und die Preisgruppen zu den Rabatten zuweisen. Es ist ein bewährtes Verfahren, Preisgruppen nicht mit unterschiedlichen Arten von Rabattentitäten zu kombinieren.  Verwenden Sie beispielsweise nicht die gleiche Preisgruppe für einen Treuerabatt und einen Kanalrabatt.  
36. Klicken Sie im Feld "Preisgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Der Preisgruppenlink am oberen Seitenrand ist für das Treueprogramm. Der Preisgruppenlink im Programmstufen-Inforegister ist nur für eine bestimmte Treueebene.  
37. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
38. Klicken Sie auf "Speichern".
39. Schließen Sie die Seite.
40. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]