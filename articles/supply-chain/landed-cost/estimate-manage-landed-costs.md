---
title: Gesamttransportkosten kalkulieren und verwalten
description: Das System verwendet Ihre Autokalkulation, um eine Schätzung für Ihre gelandeten Kosten zu ermitteln. Dieses Thema erklärt, wie Sie verschiedene Szenarien definieren können, um eine genauere Schätzung zu erhalten.
author: sherry-zheng
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 174b80adbe61c455983307c6065b75704ce93ce9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021247"
---
# <a name="estimate-and-manage-landed-costs"></a>Gesamttransportkosten kalkulieren und verwalten

[!include [banner](../../includes/banner.md)]

Das System verwendet Ihre [Autokalkulation](auto-cost-setup.md), um eine Schätzung für Ihre gelandeten Kosten zu ermitteln. Zusätzlich können Sie verschiedene Szenarien definieren, um eine genauere Schätzung zu erhalten. Diese Szenarien werden gespeichert. Daher können Sie sie später überprüfen und in einem Bericht mit den Ist-Werten vergleichen. Sie können auch den Preis des Artikels aktualisieren.

## <a name="set-up-cost-estimates"></a>Festlegen von Kalkulationen

### <a name="set-up-cost-templates"></a>Kostenvorlagen einrichten

Kalkulationsvorlagen legen Standardeinstellungen fest, die Benutzer, die die Kalkulation erhalten, nicht unbedingt kennen. Vorlagen können dazu beitragen, die Komplexität im Kalkulationsprozess zu reduzieren, indem sie die Auswahlen minimieren, die Benutzer angeben müssen, um eine genaue Kalkulation zu erhalten. Wenn Sie das Standard-Kostenmodell verwenden, können Sie beim Festlegen der Kosten für Waren Kostenvorlagen verwenden.

Um Ihre Kostenvorlagen festzulegen, gehen Sie zu **Gesamttransportkosten \> Kalkulation einrichten \> Kostenvorlagen**. Auf der Seite **Kostenvorlagen** zeigt der Listenbereich auf der linken Seite alle aktuellen Kalkulationsvorlagen an. Mit den Schaltflächen im Aktivitätsbereich können Sie Vorlagen erstellen, löschen und bearbeiten.

Die folgende Tabelle beschreibt die Felder, die für jede Vorlage verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Kostenvorlage | Geben Sie einen eindeutigen Namen für die Kalkulationsvorlage ein. Der Name beschreibt typischerweise den Faktor oder Kostenmultiplikator für die Vorlage. |
| Beschreibung | Geben Sie eine Beschreibung für die Kalkulationsvorlage ein. |
| Versandunternehmen | Wählen Sie die Firma, die bei Verwendung der Vorlage angewendet werden soll. |
| Lieferart | Wählen Sie die Versandart, z. B. See- oder Luftfracht, die bei Verwendung der Vorlage angewendet werden soll. Dieses Feld hilft bei der Bestimmung der Autokalkulationen, die mit den Waren auf einer Kalkulation verbunden sind. |
| Versandcontainertyp | Wählen Sie den Typ des Transportcontainers, der angewendet werden soll, wenn die Vorlage verwendet wird. Dieses Feld hilft bei der Bestimmung der Autokalkulationen, die mit den Waren auf einer Kalkulation verbunden sind. |
| Zollbroker | Der Zoll Broker (Lieferant), der verwendet werden soll, wenn die Vorlage verwendet wird. Dieses Feld hilft bei der Bestimmung der Autokalkulationen, die mit der Kalkulation verbunden sind. |
| Faktor | Geben Sie den Multiplikator (Prozentsatz) ein, der automatisch auf die Kalkulation angewendet werden soll, wenn die Vorlage verwendet wird. Um z.B. 10 Prozent auf die kalkulierte Kalkulation zu addieren, geben Sie *1,10* ein. |

### <a name="create-a-cost-estimate"></a>Erzeugen einer Kalkulation

Verwenden Sie das Dialogfeld **Kalkulation**, um eine neue Kalkulation zu erstellen, die auf einer ausgewählten Kostenvorlage, einem ausgewählten Satz von Artikeln und anderen Details einer Route basiert. Diese Einstellungen werden dann verwendet, um die geschätzten Gesamttransportkosten der Waren zu ermitteln. Diese Kostenschätzungen werden hauptsächlich für die Arbeit mit Standard-Kalkulationen verwendet. Indem Sie die geschätzten Wareneinstandskosten zu den Standardkosten der Waren im Bestand addieren, sollten Sie kleinere Abweichungstransaktionen erleben, wenn die Waren zu einer Fahrt hinzugefügt werden, da die Standardkosten die Schätzungen dieser Wareneinstandskosten widerspiegeln werden.

Um das Dialogfenster **Kalkulation** zu öffnen, gehen Sie auf **Gesamttransportkosten \> Periodische Aufgaben \> Kalkulation**. Legen Sie dann die Felder fest, die in den folgenden Unterkapiteln beschrieben werden. Wählen Sie schließlich **OK**, um den Kostenvoranschlag zu erstellen. Die Seite **Kostenvoranschlag** (**Gesamttransportkosten \> Abfragen \> Kalkulationen**) erscheint dann und zeigt Ihre neue Kalkulation an, wie später in diesem Thema beschrieben.

### <a name="settings-on-the-parameters-tab"></a>Einstellungen auf der Registerkarte Parameter

Die folgende Tabelle beschreibt die Felder, die auf der Registerkarte **Parameter** des Dialogfelds **Kalkulation** zur Verfügung stehen.


| Feld | Beschreibung |
|---|---|
| Kostenvorlage | Wählen Sie eine Kalkulationsvorlage aus. Die Einstellungen, die mit der gewählten Vorlage verbunden sind, werden verwendet, um die Autokalkulationen festzulegen, die angewendet werden. |
| Vorkalkulationsdatum | Standardmäßig ist dieses Feld auf das heutige Datum festgelegt, aber Sie können den Wert ändern. Das angegebene Datum wird verwendet, um die entsprechenden Verkaufspreise, Kaufpreise, Autokalkulationen und den Wechselkurs, wenn ein Versandkurs verwendet wird, auszuwählen. |
| Verbrauchsberechnung | Die Kalkulation kann von einer Messung abhängen. Wenn z. B. Luftfracht verwendet wird, kann ein volumetrischer Preis gelten. Wenn die Kalkulation von einer Messung abhängt, geben Sie den Wert dieser Messung ein. Andernfalls empfehlen wir, dieses Feld auf *1* festzulegen, es sei denn, Sie sind sicher, dass keine Aufteilung durch die Verwendung von Kennzahlen erfolgt. Geben Sie einen dezimalen Wert ein. Die Einheit ist diejenige, die im entsprechenden Datensatz der Autokalkulation definiert ist. |
| Reisevorlage | Wählen Sie eine [Fahrtvorlage](multi-leg-journey-setup.md). Dieses Feld wird verwendet, um die korrekten Autokalkulationen zu bestimmen, die angewendet werden sollen. |
| Von-Port | Der Hafen, von dem aus die Artikel verschickt werden. Dieses Feld wird basierend auf der gewählten Route-Vorlage festgelegt. |
| Bis-Port | An Hafen, an den die Artikel verschickt werden sollen. Dieses Feld wird basierend auf der gewählten Route-Vorlage festgelegt. |
| Währung | Wählen Sie die Währung, in der die Artikel gekauft werden sollen. |
| Container | Wenn normalerweise mehrere Container verwendet werden, geben Sie die Anzahl der Container an. Das System wird dann bei der Kalkulation die Kosten für mehrere Container verwenden. |
| Folios | Wenn typischerweise mehrere Paletten verwendet werden, geben Sie die Menge an. (Die Menge ist normalerweise *1*.) |
| Standort | Geben Sie den Standort an, an den die Waren geliefert werden sollen. |

### <a name="settings-on-the-items-tab"></a>Einstellungen auf der Registerkarte Artikel

Auf der Registerkarte **Positionen** können Sie dem Kostenvoranschlag so viele Artikel hinzufügen, wie Sie benötigen. Verwenden Sie die Symbolleiste, um dem Raster Artikel hinzuzufügen oder Artikel zu entfernen. Wählen Sie **Bestand \> Dimensionen anzeigen** in der Symbolleiste, um ein Dialogfeld zu öffnen, in dem Sie dem Raster Dimensionsspalten hinzufügen oder Spalten entfernen können.

Die folgende Tabelle beschreibt die Felder, die für jeden Artikel verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Artikelnummer | Wählen Sie den Artikel aus, für den Sie den Preis bestimmen wollen. (Wenn der Artikel noch nicht im System vorhanden ist, erstellen Sie einen Dummy-Artikel, fügen Sie ihn optional einer Kostengruppe für Fahrt-Artikel zu und lassen Sie dann den Preis entweder leer oder erstellen oder ändern Sie ihn). |
| Kreditorenkonto | Wählen Sie den Lieferanten, der für die Schätzung dieses Artikels verwendet werden soll. Wenn dem Artikel ein Standardlieferant zugewiesen ist, wird dieses Feld automatisch festgelegt. |
| Leistung | Wählen Sie die Menge, die Sie kaufen wollen. |
| Einstandspreis | Das System verwendet seine Preisfindungsregeln, um einen Anfangspreis zu finden, aber Sie können diesen Preis bei Bedarf überschreiben. |
| Verkaufspreis | Geben Sie den erwarteten Verkaufspreis der Waren ein. |
| Verbrauchsberechnung | Geben Sie einen Dezimalwert für die Messung der Waren ein. Die Einheit ist diejenige, die für das entsprechende freigegebene Produkt festgelegt ist. |
| Artikelgewicht/-volumen aktualisieren | Aktivieren Sie dieses Kontrollkästchen, um die Gewichts- oder Volumenmessung des freigegebenen Produkts so zu aktualisieren, dass sie mit dem **Maß**-Wert übereinstimmt, der für diese Zeile eingegeben wurde. |
| (Andere Dimensionen) | Abhängig von den Dimensionen, die Sie zur Anzeige ausgewählt haben, sehen Sie möglicherweise zusätzliche Spalten mit Informationen zu jedem Artikel. |

Um die Volumen- und/oder Gewichtsangaben für einen Artikel anzuzeigen oder anzupassen, wählen Sie den Artikel im Raster aus und verwenden dann die Felder am unteren Rand der Seite.

## <a name="manage-estimated-costs"></a>Kalkulationen verwalten

Um die von Ihnen erstellten Kalkulationen anzusehen und zu bearbeiten, gehen Sie zu **Gesamttransportkosten \> Abfragen \> Kostenvoranschläge**. Auf der Seite **Kostenvoranschläge** zeigt der Listenbereich auf der linken Seite alle aktuellen Kalkulationen an. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um mit einem ausgewählten Kostenvoranschlag zu arbeiten. Beachten Sie, dass Sie auf der Seite **Kalkulationen** keine neue Kalkulation erstellen können. Verwenden Sie stattdessen das Dialogfeld **Kostenvoranschlag** (**Gesamttransportkosten \> Periodische Aufgaben \> Kalkulation**), wie weiter oben in diesem Thema beschrieben.

Die Seite **Kostenvoranschlag** zeigt, wie die einzelnen Kalkulationen zustande gekommen sind. Sie zeigt auch die geschätzten Gesamttransportkosten für jeden Artikel an. Sie können eine Kalkulation modifizieren, indem Sie den Selbstkostenpreis und/oder die Währung ändern, die mit den verschiedenen Waren verbunden ist. Sie können auch die zugehörigen Kalkulationen sowohl auf Fahrt- als auch auf Containerebene ändern. Wenn Sie diese Seite zum Ändern der Kosten verwenden, werden Sie aufgefordert, die geschätzten Kosten für die Artikel in der Kalkulation neu zu berechnen. Wenn Sie fertig sind, können Sie die Schätzungen verwenden, um die Selbstkosten der Artikel in der Kalkulation zu aktualisieren.

### <a name="information-on-the-header"></a>Informationen in der Kopfzeile

Der Kopf der Seite **Kalkulationen** zeigt die Einstellungen, mit denen die ausgewählte Kalkulation erzeugt wurde, wie im vorherigen Abschnitt beschrieben. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Einstellungen und Schaltflächen auf dem Inforegister Zeilen

Das Inforegister **Zeilen** listet jeden Artikel auf, der in der aktuellen Kalkulation enthalten ist. Die folgende Tabelle beschreibt die Felder, die für jede Zeile verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Kreditorenkonto | Das Kreditorenkonto, das mit dem Artikel verknüpft ist. |
| Artikelnummer | Die Nummer des Artikels. |
| Leistung | Die Anzahl der Artikel, die zur Ermittlung der Kalkulation verwendet werden. |
| Einstandspreis | Der Selbstkostenpreis gemäß der Handelsvereinbarung. Dieser Wert wird in der lokalen Währung angezeigt. |
| Verbrauchsberechnung | Die individuelle Messung. Die Einheit ist diejenige, die für das jeweilige freigegebene Produkt definiert ist. |
| Vorkalkulierte Gesamttransportkosten | Die geschätzten Gesamttransportkosten für die Gesamtmenge. |
| Pro Einheit | Die geschätzten Gesamttransportkosten geteilt durch die Menge. |
| (Andere Dimensionen) | Abhängig von den Dimensionen, die Sie zur Anzeige ausgewählt haben, sehen Sie möglicherweise zusätzliche Spalten mit Informationen zu jedem Artikel. |

Die folgende Tabelle beschreibt die Schaltflächen, die in der Symbolleiste auf dem Inforegister **Zeilen** verfügbar sind.

| Schaltfläche | Beschreibung |
|---|---|
| Einfügen | Artikel zur Kalkulation hinzufügen. Nachdem Sie Artikel hinzugefügt haben, müssen Sie **Neu berechnen** im Aktivitätsbereich wählen. |
| Entfernen | Artikel aus der Kalkulation entfernen. Nachdem Sie Artikel entfernt haben, müssen Sie **Neu berechnen** im Aktivitätsbereich wählen. |
| Seereisekosten | Öffnen Sie eine Seite, auf der Sie verschiedene Arten von Kalkulationen für den Artikel anzeigen und bearbeiten können. |
| Bestand \> Dimensionen anzeigen | Öffnen Sie ein Dialogfeld, in dem Sie dem Raster Dimensionsspalten hinzufügen oder Spalten entfernen können. |

### <a name="settings-on-the-general-fasttab"></a>Einstellungen auf der Registerkarte Allgemein

Das Inforegister **Allgemein** zeigt Details über den Artikel, der gerade auf dem Inforegister **Zeilen** ausgewählt ist. Viele dieser Informationen werden im Inforegister **Zeilen** wiederholt und können an beiden Stellen bearbeitet werden. Allerdings sind hier auch zusätzliche Details verfügbar. Die Werte der zusätzlichen Felder basieren auf dem Einrichten des jeweiligen freigegebenen Produkts.

### <a name="settings-on-the-dimension-fasttab"></a>Einstellungen auf dem Inforegister Dimension

Das **Dimension** Inforegister zeigt Werte für alle verfügbaren Bestandsdimensionen für den Artikel an, der auf dem **Zeilen** Inforegister ausgewählt ist, unabhängig von den Dimensionen, die Sie dort ausgewählt haben, um sie anzuzeigen. Alle Werte, die hier angezeigt werden, stammen aus der jeweiligen Kalkulationsvorlage. Sie sind in der Kalkulationsvorlage optional.

### <a name="buttons-on-the-action-pane"></a>Schaltflächen im Aktivitätsbereich

Sie können die Schaltflächen im Aktivitätsbereich der Seite **Kalkulationen** verwenden, um mit der ausgewählten Kalkulation zu arbeiten. Die folgende Tabelle beschreibt die zur Verfügung stehenden Schaltflächen.

| Vorgang | Beschreibung |
|---|---|
| Abfrage der Kalkulation | Zeigt alle Kalkulationen für die Fahrt an. Bei Bedarf können Sie die Kalkulationen auf der Ebene des einzelnen Artikels anzeigen. |
| Standardkosten aktualisieren | <p>Aktualisieren Sie die Standardkosten unter Verwendung der Standardversion der Kalkulation, die auf der Seite **Gesamttransportkosten-Parameter** definiert ist. Sie können diese Version außer Kraft setzen.</p><p>**Hinweis:** Wenn ein Artikel mehrere Dimensionen hat (z.B. verschiedene Größen, Farben und Konfigurationen), diese Dimensionen aber nicht für die Kalkulation ausgewählt wurden, erstellt das System für jede Kombination einen ausstehenden Preis.</p><p>**Wichtig:** Die Preisaufschlüsselung wird erstellt und dient zur Bestimmung der Standardkostenabweichung pro Gesamttransportkosten.</p> |
| Seereisekosten | Zeigen Sie die Kalkulationen der Fahrten für alle Waren in der Sendung an und bearbeiten Sie sie. |
| Neu berechnen | Aktualisieren Sie die geschätzten gelandeten Kosten, nachdem Fahrtkosten aktualisiert, hinzugefügt oder entfernt wurden. |
| Sperren | Sperren Sie den Datensatz der Kalkulation, so dass keine Änderungen mehr vorgenommen werden können. |

## <a name="item-cost-price-update"></a>Einstandspreisaktualisierung für Artikel

Die periodische Aufgabe **Artikel-Selbstkostenpreis-Aktualisierung** aktualisiert alle Kalkulationen, die den Filtern entsprechen, die Sie beim Ausführen der Aufgabe festgelegt haben. Der Effekt ist ähnlich wie der Effekt der Auswahl von **Standardkosten aktualisieren** im Aktivitätsbereich für eine einzelne Kalkulation. In diesem Fall gilt die Aktualisierung jedoch für alle passenden Schätzungen.

Um die periodische Aufgabe auszuführen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Gesamttransportkosten \> Periodische Aufgaben \> Artikel Selbstkostenpreis aktualisieren**.
1. Legen Sie im Dialogfeld **Selbstkostenpreis aus Kalkulation aktualisieren** die folgenden Felder nach Bedarf fest, um den Umfang der Aktualisierung zu begrenzen:

    - **Version** - Aktualisieren Sie nur Kalkulationen, die die angegebene Version der Kalkulation verwenden.
    - **Standort** - Aktualisieren Sie nur Kostenvoranschläge, die den angegebenen Standort verwenden.
    - **Kalkulationsvorlage** - Aktualisieren Sie nur Kalkulationen, die die angegebene Vorlage verwenden.
    - **An Hafen** - Aktualisieren Sie nur Schätzungen, die den angegebenen „An Hafen“ verwenden.
    - **Kostenvoranschlag-Datum** - Aktualisieren Sie nur Kostenvoranschläge, die das angegebene Datum haben.

1. Legen Sie die Optionen auf den Inforegistern **Einzuschließende Datensätze** und **Im Hintergrund laufen lassen** wie bei periodischen Aufgaben fest.
1. Wählen Sie **OK**, um die Aufgabe auszuführen.

> [!NOTE]
> Diese periodische Aufgabe wird nur dann erfolgreich ausgeführt, wenn die folgenden Informationen vorhanden sind:
>
> - Für jedes relevante Produkt muss eine **Bruttotiefe**, **Brutto-Breite** und **Brutto-Höhe** definiert sein.
> - Für jeden relevanten Hersteller muss ein **Von Hafen** definiert sein.
