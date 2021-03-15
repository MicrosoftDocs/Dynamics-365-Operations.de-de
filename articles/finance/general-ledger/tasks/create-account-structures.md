---
title: Kontostrukturen erstellen
description: Dieser Aufgabenleitfaden führt Sie durch die Erstellung einer Kontostruktur.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a8df7d7d9c4555bf46ac1cc3f71695837b1369b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968579"
---
# <a name="create-account-structures"></a>Kontostrukturen erstellen

[!include [banner](../../includes/banner.md)]

Dieser Aufgabenleitfaden führt Sie durch die Erstellung einer Kontostruktur. Bei den Schritten wird das Demodatunternehmen USMF verwendet.

1. Gehen Sie zu **Navigationsbereich > Module > Hauptbuch > Kontenplan > Strukturen > Kontostrukturen konfigurieren**.
2. Klicken Sie im **Aktivitätsbereich** auf **Neu**, um das Dropdown-Dialogfeld zu öffnen.
3. Im Feld **Kontostruktur** geben Sie einen Namen ein, um den Zweck der Kontostruktur zu beschreiben.
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein, um den Zweck der Kontostruktur zu beschreiben.
5. Klicken Sie auf **Erstellen**.
6. Klicken Sie in **Segmente und zulässige Werte** auf **Segment hinzufügen**.
7. Wählen Sie in er Liste „Dimensionen“ die Dimension aus, um sie der Kontostruktur hinzuzufügen.
8. Am Ende der Liste klicken Sie auf **Segment hinzufügen**.
9. Wiederholen Sie die Schritte 6 bis 9 nach Bedarf.
10. Wählen Sie im Abschnitt **Details zu zulässigem Wert** das Segment aus, um die zulässigen Werte zu bearbeiten.
    Beispielsweise klicken Sie auf das Feld **Hauptkonto**.  
11. Wählen Sie im Feld **Operator** eine Option aus (z. B. „liegt zwischen“ und „schließt ein“).
12. Geben Sie im Feld **Wert** einen Wert ein. Beispiel: 600000.  
13. Geben Sie im Feld **Bis** einen Wert ein. Beispiel: 699999.  
14. Im Abschnitt **Details zu zulässigem Wert** klicken Sie auf **Übernehmen**.
15. Wiederholen Sie die Schritte 10 bis 15 nach Bedarf.  
16. Im Abschnitt **Details zu zulässigem Wert** klicken Sie auf **Neue Kriterien hinzufügen**.
17. Wählen Sie im Feld "Operator" eine Option aus (z. B., "liegt zwischen" und "schließt ein").
18. Geben Sie im Feld **Wert** einen Wert ein. Beispiel: 033.  
19. Geben Sie im Feld **Bis** einen Wert ein. Beispiel: 034.  
20. Klicken Sie auf **Übernehmen**.
21. Wählen Sie im Raster das Segment aus, um die zulässigen Werte zu bearbeiten. Beispiel: "Kostenstelle".  
22. Geben Sie im **CostCenter-Feld** einen Wert ein. Beispiel: 007..021.  
23. Klicken Sie in **Segmente und zulässige Werte** auf **Hinzufügen**.
24. Geben Sie im Feld **MainAccount** einen Wert ein. Beispiel: 600000..699999  
25. Wählen Sie im Raster das Segment aus, um die zulässigen Werte zu bearbeiten. Beispiel: "Abteilung".  
26. Geben Sie im Feld "Abteilung" einen Wert ein. Beispiel: 032.  
27. Geben Sie im Feld "CostCenter" einen Wert ein. Beispiel: 086.  
28. Klicken Sie im **Aktivitätsbereich** auf **Überprüfen**.
29. Klicken Sie im **Aktivitätsbereich** auf **Aktivieren**.
30. Klicken Sie auf **Aktivieren**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]