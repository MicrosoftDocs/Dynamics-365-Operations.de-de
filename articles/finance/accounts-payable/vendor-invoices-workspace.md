---
title: Arbeitsbereich für die Kreditor-Rechnungsautomatisierung
description: In diesem Thema wird erläutert, wie Sie den Arbeitsbereich einrichten, der sich auf Lieferantenrechnungen bezieht und die Informationen anzeigt, die über Microsoft Power BI verfügbar sind.
author: abruer
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f28cc5f63df2f0d8a4c8cae407f7166aa4fa03db
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182578"
---
# <a name="vendor-invoice-automation-workspace"></a>Arbeitsbereich für die Kreditor-Rechnungsautomatisierung

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Sie den Arbeitsbereich einrichten, der sich auf Lieferantenrechnungen bezieht und die Informationen anzeigt, die über Microsoft Power BI verfügbar sind. Die Lieferantenrechnungsinformationen in diesem Arbeitsbereich werden nach bestimmten Benutzern gefiltert und in einem grafischen Format angezeigt.

## <a name="overview"></a>Übersicht

Der Arbeitsbereich **Automatisierung von Lieferantenrechnungen** zeigt Informationen an, die sich auf die Verarbeitung von Lieferantenrechnungen beziehen. Der Arbeitsbereich umfasst eine Ansicht **Meine Arbeit** und eine Seite **Analyse - Alle Unternehmen**. Die Ansicht **Meine Arbeit** zeigt zusammenfassende Kacheln, Lieferantentransaktionsrater und zugehörige Kreditoreninformationen. Die Seite **Analyse - Alle Unternehmen** verwendet die Funktionen von Microsoft Power BI, um grafische Elemente hinsichtlich der Lieferantenrechnungen anzuzeigen.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Richten Sie den anzuzeigenden Arbeitsbereich ein, um Power BI Inhalt anzuzeigen

Sie müssen dieses Einrichten abschließen, bevor Daten in Power BI-Visualisierungen im Arbeitsbereich **Lieferantenrechnungsautomatisierung** angezeigt werden können.

1. In dem **Funktionsverwaltung** Arbeitsbereich filtern Sie die Liste, um die Funktion **Automatisierung von Lieferantenrechnungen** zu suchen.
3. Wählen Sie **Jetzt aktivieren**.
4. Richten Sie einen Workflow für Lieferantenrechnungen ein, um sicherzustellen, dass Rechnungen von Anfang bis Ende verarbeitet werden können, ohne dass manuelle Eingriffe erforderlich sind. Um einen Workflow einzurichten gehen Sie zu **Kreditorenkonten \> Einrichtung \> Kreditorenkontenworkflows**.
5. Gehen Sie zu **Kreditorenkonten \> Konfiguration \> Kreditorenkontenparameter** und wählen Sie die Registerkarte **Automatisierung von Lieferantenrechnungen**. Weitere Informationen finden Sie unter [Einrichtungs-Optionen für die Automatisierung von Lieferantenrechnungen](vnd-invoice-set-up-options.md).
6. Legen Sie Option **Senden Sie importierte Rechnungen automatisch an das Workflowsystem** auf **Ja** fest.
7. Wenn Produktbelege automatisch abgeglichen werden sollen, legen Sie die Option **Ordnen Sie Produktbelege automatisch Rechnungsrechnungen zu** auf **Ja** fest.
8. Überprüfen Sie die verbleibenden optionalen Einstellungen und konfigurieren Sie sie gemäß den Anforderungen Ihres Unternehmens.
9. Wechseln Sie zu **Systemverwaltung** \> Einrichtung \> Systemparameter und legen Sie die Felder **Systemwährung** und **Systemwechselkurs** fest.
10. Wechseln Sie zu **Hauptbuch** \> Einrichtung \> Sachkonto und legen Sie die **Buchhaltungswährung** und den **Wechselkurstyp** fest.
11. Gehen Sie zu **Hauptbuch \> Währungen \> Wechselkurse** und geben Sie die Wechselkurse zwischen der Transaktionswährung und der Buchhaltungswährung sowie zwischen der Buchhaltungswährung und der Systemwährung ein.
12. Gehen Sie zu **Systemadministration \> Konfiguration \> Entitätsstore** und suchen Sie nach **Automatisierungsmaßnahme für Lieferantenrechnungen**. Wählen Sie **Aktualisieren** aus.

Um die im Arbeitsbereich angezeigten Informationen anzuzeigen, müssen Sie über die Sicherheitsrolle Kreditorenbuchhalter-Manager oder Kreditorenbuchhalter verfügen.

## <a name="my-work-view"></a>Ansicht "Meine Arbeit"

### <a name="company-selection"></a>Unternehmensauswahl

Wenn die Funktion **Automatisierung von Kreditor-Rechnungen** eingeschaltet ist, erscheint oben im Arbeitsbereich ein Feld **Firma**. Die Auswahl im Feld **Unternehmen** wirkt sich auf alle im Arbeitsbereich angezeigten Informationen aus. Standardmäßig werden in der Ansicht Informationen zu dem Unternehmen angezeigt, bei dem Sie sich angemeldet haben. Durch Auswahl eines anderen Unternehmens im Feld **Unternehmen** können Sie Informationen für dieses Unternehmen im Arbeitsbereich anzeigen. Sie können dann eine Kachel im Arbeitsbereich auswählen, um zur zugehörigen Seite in der ausgewählten Firma zu gelangen.

### <a name="summary-tiles"></a>Zusammenfassungskacheln

Die Kacheln im Abschnitt **Zusammenfassung ausstehender Rechnungen** in der Ansicht **Meine Arbeit** geben einen Überblick über den Status Ihrer Lieferantenrechnungen. Sie können noch nicht gebuchte Journale und gesperrte Rechnungen sehen. Darüber hinaus gibt es die vier Kacheln, die der Automatisierungsfunktion für Lieferantenrechnungen zugeordnet sind:

- **Manuelle Zugangsübereinstimmung erforderlich**
- **Übereinstimmungsprüfung nicht erfolgreich**
- **Rechnungen wurden nicht an Workflow übermittelt**
- **Rechnungen wurden nicht importiert.**

(Für diese vier Kacheln muss die Funktion zur Automatisierung von Kreditorenrechnungen in der **Funktionsverwaltung** aktiviert sein.)

Um die Kachel **Kreditorenrechnungen wiederherstellen** zu verwenden, muss die Funktion in den **Kreditorenparametern** aktiviert sein. Gehen Sie zu **Kreditorenkonten \> Kreditorenkontenparameter** und legen dann auf der Registerkarte **Rechnung** die Option **Zulassen der Wiederherstellung von Lieferantenrechnungen** auf **Ja** fest.

Wenn die Funktion aktiviert ist, werden auch drei Kacheln im Arbeitsbereich namens **Erfassungen** zusammengefasst. Die Kacheln sind betitelt mit **Erfassungen**, **Erfassungen – Mir zugewiesen**, und **Rechnungspool**. 

Die Informationen im Abschnitt **Zusammenfassung ausstehender Rechnungen** bezieht sich auf die Firma, die als Standardfirma für Ihre Anmeldung festgelegt ist.

### <a name="creating-new-records"></a>Neue Einträge erstellen

Wählen Sie zum Erstellen eines neuen Rechnungsdatensatzes **Neu** und wählen Sie dann einen der folgenden Datensatztypen in der Liste aus:

- Kreditorenrechnung
- Rechnungserfassung
- Globale Rechnungserfassung
- Rechnungsregister
- Rechnungsgenehmigung

Beachten Sie, dass der von Ihnen erstellte Datensatz auf dem Firmenfilter basiert und nicht auf der Firma, bei der Sie angemeldet sind. Sie sind beispielsweise bei der **UMSF** Firma angemeldet, aber der Firmenfilter ist auf **GBSI** gesetzt. In diesem Fall, wenn Sie **Neu** auswählen und dann einen Datensatztyp in der Liste auswählen wird der Datensatz in der GBSI-Firma erstellt.

### <a name="documents-not-invoiced-grids"></a>Dokumente nicht in Rechnung gestellte Raster

Der Abschnitt **Dokumente nicht in Rechnung gestellt** enthält Raster, in denen Dokumente angezeigt werden, die auf Lieferantenrechnungen warten.

Der Raster **Bestellungen öffnen** zeigt alle Bestellungen an, die noch nicht vollständig in Rechnung gestellt wurden. Sie können die Schaltfläche **Rechnung jetzt** verwenden, um eine Lieferantenrechnung für eine Bestellung zu erstellen. Sie können die Schaltfläche **Vorauszahlungsrechnung jetzt** verwenden, um eine Vorauszahlungsrechnung für eine Bestellung zu erstellen.

Der Raster **Produktzugänge** zeigt alle Bestellungen an, die noch nicht vollständig in Rechnung gestellt wurden. Sie können die Schaltfläche **Rechnung jetzt** verwenden, um eine Lieferantenrechnung für eine Bestellung zu erstellen.

Der Raster **Ausstehende Lieferantenrechnungen** zeigt alle Lieferantenrechnungen an, die nicht an das Workflow-System gesendet wurden. Sie können das Feld **Suche** und/oder den Firmenfilter verwenden, um nach einer bestimmten Lieferantenrechnung zu suchen. Sie können die Schaltfläche **Bearbeiten** zum Bearbeiten einer Transaktion verwenden, die im Raster angezeigt wird.

Auf dem Raster **Bestellung finden** können Sie das Feld **Suche** verwenden, um nach einer bestimmten Bestellung zu suchen.

### <a name="related-information"></a>Zugehörige Informationen

Sie können Informationen zu gebuchten Rechnungen anzeigen, indem Sie die Links auf der rechten Seite des Arbeitsbereichs verwenden. Diese Links enthalten **Öffnen Sie Lieferantenrechnungen**, **Rechnungserfassung**, und **Rechnungsverlauf und übereinstimmende Details**. In dem Abschnitt **Anbieter** können Sie auf eine gefilterte Liste zugreifen, in der alle Anbieter angezeigt werden, die sich in der Warteschleife befinden, oder Sie können die Verknüpfung **Alle Anbieter** verwenden. **Alle Bestellungen** und **Offene Vorauszahlungen** Links sind ebenfalls verfügbar.

### <a name="analytics--all-companies-page"></a>Analyse – Seite alle Unternehmen

Wenn die Option **Importierte Rechnungen automatisch an den Workflow senden** auf **Ja** gesetzt wird auf der Seite **Kreditorenparameter** können Sie Automatisierungsanalysen anzeigen. Die Seite **Analytics – Alle Unternehmen** enthält wichtige Kennzahlen, z. B. Lieferantenrechnungen, die vom Genehmigenden und vom Unternehmen genehmigt werden. Diese Seite enthält fünf Berichtsseiten. Eine Seite enthält einen Überblick und die anderen Seiten enthalten Details zu Kreditorenkontenautomation.

Die folgende Tabelle enthält die Visualisierungen, die für jede Berichtsseite verfügbar ist.

| Berichtsseiten                    | Visualisierung |
|--------------------------------|----------------|
| Kreditorenrechnungen Übersicht        | <ul><li>Ausstehende Lieferantenrechnungen in der Automatisierung in Systemwährung</li><li>Rechnungen, die nicht importiert werden konnten</li><li>Rechnungen im Workflow</li><li>Berührungslose Rechnungen dauern 30 Tage</li><li>Die gesamten automatisierten Rechnungen dauern 30 Tage</li><li>Saldo offener Rechnungen in Systemwährung</li><li>Gründe für Ausfälle, letzte 30 Tage</li><li>Prozent der gebuchten Rechnungen, die automatisch verarbeitet wurden</li><li>Tage, um eine Rechnung zu bearbeiten</ul></li> |
| Automatisierungsstatus              | <ul><li>Berührungslose Rechnungen dauern 30 Tage</li><li>Berührungslose Rechnungen dauern 30 Tage nach Unternehmen</li><li>Berührungslose Rechnungen dauern 30 Tage nach Kreditorengruppe</li><li>Prozent der gebuchten Rechnungen, die automatisch verarbeitet wurden</li><li>Tage, um eine Rechnung zu bearbeiten</li></ul> |
| Rechnungen, die nicht importiert werden konnten | <ul><li>Rechnungen, die nicht importiert werden konnten</li><li>Rechnungen, die nicht importiert werden konnten nach Unternehmen</li></ul> |
| Gründe für einen Automatisierungsfehler | <ul><li>Rechnungen fehlgeschlagen</li><li>Rechnungen von Unternehmen fehlgeschlagen</li><li>Rechnungen nach Lieferantengruppe fehlgeschlagen</li></ul> |
| Workflowstatus                | <ul><li>Rechnungen im Workflow</li><li>Kreditorenrechnungsworkflowinstanzen</li><li>Zuordnung pro Genehmiger</li><li>Workflow der Lieferantenrechnung pro Unternehmen</li><li>Durchschnittliche Tage im Arbeitsplan nach Genehmiger</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
