---
title: Finanzdimensionen
description: In diesem Artikel werden die unterschiedlichen Arten von Finanzdimensionen und deren Einrichtung beschrieben.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>Finanzdimensionen

In diesem Artikel werden die unterschiedlichen Arten von Finanzdimensionen und deren Einrichtung beschrieben.

Mithilfe der Seite "Finanzdimensionen" können Sie Finanzdimensionen erstellen, die als Kontosegmente für Kontenpläne verwendet werden können. Es gibt zwei Typen von Finanzdimensionen, benutzerdefinierte Dimensionen und entitätsunterstützte Dimensionen. Benutzerdefinierte Dimensionen werden von mehreren juristischen Personen gemeinsam genutzt und die Werte werden vom Benutzer eingegeben und verwaltet. Entitätsunterstützte Dimensionen sind Dimensionen, deren Werte in anderen Teilen des Systems, wie "Debitoren" oder "Filialen" definiert werden. Einige entitätsunterstützte Dimensionen werden von mehreren juristischen Personen gemeinsam genutzt und manche entitätsunterstützte Dimensionen sind unternehmensspezifisch. 

Nachdem Sie die Finanzdimensionen erstellt haben, weisen Sie jeder Finanzdimension auf der Seite "Finanzdimensionswerte" weitere Eigenschaften zu. 

Zwar können Finanzdimensionen verwendet werden können, die juristische Personen finden stehen, ohne die juristischen Personen in Microsoft Dynamics 365 für Arbeitsgänge erstellen, werden keine Finanzdimensionen der Adresse die betrieblichen oder die Anforderungen von juristischen Personen vorgesehen. Die Einheitenbezogene Buchhaltungs-Funktionen in Microsoft Dynamics 365 für Arbeitsgänge sind zur Adresse nur die Buchhaltungseinträge konzipiert, die durch keine Buchung erstellt werden. 

Bevor Sie Finanzdimensionen als juristische Personen einrichten, prüfen Sie Ihre Geschäftsprozesse in den folgenden Bereichen, um zu bestimmen, ob diese Einstellung für Ihre Organisation sinnvoll ist:

-   Bestand
-   Verkäufe und Einkäufe zwischen Finanzdimensionen und juristischen Personen
-   Mehrwertsteuerberechnung und -erklärung
-   Betriebliche Berichterstellung

Einige Beispiele für Einschränkungen sind:

-   Sie können die Mehrwertsteuerfunktion nur mit juristischen Personen, nicht mit Finanzdimensionen, verwenden.
-   Einige Berichte enthalten keine Finanzdimensionen, sodass Sie nicht immer nach Finanzdimension berichten können, sofern diese berichte nicht modifiziert werden.

**Custom dimensions** 

Um eine benutzerdefinierte Finanzdimension, in den Verwendungswerten im Feld erstellen, wählen benutzerdefinierte &lt; Dimension aus &gt;. Sie können auch eine Kontenmaske angeben. Sie beschränkt die Menge und die Art von Informationen, die für Dimensionswerte eingegeben werden können. Sie können Zeichen eingeben, die dieselben bleiben für jeden Dimensionswert, wie Buchstaben oder einen Bindestrich. Sie können \#Nummernzeichen () und kaufmännischen Und-Zeichen (&.) als Platzhalter für Zahlen und Buchstaben auch eingeben, die jedes Mal geändert, dass ein Dimensionswert erstellt wird. Verwenden Sie ein Nummernzeichen (\#) als Platzhalter für eine Anzahl und ein kaufmännisches Und-Zeichen (&.) als Platzhalter für ein Ablehnungsschreiben gedruckt. 

**Beispiel** 

Um den Dimensionswert für den Brief CC und zu drei einzuschränken, geben Sie Zahlen cm \#\#\# als Formatmaske ein. Dieses Feld ist nur verfügbar, wenn Sie benutzerdefinierte Dimension &gt; in den Verwendungswerten im Feld auswählen. 

** Entität unterstützte ** Dimensionen 

Um eine Entität erstellen unterstützte Finanzdimension, in den Verwendungswerten im Feld, wählen Sie eine vom System definierte Entität auf der die Finanzdimension basieren soll. Basierend auf dieser Auswahl sind Finanzdimensionswerte erstellt. Um beispielsweise Dimensionswerte für Projekte zu erstellen. Für jeden Projektnamen wird ein Dimensionswert erstellt. Die Dimensionswerteseite zeigt die Werte für die Entität an und wenn sie unternehmensspezifisch sind, zeigt sie das Unternehmen für den Wert an. 

** ** Die Aktivierung der Dimensionen 

"Aktivieren der Finanzdimension" aktualisiert die Tabelle mit dem Finanzdimensionsnamen und entfernt gelöschte Dimensionen. Sie können Dimensionswerte eingegeben, bevor Sie eine Finanzdimension aktivieren, aber eine Finanzdimension kann nirgends verwendet werden, bis sie aktiviert ist. Sie können beispielsweise nicht eine Finanzdimension einer Kontostruktur hinzufügen, bis die Finanzdimension aktiviert wurde. Das Klicken auf "Aktivieren" aktualisiert alle Dimensionen mit Statusänderungen. 

**Translations** 

Die Textübersetzungsseite ermöglicht es Ihnen, die in verschiedenen Sprachen für die ausgewählte Finanzdimension angezeigt wird Text eingeben. Auf der Seite "Hauptkontoübersetzung" können Sie Text eingeben, der für das Hauptkonto in verschiedenen Sprachen angezeigt werden soll. 

**Legal entity overrides** 

Nicht alle Dimensionen sind für alle juristischen Personen gültig und andere werden möglicherweise nur für eine bestimmte Zeitperiode relevant. In diesem kann der Abschnitt "Überschreibungen der juristischen Person" dazu verwendet werden, um festzulegen, für welche Unternehmen die Dimension ausgesetzt werden soll, wer der Besitzer ist und die Zeitperiode, während der die Dimension aktiv ist.




