---
title: Dispositionscodes einrichten
description: Fokusse dieser Prozedur auf den Einstellungen eines Dispositionscodes, der mit einem mobilen Gerät für die Rücklieferung verwendet werden kann, die Prozess erhält.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16458f709788e538d036cc4d3b3239f4ffa3c42e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830928"
---
# <a name="set-up-dispositions-codes"></a>Dispositionscodes einrichten

[!include [banner](../../includes/banner.md)]

Fokusse dieser Prozedur auf den Einstellungen eines Dispositionscodes, der mit einem mobilen Gerät für die Rücklieferung verwendet werden kann, die Prozess erhält. Dispositionscodes sind eine Regelsammlung, die verwendet wird, wenn Artikel eingegangen sind. Wird beispielsweise ein Arbeitsbenutzer ein mobiles Gerät verwendet, um Artikel zu erhalten, die beschädigt wurden, muss der Benutzer einen Dispositionscode für beschädigte Artikel scannen. Der Bestandsstatus der Wareneingänge verschaffen, der Arbeitsvorlage und der Lagerplatzdirektive kann über gescannten Dispositionscode bestimmt werden. Für die Bestellung, die Prozess und den Produktionsauftragsbericht als um Prozess erhält, ist der Verwendung von einem Dispositionscode optional. Für den empfangenden Rückholprozess des Auftrags wenn die Artikel mithilfe eines mobilen Geräts erfasst werden, ist der Verwendung von Dispositionscode erforderlich.  Dieses Handbuch wurde mit dem Demodatenunternehmen USMF erstellt. Diese Prozedur ist für die Lagerverwaltung vorgesehen. 

1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobile Geräte" > "Bereitstellungscodes".
2. Klicken Sie auf "Neu".
    * Erstellen Sie einen neuen Dispositionscode, um für Debitorenrücklieferungen zu verwenden.  
3. Geben Sie im Feld "Bereitstellungscode" einen Wert ein.
4. Wählen Sie im Bestandsstatusgebiet wählen Sie einen Bestandsstatus aus, mit dem er Sperrung von Lagerbestand ausreicht.
    * Wählen Sie bei Verwendung von USMF "Sperrung" aus. Sie können einen Bestandsstatus dem Dispositionscode hinzufügen, um den Standardstatus zu überschreiben, der in den Auftragspositionen lautet.  
5. Geben Sie im Feld "Arbeitsvorlage" einen Wert ein.
    * Optional: Wählen Sie einen Arbeitsvorlagencode aus, der mit einer Rücklieferung zugeordnet ist. Wenn kein Wert angegeben, wird die Arbeitsvorlage mithilfe von Standardregeln aufgelöst, die in Ihrem System entsprechend konfiguriert werden. Eine Arbeitsvorlage ausgewählt, beschränkt die Prozesse ein, die dieser Dispositionscode mit verwendet werden kann. Wird beispielsweise ein Dispositionscode eine Arbeitsvorlage mit einem Arbeitsauftrag der Typ Bestellung hat, kann er nicht verwendet werden, um Artikel zu erfassen, die von Debitoren zurückgegeben werden.  
6. Geben Sie im Feld "Rückgabe Bereitstellungscode" einen Wert ein.
    * Der Rückholdispositionscode bestimmt den Rest des Rücklieferungsprozesses für die erfassten Artikel. In diesem Beispiel sollte der Debitor eine Gutschrift erhalten. Hinzufügen eines Rückgabedispositionscode hinzu, der einen Aktivität Haben enthält.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]