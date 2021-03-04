---
title: Schlanker Bedarfsverursacher aus Aufträgen
description: Ziel dieser Prozedur ist die Prüfung der Bedarfsverursacherstruktur von einer Verkaufsposition, in der der Artikel mit Kanbans produziert wird.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e429fef6101f611d7a2c1b5323d6fe1e39d1cdd3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428670"
---
# <a name="lean-pegging-from-sales-orders"></a>Schlanker Bedarfsverursacher aus Aufträgen

[!include [banner](../../includes/banner.md)]

Ziel dieser Prozedur ist die Prüfung der Bedarfsverursacherstruktur von einer Verkaufsposition, in der der Artikel mit Kanbans produziert wird. Nach Überrpüfung der Bedarfsverursacherstruktur geprüft, werden alle Kanban-Einzelvorgänge geplant. Dies ist für Auftragsszenarien hilfreich, in denen die Auftragsannahme sicherstellen muss, dass Produktion unverzüglich beginnen kann. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Vorgehensweise ist für die erweiterte Auftragsannahme kleiner Unternehmen vorgesehen.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Erstellen Sie einen Auftrag für einen Kanban gesteuerten Artikel
1. Wechseln Sie zu "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
    * US-001 verwenden.  
4. Klicken Sie auf "OK".
5. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "L0001" ein.
6. Legen Sie die Menge auf "30" fest.
    * Es ist wichtig, dass die Menge höher als 24 ist, um die Ereignis-Kanban-Regel auszulösen.  

## <a name="open-a-pegging-tree"></a>Öffnen Sie den Bedarfsverursacherstruktur - Überblick 
1. Klicken Sie auf "Produkt und Beschaffung".
2. Klicken Sie auf "Bedarfsverursacherstruktur anzeigen".
    * Beachten Sie, dass die Bedarfsverursacherstruktur alle Projektebenen des Bedarfsverursachers anzeigt, die für die Auftragsposition erforderlich ist. In diesem Fall gibt es zwei Ebenen von Kanbans und allen erforderlichen Komponenten.  

## <a name="plan-the-pegging-tree"></a>Bedarfsverursacherstruktur planen
1. Wählen Sie in der Struktur "Verkaufsposition 000832 \ Kanban 000558 "aus.
2. Erweitern Sie den Abschnitt "Kanban-Einzelvorgang".
    * Beachten Sie, dass der Einzelvorgangsstatus für den Kanban-Einzelvorgang nicht geplant wird.  
3. Klicken Sie "Gesamte bedarfsverursachende Struktur planen".
    * Dieses plant alle Kanban-Einzelvorgänge in der Bedarfsverursacherstruktur und ändert den Einzelvorgangsstatus "Nicht geplant" nach "Geplant".  
4. Aktualisieren Sie die Seite.
    * Beachten Sie, dass sich der Kanban-Einzelvorgangsstatus von "Nicht geplant" nach "Geplant" geändert hat.  
5. Wählen Sie in der Struktur "Verkaufsposition Kanban 000832 \ 000558 \ Problem für L0001 \ Kanban 000559 ".
    * Der Einzelvorgang für den zweiten Kanban wird auch geplant, da die gesamte Bedarfsverursacherstruktur geplant wird. Beachten Sie, dass sich der Kanban-Einzelvorgangsstatus von "Nicht geplant" nach "Geplant" geändert hat.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]