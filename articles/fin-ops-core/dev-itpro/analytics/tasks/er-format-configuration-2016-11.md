---
title: ER Erstellen eine Formatkonfiguration (November 2016)
description: In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen ist, eine Format-Konfiguration für elektronische Berichterstellung (ER) erstellen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fd41b1724eb2e0405c0e7a7e0ff0aea4a945e0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184944"
---
# <a name="er-create-a-format-configuration-november-2016"></a>ER Erstellen eine Formatkonfiguration (November 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ zugewiesen ist, eine Format-Konfiguration für elektronische Berichterstellung (ER) erstellen kann. Diese Formatkonfiguration definiert das Format von elektronischen Dokumenten, die für die Verarbeitung von Zahlungen verwendet werden. In diesem Beispiel erstellen Sie eine Formatkonfiguration für das Beispielunternehmen Litware, Inc. Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte in der Prozedur "Modell für ausgewählte Datenquellen zuweisen abschließen".


## <a name="create-a-new-format-configuration"></a>Dient zum Erstellen einer neuen Format-Konfiguration.
1. Wechseln Sie zu **Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung**.
2. Klicken Sie auf **Berichterstellungskonfigurationen**.
3. Wählen Sie **Zahlungen (vereinfachtes Modell)** in der Struktur aus.
4. Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.

 > [!NOTE]
 > Wenn **Konfiguration erstellen** nicht angezeigt wird, müssen Sie den Entwurfsmodus der Seite **Elektronische Berichterstellungsparameter** aktivieren. 
 
5. Im **neuen** Feld geben Sie **Format auf Grundlage Datenmodell PaymentModel** ein.
6. Geben Sie im Feld **Name** **BACS (Großbritannien fiktiv)** ein.
7. Geben Sie im Feld **Beschreibung** den Typ **BACS-Kreditorenzahlungsformat (Großbritannien fiktiv**en Namens)" ein.
    * Der aktive Konfigurationsanbieter wird automatisch hier eingegeben. Dieser Anbieter ist in der Lage, diese Konfiguration verwalten. Andere Anbieter können diese Konfiguration verwenden, werden jedoch nicht in der Lage sein, sie zu verwalten.  
    * Ein spezielles Format elektronischer Dokumente kann definiert werden. Lassen Sie das Feld leer, wenn Sie ein Format zur Laufzeit auswählen möchten.  
8. Geben Sie im Feld **Datenmodelldefinition** einen Wert ein, oder wählen Sie einen Wert aus.
9. Klicken Sie auf **Konfiguration erstellen**. Ein neuer Konfiguration wurde erstellt. Die Entwurfsversion kann verwendet werden, um das Designformat für die Verwaltung von elektronischen Dokumenten zu speichern.  

## <a name="design-the-format-of-an-electronic-document"></a>Entwerfen Sie Format elektronischer Dokumente
1. Klicken Sie auf **Designer**.
2. Klicken Sie auf **Stamm hinzufügen**, um das Ablagedialogfeld zu öffnen.
3. Wählen Sie in der Struktur **Common\File** aus.
4. Geben Sie im Feld **Name** **Xml** ein.
5. Geben Sie im Feld **Kodierung** **UTF-8** ein.
6. Klicken Sie auf **OK**.
7. Klicken Sie auf **Hinzufügen**.
8. Wählen Sie in der Struktur den Knoten **XML\Element**.
9. Geben Sie im Feld **Name** **Nachricht** ein.
10. Klicken Sie auf **OK**.
11. Wählen Sie in der Struktur **XML\Nachricht** aus.
12. Klicken Sie auf **Element hinzufügen**.
13. Geben Sie im Feld **Name** **ProcessingDate** ein.
14. Klicken Sie auf **OK**.
15. Klicken Sie auf **Element hinzufügen**.
16. Geben Sie im Feld Name **MessageId** ein.
17. Klicken Sie auf **OK**.
18. Klicken Sie auf **Element hinzufügen**.
19. Geben Sie im Feld **Name** **Zahlungen** ein.
20. Klicken Sie auf **OK**.
21. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen** aus.
22. Klicken Sie auf **Element hinzufügen**.
23. Geben Sie im Feld **Name** **Item** ein.
24. Klicken Sie auf **OK**.
25. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel** aus.
26. Klicken Sie auf **Hinzufügen**.
27. Wählen Sie in der Struktur **XML\Attribute** aus.
28. Geben Sie im Feld Name **Id** ein.
29. Klicken Sie auf **OK**.
30. Klicken Sie auf **Hinzufügen**.
31. Wählen Sie in der Struktur den Knoten **XML\Element**.
32. Geben Sie im Feld Name **Lieferant** ein.
33. Klicken Sie auf **OK**.
34. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor** aus.
35. Klicken Sie auf **Element hinzufügen**.
36. Geben Sie im Feld "Typ" **Name** ein.
37. Klicken Sie auf **OK**.
38. Klicken Sie auf **Element hinzufügen**.
39. Geben Sie im Feld **Name** **Bank** ein.
40. Klicken Sie auf **OK**.
41. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank** aus.
42. Klicken Sie auf **Element hinzufügen**.
43. Geben Sie im Feld **Name** **RoutingNumber** ein.
44. Klicken Sie auf **OK**.
45. Klicken Sie auf **Element hinzufügen**.
46. Geben Sie im Feld **Name** **AccountNumber** ein.
47. Klicken Sie auf **OK**.
48. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor** aus.
49. Klicken Sie auf **Kopieren**.
50. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel** aus.
51. Klicken Sie auf **Einfügen**.
52. Geben Sie im Feld **Name** **Zahler** ein.
53. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel** aus.
54. Klicken Sie auf **Element hinzufügen**.
55. Geben Sie im Feld **Name** **Währung** ein.
56. Klicken Sie auf **OK**.
57. Klicken Sie auf **Element hinzufügen**.
58. Geben Sie im Feld **Name** **Beschreibung** ein.
59. Klicken Sie auf **OK**.
60. Klicken Sie auf **Element hinzufügen**.
61. Geben Sie im Feld Typ **TransDate** ein.
62. Klicken Sie auf **OK**.
63. Klicken Sie auf **Element hinzufügen**.
64. Geben Sie im Feld Namen **Betrag** ein.
65. Klicken Sie auf **OK**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Bereiten Sie Formatkomponenten für das Zuordnen zu den Datenmodellelementen vor
1. Wählen Sie in der Struktur **XML\Nachricht\ProcessingDate** aus.
2. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.
3. Wählen Sie in der Struktur **Text\DateTime** aus.
4. Geben Sie im Feld **Format** **yyyy-MM-dd** ein.
5. Klicken Sie auf **OK**.
6. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\TransDate** aus.
7. Klicken Sie auf **DateTime hinzufügen**.
8. Geben Sie im Feld **Format** **yyyy-MM-dd** ein.
9. Wählen Sie im Feld **DateTime**-Typ die Option **Date** aus.
10. Klicken Sie auf **OK**.
11. Wählen Sie in der Struktur **XML\Nachricht\MessageId** aus.
12. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.
13. Wählen Sie in der Struktur **Text\String** aus.
14. Klicken Sie auf **OK**.
15. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Name** aus.
16. Klicken Sie auf **Zeichenfolge hinzufügen**.
17. Klicken Sie auf **OK**.
18. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\RoutingNumber** aus.
19. Klicken Sie auf **Zeichenfolge hinzufügen**.
20. Klicken Sie auf **OK**.
21. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\AccountNumber** aus.
22. Klicken Sie auf **Zeichenfolge hinzufügen**.
23. Klicken Sie auf **OK**.
24. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Zahlender\Name** aus.
25. Klicken Sie auf **Zeichenfolge hinzufügen**.
26. Klicken Sie auf **OK**.
27. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\RoutingNumber** aus.
28. Klicken Sie auf **Zeichenfolge hinzufügen**.
29. Klicken Sie auf **OK**.
30. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\AccountNumber** aus.
31. Klicken Sie auf **Zeichenfolge hinzufügen**.
32. Klicken Sie auf **OK**.
33. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Währung** aus.
34. Klicken Sie auf **Zeichenfolge hinzufügen**.
35. Klicken Sie auf **OK**.
36. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Beschreibung** aus.
37. Klicken Sie auf **Zeichenfolge hinzufügen**.
38. Klicken Sie auf **OK**.
39. Wählen Sie in der Struktur **XML\Nachricht\Zahlungen\Artikel\Betrag** aus.
40. Klicken Sie auf **Zeichenfolge hinzufügen**.
41. Klicken Sie auf **OK**.
42. Klicken Sie auf **Speichern**.
43. Schließen Sie die Seite.

