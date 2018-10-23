---
title: Finanzdimensionen
description: "In diesem Thema werden die verschiedenen Arten von wertmäßigen Dimensionen beschrieben und wie sie eingerichtet wurden."
author: aprilolson
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: d6b7b1219974cb5de1a625d87c3bce2a4439470b
ms.openlocfilehash: 9973d03de031ad2fa5647bb167c12b9231633a22
ms.contentlocale: de-de
ms.lasthandoff: 10/01/2018

---

# <a name="financial-dimensions"></a>Finanzdimensionen

[!include [banner](../includes/banner.md)]

In diesem Thema werden die verschiedenen Arten von wertmäßigen Dimensionen erklärt und wie sie eingerichtet wurden.

Mithilfe der Seite **Finanzdimensionen** können Sie Finanzdimensionen erstellen, die als Kontosegmente für Kontenpläne verwendet werden können. Es gibt zwei Typen von Finanzdimensionen: benutzerdefinierte Dimensionen und entitätsunterstützte Dimensionen. Benutzerdefinierte Dimensionen werden von mehreren juristischen Personen gemeinsam genutzt und die Werte werden von Benutzern eingegeben und verwaltet. Bei entitätsunterstützten Dimensionen sind die Werte an anderen Stelle im System, wie in "Debitoren"- oder "Filialen"-Entitäten definiert. Einige entitätsunterstützte Dimensionen werden von mehreren juristischen Personen gemeinsam genutzt, wobei andere entitätsunterstützten Dimensionen unternehmensspezifisch sind.

Nachdem Sie die Finanzdimensionen erstellt haben, weisen Sie jeder Finanzdimension auf der Seite **Finanzdimensionswerte** weitere Eigenschaften zu.

Sie können Finanzdimensionen verwenden, um juristische Personen darzustellen. Sie müssen in Microsoft Dynamics 365 for Finance and Operations keine juristischen Personen erstellen. Allerdings wurden Finanzdimensionen nicht für  die betrieblichen oder geschäftlichen Anforderungen von juristischen Personen entworfen. Die Interunit-Buchhaltungsfunktionen in Finance and Operations sind nur für die Buchhaltungseinträge vorgesehen, die durch die einzelnen Buchungen erstellt werden.

Bevor Sie Finanzdimensionen als juristische Personen einrichten, prüfen Sie Ihre Geschäftsprozesse in den folgenden Bereichen, um zu bestimmen, ob diese Einstellung für Ihre Organisation sinnvoll ist:

- Lager
- Verkäufe und Einkäufe zwischen Finanzdimensionen und juristischen Personen
- Mehrwertsteuerberechnung und -erklärung
- Betriebliche Berichterstellung

Im Folgenden finden Sie einige der Beschränkungen:

- Sie können die Mehrwertsteuerfunktion nur mit juristischen Personen, nicht mit Finanzdimensionen, verwenden.
- Einige Berichte enthalten keine Finanzdimensionen. Daher müssen Sie die Berichte für Meldung nach Finanzdimension ggf. ändern.

## <a name="custom-dimensions"></a>Benutzerdefinierte Dimensionen

Um eine benutzerdefinierte Finanzdimension zu erstellen, wählen Sie im Feld **Werte nutzen ab** **&lt;&nbsp;Benutzerdefinierte Dimension&nbsp;&gt;**.

Sie können auch eine Kontenmaske angeben. Sie beschränkt die Menge und die Art von Informationen, die für Dimensionswerte eingegeben werden können. Sie können Zeichen eingeben, die dieselben bleiben für jeden Dimensionswert, wie Buchstaben oder einen Bindestrich (-). Sie können auch Nummernzeichen (\#) und kaufmännische Und-Zeichen (&) als Platzhalter für Buchstaben und Zahlen eingeben, die sich jedes Mal ändern, wenn ein Dimensionswert erstellt wird. Verwenden Sie ein Nummernzeichen (\#) als Platzhalter für eine Zahl und ein kaufmännisches Und-Zeichen (&) als Platzhalter für einen Buchstaben. Das Feld für die Formatmaske ist nur verfügbar, wenn Sie **&lt;&nbsp;Benutzerdefinierte Dimension&nbsp;&gt;** im Feld **Werte nutzen ab**.

**Beispiel**

Um den Dimensionswert auf die Buchstaben "CC" und drei Zahlen einzuschränken, geben Sie **CC-\#\#\#** als Formatmaske ein.

## <a name="entity-backed-dimensions"></a>Entitätsunterstützte Dimensionen

Um eine entitätsunterstützte Finanzdimension zu erstellen, wählen Sie im Feld **Werte verwenden** eine vom System definierte Entität aus, auf der die Finanzdimension basieren soll. Basierend auf dieser Entität werden dann Finanzdimensionswerte erstellt. Um beispielsweise Dimensionswerte für Projekte zu erstellen, wählen Sie **Projekte** aus. Für jeden Projektnamen wird dann ein Dimensionswert erstellt. Die Seite **Finanzdimensionswerte** zeigt die Werte für die Entität. Wenn diese Werte unternehmensspezifisch sind, zeigt die Seite auch das Unternehmen an.

## <a name="activating-dimensions"></a>Dimensionen aktivieren

Wenn Sie eine Finanzdimension aktivieren, wird die Tabelle aktualisiert, sodass sie den Namen der Finanzdimension enthält. Gelöschte Dimensionen werden entfernt. Sie können Dimensionswerte eingeben, bevor Sie eine Finanzdimension aktivieren. Allerdings kann eine Finanzdimension nirgendwo genutzt werden, bis sie aktiviert wurde. Sie können beispielsweise nicht eine Finanzdimension einer Kontostruktur hinzufügen, bis die Finanzdimension aktiviert wurde. Wenn Sie **Aktivieren** wählen, werden alle Dimensionen aktualisiert und zeigen Statusänderungen.

## <a name="translations"></a>Texte

Auf der Seite **Textübersetzung** können Sie den Text für die ausgewählte Finanzdimension in verschiedenen Sprachen eingeben. Auf der Seite **Hauptkontoübersetzung** können Sie den Text für das Hauptkonto in verschiedenen Sprachen eingeben. 

## <a name="legal-entity-overrides"></a>Juristische Person überschreibt

Nicht alle Dimensionen sind für alle juristischen Personen gültig. Darüber hinaus sind möglicherweise mehrere Dimensionen nur während eines bestimmten Zeitraums relevant. In diesen Fällen können Sie den Abschnitt **Überschreibungen der juristischen Person** verwenden, um die Unternehmen, für die die Dimension ausgesetzt werden soll, den Besitzer und den Zeitraum, zu dem die Dimension aktiv ist, anzugeben.

## <a name="deleting-financial-dimensions"></a>Löschen von Finanzdimensionen

Zur Unterstützung bei der Wahrung der referenziellen Integrität der Daten können Finanzdimensionen nur in seltenen Fällen gelöscht werden. Wenn Sie versuchen, eine Finanzdimension zu löschen, werden folgende Kriterien überprüft:

- Wird die Finanzdimension auf gebuchten oder nicht gebuchten Buchungen oder einer Art von Dimensionswertkombinationen verwendet?
- Wird die Finanzdimension in einer aktiven Kontostruktur, erweiterten Regelstruktur oder in einem Finanzdimensionssatz verwendet?
- Wird die Finanzdimensionsteil von einem Standardfinanzdimensions-Integrationsformat verwendet?
- Wurde die Finanzdimension als Standarddimension eingerichtet?

Wenn irgendwelche dieser Kriterien erfüllt sind, kann die Finanzdimension nicht gelöscht erfüllt.

## <a name="default-dimension-values"></a>Standarddimensionswerte

Sie können Werte in den Hauptdatensätzen, wie Debitoren und Kreditoren, als Standardwerte in den neuen Dimensionen verwenden. Wenn die neuen Dimensionen erstellt werden, wird die Hauptdatensatz-Kennung in die Dimensionswerte für diese Hauptdatensätze eingegeben. Wenn Sie beispielsweise einen neuen Debitor erstellen, wird die Debitorkennung in die Debitorendimension eingegeben. Wenn Sie Aufträge, Rechnungen oder andere Dokumente erstellen, die eine Debitorenkennung erfordern, werden die vorhandenen Standardregeln verwendet und die Debitorkennung wird dem Dokument hinzugefügt.

Diese Funktion wird durch die Einstellungen in der Dimension gesteuert. Diese Einstellung hat den Namen **Kopieren Sie Werte dieser Dimension bei jedem neu erstellten DimensionName**, wobei **DimensionName** der Name der Dimension ist. Standardmäßig ist die Funktion ausgeschaltet. Allerdings kann sie jederzeit aktiviert werden.

Wenn bereits Datensätze für die Dimension vorhanden sind, werden die Hauptdatensätze aktualisiert, , wenn Sie die Funktion aktivieren. Allerdings werden vorhandene Dokumente und Buchungen nicht aktualisiert.

## <a name="derived-dimensions"></a>Abgeleitete Dimensionen

Sie können eine Dimension konfigurieren, sodass Informationen für andere Dimensionen automatisch eingegeben werden, wenn Sie diese Dimension in einem Dokument eingeben. Wenn Sie z. B. Kostenstelle 10 eingeben, kann ein Wert **20** in die Abteilungsdimension automatisch eingegeben werden.

Sie können abgeleitete Dimensionswerte auf der Dimensionsseite einrichten.

1. Wählen Sie eine Dimension aus und wählen Sie dann **Abgeleitete Dimensionen** aus.

    Die Seite **Abgeleitete Dimensionen** enthält ein Raster. Das ausgewählte Dimensionssegment ist die erste Spalte in diesem Raster.

2. Fügen Sie die Segmente hinzu, die berechnet werden sollen. Jedes Segment wird als Spalte angezeigt.

Geben Sie die Dimension an, die von der Dimension in der ersten Spalte berechnet werden sollen. Um beispielsweise die Kostenstelle als die Dimension zu verwenden, von der die Abteilung und die elektronische Adresse abgeleitete werden, geben Sie Kostenstelle 10, Abteilung 20 und elektronische Adresse 30 ein. Wenn Sie Kostenstelle 10 in einem Rahmen-Datensatz oder in einer Transaktionsseite erfassen, werden Abteilung 20 und elektronische Adresse 30  standardmäßig eingegeben.

Der abgeleitete Dimensionsprozess ersetzt nicht vorhandene Werte für abgeleitete Dimensionen. Wenn Sie z.B. Kostenstelle 10 eingeben, und keine andere Dimension eingegeben wird, werden Abteilung 20 und elektronische Adresse 30 standardmäßig eingegeben. Wenn Sie aber die Kostenstelle ändern, werden die eingegebenen Werte, die bereits eingerichtet wurden, nicht geändert. Daher können Sie Standarddimensionen auf Hauptdatensätzen einrichten, und diese Dimensionen werden nicht über abgeleitete Dimensionen geändert.

### <a name="derived-dimensions-and-entities"></a>Abgeleitete Dimensionen und Entitäten

Sie können Dimensionssegmente und die abgeleiteten Werte einrichten, indem Sie Entitäten verwenden.

- Die abgeleitete Dimensionsentität richtet die treibenden Dimensionen und die Segmente ein, die für diese Dimensionen verwendet werden.
- Mit der DerivedDimensionValue-Entität können Sie die Werte importieren, die für jede treibende Dimension berechnet werden sollen.

Wenn Sie eine Entität verwenden, um Daten zu importieren, wenn diese Dimensionen Entität importiert wird, werden die abgeleiteten Dimensionsregeln beim Import verwendet, es sei denn, die Entität überschreibt diese Dimensionen explizit.

Weitere Informationen finden Sie in folgenden Themen:

- [Finanzdimensionen definieren](tasks/define-financial-dimensions.md)
- [Standardvorlagen für Finanzdimension verwalten](tasks/maintain-financial-dimension-default-templates.md)

