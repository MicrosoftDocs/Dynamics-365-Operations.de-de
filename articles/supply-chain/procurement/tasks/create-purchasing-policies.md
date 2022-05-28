---
title: Einkaufsrichtlinien erstellen
description: In diesem Thema wird erläutert, wie Einkaufsrichtlinien so erstellt werden, dass sie sich an Ihren Geschäftsprozessen für den Einkauf ausrichten.
author: GalynaFedorova
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f51c88506044359787257ba0e0a6668213a170d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677869"
---
# <a name="create-purchasing-policies"></a>Einkaufsrichtlinien erstellen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Einkaufsrichtlinien so erstellt werden, dass sie sich an Ihren Geschäftsprozessen für den Einkauf ausrichten. Bevor Sie Einkaufsrichtlinien erstellen können, sind die Einkaufsrichtlinienparameter einzurichten. Es ist möglich, eine Einkaufsrichtlinie zu erstellen, zu ändern und außer Kraft zu setzen, aber Sie können keine Einkaufsrichtlinie löschen. Diese Prozedur würde normalerweise von einem Einkaufsleiter ausgeführt werden. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.


## <a name="set-up-policy-parameters"></a>Einrichten von Richtlinienparametern
1. Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Einstellungen > Richtlinien > Einkaufsrichtlinien**.
2. Wählen Sie im Aktivitätsbereich **Parameter** aus.
- Richtlinienrangfolgenregeln gelten für verschiedene Ebenen in Ihrer Organisation. Die organisatorischen Einheiten, die hier angezeigt werden, sind von der Hierarchie in Ihrer Organisation abhängig sowie von den Ebenen in der Hierarchie, denen der Zweck der "Beschaffung - interne Kontrolle" zugewiesen wird. Beispielsweise hat Ihre Organisation möglicherweise juristische Personen, Kostenstellen, Regionen und Abteilungen, aber möglicherweise haben nur einige von ihnen einen Hierarchiezweck "Beschaffung - interne Kontrolle". Als Standard ist die Organisation vom Typ "Unternehmen" verfügbar.  
3. Wählen Sie die Registerkarte **Parameter für den Richtlinienregeltyp** aus.
4. Wechseln Sie im Baum zu **Einkaufsrichtlinie > Bestellanforderungs-Steuerungsregel**.
- Sie definieren die Prioritätsreihenfolge für die Richtlinienauflösung auf Richtlinienebene. Bei einigen Richtlinientypen lässt sich jedoch die Prioritätsreihenfolge für einzelne Richtlinienregeltypen überschreiben. Zum Beispiel definieren Sie möglicherweise die Prioritätsreihenfolge für Einkaufsrichtlinien folgendermaßen: Kostenstelle, Abteilung, Unternehmen. Für die Katalogrichtlinienregel möchten Sie möglicherweise folgende Prioritätsreihenfolge festlegen: Abteilung, Kostenstelle, Unternehmen. Sie können die Prioritätsreihenfolge für die Katalogrichtlinienregel ändern. Wenn eine Arbeitskraft eine Anforderung erstellt, wird der angezeigte Katalog anhand der Richtlinien bestimmt, die zunächst der Abteilung der betreffenden Arbeitskraft, dann der zugehörigen Kostenstelle und dann ihrem Unternehmen zugeordnet werden.  
- Wenn mehr als eine Organisationsebene aufgelistet ist, können Sie die Pfeile nach oben/nach unten verwenden, um die Prioritätsreihenfolge für die Steuerungsregel für Bestellanforderung festzulegen.  
5. Schließen Sie die Seite.

## <a name="create-a-new-policy"></a>Neue Richtlinie erstellen
1. Wählen Sie **Neu** aus.
2. Geben Sie im Feld **Name** einen Wert ein.
3. Geben Sie im Feld **Beschreibung** einen Wert ein.
- Eine einzelne Einkaufsrichtlinie kann nur für eine Organisationshierarchie gelten. Zum Beispiel könnten Sie eine Hierarchie genannt Geographisch haben und eine mit der Bezeichnung Abteilung und Sie könnten für jede von ihnen eine unterschiedliche Einkaufsrichtlinie haben.  
- Wählen Sie eine Organisation aus, für die die Richtlinie gelten soll.  
4. Klicken Sie auf den Pfeil, um die ausgewählte Organisation hinzuzufügen.
- Sie können diesen Prozess wiederholen, um mehr Organisationen hinzuzufügen.  

## <a name="add-a-policy-rule"></a>Eine Richtlinienregel hinzufügen
1. Wählen Sie in der Liste **Richtlinienregeltyp** die **Anforderungszweckregel** aus.
- Sie schaffen eine Regel, die den Standardanforderungszweck auf den Typ Verbrauch festlegt, aber zulässt, dass der Typ Wiederbeschaffung stattdessen ausgewählt wird.  
2. Wählen Sie **Richtlinienregel erstellen** aus.
3. Wählen Sie **Ja** im Feld **Manuelles Überschreiben zulassen** aus.
4. Wählen Sie **Schließen** aus.
- Jetzt können Sie andere Richtlinienregeln für die Einkaufsrichtlinie haben. Beachten Sie, dass ein Richtlinienregeltyp keine sich überschneidenden Regeln haben kann, die gleichzeitig innerhalb einer einzelnen Beschaffungsrichtlinie aktiv sind.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]