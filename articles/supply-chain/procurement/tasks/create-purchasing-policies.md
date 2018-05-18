--- 
title: Erstellen von Einkaufsrichtlinien
description: "Diese Prozedur zeigt Ihnen, wie Einkaufsrichtlinien so erstellt werden, dass sie sich an Ihren Geschäftsprozessen für den Einkauf ausrichten."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2b3a66443394f5bfbe51b6685513281025d68fd
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-purchasing-policies"></a>Erstellen von Einkaufsrichtlinien

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt Ihnen, wie Einkaufsrichtlinien so erstellt werden, dass sie sich an Ihren Geschäftsprozessen für den Einkauf ausrichten. Bevor Sie Einkaufsrichtlinien erstellen können, sind die Einkaufsrichtlinienparameter einzurichten. Es ist möglich, eine Einkaufsrichtlinie zu erstellen, zu ändern und außer Kraft zu setzen, aber Sie können eine Einkaufsrichtlinie nicht löschen. Diese Prozedur würde normalerweise von einem Einkaufsleiter ausgeführt werden. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.


## <a name="set-up-policy-parameters"></a>Einrichten von Richtlinienparametern
1. Wechseln Sie zu "Einkaufsrichtlinien".
2. Klicken Sie auf "Parameter".
    * Richtlinienrangfolgenregeln gelten für verschiedene Ebenen in Ihrer Organisation. Die organisatorischen Einheiten, die hier angezeigt werden, sind von der Hierarchie in Ihrer Organisation abhängig sowie von den Ebenen in der Hierarchie, denen der Zweck der "Beschaffung - interne Kontrolle" zugewiesen wird. Beispielsweise hat Ihre Organisation möglicherweise juristische Personen, Kostenstellen, Regionen und Abteilungen, aber möglicherweise haben nur einige von ihnen einen Hierarchiezweck "Beschaffung - interne Kontrolle". Als Standard ist die Organisation vom Typ "Unternehmen" verfügbar.  
3. Klicken Sie auf die Registerkarte "Parameter für den Richtlinienregeltyp".
4. Im Baum wählen Sie die "Einkaufsrichtlinien-\Bestellanforderungssteuerungsregel" aus.
    * Sie definieren die Prioritätsreihenfolge für die Richtlinienauflösung auf Richtlinienebene. Bei einigen Richtlinientypen lässt sich jedoch die Prioritätsreihenfolge für einzelne Richtlinienregeltypen überschreiben. Zum Beispiel definieren Sie möglicherweise die Prioritätsreihenfolge für Einkaufsrichtlinien folgendermaßen: Kostenstelle, Abteilung, Unternehmen. Für die Katalogrichtlinienregel möchten Sie möglicherweise folgende Prioritätsreihenfolge festlegen: Abteilung, Kostenstelle, Unternehmen. Sie können die Prioritätsreihenfolge für die Katalogrichtlinienregel ändern. Wenn eine Arbeitskraft eine Anforderung erstellt, wird der angezeigte Katalog anhand der Richtlinien bestimmt, die zunächst der Abteilung der betreffenden Arbeitskraft, dann der zugehörigen Kostenstelle und dann ihrem Unternehmen zugeordnet sind.  
    * Wenn mehr als eine Organisationsebene aufgelistet ist, können Sie die Pfeile nach oben/unten verwenden, um die Prioritätsreihenfolge für die "Steuerungsregel für Bestellanforderung" festzulegen.  
5. Schließen Sie die Seite.

## <a name="create-a-new-policy"></a>Neue Richtlinie erstellen
1. Klicken Sie auf "Neu".
2. Geben Sie im Feld "Name" einen Wert ein.
3. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Eine einzelne Einkaufsrichtlinie kann nur für eine Organisationshierarchie gelten. Zum Beispiel könnten Sie eine Hierarchie genannt "Geographisch" haben und eine mit der Bezeichnung "Abteilung" und Sie könnten für jede von ihnen eine unterschiedliche Einkaufsrichtlinie haben.  
    * Wählen Sie eine Organisation aus, für die die Richtlinie gelten soll.  
4. Klicken Sie auf den Pfeil, um die ausgewählte Organisation hinzuzufügen.
    * Sie können diesen Prozess wiederholen, um mehr Organisationen hinzuzufügen.  

## <a name="add-a-policy-rule"></a>Eine Richtlinienregel hinzufügen
1. Wählen Sie in der Liste "Richtlinienregeltyp" die Anforderungszweckregel aus.
    * Sie schaffen eine Regel, die den Standardanforderungszweck auf den Typ "Verbrauch" festlegt, aber zulässt, dass der Typ "Wiederbeschaffung" stattdessen ausgewählt wird.  
2. Klicken Sie auf "Richtlinienregel erstellen".
3. Wählen Sie "Ja" im Feld "Manuelle Außerkraftsetzung zulassen" aus.
4. Klicken Sie auf "Schließen".
    * Jetzt können Sie andere Richtlinienregeln für die Einkaufsrichtlinie haben.   Beachten Sie, dass ein Richtlinienregeltyp keine sich überschneidenden Regeln haben kann, die gleichzeitig innerhalb einer einzelnen Beschaffungsrichtlinie aktiv sind.  
5. Schließen Sie die Seite.
6. Schließen Sie die Seite.


