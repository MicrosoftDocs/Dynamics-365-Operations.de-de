---
title: Kanban-Status aktualisieren
description: Wenn ein Kanban versehentlich geleert wird, oder ein empfangener Kanban geleert werden muss, müssen Sie den Kanbanstatus aktualisieren.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a0e03da4671ffec4ecf4835b20a00ef87971c94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831816"
---
# <a name="update-kanban-status"></a>Kanban-Status aktualisieren

[!include [banner](../../includes/banner.md)]

Wenn ein Kanban versehentlich geleert wird, oder ein empfangener Kanban geleert werden muss, müssen Sie den Kanbanstatus aktualisieren. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Prozedur ist für den Filialleiter vorgesehen.


## <a name="find-the-kanban"></a>Suchen Sie den Kanban.
1. Wechseln Sie zu "Produktionssteuerung" > "Kanban" > "Kanbans".
2. Öffnen Sie den Spaltenfilter "Status der Handhabungseinheit".
3. Auf 'Löschen' klicken
    * Dies setzt die Filter zurück.  
4. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise nach dem Feld "Kartennummer" mit dem Wert "000149".

## <a name="change-emptied-status-to-received-status"></a>Ändern Sie den Status "Geleert" zum Status "Eingegangen".
1. Klicken Sie auf "Leere Handhabungseinheit zurücksetzen".
2. Klicken Sie auf "OK".
    * Beachten Sie, dass der "Status der Handhabungseinheit" den Wert "Eingegangen" hat.  

## <a name="change-received-status-to-emptied-status"></a>Ändern Sie den Status "Eingegangen" zum Status "Geleert".
1. Klicken Sie auf "Kanban leeren".
2. Markieren Sie in der Liste die ausgewählte Zeile.
    * Beachten Sie, dass die "Handhabungseinheit" den Status "Geleert" hat.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]