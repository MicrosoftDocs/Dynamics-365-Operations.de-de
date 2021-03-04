---
title: Übersicht über den Zustand des Produktlebenszyklus
description: Ein Produktlebenszyklusstatus dokumentiert den Lebenszyklusstatus eines freigegebenen Produkts oder Produktvariante.
author: cvocph
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 51a6b19e84f368bf72b664e120f262ddcf7c7611
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4429162"
---
# <a name="product-lifecycle-state-overview"></a>Übersicht über den Zustand des Produktlebenszyklus

[!include [banner](../includes/banner.md)]

Ein Produktlebenszyklusstatus dokumentiert den Lebenszyklusstatus eines freigegebenen Produkts oder Produktvariante. Produktlebenszyklusstatus werden vom Benutzer, in der Regel ein Produktmanager oder ein Produktmasterdatenmanager, definiert. Bestimmte Geschäftsprozesse, wie Produktprogrammplan, können von einem bestimmten Lebenszyklusstatus betroffen sein.

Ein freigegebenes Produkt oder Produktvariante können einem Produktlebenszyklusstatus zugeordnet werden, der dokumentiert, in welchem Lebenszyklusstatus sich ein bestimmtes Produkt oder eine bestimmte Variante gerade befindet. Sie können eine beliebige Anzahl von Produktlebenszyklusstatus definieren, indem Sie einen Statusname und eine Beschreibung zuweisen. Sie können einen Lebenszyklusstatus als Standardstatus für neu freigegebene Produkte auswählen. Freigegebene Produktvarianten erben ihren Produktlebenszyklusstatus von ihrem freigegebenen Produktmaster bei der Erstellung. Wenn Sie den Lebenszyklusstatus bei einem freigegebenen Produktmaster ändern, können Sie wählen, dass alle vorhandenen Varianten aktualisiert werden, die denselben ursprünglichen Status haben.  

## <a name="create-a-new-product-lifecycle-state"></a>Neuen Status für Produktlebenszyklus erstellen

- Um einen neuen Status für den Produktlebenszyklus zu erstellen, siehe [Erstellen eines neuen Status für den Produktlebenszyklus](tasks/new-product-lifecycle-state.md).

- Um einen Standard-Produktlebenszyklusstatus zu erstellen, siehe [Erstellen eines Standard-Produktlebenszyklusstatus](tasks/default-product-lifecycle-state.md).

## <a name="associate-product-lifecycle-states-to-released-products"></a>Produktlebensyklusstatus freigegebenen Produkten zuordnen  

Es gibt mehrere Möglichkeiten, einen Produktlebenszyklusstatus freigegebenen Produkten oder Produktvarianten zuzuordnen.

- Bei Erstellung eines neuen freigegebenen Produkts wird der standardmäßige **Produktlebenszyklusstatus** automatisch zugewiesen.
- Bei Freigabe eines Produkts für eine juristische Person wird der standardmäßige **Produktlebenszyklusstatus** automatisch zugewiesen.
- Bei Freigabe einer Produktvariante für eine juristische Person wird der **Produktlebenszyklusstatus**, der dem freigegebenen Produktmaster in dieser juristischen Person zugeordnet ist, automatisch der neuen Variante zugewiesen.

Sie können den Produktlebenszyklusstatus manuell aktualisieren mithilfe von:

- Die Listenseite **Freigegebene Produkte** oder **Detailansicht**.
- Die Listenseite **Freigegebene Produktvarianten** oder **Detailansicht**.
- Suchen Sie die veralteten Produkte oder Produktvarianten auf Grundlage von Bedarf und ordnen Sie einen Lebenszyklusstatus zu.  

Für weitere Informationen:

- Um einen Produktlebenszyklus-Status einem freigegebenen Produktmaster zuzuordnen, siehe [Zuordnen eines Produktlebenszyklus-Status zu einem freigegebenen Produktmaster](tasks/product-lifecycle-state-released-product-master.md).

- Um einen Produktlebenszyklus-Status einem freigegebenen Produkt zuzuordnen, siehe [Zuordnen eines Produktlebenszyklus-Status zu einem freigegebenen Produkt](tasks/product-lifecycle-state-released-product.md).

## <a name="impact-on-master-planning"></a>Auswirkung auf Produktprogrammplan

Der Produktlebenszyklusstatus hat nur ein Steuerungskennzeichen: **Ist aktiv für die Planung**. Standardmäßig ist dieses auf **Ja** für alle erstellten Produktlebenszyklusstatus festgelegt, doch es kann zu **Nein** geändert werden. Wenn es auf **Nein** festgelegt ist, sind die zugeordneten freigegebenen Produkte oder freigegebenen Produktvarianten Folgende:

- Ausgeschlossen aus dem Produktprogrammplan.
- Ausgeschlossen aus der Stücklistenebeneberechnung.

Ausführliche Informationen darüber, wie Sie den Status „Produktlebenszyklus“ verwenden, um Produkte von der Produktprogrammplanung und der Berechnung auf Stücklistenebene auszuschließen, finden Sie unter [Erstellen Sie einen Status „Produktlebenszyklus“, um Produkte von der Produktprogrammplanung auszuschließen](tasks/exclude-products-master-planning.md)

> [!NOTE]
> Aus Leistungsgründen wird dringend empfohlen, alle veralteten freigegebenen Produkte oder Produktvarianten zuzuordnen, insbesondere wenn Sie mit nicht wiederverwendbaren Produktkonfigurationsvarianten arbeiten, mit einem Produktlebensyklusstatus, der für den Produktprogrammplan deaktiviert ist.  

## <a name="default-migration-import-and-export"></a>Standardmäßige Migration, Import und Export

Die Produktlebenszyklusstatus werden durch Datenentitäten unterstützt, und der Lebenszyklusstatus kann nicht auf einen variables Status durch die freigegebenen Produktdatenentitäten oder der freigegebenen Variantendatenentität festgelegt werden.

## <a name="find-obsolete-products-and-products-variants"></a>Veraltete Produkte und Produktvarianten suchen

Sie können eine Simulationsanalyse ausführen, um veraltete freigegebene Produkte oder Produktvarianten zu finden, und dann ihren Produktlebenszyklusstatus aktualisieren. Wie Sie veraltete Produkte finden, finden Sie unter [Veraltete Produktvarianten finden und einen Produktlebenszyklusstatus zuweisen](tasks/obsolete-product-variants.md). Dieses Thema zeigt, wie Sie veraltete, freigegebene Produkte oder Produktvarianten finden und den veralteten Produkten einen Produktlebenszyklusstatus zuweisen können. Er zeigt auch, wie Simulationsergebnisse angezeigt werden und wie beurteilt wird, wie viele Produkte und Produktvarianten einem neuen Produktlebenszyklusstatus zugeordnet werden, wenn das Update ohne Simulation ausgeführt wird.  

Indem Sie die Analyse in einem Simulationsmodus ausführen, werden die Produkte und Produktvarianten, die als veraltet identifiziert werden, in einem spezifischen Formular angezeigt, in dem sie einfach überprüft werden können. Durch die Analyse wird nach Transaktionen und spezifischen Masterdaten gesucht, um Produkte zu identifizieren, für die es keinen Bedarf innerhalb einer variablen Periode gibt und keine Masterdaten, die in einem Bedarf resultieren können. Neue freigegebene Produkte innerhalb einer variablen Periode können aus der Analyse ausgeschlossen werden. Wenn die Analysesimulation das erwartete Ergebnis zurückgibt, kann der Benutzer die Analyse ausführen und einen neuen Produktlebenszyklusstatus für alle Produkte festlegen, die durch die Analyse als veraltet identifiziert wurden.  

> [!NOTE]
> Beachten Sie, dass sämtliche Analysen und Updates innerhalb derselben juristischen Person erfolgen müssen.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Kriterien zum Auswählen und Aktualisieren freigegebener Produkte oder Produktvarianten

Verwenden Sie die folgenden Kriterien, um die freigegebenen Produkte und Produktvarianten auszuwählen und zu aktualisieren:

- Der Produktlebenszyklusstatus des Produkts oder der Produktvariante muss sich vom neuen erwünschten Status unterscheiden.
- Das Produkt oder die Produktvariante wurde vor mehreren Tagen erstellt, basierend auf der Anzahl von Tagen, die Sie im Auswahldialogfeld eingeben.
- Es gibt keine offenen Produktionsaufträge (= Status < beendet) für das Produkt oder die Produktvariante.
- Es gibt keine offenen Lagerbuchungen (= Statusabgang „ReservPhysical” zu „QuotationIssue” oder Statuszugang „Registered” zu „QuotationReceipt”) für das Produkt oder die Produktvariante.
- Es gibt keine Lagerbuchungen innerhalb der letzten Anzahl von Tagen für das Produkt oder die Produktvariante.
- Es gibt keinen zukünftigen Bedarf oder Beschaffungsplanung für das Produkt oder die Produktvariante.  
- Kein Minimaler Lagerbestand wurde in der Artikeldeckung für das Produkt oder die Produktvariante festgelegt.
- Keine aktive Kanbanregel für feste Menge für das Produkt oder die Produktvariante.  
- Keine Serviceauftragsposition für das Produkt oder die Produktvariante.
- Keine aktiven oder zukünftigen Kaufvertrags- oder Bestellpositionen für das Produkt oder die Produktvariante.
- Das Produkt oder die Produktvariante wird nicht in einer Stückliste verwendet, die einer nicht abgelaufenen, genehmigten Stücklistenversion für ein Produkt oder eine Variante zugeordnet ist, das/die für die Planung aktiv ist.

## <a name="related-topics"></a>Verwandte Themen

- [Neuen Status für Produktlebenszyklus erstellen](tasks/new-product-lifecycle-state.md)
- [Status für Standardproduktlebenszyklus erstellen](tasks/default-product-lifecycle-state.md)
- [Einem veröffentlichten Produktmaster einen Produktlebenszyklus-Status zuweisen](tasks/product-lifecycle-state-released-product-master.md)
- [Einem veröffentlichten Produkt einen Produktlebenszyklus-Status zuweisen](tasks/product-lifecycle-state-released-product.md)
- [Finden Sie veraltete Produktvarianten und weisen Sie einen Produktlebenszyklusstatus zu](tasks/obsolete-product-variants.md)
- [Ein Produktlebenszyklusstatus erstellen, um Produkte vom Produktprogrammplan auszuschließen](tasks/exclude-products-master-planning.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]