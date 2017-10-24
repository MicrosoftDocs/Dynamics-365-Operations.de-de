---
title: Finanzdimensionen
description: "In diesem Thema werden die verschiedenen Arten von wertmäßigen Dimensionen beschrieben und wie sie eingerichtet wurden."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3950dc3fcd1e293802c88bf2616a27e139b48399
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="financial-dimensions"></a>Finanzdimensionen

[!include[banner](../includes/banner.md)]

In diesem Thema werden die verschiedenen Arten von wertmäßigen Dimensionen erklärt und wie sie eingerichtet wurden.

Mithilfe der Seite **Finanzdimensionen** können Sie Finanzdimensionen erstellen, die als Kontosegmente für Kontenpläne verwendet werden können. Es gibt zwei Typen von Finanzdimensionen: benutzerdefinierte Dimensionen und entitätsunterstützte Dimensionen. Benutzerdefinierte Dimensionen werden von mehreren juristischen Personen gemeinsam genutzt und die Werte werden von Benutzern eingegeben und verwaltet. Bei entitätsunterstützten Dimensionen sind die Werte an anderen Stelle im System, wie "Debitoren"- oder "Filialen"-Entitäten definiert. Einige entitätsunterstützte Dimensionen werden von mehreren juristischen Personen gemeinsam genutzt, wobei andere entitätsunterstützten Dimensionen unternehmensspezifisch sind. 

Nachdem Sie die Finanzdimensionen erstellt haben, weisen Sie jeder Finanzdimension auf der Seite **Finanzdimensionswerte** weitere Eigenschaften zu. 

Sie können Finanzdimensionen verwenden, um juristische Personen darzustellen. Sie müssen in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, keine juristischen Personen erstellen. Allerdings wurden Finanzdimensionen nicht für betriebliche oder geschäftliche Anforderungen von juristischen Personen entworfen. Die Interunit-Buchhaltungsfunktionen in Finance and Operations sind nur für die Buchhaltungseinträge vorgesehen, die durch die einzelnen Buchungen erstellt werden. 

Bevor Sie Finanzdimensionen als juristische Personen einrichten, prüfen Sie Ihre Geschäftsprozesse in den folgenden Bereichen, um zu bestimmen, ob diese Einstellung für Ihre Organisation sinnvoll ist:

- Lager
- Verkäufe und Einkäufe zwischen Finanzdimensionen und juristischen Personen
- Mehrwertsteuerberechnung und -erklärung
- Betriebliche Berichterstellung

Im Folgenden finden Sie einige der Beschränkungen:

- Sie können die Mehrwertsteuerfunktion nur mit juristischen Personen, nicht mit Finanzdimensionen, verwenden.
- Einige Berichte enthalten keine Finanzdimensionen. Daher müssen Sie die Berichte für Meldung nach Finanzdimension ggf. ändern.

## <a name="custom-dimensions"></a>Benutzerdefinierte Dimensionen

Um eine benutzerdefinierte Finanzdimension zu erstellen, wählen Sie im Feld **Werte verwenden** die Option **&lt;Benutzerdefinierte Dimension&gt;** aus. Sie können auch eine Kontenmaske angeben. Sie beschränkt die Menge und die Art von Informationen, die für Dimensionswerte eingegeben werden können. Sie können Zeichen eingeben, die dieselben bleiben für jeden Dimensionswert, wie Buchstaben oder einen Bindestrich (-). Sie können auch Nummernzeichen (\#) und kaufmännische Und-Zeichen (&) als Platzhalter für Buchstaben und Zahlen eingeben, die sich jedes Mal ändern werden, wenn ein Dimensionswert erstellt wird. Verwenden Sie ein Nummernzeichen (\#) als Platzhalter für eine Zahl und ein kaufmännisches Und-Zeichen (&) als Platzhalter für einen Buchstaben. Das Feld für die Formatmaske ist nur verfügbar, wenn Sie **&lt;Benutzerdefinierte Dimension&gt;** im Feld **Verwendungswerte** auswählen.

**Beispiel**

Um den Dimensionswert auf die Buchstaben "CC" und drei Zahlen einzuschränken, geben Sie **CC-\#\#\#** als Formatmaske ein.

## <a name="entity-backed-dimensions"></a>Entitätsunterstützte Dimensionen

Um eine entitätsunterstützte Finanzdimension zu erstellen, wählen Sie im Feld **Werte verwenden** eine vom System definierte Entität aus, auf der die Finanzdimension basieren soll. Basierend auf dieser Entität werden dann Finanzdimensionswerte erstellt. Um beispielsweise Dimensionswerte für Projekte zu erstellen, wählen Sie **Projekte** aus. Für jeden Projektnamen wird dann ein Dimensionswert erstellt. Die Seite **Finanzdimensionswerte** zeigt die Werte für die Entität. Wenn diese Werte unternehmensspezifisch sind, zeigt die Seite auch das Unternehmen an.

## <a name="activating-dimensions"></a>Dimensionen aktivieren

Wenn Sie eine Finanzdimension aktivieren, wird die Tabelle aktualisiert, sodass sie den Namen der Finanzdimension enthält. Gelöschte Dimensionen werden entfernt. Sie können Dimensionswerte eingeben, bevor Sie eine Finanzdimension aktivieren. Allerdings kann eine Finanzdimension nirgendwo genutzt werden, bis sie aktiviert wurde. Sie können beispielsweise nicht eine Finanzdimension einer Kontostruktur hinzufügen, bis die Finanzdimension aktiviert wurde. Wenn Sie auf **Aktivieren** klicken, werden alle Dimensionen aktualisiert und zeigen Statusänderungen. 

## <a name="translations"></a>Texte

Auf der Seite **Textübersetzung** können Sie den Text für die ausgewählte Finanzdimension in verschiedenen Sprachen eingeben. Auf der Seite **Hauptkontoübersetzung** können Sie den Text für das Hauptkonto in verschiedenen Sprachen eingeben. 

## <a name="legal-entity-overrides"></a>Juristische Person überschreibt

Nicht alle Dimensionen sind für alle juristischen Personen gültig. Darüber hinaus sind möglicherweise mehrere Dimensionen nur während eines bestimmten Zeitraums relevant. In diesen Fällen können Sie den Abschnitt **Überschreibungen der juristischen Person** verwenden, um die Unternehmen, für die die Dimension ausgesetzt werden soll, den Besitzer und den Zeitraum, zu dem die Dimension aktiv ist, anzugeben.

## <a name="deleting-financial-dimensions"></a>Löschen von Finanzdimensionen

Zur Unterstützung bei der Wahrung der referenziellen Integrität der Daten können Finanzdimensionen nur in seltenen Fällen gelöscht werden. Wenn Sie versuchen, eine Finanzdimension zu löschen, werden folgende Kriterien überprüft:

- Wird die Finanzdimension auf gebuchten oder nicht gebuchten Buchungen oder einer Art von Dimensionswertkombination verwendet?
- Wird die Finanzdimension in einer aktiven Kontostruktur, erweiterten Regelstruktur oder in einem Finanzdimensionssatz verwendet?
- Wird die Finanzdimensionsteil von einem Standardfinanzdimensions-Integrationsformat verwendet?
- Wurde die Finanzdimension als Standarddimension eingerichtet?

Wenn irgendwelche dieser Kriterien erfüllt sind, kann die Finanzdimension nicht gelöscht erfüllt.


Weitere Informationen finden Sie in folgenden Themen:
- [Finanzdimensionen definieren](tasks/define-financial-dimensions.md)
- [Standardvorlagen für Finanzdimension verwalten](tasks/maintain-financial-dimension-default-templates.md)

