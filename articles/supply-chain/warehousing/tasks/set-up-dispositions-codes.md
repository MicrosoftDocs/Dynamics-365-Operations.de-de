---
title: Dispositionscodes einrichten
description: Fokusse dieser Prozedur auf den Einstellungen eines Dispositionscodes, der mit einem mobilen Gerät für die Rücklieferung verwendet werden kann, die Prozess erhält.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85402e05d55367da5fe89b242ad8eafc727b441e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "324122"
---
# <a name="set-up-dispositions-codes"></a>Dispositionscodes einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

