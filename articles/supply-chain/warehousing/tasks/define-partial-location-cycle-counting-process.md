---
title: Partiellen Lagerplatzzykluszählungsprozess definieren
description: Wenn Sie Zykluszählungspläne verwenden, um Inventurarbeit zu erstellen, können Sie die tatsächlichen Zähleroperationen verwalten, indem Sie diese nur für bestimmte Produkte und Produktvarianten anfordern,  anstelle aller verfügbaren Lagerbestands am Lagerplatz zu zählen.
author: ShylaThompson
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcda301934c6ccc06f17ed8ae13c52754336d2ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830905"
---
# <a name="define-partial-location-cycle-counting-process"></a>Partiellen Lagerplatzzykluszählungsprozess definieren 

[!include [banner](../../includes/banner.md)]

Wenn Sie Zykluszählungspläne verwenden, um Inventurarbeit zu erstellen, können Sie die tatsächlichen Zähleroperationen verwalten, indem Sie diese nur für bestimmte Produkte und Produktvarianten anfordern,  anstelle aller verfügbaren Lagerbestands am Lagerplatz zu zählen. Indem Sie nach bestimmten Produkten filtern, kann der Lagerortleiter Prüfungsgemeinkosten senken, Konsolidierungsfehler vermeiden und Zeit sparen. Normalerweise werden diese Aufgaben von einem Lagerortleiter ausgeführt. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.


## <a name="create-a-cycle-counting-work-template"></a>Zykluszählungsarbeitsvorlage automatisch erstellen
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Arbeit" > "Arbeitsvorlagen".
2. Wählen Sie im Feld "Arbeitsauftragstyp" die Option "Zykluszählung" aus.
3. Klicken Sie auf "Neu".
4. Geben Sie im Feld "Laufende Nummer" eine Zahl ein.
    * Die Sortierreihenfolge ist von der kleinsten Nummer zur größten Nummer. Der Wert muss größer als 0 (null) sein.  
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Geben Sie im Feld "Arbeitsvorlage" einen Wert ein.
7. Geben Sie im Feld "Arbeitsvorlagenbeschreibung" einen Wert ein.
8. Geben Sie im Feld "Pool-ID" einen Wert ein, oder wählen Sie einen Wert aus.
9. Geben Sie im Feld "Arbeits-Priorität" eine Zahl ein.
10. Klicken Sie auf "Speichern".
11. Klicken Sie auf "Neu".
12. Markieren Sie in der Liste die ausgewählte Zeile.
13. Wählen Sie im Feld "Arbeitstyp" die Option "Zählung" aus.
14. Geben Sie im Feld "Arbeitsklassenkennung" einen Wert ein, oder wählen Sie einen Wert aus.
15. Klicken Sie auf "Speichern".
16. Arbeitspositionsumbrüche anklicken.
17. Klicken Sie auf "Neu".
18. Geben Sie im Feld "Laufende Nummer" eine Zahl ein.
    * Die Sortierreihenfolge ist von der kleinsten Nummer zur größten Nummer. Der Wert muss größer als 0 (null) sein.  
19. Klicken Sie auf "Speichern".
20. Schließen Sie die Seite.
21. Schließen Sie die Seite.

## <a name="create-a-cycle-counting-plan"></a>Zykluszählungsplan erstellen
1. Wechseln Sie zu Lagerortverwaltung > Einrichten > Permanente Inventur > Permanenten Inventurplan erstellen.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Zykluszählungs-Plankennung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Maximale Anzahl von Zykluszählungen" eine Zahl ein.
6. Geben Sie im Feld "Arbeitsvorlage" einen Wert ein, oder wählen Sie einen Wert aus.
7. Klicken Sie auf "Neu".
8. Geben Sie im Feld "Laufende Nummer" eine Zahl ein.
    * Die Sortierreihenfolge ist von der kleinsten Nummer zur größten Nummer. Der Wert muss größer als 0 (null) sein.  
9. Geben Sie im Feld "Beschreibung" einen Wert ein.
10. Klicken Sie auf "Speichern".
11. Produktabfrage definieren anklicken.
12. Markieren Sie in der Liste die ausgewählte Zeile.
13. Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.
14. Klicken Sie auf "OK".
15. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]