---
title: Eine Organisationsberichtshierarchie erstellen
description: Gehen Sie folgendermaßen vor, um eine Berichtshierarchie für Organisationsberichterstellung zu erstellen.
author: twheeloc
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e247ad7ac79607ce5f7209c343aabc5e3b66163a
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734718"
---
# <a name="create-an-organization-report-hierarchy"></a>Eine Organisationsberichtshierarchie erstellen

[!include [banner](../../includes/banner.md)]

Gehen Sie folgendermaßen vor, um eine Berichtshierarchie für Organisationsberichterstellung zu erstellen. Der Zweck dieser Buchung ist, Sie durch die Dimensionshierarchie zu führen, sodass Sie den Vorgang fortsetzen können, bis die gesamte Organisationsberichterstellungsstruktur erstellt wurde. Für diese Aufzeichnung wird das Demo-Datenunternehmen USP2 verwendet.

1. Wechseln Sie zu **Kostenrechnung > Dimensionen > Dimensionshierarchien**.
2. Klicken Sie auf **Neu**.
3. Wählen Sie im Feld **HierarchyTypeComboBox** „Dimensionsklassifizierungshierarchie“ aus.
    * Wählen Sie Dimensionsklassifizierungs-Hierarchie aus. Der Typ Dimensionsklassifizierungshierarchie wird zur Regeldefinition und zu Berichterstellungszwecken verwendet. Er unterstützt alle Dimensionen, wie Kostenobjekte, Kostenelemente und statistischen Dimensionen.  
4. Klicken Sie auf **Erstellen**.
5. Geben Sie im Feld **Dimensionshierarchiename** „Organisation USP2“ ein.
6. Geben Sie im Feld **Dimension** einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie Kostenstellen.  
7. Klicken Sie auf **Speichern**.
8. Klicken Sie auf **Hierarchie anzeigen**.
9. Klicken Sie auf **Neu**.
10. Geben Sie im Feld **Knotenname** „CEO“ ein.
11. Klicken Sie auf **Speichern**.
12. Klicken Sie auf **Neu**.
13. Geben Sie im Feld **Knotenname** „CEO-Kostenstellen“ ein.
14. Klicken Sie auf **Speichern**.
15. Klicken Sie auf **Neu**.
16. Geben Sie im Feld **Knotenname** „Region Ost“ ein.
17. Klicken Sie auf **Speichern**.
18. Klicken Sie auf **Neu**.
19. Markieren Sie in der Liste die ausgewählte Zeile.
20. Geben Sie im Feld **Von Dimensionsmitglied** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie das Dimensionsmitglied aus, das dem Knoten entspricht.  
21. Klicken Sie auf **Speichern**.
22. Wählen Sie in der Strukturdarstellung Oganisation USP2\CEO\CEO Kostenstellen
23. Klicken Sie auf **Neu**.
24. Geben Sie im Feld **Knotenname** „Region West“ ein.
25. Klicken Sie auf **Speichern**.
26. Klicken Sie auf **Neu**.
27. Markieren Sie in der Liste die ausgewählte Zeile.
28. Geben Sie im Feld **Von Dimensionsmitglied** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie das Dimensionsmitglied aus, das dem Knoten entspricht.  
29. Klicken Sie auf **Speichern**.
30. Wählen Sie in der Struktur Organisation USP2\CEO ein.
31. Klicken Sie auf **Neu**.
32. Geben Sie im Feld **Knotenname** „CFO-Kostenstellen“ ein.
33. Klicken Sie auf **Speichern**.
34. Klicken Sie auf **Neu**.
35. Geben Sie im Feld **Knotenname** „Marketing-Kampagne“ ein.
36. Geben Sie im Feld **Knotenname** „Marketing-Kampagne“ ein.
37. Klicken Sie auf **Speichern**.
38. Klicken Sie auf **Neu**.
39. Markieren Sie in der Liste die ausgewählte Zeile.
40. Geben Sie im Feld **Von Dimensionsmitglied** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie das Dimensionsmitglied aus, das dem Knoten entspricht.  
41. Klicken Sie auf **Speichern**.
42. Wählen Sie in der Strukturdarstellung "Organisation USP2\CEO\CFO Kostenstellen".
43. Klicken Sie auf **Neu**.
44. Geben Sie im Feld **Knotenname** „Handelsmessen“ ein.
45. Klicken Sie auf **Speichern**.
46. Klicken Sie auf **Neu**.
47. Markieren Sie in der Liste die ausgewählte Zeile.
48. Geben Sie im Feld **Von Dimensionsmitglied** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie das Dimensionsmitglied aus, das dem Knoten entspricht.  
49. Klicken Sie auf **Speichern**.
50. Wählen Sie in der Struktur Organisation USP2\CEO ein.
51. Geben Sie im Feld **Knotenname** „CIO-Kostenstellen“ ein.
52. Klicken Sie auf **Speichern**.
53. Klicken Sie auf **Neu**.
54. Geben Sie im Feld **Knotenname** „Callcenter“ ein.
55. Klicken Sie auf **Speichern**.
56. Klicken Sie auf **Neu**.
57. Markieren Sie in der Liste die ausgewählte Zeile.
58. Geben Sie im Feld **Von Dimensionsmitglied** einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie das Dimensionsmitglied aus, das dem Knoten entspricht.  
59. Klicken Sie auf **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
