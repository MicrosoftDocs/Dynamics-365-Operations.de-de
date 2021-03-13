---
title: Elektronische Rechnungen in Finance und Supply Chain Management ausstellen
description: In diesem Thema wird erläutert, wie elektronische Rechnungen in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management über das Add-On für die elektronische Rechnungsstellung ausgestellt werden.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104384"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Elektronische Rechnungen in Finance und Supply Chain Management ausstellen

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie elektronische Rechnungen in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management über das Add-On für die elektronische Rechnungsstellung ausgestellt werden.


## <a name="feature-activation"></a>Funktionsaktivierung

Um mit der Ausstellung elektronischer Rechnungen über das Add-On für die elektronische Rechnungsstellung zu beginnen, muss die Funktionsreferenz in Finance und Supply Chain Management aktiviert werden.

Jede Funktionsreferenz entspricht einer bestimmten Funktion für die elektronische Rechnungsstellung, die den Anforderungen eines Landes/einer Region an die elektronische Rechnungsstellung entspricht.

Die folgende Tabelle zeigt die Liste der Funktionsreferenzen an, die das Add-On für die elektronische Rechnungsstellung unterstützt.

| Funktionsreferenz | Name                                              | Land/Region |
|-------------------|---------------------------------------------------|----------------|
| BR-00053          | NF-e – elektronische Rechnung Brasilien       | Brasilien         |
| BR-00095          | NFS-e – elektronische Rechnungen Brasilien               | Brasilien         |
| DK-00001          | Elektronische Rechnungsstellung für den öffentlichen Sektor (OIOUBL) – DK    | Dänemark        |
| EG-00008          | Elektronische Rechnungsstellung für Ägypten                             | Ägypten          |
| ES-00025          | Elektronische Rechnung an den öffentlichen Sektor           | Spanien          |
| EUR-00023         | Elektronische Rechnungsstellung der Europäischen Union für den öffentlichen Sektor       | Europa         |
| ITA-00036         | IT – elektronische Rechnungsstellung für den öffentlichen Sektor (FatturaPA) | Italien          |
| MX-00010          | E-Rechnungsstellung CFDI                                  | Mexiko         |
| MX-00016          | Elektronische Rechnungsstellung CFDI – Stornierungsvorgang           | Mexiko         |

In den Fällen, in denen eine ältere Funktion für die elektronische Rechnungsstellung vorhanden ist, die den Geltungsbereich der Länderlokalisierung unterstützt, ermöglicht die Aktivierung der Funktionsreferenz die Ausstellung elektronischer Rechnungen über das Add-On für die elektronische Rechnungsstellung und deaktiviert die vorherige Funktion.

## <a name="submit-electronic-documents"></a>Elektronische Belege übermitteln

Das Einreichen elektronischer Dokumente stellt den zentralen Kommunikationspunkt zwischen Finance und Supply Chain Management sowie dem Add-On für die elektronische Rechnungsstellung dar. Während jedes Übermittlungsereignisses fließt die Kommunikation in beide Richtungen:

- **Von Finance und Supply Chain Management zum Add-On für die elektronische Rechnungsstellung** – Finance und Supply Chain Management senden die abstrakten Rechnungen an das Add-On für die elektronische Rechnungsstellung. Bei Bedarf senden sie auch den Inhalt von Variablen, die im Rahmen der elektronischen Rechnungsstellung konfiguriert wurden.
- **Vom Add-On für die elektronische Rechnungsstellung zum Finance und Supply Chain Management** – Abhängig von der Funktion für die elektronische Rechnungsstellung erhalten das Finance und Supply Chain Management vom Add-On für die elektronische Rechnungsstellung Aktualisierungen zu den Verarbeitungsergebnissen von Rechnungen, die zuvor eingereicht wurden. Sie empfangen auch die Inhalte von Variablen, die im Rahmen der elektronischen Rechnungsstellung konfiguriert wurden.

Rufen Sie **Organisationsverwaltung &gt; Periodisch &gt; Elektronische Dokumente &gt; Elektronische Dokumente übermitteln** auf, um elektronische Dokumente an das Add-On für die elektronische Rechnungsstellung in Finance und Supply Chain Management zu übermitteln.

Ausgangspunkt ist eine gebuchte Rechnung. Diese Rechnung kann unterschiedlichen Ursprungs sein, z. B. Aufträge, Projektrechnungen oder Freitextrechnungen.

Der Übermittlungsvorgang kann manuell oder im Hintergrund ausgeführt werden.

- **Manuelle Ausführung** – Für die manuelle Ausführung müssen Sie die **Filtern**-Option zum Definieren des Bereichs von Dokumenten, die eingereicht werden müssen, verwenden. Auf der **Filter**-Seite können Sie Ihre eigene Abfrage konfigurieren, um die gebuchten Rechnungen auszuwählen, die übermittelt werden müssen. Sobald die Auswahl getroffen wurde, müssen Sie die Ausführung der Verarbeitung manuell starten und warten, bis sie vollständig ausgeführt ist. Nach Abschluss der Verarbeitung zeigt eine Meldung im Aktionszentrum die Anzahl der erfolgreich übermittelten elektronischen Dokumente an.
- **Hintergrundausführung** – Die Hintergrundausführung wird ausgeführt, ohne dass Sie angemeldet sein oder das Übermittlungsdialogfeld geöffnet lassen müssen. Sie können die Ausführung des Prozesses planen und die Ausführungshäufigkeit definieren.

## <a name="view-the-submission-logs"></a>Übermittlungsprotokolle anzeigen

In Finance und Supply Chain Management können Sie die Übermittlungsprotokolle verwenden, um die Verarbeitungsergebnisse der Übermittlung an das Add-On für die elektronische Rechnungsstellung anzuzeigen. Rufen Sie **Organisationsverwaltung &gt; Periodisch &gt; Elektronische Dokumente &gt; Übermittlung elektronischer Dokumente** auf, und wählen Sie anschließend im Feld **Dokumenttyp** einen Wert aus, um den in den Protokollen angezeigten Rechnungstyp zu filtern.

Es gibt drei mögliche Übermittlungsstatus:

- **Geplant** – Das Add-On für die elektronische Rechnungsstellung hat die Übermittlung von Finance und Supply Chain Management erhalten, und die Verarbeitung der Funktion für die elektronische Rechnungsstellung ist im Gange.
- **Abgeschlossen** – Das Add-On für die elektronische Rechnungsstellung hat die Funktion für die elektronische Rechnungsstellung erfolgreich verarbeitet, da sie für die Ausführung konfiguriert wurde.
- **Gescheitert** – Das Add-On für die elektronische Rechnungsstellung hat einen Fehler festgestellt oder wurde während der Verarbeitung der Funktion für die elektronische Rechnungsstellung durch eine Ausnahme gestoppt.

> [!IMPORTANT]
> Der Übermittlungsstatus bezieht sich auf den Status der Verarbeitung, die das Add-On für die elektronische Rechnungsstellung auf der Funktion für die elektronische Rechnungsstellung ausführt. Er bezieht sich nicht auf den endgültigen Status der elektronischen Rechnung selbst.
>
> Wenn beispielsweise eine elektronische Rechnung zur Genehmigung an einen externen Webdienst übermittelt werden muss, lautet der Übermittlungsstatus möglicherweise **Abgeschlossen**, aber der Status der elektronischen Rechnung könnte **Abgelehnt** sein. In diesem Fall konnte das Add-On für die elektronische Rechnungsstellung die Funktion für die elektronische Rechnungsstellung erfolgreich verarbeiten, da es für die Verarbeitung dieser Funktion konfiguriert wurde. Die elektronische Rechnung wurde jedoch abgelehnt, da sie nicht den Kriterien entsprach, die der Webdienst für die Rechnungsgenehmigung festgelegt hatte.

Die Übermittlungsprotokolle enthalten die folgenden zusätzlichen Funktionen:

- **Übermittlungsdetails** – Sehen Sie sich die Details der Hauptübermittlung an. Die Visualisierung zeigt das vollständige Ausführungsprotokoll der Aktionen, die in der Funktion für die elektronische Rechnungsstellung konfiguriert sind. Außerdem können Benutzer die Dateien herunterladen, die während der Verarbeitung erstellt werden. In Szenarien, in denen die Rechnung von einem externen Webdienst genehmigt werden muss, können Benutzer sich den Status der Rechnung anzeigen lassen.
- **Zugehörige Übermittlungen** – Sehen Sie sich die Details der untergeordneten Übermittlungen an.
- **Übermittlungen abbrechen** – Diese Funktion ermöglicht einen speziellen Übermittlungsvorgang in Szenarien, in denen die elektronische Rechnung von einem externen Webdienst genehmigt werden muss. Es weist das Add-On für die elektronische Rechnungsstellung an, dem Webdienst eine bestimmte Meldung zu senden, mit der der Status einer genehmigten elektronischen Rechnung in der Webdienstdatenbank gelöscht werden soll.
- **Dokument erneut übermitteln** – Übermitteln Sie ein elektronisches Dokument erneut, das bereits an das Add-On für die elektronische Rechnungsstellung übermittelt wurde. Auf der Seite **Übermittlungsdetails** wird ein ganz neues Protokoll erstellt.
- **Verknüpfte Übermittlung senden**
