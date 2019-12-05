---
title: Buchen von Anlagenbuchungen auf Buchungsebenen
description: Dieser Artikel gibt eine Übersicht über das Buchen von Ebenenfunktionen für Anlagenbuchungen.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc8c4f4f41ed39447ae441dd8e01cfcf80c939b5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770711"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Buchen von Anlagenbuchungen auf Buchungsebenen

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt eine Übersicht über das Buchen von Ebenenfunktionen für Anlagenbuchungen.

Eine Anlage wird für unterschiedliche Zwecke häufig mit unterschiedlichen Methoden abgeschrieben. Die Abschreibung zu steuerlichen Zwecken wird anhand der aktuellen Steuerregeln berechnet, um die höchstmögliche Abschreibung vor Steuern zu erreichen, wohingegen die Abschreibung zu Berichtszwecken entsprechend den Buchhaltungsgesetzen und -standards berechnet wird. Die unterschiedlichen Abschreibungsarten werden auf den Buchungsebenen separat berechnet und aufgezeichnet.

Jedes Buch, das einer Anlage zugeordnet ist, wird für eine bestimmte Buchungsebene eingerichtet, die ein übergeordnetes Abschreibungsziel aufweist. Es gibt zehn Buchungsebenen: Aktuelle, Vorgänge, Steuern und sieben benutzerdefinierte Ebenen. Sie können Buchungen im Hauptbuch für das Buch deaktivieren, indem Sie das Feld Ins Hauptbuch buchen auf Nein festlegen. Das Feld Buchungsebene wird dann automatisch auf Keine gesetzt. Bücher, die nicht im Hauptbuch buchen, werden in der Regel für die Steuererklärung verwendet. Dies bietet zusätzliche Flexibilität zur Löschung von historischen Buchungen für das Anlagenbuch, da sie nicht im Hauptbuch eingerichtet wurden.

Anlagenerfassungen definieren sich durch die Nutzung der Seite  Journalnamen unter Hauptbuch > Journaleinrichtung > Journalnamen. Jede Erfassung, in der Sie Abschreibungen buchen können, wird anhand des Erfassungsnamens (Journal) für eine einzelne Buchungsebene definiert. Die Buchungsebene kann im Journal nicht geändert werden. Diese Einschränkung hilft sicherzustellen, dass Buchungen für die einzelnen Buchungsebenen getrennt gehalten werden. Für jede Buchungsebene muss mindestens ein Journal angelegt werden. Auf wenn Sie Bücher verwenden, die nicht auf das Sachkonto buchen, müssen Sie ein Journal erstellen, bei dem die Buchungsebene auf Kein festgelegt wird.

Sie können Sachkonten für Anlagenbuchungen auf der Seite Anlagenbuchungsprofile festlegen. Sie müssen für jedes Buchungsprofil die relevante Buchungsart und das Buch auswählen und können dann die Sachkonten angeben. Einrichten eines Buchungsprofildatensatz für jedes Buch, das im Hauptbuch gebucht wird.

> [!NOTE] 
> Bei Verwendung von abgeleiteten Büchern können Buchungen gleichzeitig auf unterschiedlichen Buchungsebenen durchgeführt werden. Sie erstellen die Buchungen des primären Buchs in einem Journal mit der Buchungsebene, die der Buchungsebene des Wertmodells entspricht. Beim Buchen werden die Buchungen der abgeleiteten Buchtransaktionen dann auf den entsprechenden Buchungsebenen gebucht.

Weitere Informationen finden Sie unter [Abgeleitete Bücher](derived-books.md) und [Post mit abgeleiteten Büchern](post-derived-value-models.md).



