---
title: Pläne basierend auf Angeboten und RFQs
description: In diesem Artikel wird beschrieben, wie die Produktprogrammplanung eingerichtet wird, um Angebote und Angebotsanfragen (RFQs) zu berücksichtigen, wenn Planaufträge generiert werden.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690096"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Basierend auf Angeboten und RFQs planen

[!include [banner](../../includes/banner.md)]

Angebote und Angebotsanfragen (RFQs) stellen mögliche oder sogar wahrscheinliche zukünftige Aufträge dar. Daher ist es sinnvoll, sie bei der Hauptplanung zu berücksichtigen, damit zusätzliche Lieferungen auf der Grundlage vorhandener Anfragen und der Wahrscheinlichkeit, dass jedes Angebot zu einem tatsächlichen Auftrag wird, geplant werden können. In diesem Artikel wird beschrieben, wie die Produktprogrammplanung eingerichtet wird, um Angebote und RFQs zu berücksichtigen, wenn Planaufträge generiert werden.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Masterplanung einrichten, um Verkaufsangebote und/oder Anfragen zu berücksichtigen

Gehen Sie wie folgt vor, um die Produktprogrammplanung so einzurichten, dass Verkaufsangebote und/oder Anfragen berücksichtigt werden.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie einen vorhandenen Plan im Listenbereich oder wählen Sie **Neu** im Aktivitätsbereich, um einen neuen zu erstellen.
1. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:

    - **Verkaufsangebote einschließen** – Stellen Sie diese Option auf *Ja* ein, um Verkaufsangebote zu berücksichtigen, wenn der aktuelle Plan ausgeführt wird. Stellen Sie sie auf *Nein* ein, um sie zu ignorieren.
    - **Wahrscheinlichkeit %** – Legen Sie das Mindestmaß an Konfidenz fest, das erforderlich ist, damit ein Angebot in die Hauptplanung aufgenommen wird. Die Hauptplanungsberechnung umfasst alle Angebote, die aus Verkaufschancen erstellt wurden, die diesen Wahrscheinlichkeitsprozentsatz oder höher aufweisen. Um alle Angebote einzubeziehen, einschließlich Angeboten, denen keine Wahrscheinlichkeit oder keine Verkaufschance zugeordnet ist, stellen Sie dieses Feld auf *0* (Null) ein. Weitere Informationen zu Wahrscheinlichkeiten für Angebote finden Sie im nächsten Abschnitt.
    - **Angebotsanforderungen einschließen** – Stellen Sie diese Option auf *Ja* ein, um Angebotsanforderungen zu berücksichtigen, wenn der aktuelle Plan ausgeführt wird. Stellen Sie sie auf *Nein* ein, um sie zu ignorieren. Wenn Sie sich dafür entscheiden, Anfragen zu berücksichtigen, erstellt das System geplante Bestellungen dafür, gibt aber den Lieferanten nicht an, bis die Anfrage gelöst ist. Geplante Einkaufsbestellungen, die für die Angebotsanfragen erstellt werden, können sich auf die Mengen anderer Bestellvorschläge auswirken.

1. Setzen Sie Ihren Masterplan wie gewohnt fort.

## <a name="assign-and-view-probabilities-for-quotations"></a>Wahrscheinlichkeiten für Angebote zuweisen und anzeigen

Wie im vorherigen Abschnitt erwähnt, berücksichtigt ein Masterplan nur Angebote, die den für den Plan definierten Wahrscheinlichkeitsschwellenwert erreichen oder überschreiten (falls ein Schwellenwert definiert ist). Die Wahrscheinlichkeit wird jedoch nicht direkt bei jedem Kurs festgelegt. Stattdessen wird es von der Verkaufschance geerbt, die zum Generieren des Angebots verwendet wurde. Daher wird Angeboten, die direkt auf der Seite **Alle Angebote** erstellt werden, keine Wahrscheinlichkeit zugewiesen oder eine Verkaufschance zugeordnet, und sie werden niemals von der Hauptplanung berücksichtigt (es sei denn, das Feld **Wahrscheinlichkeit %** ist auf *0* \[Null\] eingestellt). Um ihr eine Wahrscheinlichkeit zuordnen zu können, muss aus einer Verkaufschance ein Angebot generiert werden.

### <a name="create-a-quotation-from-an-opportunity"></a>Angebot aus einer Verkaufschance erstellen

Verwenden Sie das folgende Verfahren, um einer Verkaufschance eine Wahrscheinlichkeit zuzuweisen und dann ein Angebot aus dieser Verkaufschance zu erstellen.

1. Gehen Sie zu **Vertrieb und Marketing \> Beziehungen \> Verkaufschancen \> Alle Verkaufschancen**.
1. Wählen Sie eine bestehende Verkaufschance oder wählen Sie **Neu** im Aktionsbereich, um eine neue zu erstellen.
1. Füllen Sie die Verkaufschancenseite aus, um die Verkaufschance nach Ihren Wünschen zu identifizieren. Achten Sie darauf, das Feld **Wahrscheinlichkeit** auf einen geeigneten Wert einzustellen. Nur Masterpläne, die so eingerichtet sind, dass sie nach Wahrscheinlichkeiten dieses Werts oder höher suchen, berücksichtigen Angebote, die aus dieser Gelegenheit generiert werden.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Verkaufschance**, wählen Sie in der **Neu** Gruppe die Option **Verkaufsangebot** oder **Projektangebot**, abhängig von der Art des Angebots, das Sie erstellen möchten.
1. Legen Sie im Dialogfeld **Angebot erstellen** die Felder anch Bedarf fest, und wählen Sie dann **OK**.
1. Ein neues Angebot wird erstellt und geöffnet. Verwenden Sie im Inforegister **Positionen** die Symbolleiste, um Verkaufszeilen oder Projektzeilen nach Bedarf hinzuzufügen, um den Inhalt des Angebots zu definieren.
1. Wählen Sie im Aktionsbereich **Speichern** aus. Schließen Sie nun das Angebot.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Zeigen Sie die Wahrscheinlichkeit an, die einem Angebot zugeordnet ist

Die einzige Möglichkeit, die einem Angebot zugewiesene Wahrscheinlichkeit anzuzeigen, besteht darin, die Opportunity zu öffnen, die zum Erstellen dieses Angebots verwendet wurde, wie im folgenden Verfahren beschrieben.

1. Gehen Sie zu **Vertrieb und Marketing \> Verkaufsangebote \> Alle Angebote**.
1. Wenn die **Verkaufschancen-ID** Spalte nicht angezeigt wird (sie ist in einer Standardinstallation ausgeblendet), befolgen Sie diese Schritte, um sie vorübergehend anzuzeigen. (Alternativ, um die **Verkaufschancen-ID** Spalte verfügbar zu halten, erstellen Sie eine [gespeicherte Ansicht](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json), die sie einschließt.)

    1. Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) im Raster und wählen Sie dann **Spalten einfügen**.
    1. Im Dialogfeld **Spalten einfügen** finden Sie die Zeile, in der das Feld **Feld** auf *Verkaufschance* eingestellt ist, und wählen Sie das Kontrollkästchen **Auswählen** für diese Zeile aus.
    1. Wählen Sie **Aktualisieren**, um die ausgewählte Spalte zur Seite **Alle Angebote** hinzuzufügen.

1. Suchen Sie im Raster die Zeile für das entsprechende Zitat. Wählen Sie dann in der Spalte **Verkaufschancen-ID** den Wert für diese Zeile aus.

    > [!NOTE]
    > Wenn Sie nach einem Projektangebot suchen, müssen Sie möglicherweise die Spaltenüberschrift **Angebotstyp** auwählen und den Filter löschen. In einer Standardinstallation ist dieser Filter so eingestellt, dass nur Verkaufsangebote angezeigt werden.

1. Die zugehörige Verkaufschance wird geöffnet. Sie können den Wert **Wahrscheinlichkeit** jetzt anzeigen und bearbeiten, wie Sie benötigen.
