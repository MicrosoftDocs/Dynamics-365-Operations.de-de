---
title: Elektronische Rechnungen in Finance und Supply Chain Management ausstellen
description: In diesem Thema wird erläutert, wie elektronische Rechnungen in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management über die elektronische Rechnungsstellung ausgestellt werden.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 8d6ef59b64a96e13bdc2e5ddf299ef7ab98e105c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840075"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Elektronische Rechnungen in Finance und Supply Chain Management ausstellen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie elektronische Rechnungen in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management über die elektronische Rechnungsstellung ausgestellt werden.


## <a name="feature-activation"></a>Funktionsaktivierung

Um elektronische Rechnungen über die elektronische Rechnungsstellung auszustellen, müssen Sie die Funktion in Finance und Supply Chain Management aktivieren.

Jede Funktion entspricht einer bestimmten Funktion für die elektronische Rechnungsstellung, die den Anforderungen eines Landes/einer Region an die elektronische Rechnungsstellung entspricht.

Die folgende Tabelle zeigt die Liste der Funktionen an, die die elektronische Rechnungsstellung unterstützen kann.

| Name                                              | Land/Region |
|---------------------------------------------------|----------------|
|Elektronische Rechnung Österreich                        |Österreich         |
|Elektronische Rechnung Belgien                         |Belgien         |
|NF-e – Behördliche E-Rechnungen Brasilien       |Brasilien          |
|NFS-e – elektronische Rechnung für brasilianischen Dienst (Stadt)|Brasilien          |
|Elektronische Rechnung Dänemark                          |Dänemark         |
|Elektronische Rechnung Ägypten                        |Ägypten           |
|Elektronische Rechnung Estland                        |Estland         |
|Elektronische Rechnung Finnland                         |Finnland         |
|Elektronische Rechnung Frankreich                          |Frankreich          |
|Elektronische Rechnung Deutschland                          |Deutschland         |
|PEPPOL – globale elektronische Rechnung                 |Global          |
|Elektronische Rechnung Italien                         |Italien           |
|CFDI – Elektronische Rechnung Mexiko                  |Mexiko          |
|Elektronische Rechnung Niederlande                           |Niederlande     |
|Elektronische Rechnung Norwegen                       |Norwegen          |
|Elektronische Rechnung Spanien                         |Spanien           |

Wenn eine ältere Funktion für die elektronische Rechnungsstellung vorhanden ist, die im Geltungsbereich der Länder-/Regionenlokalisierung unterstützt wird, deaktiviert die Aktivierung einer dieser Funktionen die ältere Funktion und ermöglicht die Ausstellung elektronischer Rechnungen über die elektronische Rechnungsstellung.

> [!IMPORTANT]
> Nachdem die Integrationsfunktion für die elektronische Rechnungsstellung aktiviert wurde, wird die neue elektronische Rechnungsstellung standardmäßig deaktiviert. Mit dem Funktionskonzept können Sie selektiv neue Erfahrungen für juristische Personen mithilfe länder-/regionenspezifischer Funktionen aktivieren. Die Option **Global** steuert die neue Erfahrung für die verbleibenden Bezirke/Regionen, die nicht speziell in der Tabelle aufgeführt sind.

## <a name="submit-electronic-documents"></a>Elektronische Belege übermitteln

Das Einreichen elektronischer Dokumente stellt den zentralen Kommunikationspunkt zwischen Finance und Supply Chain Management sowie der elektronischen Rechnungsstellung dar. Während jedes Übermittlungsereignisses fließt die Kommunikation in beide Richtungen:

- **Von Finance und Supply Chain Management zur elektronischen Rechnungsstellung** – Finance und Supply Chain Management senden die abstrakten Rechnungen an die elektronische Rechnungsstellung. Bei Bedarf senden sie auch den Inhalt von Variablen, die im Rahmen der elektronischen Rechnungsstellung konfiguriert wurden.
- **Von der elektronischen Rechnungsstellung zu Finance und Supply Chain Management** – Abhängig von der Funktion für die elektronische Rechnungsstellung erhalten Finance und Supply Chain Management von der elektronischen Rechnungsstellung Aktualisierungen zu den Verarbeitungsergebnissen von Rechnungen, die zuvor eingereicht wurden. Sie empfangen auch die Inhalte von Variablen, die im Rahmen der elektronischen Rechnungsstellung konfiguriert wurden.

Rufen Sie **Organisationsverwaltung &gt; Periodisch &gt; Elektronische Dokumente &gt; Elektronische Dokumente übermitteln** auf, um elektronische Dokumente an die elektronische Rechnungsstellung in Finance und Supply Chain Management zu übermitteln.

Ausgangspunkt ist eine gebuchte Rechnung. Diese Rechnung kann unterschiedlichen Ursprungs sein, z. B. Aufträge, Projektrechnungen oder Freitextrechnungen.

Der Übermittlungsvorgang kann manuell oder im Hintergrund ausgeführt werden.

- **Manuelle Ausführung** – Für die manuelle Ausführung müssen Sie die **Filtern**-Option zum Definieren des Bereichs von Dokumenten, die eingereicht werden müssen, verwenden. Auf der **Filter**-Seite können Sie Ihre eigene Abfrage konfigurieren, um die gebuchten Rechnungen auszuwählen, die übermittelt werden müssen. Sobald die Auswahl getroffen wurde, müssen Sie die Ausführung der Verarbeitung manuell starten und warten, bis sie vollständig ausgeführt ist. Nach Abschluss der Verarbeitung zeigt eine Meldung im Aktionszentrum die Anzahl der erfolgreich übermittelten elektronischen Dokumente an.
- **Hintergrundausführung** – Die Hintergrundausführung wird ausgeführt, ohne dass Sie angemeldet sein oder das Übermittlungsdialogfeld geöffnet lassen müssen. Sie können die Ausführung des Prozesses planen und die Ausführungshäufigkeit definieren.

## <a name="view-the-submission-logs"></a>Übermittlungsprotokolle anzeigen

In Finance und Supply Chain Management können Sie die Übermittlungsprotokolle verwenden, um die Verarbeitungsergebnisse der Übermittlung an die elektronische Rechnungsstellung anzuzeigen. Rufen Sie **Organisationsverwaltung &gt; Periodisch &gt; Elektronische Dokumente &gt; Übermittlung elektronischer Dokumente** auf, und wählen Sie anschließend im Feld **Dokumenttyp** einen Wert aus, um den in den Protokollen angezeigten Rechnungstyp zu filtern.

Es gibt drei mögliche Übermittlungsstatus:

- **Geplant** – Die elektronische Rechnungsstellung hat die Übermittlung von Finance und Supply Chain Management erhalten, und die Verarbeitung der Funktion für die elektronische Rechnungsstellung ist im Gange.
- **Abgeschlossen** – Die elektronische Rechnungsstellung hat die Funktion für die elektronische Rechnungsstellung erfolgreich verarbeitet, da sie für die Ausführung konfiguriert wurde.
- **Gescheitert** – Die elektronische Rechnungsstellung hat einen Fehler festgestellt oder wurde während der Verarbeitung der Funktion für die elektronische Rechnungsstellung durch eine Ausnahme gestoppt.

> [!IMPORTANT]
> Der Übermittlungsstatus bezieht sich auf den Status der Verarbeitung, die die elektronische Rechnungsstellung auf der Funktion für die elektronische Rechnungsstellung ausführt. Er bezieht sich nicht auf den endgültigen Status der elektronischen Rechnung selbst.
>
> Wenn beispielsweise eine elektronische Rechnung zur Genehmigung an einen externen Webdienst übermittelt werden muss, lautet der Übermittlungsstatus möglicherweise **Abgeschlossen**, aber der Status der elektronischen Rechnung könnte **Abgelehnt** sein. In diesem Fall konnte die elektronische Rechnungsstellung die Funktion für die elektronische Rechnungsstellung erfolgreich verarbeiten, da sie für die Verarbeitung dieser Funktion konfiguriert wurde. Die elektronische Rechnung wurde jedoch abgelehnt, da sie nicht den Kriterien entsprach, die der Webdienst für die Rechnungsgenehmigung festgelegt hatte.

Die Übermittlungsprotokolle enthalten die folgenden zusätzlichen Funktionen:

- **Übermittlungsdetails** – Sehen Sie sich die Details der Hauptübermittlung an. Die Visualisierung zeigt das vollständige Ausführungsprotokoll der Aktionen, die in der Funktion für die elektronische Rechnungsstellung konfiguriert sind. Außerdem können Benutzer die Dateien herunterladen, die während der Verarbeitung erstellt werden. In Szenarien, in denen die Rechnung von einem externen Webdienst genehmigt werden muss, können Benutzer sich den Status der Rechnung anzeigen lassen.
- **Zugehörige Übermittlungen** – Sehen Sie sich die Details der untergeordneten Übermittlungen an.
- **Übermittlungen abbrechen** – Diese Funktion ermöglicht einen speziellen Übermittlungsvorgang in Szenarien, in denen die elektronische Rechnung von einem externen Webdienst genehmigt werden muss. Es weist die elektronische Rechnungsstellung an, dem Webdienst eine bestimmte Meldung zu senden, mit der der Status einer genehmigten elektronischen Rechnung in der Webdienstdatenbank gelöscht werden soll.
- **Dokument erneut übermitteln** – Übermitteln Sie ein elektronisches Dokument erneut, das bereits an die elektronische Rechnungsstellung übermittelt wurde. Auf der Seite **Übermittlungsdetails** wird ein neues Protokoll erstellt.
- **Verknüpfte Übermittlung senden**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
