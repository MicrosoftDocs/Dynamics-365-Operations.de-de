---
title: Finanzdimensionen
description: In diesem Artikel werden die unterschiedlichen Arten von Finanzdimensionen und deren Einrichtung beschrieben.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 01f189b8de3f0cc707dcc54f4cde75aed95b8e3f
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="financial-dimensions"></a>Finanzdimensionen

[!include[banner](../includes/banner.md)]


In diesem Artikel werden die unterschiedlichen Arten von Finanzdimensionen und deren Einrichtung beschrieben.

Mithilfe der Seite "Finanzdimensionen" können Sie Finanzdimensionen erstellen, die als Kontosegmente für Kontenpläne verwendet werden können. Es gibt zwei Typen von Finanzdimensionen, benutzerdefinierte Dimensionen und entitätsunterstützte Dimensionen. Benutzerdefinierte Dimensionen werden von mehreren juristischen Personen gemeinsam genutzt und die Werte werden vom Benutzer eingegeben und verwaltet. Entitätsunterstützte Dimensionen sind Dimensionen, deren Werte in anderen Teilen des Systems, wie "Debitoren" oder "Filialen" definiert werden. Einige entitätsunterstützte Dimensionen werden von mehreren juristischen Personen gemeinsam genutzt und manche entitätsunterstützte Dimensionen sind unternehmensspezifisch. 

Nachdem Sie die Finanzdimensionen erstellt haben, weisen Sie jeder Finanzdimension auf der Seite "Finanzdimensionswerte" weitere Eigenschaften zu. 

Obwohl Sie Finanzdimensionen verwenden können, um die juristische Personen darzustellen, ohne die juristischen Personen in Microsoft Dynamics 365 for Operations zu erstellen, sind Finanzdimensionen nicht dafür angelegt, auf die betrieblichen oder geschäftlichen Anforderungen von juristischen Personen einzugehen. Die Interunit-Buchhaltungsfunktionen in Microsoft Dynamics 365 for Operations sind nur für die Buchhaltungseinträge vorgesehen, die durch die einzelnen Buchung erstellt werden. 

Bevor Sie Finanzdimensionen als juristische Personen einrichten, prüfen Sie Ihre Geschäftsprozesse in den folgenden Bereichen, um zu bestimmen, ob diese Einstellung für Ihre Organisation sinnvoll ist:

-   Bestand
-   Verkäufe und Einkäufe zwischen Finanzdimensionen und juristischen Personen
-   Mehrwertsteuerberechnung und -erklärung
-   Betriebliche Berichterstellung

Einige Beispiele für Einschränkungen sind:

-   Sie können die Mehrwertsteuerfunktion nur mit juristischen Personen, nicht mit Finanzdimensionen, verwenden.
-   Einige Berichte enthalten keine Finanzdimensionen, sodass Sie nicht immer nach Finanzdimension berichten können, sofern diese berichte nicht modifiziert werden.

**Benutzerdefinierte Dimensionen** 

Um eine benutzerdefinierte Finanzdimension zu erstellen, wählen Sie im Feld "Werte verwenden" die Option &lt;Benutzerdefinierte Dimension &gt; aus. Sie können auch eine Kontenmaske angeben. Sie beschränkt die Menge und die Art von Informationen, die für Dimensionswerte eingegeben werden können. Sie können Zeichen eingeben, die dieselben bleiben für jeden Dimensionswert, wie Buchstaben oder einen Bindestrich. Sie können auch Nummernzeichen (\#) und kaufmännische Und-Zeichen (&) als Platzhalter für Buchstaben und Zahlen eingeben, die sich jedes Mal ändern werden, wenn ein Dimensionswert erstellt wird. Verwenden Sie ein Nummernzeichen (\#) als Platzhalter für eine Zahl und ein kaufmännisches Und-Zeichen (&) als Platzhalter für einen Buchstaben. 

**Beispiel** 

Um den Dimensionswert auf die Buchstaben CC und drei Zahlen einzuschränken, geben Sie CC-\#\#\# als Formatmaske ein. Dieses Feld ist nur verfügbar, wenn Sie &lt;Benutzerdefinierte Dimension &gt; in den Verwendungswerten im Feld auswählen. 

**Entität unterstützte Dimensionen** 

Um eine entitätsunterstützte Finanzdimension zu erstellen, wählen Sie im Feld "Werte verwenden" eine vom System definierte Entität aus, auf der die Finanzdimension basieren soll. Basierend auf dieser Auswahl sind Finanzdimensionswerte erstellt. Um beispielsweise Dimensionswerte für Projekte zu erstellen. Für jeden Projektnamen wird ein Dimensionswert erstellt. Die Dimensionswerteseite zeigt die Werte für die Entität an und wenn sie unternehmensspezifisch sind, zeigt sie das Unternehmen für den Wert an. 

**Dimensionen aktivieren** 

"Aktivieren der Finanzdimension" aktualisiert die Tabelle mit dem Finanzdimensionsnamen und entfernt gelöschte Dimensionen. Sie können Dimensionswerte eingegeben, bevor Sie eine Finanzdimension aktivieren, aber eine Finanzdimension kann nirgends verwendet werden, bis sie aktiviert ist. Sie können beispielsweise nicht eine Finanzdimension einer Kontostruktur hinzufügen, bis die Finanzdimension aktiviert wurde. Das Klicken auf "Aktivieren" aktualisiert alle Dimensionen mit Statusänderungen. 

**Übersetzungen** 

Auf der Seite "Textübersetzung" können Sie Text eingeben, der in verschiedenen Sprachen für die ausgewählte Finanzdimension angezeigt werden soll. Auf der Seite "Hauptkontoübersetzung" können Sie Text eingeben, der für das Hauptkonto in verschiedenen Sprachen angezeigt werden soll. 

**Juristische Person überschreiben** 

Nicht alle Dimensionen sind für alle juristischen Personen gültig und manche sind möglicherweise nur für eine bestimmte Zeitperiode relevant. In diesem kann der Abschnitt "Überschreibungen der juristischen Person" dazu verwendet werden, um festzulegen, für welche Unternehmen die Dimension ausgesetzt werden soll, wer der Besitzer ist und die Zeitperiode, während der die Dimension aktiv ist.






