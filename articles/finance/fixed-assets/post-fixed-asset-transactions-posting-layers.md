---
title: Buchen von Anlagenbuchungen auf Buchungsebenen
description: Dieser Artikel gibt eine Übersicht über das Buchen von Ebenenfunktionen für Anlagenbuchungen.
author: moaamer
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6361a3bef58bcc06ff01d0aada9ba309f283a83
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722351"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Buchen von Anlagenbuchungen auf Buchungsebenen

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt eine Übersicht über das Buchen von Ebenenfunktionen für Anlagenbuchungen.

Eine Anlage wird für unterschiedliche Zwecke häufig mit unterschiedlichen Methoden abgeschrieben. Die Abschreibung zu steuerlichen Zwecken wird anhand der aktuellen Steuerregeln berechnet, um die höchstmögliche Abschreibung vor Steuern zu erreichen, wohingegen die Abschreibung zu Berichtszwecken entsprechend den Buchhaltungsgesetzen und -standards berechnet wird. Die unterschiedlichen Abschreibungsarten werden auf den Buchungsebenen separat berechnet und aufgezeichnet.

Jedes Buch, das einer Anlage zugeordnet ist, wird für eine bestimmte Buchungsebene eingerichtet, die ein übergeordnetes Abschreibungsziel aufweist. Es gibt zehn Buchungsebenen: Aktuelle, Vorgänge, Steuern und sieben benutzerdefinierte Ebenen. Sie können Buchungen im Hauptbuch für das Buch deaktivieren, indem Sie das Feld Ins Hauptbuch buchen auf Nein festlegen. Das Feld Buchungsebene wird dann automatisch auf Keine gesetzt. Bücher, die nicht im Hauptbuch buchen, werden in der Regel für die Steuererklärung verwendet. Dies bietet zusätzliche Flexibilität zur Löschung von historischen Buchungen für das Anlagenbuch, da sie nicht im Hauptbuch eingerichtet wurden.

Anlagenerfassungen definieren sich durch die Nutzung der Seite  Journalnamen unter Hauptbuch > Journaleinrichtung > Journalnamen. Jede Erfassung, in der Sie Abschreibungen buchen können, wird anhand des Erfassungsnamens (Journal) für eine einzelne Buchungsebene definiert. Die Buchungsebene kann im Journal nicht geändert werden. Diese Einschränkung hilft sicherzustellen, dass Buchungen für die einzelnen Buchungsebenen getrennt gehalten werden. Für jede Buchungsebene muss mindestens ein Journal angelegt werden. Auf wenn Sie Bücher verwenden, die nicht auf das Sachkonto buchen, müssen Sie ein Journal erstellen, bei dem die Buchungsebene auf Kein festgelegt wird.

Sie können Sachkonten für Anlagenbuchungen auf der Seite Anlagenbuchungsprofile festlegen. Sie müssen für jedes Buchungsprofil die relevante Buchungsart und das Buch auswählen und können dann die Sachkonten angeben. Einrichten eines Buchungsprofildatensatz für jedes Buch, das im Hauptbuch gebucht wird.

Die Anlage kann in Dokumente eingetragen werden, die nur die **Aktuell**-Buchungsebene unterstützen, z. B. **Bestellung**, **Ausstehende Kreditorenrechnung**, **Auftrag** oder **Freitextrechnung**. Bei der Auswahl einer Anlagen-ID in einem dieser Dokumente wird das Anlagenbuch in das Buch mit der **Aktuell**-Buchungsebene gefiltert und während der Buchung automatisch ausgefüllt, wenn das System überprüft, ob die Buchungsebene für Anlagen handelt **Aktuell** ist. Wenn diese Validierung nicht abgeschlossen werden kann, wird der Buchungsvorgang gestoppt. 

> [!NOTE] 
> Bei Verwendung von abgeleiteten Büchern können Buchungen gleichzeitig auf unterschiedlichen Buchungsebenen durchgeführt werden. Die Transaktionen dieses primären Buchs werden in einer Erfassung oder einem Quelldokument erstellt, in dem die Buchungsebene der Buchungsebene des Buchs entspricht. Beim Buchen werden die Buchungen der abgeleiteten Buchtransaktionen dann auf den entsprechenden Buchungsebenen gebucht. 


Weitere Informationen finden Sie unter [Abgeleitete Bücher](derived-books.md) und [Post mit abgeleiteten Büchern](post-derived-value-models.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
