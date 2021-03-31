---
title: Kostensteuerungs-Arbeitsbereichsparameter konfigurieren
description: Verwenden Sie das folgende Verfahren, um den Kostenkontrollearbeitsbereich zu konfigurieren, damit die Manager auf verschiedenen Stufen in einer Organisation Einblick in ihre Kostenträger, wie Kostenstellen und Produktgruppen erhalten können.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61f25b93440495b2d1b70227ecda011c43c2e564
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208774"
---
# <a name="configure-cost-control-workspace-parameters"></a>Kostensteuerungs-Arbeitsbereichsparameter konfigurieren

[!include [banner](../../includes/banner.md)]

Verwenden Sie das folgende Verfahren, um den Kostenkontrollearbeitsbereich zu konfigurieren, damit die Manager auf verschiedenen Stufen in einer Organisation Einblick in ihre Kostenträger, wie Kostenstellen und Produktgruppen erhalten können. Das Demodatenunternehmen USP2 wurde dazu verwendet, diese Aufzeichnung zu erstellen.

1. Wechseln Sie zur Kostenbuchhaltung > Einstellungs > Kostenkontrollearbeitsbereichskonfiguration.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie "Ja" im Feld "Veröffentlichte Felder" aus.
    * Wenn Sie diese Option auf Ja setzen, können Benutzer, denen eine der Rollen zugewiesen wurde, den Bericht im Kostenkontrollerarbeitsbereich sehen: Kostenrechnungsmanager, Buchhalter, Kostenbuchhalter oder Kostenträgercontroller. Wenn Sie diese Option auf Nein setzen, können nur Benutzer, denen eine der Rollen zugewiesen wurde, den Bericht im Kostenkontrollerarbeitsbereich sehen: Kostenrechnungsmanager, Buchhalter, Kostenbuchhalter oder Kostenträgercontroller.  
6. Erweitern Sie den Datenenfilterungsabschnitt.
7. Geben Sie im Feld "Kostenkontrolleinheit" einen Wert ein oder wählen Sie einen Wert aus.
8. Geben Sie im Feld "Ursprüngliche Budgetversion" einen Wert ein, oder wählen Sie einen Wert aus.
9. Geben Sie im Feld "Kostenelementdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.
10. Geben Sie im Feld "Kostenobjektdimensionshierarchie" einen Wert ein oder wählen Sie einen Wert aus.
11. Erweitern Sie den Kalkulationsdatensatzabschnitt zuweisen.
12. Klicken Sie auf "Neu".
13. Markieren Sie in der Liste die ausgewählte Zeile.
14. Geben Sie im Feld "Steuerperiode" einen Wert ein oder wählen Sie einen Wert aus.
15. Geben Sie im Feld „Aktuelle Version” einen Wert ein oder wählen Sie einen Wert aus.
16. Erweitern Sie Steuerperioden pro Spaltenabschnitt.
17. Wählen Sie "Ja" im Feld Aktuelle Periode aus.
18. Erweitern Sie die Spalten, um die Kostenabschnitte anzuzeigen.
19. Wählen Sie "Ja" im Feld "Fixkosten" aus.
20. Wählen Sie "Ja" im Feld "Varialble Fixkosten" aus.
21. Wählen Sie "Ja" im Feld "Totale Fixkosten" aus.
22. Klicken Sie auf "Speichern".
23. Schließen Sie die Seite.
24. Wechseln Sie zu Buchhaltung > Arbeitsbereich  Kostenkontrolle.
25. Wählen Sie eine Anweisung aus, um die festen, variable, und nicht klassifizierten Gesamtkosten für den ausgewählten Buchhaltungszeitraum anzuzeigen.
26. Geben Sie im Feld "Steuerperiode" einen Wert ein oder wählen Sie einen Wert aus.
27. Geben Sie im Feld "Kostenobjektdimensionshierarchieknoten" einen Wert ein oder wählen Sie einen Wert aus.
    * Nachdem Sie eine Kostenträgerdimensionshierarchie ausgewählt haben, erweitern Sie die Kostenfaktordimensionshierarchie, um die gewünschten Kostenwerte anzuzeigen. So können Sie die Hierarchie zu den Produktionsgeschäftskosten erweitern, um den Wert zu finden.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]