---
title: Produktnummernbezeichnung für konfigurierte Produktvarianten erstellen
description: Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für konfigurierte Produktvarianten eingerichtet wird und sie einem konfigurierbaren Produktmaster zugeordnet werden kann.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f75d7e493255b9c09c10b121f388854861cb0fc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428700"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Produktnummernbezeichnung für konfigurierte Produktvarianten erstellen

[!include [banner](../../includes/banner.md)]

Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für konfigurierte Produktvarianten eingerichtet wird und sie einem konfigurierbaren Produktmaster zugeordnet werden kann. Dieses Verfahren beschreibt auch, wie eine Konfigurationsbezeichnung für eine Produktkonfigurationsmodellkomponente erstellen wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Die neue Produktnummernbezeichnung wird dem Produktmaster D0004 zugewiesen. Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Erstellen eine Produktnummerbezeichnung
1. Klicken Sie auf "Produktvariantenmodell-Definition".
2. Klicken Sie auf "Produktbezeichnung".
3. Klicken Sie auf "Neu".
4. Geben Sie im Feld "Name" einen Wert ein.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Klicken Sie auf Hinzufügen.
7. Klicken Sie auf "Produktmasternummer".
8. Klicken Sie auf Hinzufügen.
9. Klicken Sie auf Textkonstante.
10. Markieren Sie in der Liste die ausgewählte Zeile.
11. Geben Sie im Feld "Text" einen Wert ein.
12. Klicken Sie auf Hinzufügen.
13. Klicken Sie auf "Konfiguration".
14. Schließen Sie die Seite.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Zuweisen der Produktnummernbezeichnung zu einem Produktmaster
1. Klicken Sie auf "Produktmaster".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Produktnummer" mit dem Wert "D".
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie auf Bearbeiten.
5. Wählen Sie "Ja" im Feld "Bezeichnungen verwenden".
6. Geben Sie im Feld "Produktvariantennummerbezeichnung" eine Bezeichnung ein oder wählen Sie eine aus.
7. Schließen Sie die Seite.
8. Schließen Sie die Seite.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Erstellen einer Bezeichnung für eine Produktkonfigurationsmodellkomponente
1. Klicken Sie auf "Produktkonfigurationsmodelle".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie auf Bearbeiten.
5. Wählen Sie "Ja" im Feld "Konfigurationsbezeichnungen verwenden".
6. Klicken Sie auf Hinzufügen.
7. Klicken Sie auf Attributwert.
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.
10. Klicken Sie auf Hinzufügen.
11. Klicken Sie auf Textkonstante.
12. Markieren Sie in der Liste die ausgewählte Zeile.
13. Geben Sie im Feld "Text" einen Wert ein.
14. Klicken Sie auf Hinzufügen.
15. Klicken Sie auf Attributwert.
16. Markieren Sie in der Liste die ausgewählte Zeile.
17. Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.
18. Klicken Sie auf Hinzufügen.
19. Klicken Sie auf Textkonstante.
20. Markieren Sie in der Liste die ausgewählte Zeile.
21. Geben Sie im Feld "Text" einen Wert ein.
22. Klicken Sie auf Hinzufügen.
23. Klicken Sie auf Attributwert.
24. Markieren Sie in der Liste die ausgewählte Zeile.
25. Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.
26. Klicken Sie auf Hinzufügen.
27. Klicken Sie auf Textkonstante.
28. Markieren Sie in der Liste die ausgewählte Zeile.
29. Geben Sie im Feld "Text" einen Wert ein.
30. Klicken Sie auf Hinzufügen.
31. Klicken Sie auf Attributwert.
32. Markieren Sie in der Liste die ausgewählte Zeile.
33. Geben Sie im Feld 'Attribut' einen Wert ein, oder wählen Sie einen Wert aus.
34. Klicken Sie auf Hinzufügen.
35. Klicken Sie auf Textkonstante.
36. Markieren Sie in der Liste die ausgewählte Zeile.
37. Geben Sie im Feld "Text" einen Wert ein.
38. Klicken Sie auf Hinzufügen.
39. Klicken Sie auf Nummernkreiswert.
40. Markieren Sie in der Liste die ausgewählte Zeile.
41. Geben Sie im Feld "Nummernkreis" einen Wert ein, oder wählen Sie einen Wert aus.
42. Schließen Sie die Seite.
43. Schließen Sie die Seite.
44. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]