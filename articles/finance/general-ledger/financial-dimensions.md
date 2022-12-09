---
title: Finanzdimensionen
description: In diesem Artikel werden die verschiedenen Arten von Finanzdimensionen beschrieben und es wird erörtert, wie sie eingerichtet werden.
author: aprilolson
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: adfa2c1164550e32b07da25de0d96aa82430b980
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799625"
---
# <a name="financial-dimensions"></a>Finanzdimensionen

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die verschiedenen Arten von Finanzdimensionen erklärt und es wird erörtert, wie sie eingerichtet werden.

Mithilfe der Seite **Finanzdimensionen** können Sie Finanzdimensionen erstellen, die als Kontosegmente für Kontenpläne verwendet werden können. Es gibt zwei Typen von Finanzdimensionen: benutzerdefinierte Dimensionen und entitätsunterstützte Dimensionen. Benutzerdefinierte Dimensionen werden von mehreren juristischen Personen gemeinsam genutzt und die Werte werden von Benutzern eingegeben und verwaltet. Bei entitätsunterstützten Dimensionen sind die Werte an anderen Stelle im System, wie in "Debitoren"- oder "Filialen"-Entitäten definiert. Einige entitätsunterstützte Dimensionen werden von mehreren juristischen Personen gemeinsam genutzt, wobei andere entitätsunterstützten Dimensionen unternehmensspezifisch sind.

Nachdem Sie die Finanzdimensionen erstellt haben, weisen Sie jeder Finanzdimension auf der Seite **Finanzdimensionswerte** weitere Eigenschaften zu.

Sie können Finanzdimensionen verwenden, um juristische Personen darzustellen. Sie müssen in Dynamics 365 Finance keine juristischen Personen erstellen. Allerdings wurden Finanzdimensionen nicht für die betrieblichen oder geschäftlichen Anforderungen von juristischen Personen entworfen. Die Interunit-Buchhaltungsfunktionen in Finance sind nur für die Buchhaltungseinträge vorgesehen, die durch die einzelnen Buchung erstellt werden.

Bevor Sie Finanzdimensionen als juristische Personen einrichten, prüfen Sie Ihre Geschäftsprozesse in den folgenden Bereichen, um zu bestimmen, ob diese Einstellung für Ihre Organisation sinnvoll ist:

- Lager
- Verkäufe und Einkäufe zwischen Finanzdimensionen und juristischen Personen
- Mehrwertsteuerberechnung und -erklärung
- Betriebliche Berichterstellung

Im Folgenden finden Sie einige der Beschränkungen:

- Sie können die Mehrwertsteuerfunktion nur mit juristischen Personen, nicht mit Finanzdimensionen, verwenden.
- Einige Berichte enthalten keine Finanzdimensionen. Daher müssen Sie die Berichte für Meldung nach Finanzdimension ggf. ändern.

## <a name="custom-dimensions"></a>Benutzerdefinierte Dimensionen

Um eine benutzerdefinierte Finanzdimension zu erstellen, wählen Sie im Feld **Werte verwenden ab** die Option **Benutzerdefinierte Dimension** aus.

Sie können auch eine Kontenmaske angeben. Sie beschränkt die Menge und die Art von Informationen, die für Dimensionswerte eingegeben werden können. Sie können Zeichen eingeben, die dieselben bleiben für jeden Dimensionswert, wie Buchstaben oder einen Bindestrich (-). Sie können auch Nummernzeichen (\#) und kaufmännische Und-Zeichen (&) als Platzhalter für Buchstaben und Zahlen eingeben, die sich jedes Mal ändern, wenn ein Dimensionswert erstellt wird. Verwenden Sie ein Nummernzeichen (\#) als Platzhalter für eine Zahl und ein kaufmännisches Und-Zeichen (&) als Platzhalter für einen Buchstaben. Das Feld für die Formatmaske ist nur verfügbar, wenn Sie **Benutzerdefinierte Dimension** im Feld **Werte nutzen** auswählen.

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
- Wurde die Finanzdimension in den Financial Reporting-Einstellungen nicht ausgewählt? 

Wenn irgendwelche dieser Kriterien erfüllt sind, kann die Finanzdimension nicht gelöscht erfüllt.

> [!NOTE]
> Ab Finance-Version 10.0.27 werden Finanzdimensionen nicht mehr automatisch für die Finanzberichterstellungseinrichtung ausgewählt, wenn sie erstellt werden.

## <a name="default-dimension-values"></a>Standarddimensionswerte

Sie können Werte in den Hauptdatensätzen, wie Debitoren und Kreditoren, als Standardwerte in den neuen Dimensionen verwenden. Wenn die neuen Dimensionen erstellt werden, wird die Hauptdatensatz-Kennung in die Dimensionswerte für diese Hauptdatensätze eingegeben. Wenn Sie beispielsweise einen neuen Debitor erstellen, wird die Debitorkennung in die Debitorendimension eingegeben. Wenn Sie Aufträge, Rechnungen oder andere Dokumente erstellen, die eine Debitorenkennung erfordern, werden die vorhandenen Standardregeln verwendet und die Debitorkennung wird dem Dokument hinzugefügt.

Diese Funktion wird durch die Einstellungen in der Dimension gesteuert. Diese Einstellung hat den Namen **Kopieren Sie Werte dieser Dimension bei jedem neu erstellten DimensionName**, wobei **DimensionName** der Name der Dimension ist. Standardmäßig ist die Funktion ausgeschaltet. Allerdings kann sie jederzeit aktiviert werden.

Wenn bereits Datensätze für die Dimension vorhanden sind, werden die Hauptdatensätze aktualisiert, , wenn Sie die Funktion aktivieren. Allerdings werden vorhandene Dokumente und Buchungen nicht aktualisiert.

Wenn Sie eine Vorlage verwenden, um einen Hauptdatensatz zu erstellen, stellen Sie sicher, dass der Vorlagenwert für das Vorlagenpassungsmaß leer ist. Wenn Sie beispielsweise Debitoren aus einer Vorlage erstellen, stellen Sie sicher, dass die in der Vorlage Debitorendimension leer ist. Der Debitorendimensionswert wird als Standard die neuen Debitornummer, wenn Sie den neuen Debitor erstellen.  

## <a name="derived-dimensions"></a>Abgeleitete Dimensionen

Sie können eine Dimension konfigurieren, sodass Informationen für andere Dimensionen automatisch eingegeben werden, wenn Sie diese Dimension in einem Dokument eingeben. Wenn Sie z. B. Kostenstelle 10 eingeben, kann ein Wert **20** in die Abteilungsdimension automatisch eingegeben werden.

Sie können abgeleitete Dimensionswerte auf der Dimensionsseite einrichten.

1. Wählen Sie eine Dimension aus und wählen Sie dann **Abgeleitete Dimensionen** aus.

    Die Seite **Abgeleitete Dimensionen** enthält ein Raster. Das ausgewählte Dimensionssegment ist die erste Spalte in diesem Raster.

2. Fügen Sie die Segmente hinzu, die berechnet werden sollen. Jedes Segment wird als Spalte angezeigt.

Geben Sie die Dimension an, die von der Dimension in der ersten Spalte berechnet werden sollen. Um beispielsweise die Kostenstelle als die Dimension zu verwenden, von der die Abteilung und die elektronische Adresse abgeleitete werden, geben Sie Kostenstelle 10, Abteilung 20 und elektronische Adresse 30 ein. Wenn Sie Kostenstelle 10 in einem Rahmen-Datensatz oder in einer Transaktionsseite erfassen, werden Abteilung 20 und elektronische Adresse 30 standardmäßig eingegeben.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Vorhandene Dimensionswerte mit abgeleiteten Werten ersetzen
 
Der abgeleitete Dimensionsprozess ersetzt nicht vorhandene Werte für abgeleitete Dimensionen. Wenn Sie z.B. Kostenstelle 10 eingeben, und keine andere Dimension eingegeben wird, werden Abteilung 20 und elektronische Adresse 30 standardmäßig eingegeben. Wenn Sie aber die Kostenstelle ändern, werden die eingegebenen Werte, die bereits eingerichtet wurden, nicht geändert. Daher können Sie Standarddimensionen auf Hauptdatensätzen einrichten, und diese Dimensionen werden nicht über abgeleitete Dimensionen geändert.

Sie können das Verhalten von abgeleiteten Dimensionen ändern, um vorhandene Werte zu überschreiben, indem Sie das Kontrollkästchen **Ersetzen Sie vorhandene Dimensionswerte über abgeleitete Werte** auf der Seite **Abgeleitete Dimensionen** auswählen. Wenn dieses Feld aktiviert ist, können Sie eine Dimension mit abgeleiteten Dimensionswerten eingeben und die abgeleiteten Dimensionswerte überschreiben danm alle Werte, die bereits vorhanden sind. Wenn Sie das vorhergehende Beispiel verwenden, wenn Sie Kostenstelle 10 eingeben, und keine andere Dimension eingegeben wird, werden Abteilung 20 und elektronische Adresse 30 standardmäßig eingegeben. Wenn die Werte bereits Abteilung 50 und elektronische Adresse 60 waren, werden die Werte jetzt zu Abteilung 20 bzw. elektronische Adresse 30 geändert.
 
Abgeleitete Dimensionen mit dieser Einstellung ersetzen nicht automatisch die vorhandenen Dimensionswerte, wenn Dimensionswerte übernommen werden. Dimensionswerte werden nur überschrieben, wenn Sie einen neuen Dimensionswert auf einer Seite eingeben und es abgeleitete vorhandene Werte für diese Dimension auf der Seite gibt.

### <a name="preventing-changes-with-derived-dimensions"></a>Verhindert Änderungen mit abgeleiteten Dimensionen
 
Wenn Sie **Segment hinzufügen** auf **Abgeleitete Dimensionsseite** verwenden, um ein Segment als abgeleitete Dimension hinzuzufügen, wird eine Option im unteren Bereich der Seite **Segment hinzufügen** angegeben, die es Ihnen ermöglicht, Änderungen für diese Dimension zu verhindern, wenn sie auf einer Seite abgeleitet wird. Die Standardeinstellung ist deaktiviert, damit sie nicht verhindert, dass die abgeleiteten Werte geändert werden. Ändert die Einstellungen auf **Ja**, wenn Sie verhindern möchten, dass die Dimension geändert wird, nachdem sie abgeleitet wurde. Wenn beispielsweise der Wert für die Abteilungsdimension von der Kostenstellendimension berechnet wird, kann der Wert für die Abteilung nicht geändert werden, wenn die Einstellung **Sperren Sie Änderungen** auf **Ja** festgelegt ist. 
 
Die Einstellung verhindert nicht Änderungen, wenn der Dimensionswert gültig ist, aber nicht in der abgeleiteten Dimensionsliste aufgeführt ist. Wenn beispielsweise Abteilung 20 von Kostenstelle 10 berechnet wird und Sie die Kostenstelle 10 eingeben, können Sie Abteilung 20 nicht bearbeiten. Wenn Sie jedoch Kostenstelle 20 eingeben und diese nicht in der Liste mit abgeleiteten Dimensionen für Kostenstelle ist, dann können Sie den Wert für die Abteilung bearbeitet. 
 
In allen Fällen werden der Kontowert und alle Dimensionswerte mit den Kontostrukturen geprüft, nachdem die abgeleiteten Dimensionswerte angewendet wurden. Wenn Sie abgeleitete Dimensionen verwenden und die Prüfung fehlschlägt, wenn sie auf einer Seite verwendet werden, müssen Sie die abgeleitete Dimensionswerte auf der abgeleiteten Dimensionsseite ändern, bevor Sie sie in Transaktionen verwenden können. 
 
Wenn Sie Dimensionen auf dem Inforegister **Finanzverhältnisdimensionen** ändern, ist die Dimension, die markiert wird, um Änderungen zu verhindern, nicht bearbeitbar. Wenn Sie ein Konto und Dimensionen in das segmentierte Eintragssteuerelement auf einer Seite eingeben, sind die Dimensionen bearbeitbar. Wenn Sie jedoch das Hervorgehoben vom segmentierten Eintragssteuerelement verschieben in ein anderes Feld, werden das Konto und die Dimensionen mit der abgeleitete Dimensionsliste verglichen und die Kontostrukturen geprüft, um sicherzustellen, dass Sie die entsprechenden Werten eingegeben haben. 

### <a name="derived-dimensions-and-entities"></a>Abgeleitete Dimensionen und Entitäten

Sie können Dimensionssegmente und die abgeleiteten Werte einrichten, indem Sie Entitäten verwenden.

- Die abgeleitete Dimensionsentität richtet die treibenden Dimensionen und die Segmente ein, die für diese Dimensionen verwendet werden.
- Die abgeleiteten Dimensionswertentität ermöglicht es Ihnen, die Werte zu importieren, die für jede treibende Dimension berechnet werden sollen.

Wenn Sie eine Entität verwenden, um Daten zu importieren, wenn diese Dimensionen Entität importiert wird, werden die abgeleiteten Dimensionsregeln beim Import verwendet, es sei denn, die Entität überschreibt diese Dimensionen explizit.

## <a name="financial-dimension-service"></a>Finanzdimensionsdienst

Das Add-In für den Finanzdimensionsdienst ist in Ihrer Microsoft Dynamics Lifecycle Services-Umgebung verfügbar. Es bietet eine verbesserte Leistung, wenn Sie das Datenverwaltungs-Framework verwenden, um ein Journal mit einer großen Anzahl von Zeilen zu importieren. Um den Dienst zu verwenden, müssen Sie ihn auf der Seite **Parameter für Finanzdimensionsdienst** aktivieren. Derzeit funktioniert der Dienst nur bei importierten Journals mit 500 oder mehr Zeilen. Darüber hinaus kann es derzeit nur allgemeine Buchungen verarbeiten, bei denen der Kontotyp **Sachkonto** in den Erfassungspositionen festgelegt ist. Andere Kontotypen in Erfassungspositionen, wie **Debitor**, **Kreditor** und **Bank**, werden derzeit nicht unterstützt. Dieser Dienst wird nicht aufgerufen, wenn abgeleitete Dimensionen im System eingerichtet werden.

Der Finanzdimensionsdienst bietet eine verbesserte Leistung, wenn Journale importiert werden, indem ein neuer Dienst verwendet wird, der parallel zum Datenimport ausgeführt wird. Es wird nur für die Hauptkonto- und Finanzdimensionsdaten im Journal ausgeführt und generiert die Dimensionskombinationen, die im Sachkonto-Zeichenfolgenfeld in den Erfassungspositionen angegeben sind. Die Verarbeitung wandelt diese Zeichenfolge in den strukturierten Datenspeicher um, den das Finanzdimensions-Framework im Rest des Produkts für Prüfung, zusammenfassende Berichte und Abfragen verwendet. Weitere Informationen zum zusammenfassenden Berichten von Finanzdimensionsdaten finden Sie unter [Finanzdimensionssätze](financial-dimension-sets.md).

Weitere Informationen finden Sie in folgenden Themen:

- [Finanzdimensionen definieren](tasks/define-financial-dimensions.md)
- [Standardvorlagen für Finanzdimension verwalten](tasks/maintain-financial-dimension-default-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
