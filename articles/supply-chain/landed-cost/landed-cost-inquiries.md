---
title: Abfragen der Gesamttransportkosten
description: In diesem Thema wird beschrieben, wie Sie die verschiedenen Arten von Abfragen, die für das Modul Gesamttransportkosten verfügbar sind, finden und verwenden.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b1d94621b68e443175102a1af5a5fdb4a25d0d1e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571760"
---
# <a name="landed-cost-inquiries"></a>Gesamttransportkosten-Abfragen

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Abfragen für Fahrten

Die Abfrage **Fahrtzeilen** zeigt alle Fahrtzeilen an, die sich auf den Bestand beziehen. Diese Abfrage kann als Filter verwendet werden, um einen Artikel, eine Einkaufsbestellung oder eine andere nützliche Information zu finden. Sie kann auch verwendet werden, um das voraussichtliche Lieferdatum eines Artikels zu ermitteln, der sich möglicherweise auf einer oder mehreren Fahrten befindet. Auf diese Weise kann es Ihnen helfen, den erwarteten Bestandseingang zu verwalten.

Um diese Abfrage zu öffnen, gehen Sie zu **Gesamttransportkosten \> Abfragen \> Fahrten**.

### <a name="overview-tab"></a>Registerkarte Übersicht

Die Registerkarte **Übersicht** der Abfrageseite **Fahrtrouten** enthält ein Raster, das grundlegende Informationen über jede relevante Fahrt anzeigt. Die folgende Tabelle beschreibt die Spalten im Raster.

| Spalte | Beschreibung |
|---|---|
| **Artikelnummer** | Der Artikel für die Fahrt-Linie. |
| **Referenz** | Die Art der Bestellung (Einkaufsbestellung oder Umlagerungsauftrag). |
| **Anzahl** | Die Nummer der Einkaufsbestellung oder des Umlagerungsauftrags. |
| **Folio** | Die Palette, die mit der Fahrt-Zeile verknüpft ist. |
| **Versandcontainer** | Der Transportcontainer, der mit der Zeile der Fahrt verknüpft ist. |
| **Seereise** | Die Fahrt, die mit der Zeile verbunden ist. |
| **Leistung** | Die Menge des Artikels für die Fahrtzeile. |
| (Andere Dimensionen) | Sie können nach Bedarf Spalten für weitere Dimensionen einblenden. Zu diesen Dimensionen gehören Chargennummer, Bestandsstatus und Lagerort. Wählen Sie im Aktivitätsbereich **Inventar \> Dimensionen anzeigen**, um ein Dialogfeld zu öffnen, in dem Sie die einzuschließenden Dimensionen auswählen können. |

### <a name="general-tab"></a>Registerkarte „Allgemeines“

Wählen Sie die Registerkarte **Allgemein**, um weitere Informationen über die Zeile anzuzeigen, die gerade auf der Registerkarte **Übersicht** ausgewählt ist.

### <a name="dimensions-tab"></a>Registerkarte Dimensionen

Wählen Sie die Registerkarte **Dimensionen**, um Werte für alle verfügbaren Dimensionen für die Zeile anzuzeigen, die aktuell auf der Registerkarte **Übersicht** ausgewählt ist, unabhängig von den Dimensionen, die Sie zur Anzeige auf dieser Registerkarte ausgewählt haben.

## <a name="cost-estimate-inquiries"></a>Abfragen der Kalkulation

Jedes Mal, wenn Sie eine Kalkulation erzeugen, wird die Kalkulation zur **Kostenvoranschläge** Abfrage-Seite hinzugefügt. Ausführliche Informationen zum Erzeugen, Anzeigen und Arbeiten mit Kostenvoranschlägen (einschließlich der Kostenvoranschläge auf der Abfrage-Seite) finden Sie unter [Kalkulationen und Gesamttransportkosten verwalten](estimate-manage-landed-costs.md).

## <a name="item-tracking"></a>Artikelverfolgung

Verwenden Sie die Seite **Postenverfolgung**, um offene Zeilen von Einkaufsbestellungen und deren aktuellen Status anzuzeigen. Zeilen müssen nicht mit einer Fahrt verknüpft sein, um hier zu erscheinen. Wenn jedoch ein Artikel mit einer Fahrt verbunden ist, zeigt die Zeile des Artikelverfolgungsdatensatzes die Fahrt-ID an.

Um diese Seite zu öffnen, gehen Sie auf **Gesamttransportkosten \> Abfragen \> Tracking \> Artikelverfolgung**.

Da Ihr System wahrscheinlich sehr viele Zeilen der Einkaufsbestellung enthält, zeigt die Seite **Artikelverfolgung** zunächst keine Datensätze an. Beginnen Sie damit, mithilfe der Filterfelder oben auf der Seite die Zeilen der Einkaufsbestellung festzulegen, nach denen Sie suchen. Wählen Sie dann **Aktualisieren** im Aktivitätsbereich, um die Liste zu erzeugen. Sie können ein Sternchen (\*) als Platzhalterzeichen in jedem der Filterfelder verwenden. Um z.B. alle Zeilen einer Einkaufsbestellung für Artikel zu finden, die das Wort „DVD“ in ihrem Namen enthalten, legen Sie das Feld **Typ** auf **Produktname** fest und geben *\*DVD \** in das Feld **Feldwert** ein.

> [!NOTE]
> Zurzeit umfassen Rückstände nur Aufträge. Verkaufsangebote werden nicht angezeigt und gelten nicht als Rückstände.

Die folgende Tabelle beschreibt die Spalten im Raster auf der Seite **Artikelverfolgung**.

| Spalte | Beschreibung |
|---|---|
| **Bis-Port** | Der endgültige Bestimmungsort. |
| **Bestätigt** | Das bestätigte Datum der Zeile für die Einkaufsbestellung. |
| **Lieferdatum** | Das Lieferdatum der Zeile mit der Einkaufsbestellung. |
| **Seereise** | Wenn die Zeile mit einer Fahrt verbunden ist, die Fahrt-ID. |
| **Transportcontainer** | Wenn die Zeile mit einem Transportcontainer verbunden ist, die Container-ID. |
| **Lieferhafen** | Der aktuelle Hafen, basierend auf dem ersten Abschnitt im Tracking-Formular, in dem kein aktuelles Datum für den Transportcontainer festgelegt ist, der mit der Einkaufsbestellung verbunden ist. |
| **Aktivität** | Die aktuelle Aktivität, basierend auf dem ersten Abschnitt im Tracking-Formular, in dem kein aktuelles Datum für den Transportcontainer festgelegt ist, der mit der Zeile der Einkaufsbestellung verknüpft ist. |
| **Geschätztes Enddatum** | Das Datum, an dem die Fahrt voraussichtlich im Ziellagerort eintrifft. |
| **Name** | Der Name des Kreditors. |
| **Fahrt-Status** | Der Versandstatus, der an die Zeile der Einkaufsbestellung angehängt ist. |
| **Artikelnummer** | Die Nummer des Artikels für die Zeile der Einkaufsbestellung. |
| **Extern** | Der Name des Artikels des Lieferanten. |
| **Produktname** | Der Name des Artikels für die Zeile der Einkaufsbestellung. |
| **Leistung** | Die Menge der Bestellzeile für die Einkaufsbestellung. |
| **Einheit** | Die Maßeinheit für die Zeile der Einkaufsbestellung. |
| **Referenz** | Die Art der Bestellung (Einkaufsbestellung oder Umlagerungsauftrag) |
| **Referenznummer** | Die Nummer der Einkaufsbestellung oder des Umlagerungsauftrags. |
| **Rückstand** | Ein Symbol zeigt an, dass es für den Artikel Rückstände im Verkauf gibt. |
| (Andere Dimensionen) | Sie können nach Bedarf Spalten für weitere Dimensionen einblenden. Zu diesen Dimensionen gehören Chargennummer, Bestandsstatus und Lagerort. Wählen Sie im Aktivitätsbereich **Dimensionen anzeigen**, um ein Dialogfeld zu öffnen, in dem Sie die einzubeziehenden Dimensionen auswählen können. |

### <a name="related-information-about-backorders"></a>Verwandte Informationen über Rückstände

Um weitere Informationen über Rückstände anzuzeigen, wählen Sie die Registerkarte **Zugehörige Informationen** auf der rechten Seite und dann **Rückstände**. Um noch mehr Informationen über einen bestimmten Rückstand anzuzeigen, wählen Sie die entsprechende Zeile und dann den Link **Mehr**.

## <a name="individual-shipping-container-tracking"></a>Nachverfolgung von einzelnen Versandcontainern

Die Abfrage **Einzelne Transportcontainer-Verfolgung** bietet einen Filter, mit dem Sie einen Transportcontainer finden und dann alle Fahrten in diesem Container identifizieren können.

Um diese Abfrage zu öffnen, gehen Sie auf **Gesamttransportkosten \> Abfragen \> Tracking \> Einzelne Transportcontainer-Verfolgung**.

## <a name="multiple-shipping-container-tracking"></a>Nachverfolgung mehrerer Versandcontainer

Die Abfrage **Mehrere Transportcontainer verfolgen** bietet einen Filter, mit dem Sie eine Sammlung von Transportcontainern finden und dann alle Fahrten in diesen Containern identifizieren können.

Um diese Abfrage zu öffnen, gehen Sie zu **Gesamttransportkosten \> Abfragen \> Tracking \> Mehrfache Transportcontainer-Verfolgung**.
