---
title: Wellenverarbeitung konfigurieren – Beispiel
description: Dieses Thema enthält ein Beispiel für die Einrichtung der Kriterien, die bestimmen, welche Arbeit für einen Lagerort generiert wird, wenn eine Welle verarbeitet wird, und ob Wellen manuell oder automatisch verarbeitet werden.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10277c22f5988797dd55a33ef5151d2bc7a4b0be
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831049"
---
# <a name="configure-wave-processing-example"></a>Wellenverarbeitung konfigurieren – Beispiel

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält ein Beispiel für die Einrichtung der Kriterien, die bestimmen, welche Arbeit für einen Lagerort generiert wird, wenn eine Welle verarbeitet wird, und ob Wellen manuell oder automatisch verarbeitet werden. Sie geben die Kriterien an, indem Sie Wellenvorlagen und Abfragen einrichten, die mit einer Welle mit freigegebenen Positionen in Aufträgen, Produktionsaufträgen oder in Kanban-Aufträgen übereinstimmen.

## <a name="enable-sample-data"></a>Beispieldaten aktivieren

Um dieses Szenario mithilfe der hier angegebenen Beispieldatensätze und -werte zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen Demodaten installiert sind. Sie müssen auch die **USMF** juristische Person auswählen, bevor Sie beginnen.

## <a name="example-scenario-configure-wave-processing"></a>Beispielszenario: Wellenverarbeitung konfigurieren

In diesem Beispielszenario werden viele der verschiedenen Einstellungen beschrieben, die sich darauf auswirken, wie Wellen erstellt, ausgefüllt, verarbeitet und freigegeben werden.

1. Wechseln Sie im Navigationsbereich zu **Module > Lagerortverwaltung > Einstellungen > Wellen > Wellenvorlagen**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Wellenvorlagenname** einen Wert ein. Wenn Sie eine Wellenvorlage einrichten, geben Sie die Reihenfolge an, in der die Vorlagen mit freigegebenen Positionen in Aufträgen, Produktionsaufträge oder Kanbans abgeglichen werden. Wenn eine Position für einen Lagerort oder für die Produktion freigegeben wird, verwendet sie die erste Wellenvorlage, für die sie die Kriterien erfüllt. Es wird empfohlen, dass Sie die Vorlagen mit den spezifischsten Kriterien an den Anfang der Liste platzieren. Je breiter die Kriterien, desto wahrscheinlicher ist es, dass eine Position die Kriterien erfüllt, und dass könnte dazu führen, dass Positionen der falschen Welle zugewiesen werden.  
1. Geben Sie im Feld **Wellenvorlagenbeschreibung** einen Wert ein.
1. Geben Sie im Feld **Standort** einen Wert ein, oder wählen Sie einen Wert aus. Wenn Sie USMF verwenden, können Sie „Standort 2“ auswählen.  
1. Geben Sie im Feld **Lagerort** einen Wert ein, oder wählen Sie einen Wert aus. Wenn Sie USMF verwenden, können Sie Lagerort 24 auswählen.  
1. Legen Sie das Feld **Wellenerstellung automatisieren** auf **Ja** fest. Aktivieren Sie diese Option, um eine Welle automatisch zu erstellen, wenn ein Auftrag, ein Produktionsauftrag oder ein Kanban für den Lagerort freigegeben wird.  
1. Legen Sie die Option **Welle bei Freigabe für Lagerort verarbeiten** auf **Ja** fest. Aktivieren Sie diese Option, um die Welle automatisch zu verarbeiten und Arbeit zu erstellen, wenn eine Position an den Lagerort freigegeben wird.  
1. Legen Sie die Option **Wellenfreigabe automatisieren** auf **Ja** fest. Aktivieren Sie diese Option, um die Welle automatisch freizugeben. Die Entnahmearbeit wird auf mobilen Geräten erstellt und bereitgestellt.  
1. Legen Sie die Option **Offenen Wellen zuweisen** auf **Ja** fest. Positionen werden Wellen basierend auf den Abfragefilter für die Wellenvorlage zugewiesen.  
1. Legen Sie die Option **Welle bei Schwelle automatisch verarbeiten** auf **Ja** fest. Aktivieren Sie diese Option, um die Welle automatisch zu verarbeiten, wenn die Werte die Schwellenwerte für Gewicht, Lieferung und die Positionen erreichen, die in der Feldgruppe **Wellenschwellenwerte** angegeben sind. Diese Option steht nur zur Verfügung, wenn im Feld **Wellenvorlagentyp** das Feld **Versand** ausgewählt wurde.  
1. Legen Sie die Option **Auffüllungsarbeitsfreigabe automatisieren** auf **Ja** fest. Aktivieren Sie diese Option, um bedarfbasierte Wiederbeschaffungsarbeit zu erstellen und diese automatisch freizugeben. Sie müssen die Wiederbeschaffungswellenmethode der Wellenvorlage hinzufügen und eine Wiederbeschaffungsvorlage vom Typ **Wellenbedarf** benutzen.  
1. Verwenden Sie die Einstellungen in der Feldgruppe **Standardwerte**, um Wellenattribute zuzuweisen. Wellenattribute fungieren als Filter, um die Art von Artikeln zu beschränken, die die Welle verwenden können. Sie könnten beispielsweise eine Artikelgruppe angeben.  
1. Erweitern Sie den Abschnitt **Methoden** und legen Sie die Aktionen fest, die von der Wellenvorlage ausgeführt werden. Wellenvorlagenmethoden ermöglichen es Ihnen, die Reihenfolge von den Aktivitäten zu steuern, die jede Welle durchläuft, wenn sie verarbeitet wird. Beispielsweise haben Sie möglicherweise eine Methode für die Wellenauffüllung. Wenn Sie eine Methode hinzufügen, wird diese dann automatisch im geeigneten Speicherort in der Reihenfolge der Schritte aufgeführt. Wenn Sie die Option **Wiederbeschaffungsarbeitsfreigabe automatisieren** auf **Ja** festgelegt haben, müssen Sie die Wiederbeschaffungsmethode hier hinzufügen.  
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite.
1. Wechseln Sie zu **Lagerortverwaltung > Einstellungen > Lagerortverwaltungsparameter**.
1. Erweitern Sie den Abschnitt **Wellenverarbeitung**.
1. Geben Sie im Feld **Wellenverarbeitungs-Stapelverarbeitungsgruppe** einen Wert ein, oder wählen Sie einen Wert aus.
1. Legen Sie die Option **Wellen in einem Stapel verarbeiten** auf **Ja** fest.
1. Geben Sie im Feld **Auf Sperre (ms) warten** eine Zahl ein. Geben Sie die Uhrzeit ein, in Millisekunden, die ein Zuteilungsschritt auf eine Systemressource wartet, die von einem anderen Zuteilungsschritt gesperrt ist. Bei Überschreitung dieser Zeit wird, wird die Welle nicht verarbeitet und eine Fehlermeldung wird angezeigt.  
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite.
1. Wechseln Sie im Navigationsbereich zu **Module > Produktionssteuerung > Einstellungen > Produktionssteuerungsparameter**.
1. Wählen Sie im Feld **Für Lagerort freigeben** eine Option aus.

    Bei Aufträgen und Kanbanaufträgen muss Lagerbestand reserviert werden, bevor der Auftrag an den Lagerort freigegeben wird. Andernfalls können die Artikel oder der Verteilungspositionen nicht in einer Welle verarbeitet werden. Bei Produktionsaufträgen haben Sie auch die Option, **Teilweise Reservierung zulassen** auszuwählen. Beispielsweise ist dies hilfreich, wenn Sie die Materialien haben, die Sie zum Starten der Produktion benötigen, und warten können, bis die zusätzlichen Materialien verfügbar werden, um den Prozess abzuschließen. Wenn Sie diese Option auswählen, müssen Sie den Prozess der Freigabe für den Lagerort manuell wiederholen, wenn die zusätzlichen Materialien verfügbar werden.
1. Schließen Sie die Seite.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Wellenerstellung und -verarbeitung](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
