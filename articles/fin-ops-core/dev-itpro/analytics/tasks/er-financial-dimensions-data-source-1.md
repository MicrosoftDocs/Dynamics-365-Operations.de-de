---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)'
description: In den folgenden Schritten wird erläutert, wie ein Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92481749fa15d8a9c273edf6a79ee9fcfdc722e7
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550670"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a>ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.


## <a name="create-a-new-data-model"></a>Neues Datenmodell erstellen
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, ob "Litware, Inc." Anbieter ist verfügbar und markiert als aktiv.  
2. Klicken Sie auf "Berichterstellungskonfigurationen".
3. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
4. Geben Sie im Feld "Name" "Finanzdimensions-Beispielmodell" ein.
5. Klicken Sie auf Konfiguration erstellen.
6. Klicken Sie auf Designer.
7. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
8. Geben Sie im Feld "Name" "Erfassung" ein.
9. Klicken Sie auf Hinzufügen.
10. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
11. Geben Sie im Feld Name "Firma" ein.
12. Klicken Sie auf Hinzufügen.
    * Wir fügen unserem Modell eine neue Datensatzliste hinzu. Diese Liste enthält die Einstellungen aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen). Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Einstellungen der Dimension angezeigen.  
13. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
14. Geben Sie im Feld "Name" "Dimensionseinstellung" ein.
15. Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.
16. Klicken Sie auf Hinzufügen.
17. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
18. Geben Sie im Feld "Name" "Code" ein.
19. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
20. Klicken Sie auf Hinzufügen.
21. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
22. Geben Sie im Feld "Name" "Name" ein.
23. Klicken Sie auf Hinzufügen.
24. Wählen Sie in der Struktur 'Erfassung' aus.
25. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
26. Geben Sie im Feld "Name" "Journal" ein.
27. Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.
28. Klicken Sie auf Hinzufügen.
29. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
30. Geben Sie im Feld "Name" "Charge" ein.
31. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
32. Klicken Sie auf Hinzufügen.
33. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
34. Geben Sie im Feld "Name" "Buchung" ein.
35. Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.
36. Klicken Sie auf Hinzufügen.
37. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
38. Geben Sie im Feld "Name" "Datum" ein.
39. Wählen Sie im Feld "Artikeltyp" 'Datum' aus.
40. Klicken Sie auf Hinzufügen.
41. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
42. Geben Sie im Feld "Name" "Soll" ein.
43. Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.
44. Klicken Sie auf Hinzufügen.
45. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
46. Geben Sie im Feld "Name" "Haben" ein.
47. Klicken Sie auf Hinzufügen.
48. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
49. Geben Sie im Feld "Name" 'Währung' ein.
50. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
51. Klicken Sie auf Hinzufügen.
52. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
53. Geben Sie im Feld "Name" "Beleg" ein.
54. Klicken Sie auf Hinzufügen.
55. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
56. Geben Sie im Feld "Name" "Dimensionsdaten" ein.
57. Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.
58. Klicken Sie auf Hinzufügen.
    * Wir haben unserem Modell einen neue Datensatzliste hinzugefügt. Diese Liste enthält die Werte aus ausgewählten Finanzdimensionen (für einen ER-Berichte, die dieses Modell als Datenquelle nutzen). Jede Finanzdimension wird in dieser Liste als Datensatz mit den entsprechenden Feldern dargestellt, welche die Werte der Dimension angezeigen. Der Dimensionsname wird auch in diesem Datensatz als nutzbares Feld angezeigt (z. B. zur Auswahl).  
59. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
60. Geben Sie im Feld "Name" "Code" ein.
61. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
62. Klicken Sie auf Hinzufügen.
63. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
64. Geben Sie im Feld "Name" "Beschreibung" ein.
65. Klicken Sie auf Hinzufügen.
66. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
67. Geben Sie im Feld "Name" "Name" ein.
68. Klicken Sie auf Hinzufügen.
69. Klicken Sie auf "Speichern".
70. Schließen Sie die Seite.

