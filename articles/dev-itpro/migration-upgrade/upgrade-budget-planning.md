---
title: Budgetplanung aktualisieren
description: Zwischen Microsoft Dynamics AX 2012 und Microsoft Dynamics 365 for Finance and Operations gibt es erhebliche Unterschiede in der Budgetplanung. Einige Funktionen wurden nicht aktualisiert und erfordern daher eine Rekonfiguration. In diesem Thema wird erläutert, was umkonfiguriert werden muss und es werden auch neue Funktionen beschrieben, die berücksichtigt werden sollten, wenn die Aktualisierung abgeschlossen ist.
author: ryansandness
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: ryansand
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 3d57419ca5c59be185c87b869302b41bef05a3c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554495"
---
# <a name="upgrade-budget-planning"></a>Budgetplanung aktualisieren

[!include [banner](../includes/banner.md)]

Zwischen Microsoft Dynamics AX 2012 und Microsoft Dynamics 365 for Finance and Operations gibt es erhebliche Unterschiede in der Budgetplanung. Einige Funktionen wurden nicht aktualisiert und erfordern daher eine Rekonfiguration. In diesem Thema wird erläutert, was umkonfiguriert werden muss und es werden auch neue Funktionen beschrieben, die berücksichtigt werden sollten, wenn die Aktualisierung abgeschlossen ist.  

Die Budgetplanung in Microsoft Dynamics 365 for Finance and Operations enthält viele Erweiterungen, die in Microsoft Dynamics AX 2012 nicht verfügbar waren. In diesem Thema werden die Änderungen erklärt, die Kunden bei einer Aktualisierung durchführen müssen. Es unterstreicht auch die neuen Funktionen, die im Aktualisierungsprozess berücksichtigt werden sollen. Aufgrund der umfangreichen Änderungen können keine vorhandenen Budgetpläne geöffnet werden, bis die Änderungen vorgenommen werden, die in diesem Thema aufgeführt sind. Berichte funktionieren weiterhin und erfordern keine zusätzliche Änderungen.

## <a name="overview-of-changes"></a>Überblick über die Änderungen
Viele signifikante Veränderungen sind bei der Budgetierung für Finance and Operations vorgenommen worden. Diese Änderungen sind vorgesehen, um die Budgetplanung zu vereinfachen und zu konfigurieren, um die jährliche Wartung und der Setup zu reduzieren. Die folgenden Bereiche in AX 2012 existieren in Finance and Operations nicht mehr:

-   Budgetplanvorlagen (Budgetplanungskonfiguration)
-   Budgetplanordner (Budgetplanungskonfiguration)
-   Budgetplaneinschränkungen (Budgetplankonfiguration)
-   Vorlagen und Regeln für die Budgetplanungsphasen und Vorlagen (Budgetplanungsprozess)
-   Matrixfelder für Arbeitsblattvorlagen
-   Budgetplan Microsoft Excel Vorlagen-Assistent

Zahlreiche neue Konzepte können nicht aus früheren Funktionen direkt aktualisiert werden. Daher müssen Sie gewisse Rekonfigurationen ausführen, um diese neuen Konzepte zu adressieren. In den folgenden Abschnitten werden die Konzepte beschrieben, die die Artikel in der obigen Liste ersetzt haben.

### <a name="columns"></a>Spalten

Spalten sind ein neues Konzept, das Teile der Excel-Vorlagen und auch Matrixfelder ersetzen. Spalten können eine Periode, einen Monat, ein Quartal, ein Jahr oder alle Zeiten darstellen. Die Zeitreferenz ist dynamisch. Sie weist auf eine relative Periode oder ein Jahr im Budgetprozess hin. Beispielsweise verweist eine Spalte **Vorjahr Januar** auf den Finanzzeitraum 1 für Jahr -1. Eine Spalte entspricht einem Budgetplanszenario, wie Actuals oder Budgetanforderungen.

### <a name="layouts"></a>Layouts

Layouts sind ein neues Konzept, die Excel-Vorlagen ersetzen. Layouts enthalten die Spalten, die definieren, welche Budget- oder Actual-Daten und Perioden angezeigt werden sollten. Layouts werden auch zwischen Client und dem Excel-Add-In freigegeben. Somit ist die Benutzerfreundlichkeit, wenn Sie Daten im Finance and Operations Clients eingeben oder anzeigen besser als die Benutzerfreundlichkeit in AX 2012. Um Daten im Finance and Operations Client einzugeben, sind Sie nicht mehr zum Anzeigen und Eingeben eines einzelnen Szenarios in einer Buchungsansicht beschränkt. Stattdessen können Sie in einer Vergleichsansicht Beträge für mehrere Perioden sowie Konten gleichzeitig anzeigen und eingeben. Layouts können auch so definiert werden, dass Sie Währungen, Kommentare sowie andere optionale Daten eingeben und anzeigen können. In Layouts können Sie auch definieren, welche Sachkontodimensionen und Dimensionsbeschreibungen angezeigt werden sollen. Layouts enthalten auch Szenarioeinschränkungen, um festzulegen, welche Spalten in einer Vorlage geändert werden können und welche Spalten in Excel verfügbar sein sollen. Nachdem Sie ein Layout festlegen, wird ein Original für Sie generiert. Diese Vorlage erstellt wiederum die entsprechende Excel-Vorlage. Sie können die Excel-Vorlagee dann bearbeiten, um mehr Formeln und Formatierungen einzubeziehen und laden sie dann erneut nach oben. Layouts werden dann zu jeder Phasenregel auf der Seite **Budgetplanungsprozess** zugewiesen. Daher ersetzen die Layouts Vorlagen, die auf ähnliche Weise zugeordnet und in ähnlicher Weise angewendet wurden.

### <a name="budget-planning-processes"></a>Budgetplanungsprozesse

Budgetplanungsprozesse sind meistens gleich wie jene in AX 2012. Die signifikanteste Änderung ist die Ersetzung der Vorlagen mit Layouts zu. Wurden irgendwelche Prozesse zuvor im AX 2012 abgeschlossen, werden Prozesse auf den Status in Bearbeitung aktualisiert, damit Änderungen vorgenommen werden können. Sie müssen Layouts zuweisen müssen, damit jede Phasenregel bestimmt, welche Szenarien und Zeitperioden angezeigt werden, wenn der Plan im Client geöffnet wird. Die Layouts bestimmen auch, welche Excel-Vorlage außerhalb von Dynamics 365 for Finance and Operations geöffnet wird, sodass Sie das Budget anzeigen können. **Standardkontostruktur** ist ein neues angefordertes Feld für den Budgetplanungsprozess. Für jeden Budgetplanungsprozess, weisen Sie die primäre Kontostruktur zu, die für die Budgetierung verwendet werden soll.

### <a name="attachments"></a>Anhänge

Im AX 2012 wurden Begründungsdokumente in einem Anhangordner gespeichert. Keine vorherigen Begründungsdokumente werden aktualisiert. Begründungsdokumente werden nun in der Datenbank gespeichert. Wenn diese Informationen in der aktualisierten Version gespeichert werden, können Sie Begründungsdokumente endgültig für jeden Plan als Anhang hochladen, indem Sie die **Begründung** im Aktivitätsbereich verwenden. In AX 2012 wurden Excel-Arbeitsblätter für jeden Budgetplan auf der Vorlage erstellt. In Finane and Operations öffnen alle Pläne eine Kopie des Layouts. Allerdings werden keine Änderungen zur Excel-Datei gespeichert. Alle Formeln oder unterstützenden Informationen, die auf einer ProPlan-Grundlage verwendet wurden, müssen über Kommentare, ein Begründungsdokument oder einen anderen Prozess ergänzend hinzugefügt werden.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>Konfigurieren einer aktualisierten Umgebung von AX 2012
Um einfach zu bestimmen, wie die Aktualisierung für das System konfiguriert werden soll, nutzen die folgenden Beispiele einen aktualisierten Budgetprozess aus den AX 2012-Demodaten. Standardkonfigurationsdaten für Spalten wurden erstellt, die für gerundete Aktualisierungsprozesse nützen können. Sie können diese Standarddaten aktualisieren oder löschen, wenn sie Ihre Konfigurationsbedingungen nicht erfüllen. **Hinweis:** Es gibt neue Pflichtfelder, die nicht im System eingerichtet werden. Wenn Sie auf einer Seite festsitzen wie der Seite **Budgetplanungskonfiguration** und nicht weiter navigieren können, können Sie Ihren Browser schließen und ihn in einer anderen Seite erneut öffnen, um Details in der richtigen Reihenfolge einzugeben. Es gibt Pflichtfelder, die noch nicht festgelegt werden. Daher können möglicherweise Probleme auftreten, bis alles konfiguriert und alle Pflichtfelder festgelegt wurden. In diesem Thema wird erläutert, wie Sie diese Felder einrichten, sofern erforderlich. Hier sind einige dieser erforderlichen Felder:

-   Seite **Budgetplanungsprozess** : Feld **Standardkontostruktur**
-   Seite **Budgetplanungsprozess** : Feld **Layout** auf dem Inforegister **Budgetplanungsphasenregeln und -Layouts**

### <a name="define-columns-and-layouts"></a>Spalten und Layouts definieren

1. Klicken Sie auf der Seite **Budgetplanungskonfiguration** auf die Registerkarte **Spalten**. Als Teil der Aktualisierung werden neue Spalten automatisch basierend auf Ihren Bugetplanpositionen erstellt. Spalten verwenden nun dynamische Daten, in denen der Zeitpunkt vom Geschäftsjahr gebucht wird, das im Budgetplanungsprozess definiert wird. **Hinweis:** Aus Leistungsgründe während der Aktualisierung wird angenommen, dass alle Budgetzyklen Kalenderjahre darstellen und nicht Geschäftsjahre. Wenn Sie Geschäftsjahre verwenden, müssen Sie die Bearbeitung korrekt vornehmen, um die Spalten gemäß dem Geschäftsjahr korrekt zuzuordnen. Beispielsweise waren die folgenden Elemente in AX 2012 vorhanden:
   -   Budgetplanszenarien: Wirklichkeiten, Basiszeitraum, Budget-Anforderung, Budget genehmigt
   -   Budgetplanpositionen für alle Szenarien im Jahre 2017 und 2017 und 2016 Actuals

   Die folgenden Spalten sind in Finance and Operations erstellt:

   | Spaltenname    | Budgetplanszenario | Zeitperiode der Spalte | Jahresausgleich |
   |----------------|----------------------|--------------------|-------------|
   | Januar Szenario 1 | Istwerte              | 1                  | 0           |
   | Januar Szenario 2 | Basislinie             | 1                  | 0           |
   | Januar Szenario 3 | Budgetanforderung       | 1                  | 0           |
   | Januar Szenario 4 | Genehmigtes Budget      | 1                  | 0           |
   | Januar Szenario 5 | Istwerte              | 1                  | -1          |
   | Februar Szenario 1 | Istwerte              | 1                  | 0           |
   | ...            | ...                  | ...                | ...         |

   In diesem Beispiel wird eine Spalte mit der Bezeichnung, **Januar Szenario 1** für die neuesten Budgetplanbuchungsdaten erstellt, die gefunden werden, wenn Buchungen im Januar vorhanden sind. Eine ähnliche Spalte wird für jedes Szenario erstellt, das Daten enthält. Nachdem Spalten für alle Perioden in diesem Jahr vorhanden sind, werden für Spalten die vorherigen Jahre erstellt.
2. Ändern Sie die Registerkarte und Beschreibungen und alle sonstigen Details, entweder manuell im Client oder indem Sie Massenaktualisierungen durch das Excel-Add-In ausführen, das zu den Budgetplanspalten der Datenentität weist. Alle Filter, die zuvor für Matrixfelder festgelegt wurden, werden jetzt in der Spalten festgelegt.
3. Neues Budgetplanlayout erstellen. Ein Layout weist zu mehreren Spalten, um die Ansicht zu definieren, die in Excel und dem Client angezeigt wird. Das Layout erfordert, dass Sie zuerst einer Sachkontodimension angeben, die festgelegt wird, um zu bestimmen, welche Finanzdimensionen eingegeben werden können. Nachdem Sie den Dimensionssatz angeben, klicken Sie auf **Beschreibungen**, um weitere Dimensionsbeschreibungen auszuwählen, die im Layout berücksichtigt werden sollen.
4. Wählen Sie im Inforegister **Layoutelemente**, **Hinzufügen**, um Metadaten für jede Zeile hinzuzufügen, wie eine Währung, eine Budgetklasse oder einen Kommentar oder eine Budgetklasse, die die Einnahmenzeilen gegen die Ausgabenzeilen darstellt. Wählen Sie dann Spalten für die Zeitperiode hinzufügen und die Szenarien, die für diesen Budgetzyklus und Phase gelten. Sie können dieser Änderungen im Client oder durch Excel-Add-In manuell vornehmen, das auf die Budgetplanlayoutelemente der Datenentität hinweist.
5. Für jedes Layoutelement wählen Sie aus, ob die Spalte bearbeitbar sein soll und ob die Spalte in der Excel-Arbeitsmappe für dieses Layout auch erscheinen soll. **Hinweis:** Für unsere historischen Pläne sollten Sie ein Layout berücksichtigen, das 12 Monatsspalten für alle Budgetplanszenarien für diesen Prozess anzeigt.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Aktualisieren Sie den Budgetplanungsprozesse, um das gewünschte Layout für jede Budgetphase zu verwenden

1.  Auf der Seite **Budgetplanungsprozess** wählen Sie den Vorgang aus, der konfiguriert werden kann.
2.  Klicken Sie im Aktivitätsbereich auf **Bearbeiten**.
3.  Definieren Sie die Standardkontostruktur für diesen Budgetplanungsprozess. **Standardkontostruktur** ist ein neues angefordertes Feld, das festgelegt werden muss.
4.  Wählen Sie im Inforegister **Budgetplanungsphasenregeln und -Layouts** im Feld **Layout** und wählen Sie ein Layout aus, das zuvor konfiguriert wurde und das für diese Phase geeignet ist.
5.  Fahren Sie fort und wählen Sie die gleichen oder unterschiedliche Layouts für die verschiedenen Budgetplanungsphasen aus und speichern Sie dann die Änderungen.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Zusätzliche Funktionen, die in Ihrem Budgetierungsprozess zu berücksichtigen sind
### <a name="budget-planning-workspace"></a>Budgetplanungsarbeitsbereich

Der Arbeitsbereich ist für Budgeteigentümer- und individuelle Budgetbeteiligten vorgesehen. Er enthält Links zu beliebigen Budgetdokumenten, die Ihre Aufmerksamkeit erfordern. Es gibt auch Berichte und Key Performance Indicators (KPIs) für den Budgetprozess. Der Budgetadministrator kann den aktuellen Budgetplanungsprozess für alle Benutzer auf der Seite **Budgetierungsparameter** festlegen. Auf der Registerkarte **Arbeitsbereichseinstellungen** enthält das Inforegister ein Feld **Budgetplanung** , in dem Sie den Budgetplanungsprozess auswählen können.

### <a name="alternate-layouts"></a>Alternative Layouts

Alternative Layouts sind eine neue Funktion, mit der Sie Pläne in unterschiedliche Layouts anzeigen können. Mindestens ein Layout kann als Optionen bereitgestellt werden. Sie können einen Budgetplan in einem Monatslayout oder einen vierteljährlichen Layout anzeigen. Sie definieren alternierende Layouts im Inforegister **Budgetplanungsphasenregeln und Layouts** auf der Seite **Budgetplanungsprozess**.

### <a name="budget-milestones"></a>Budgetmeilensteine

Als Teil des Budgetprozesses ist es enorm wichtig, dass Sie Stichtage und Fristen verstehen. Sie können nun Daten konfigurieren, sodass Sie diese Beschreibungen haben. Budgetbenutzer sehen diese Beschreibungen, wenn sie Budgets öffnen, um alle Budgets zu bearbeiten oder anzuzeigen, die ihnen zugewiesen sind.

### <a name="copy-from-budget-plan-allocation"></a>Zuteilung für Budgetplanung kopieren

Mit einer neuen Zuordnungsmethode können Sie von einem übergeordneten Plan zu einem untergeordneten Plan verteilen, ohne dass Sie über eine untergeordneten Ebene in der Hierarchie gehen müssen Diese Methode ist besonders nützlich für Debitoren, die nur zuvor Finanzdimension nur für Budgetverteilung und -Genehmigungen erstellt haben.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Generieren von Budgetplänen aus den Budgetquellen.

Folgende Optionen wurden als regelmäßige Prozesse hinzugefügt. Mit diesen Optionen können Sie einen Budgetplan generieren, indem vorhandene Daten von einem anderen Modul als Ausgangspunkt verwendet werden:

-   Budgetplan aus Bedarfsplanung generieren
-   Budgetplan aus Beschaffungsplanung generieren
-   Budgetplan aus Projektplanungen generieren
-   Budgetplan aus Budgetregistereinträgen erstellen

### <a name="more-complete-tracking-of-amounts"></a>Weitere vollständige Nachverfolgung von Beträgen

Im AX 2012 weist Budgetplanung einen einzelnen Planbetrag auf, der für jeden Wert gespeichert wurde. In Finance and Operations ist das Datenmodell erweitert worden. Es gibt nun Buchungswährung, Buchhaltungswährung und Berichtswährungsbeträge für jeden Wert. Während der Aktualisierung sind diese neue Spalten automatisch für vorhandenen Daten ausgefüllt.

### <a name="do-not-convert-currency-in-aggregation"></a>Währung nicht in Aggregation konvertieren

Normalerweise wenn ein untergeordneter Plan mit einer übergeordneten Ebene zusammengefasst wird, werden die Beträge automatisch von der Buchungswährung für die Organisation der Buchhaltungswährung umgerechnet. Wenn Sie die Option **Keine Währung in der Aggregierung konvertieren** auf **Nein** festlegen, bleiben die aggregierten Beträge in der ursprünglichen Währung. Daher ermöglicht diese Option eine genauere Anpassung bei Wechselkursschwankungen.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Wir schauen zurück vom Budgetplan zu anderen Modulen, die zum Budget beitrugen

Budgetpläne können aus Bedarf oder Beschaffungsplanungen, Projekten und anderen Bereichen generiert werden. Die Abfrage der Budgetpläne nach Dimensionssätzen umfasst mehrere Optionen, über die Sie eine Abfrage ausführen lassen können, um die Quelle der Budgetplandaten zu identifizieren.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Dient zur Außerkraftsetzung oder Überschreibung von Zuweisungszeitplänen

Wenn es mehrere Quellen für Beträge gibt, die aufgeteilt werden müssen, können Sie angeben, dass die Beträge additiv werden sollen. In diesem Fall werden die Beträge keine vorhandenen Beträge überschreiben. Stattdessen werden diese zu den vorhandenen Beträgen zugeordnet.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Standardfinanzdimensionssatz für Budgetplanungskonfiguration

Die Seite **Budgetplanungskonfiguration** enthält jetzt ein Feld, in dem Sie den Standardfinanzdimensionssatz angeben können. Obwohl es sich um ein optionales Feld handelt, kann es für bestimmte Abfragen erforderlich sein. Es kann möglicherweise auch obligatorisch sein, wenn Sie Berichte nach Dimensionssatz gruppieren oder filtern möchten.

### <a name="data-entities"></a>Datenentitäten

Einige Datenentitäten wurden hinzugefügt, um eine rasche Implementierung der Budgetplanung zu aktivieren. Die Entitäten lassen es auch zu, dass Sie Änderungen über Excel vornehmen können. Daher müssen Sie Artikel nicht einzeln über den Client einrichten. Hier ist eine Liste der Entitäten der neuen Daten:

-   Entitätsname
-   Budgetparameter
-   Budgetplanparameter
-   Budgetplanszenarien
-   Budgetplanphasen
-   Budgetplan-Workflowphase
-   Zuteilungszeitpläne für Budgetplan
-   Zuteilungen für Budgetplanphase
-   Budgetplanprioritäten
-   Budgetplanspalten
-   Budgetplanlayout-Elemente




