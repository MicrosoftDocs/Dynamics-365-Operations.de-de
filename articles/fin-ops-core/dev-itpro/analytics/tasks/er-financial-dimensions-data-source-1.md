---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)'
description: In diesem Artikel wird beschrieben, wie Sie ein EB-Modell (elektronische Berichterstellung) konfigurieren, um Finanzdimensionen als Datenquelle für EB-Berichte zu verwenden. (Teil 1)
author: kfend
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
ms.openlocfilehash: 053b9cf9ea6b2845bef5d95e901c1c90fac964be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290843"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a>ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.


## <a name="create-a-new-data-model"></a>Neues Datenmodell erstellen
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, ob „Litware, Inc.“ Anbieter ist verfügbar und markiert als aktiv.  
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
69. Klicken Sie auf Speichern.
70. Schließen Sie die Seite.

![EB-Datenmodelldesignerseite.](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
