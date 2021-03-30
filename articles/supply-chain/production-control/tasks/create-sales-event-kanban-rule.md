---
title: Kanban-Regel für ein Verkaufsereignis erstellen
description: Ziel dieser Prozedur ist es, die notwendigen Einstellungen vorzunehmen, um eine Kanban-Regel zu erstellen, die während der Auftragserstellung ausgelöst wird.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e33be986886d31c5275df3e36e2ce632f32c6f0d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228562"
---
# <a name="create-a-sales-event-kanban-rule"></a>Kanban-Regel für ein Verkaufsereignis erstellen

[!include [banner](../../includes/banner.md)]

Ziel dieser Prozedur ist es, die notwendigen Einstellungen vorzunehmen, um eine Kanban-Regel zu erstellen, die während der Auftragserstellung ausgelöst wird. Die Ereignis-Kanban-Regel füllt Anforderungen auf, die von Auftragspositionen stammen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dies ist für den Verfahrenstechniker oder den Wertstrom-Manager vorgesehen, da dieser die Produktion eines neuen oder geänderten Produkts vorbereitet.




## <a name="create-a-new-kanban-rule"></a>Neue Kanban-Regel erstellen
1. Wechseln Sie zu Kanban-Regeln.
2. Klicken Sie auf "Neu".
3. Wählen Sie im Feld "Auffüllungsstrategie" "Ereignis" aus.
    * Die Auswahl "Ereignis" bedeutet, dass die Kanban-Regel durch ein Ereignis, beispielsweise die Erstellung einer Auftragsposition, ausgelöst wird.   Diese Informationen werden in den Bereichen verwendet, bei denen jeder Kanban einen bestimmten Bedarf beinhalten soll.  
4. Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie "Endmontage" aus.  
5. Erweitern Sie den Abschnitt "Details".
6. Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie L0050 aus.  

## <a name="define-an-event"></a>Ereignis definieren
1. Erweitern Sie den Abschnitt "Ereignis".
2. Wählen Sie im Feld "Verkaufsereignis" "Automatisch".
    * Wenn Sie die Verkaufsereignis "Automatisch" auswählt haben, wird diese Kanban-Regel automatisch ausgelöst, wenn eine Verkaufsposition mit dem Produkt- und Zugangslagerplatz übereinstimmt. In diesem Verfahren ist es Produkt L0050 auf Lagerort 13.  
3. Legen Sie die "Mindestmenge für Ereignis" auf '50' fest.
    * Mit einer Mindestereignismenge von 50 wird die Kanban-Regel nur von Ereignissen mit einer Menge von 50 oder mehr ausgelöst.  
4. Erweitern Sie den Abschnitt "Produktionsfluss".
    * Beachten Sie, dass der Zugangslagerplatz Lagerort 13 ist. Das bedeutet, dass diese Kanban-Regel für diesen Lagerplatz ausgelöst wird.  
    * In diesem Beispiel löst eine Verkaufsposition für Produkt L0050, mit einer Menge von 50 oder mehr, auf Lagerort 13, diese Kanban-Regel aus.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Erstellen Sie eine Verkaufsposition, um die Ereignis-Kanban-Regel auszulösen.
1. Wechseln Sie zu "Alle Aufträge".
    * Eine Warnung wird angezeigt, wenn die Kanban-Regel gespeichert wird, was bedeutet, dass Kanbans in Echtzeit während der Auftragserstellung erstellt werden.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie z.B. "US-003" aus.  
4. Klicken Sie auf "OK".
5. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "L0050" ein.
6. Geben Sie im Feld 'Standort' den Wert '1' ein.
    * Wählen Sie Standort 1 aus, da Lagerort 13 auf Standort 1. ist.  
7. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
    * Legen Sie den "Lagerort" auf 13 fest.  
8. Legen Sie die Menge auf "75" fest.
    * Geben Sie eine Menge von 50 oder höher ein, um die erstellte Kanban-Regel auszulösen.  

## <a name="verify-that-kanban-is-created"></a>Überprüfen Sie, ob ein Kanban erstellt wird.
1. Klicken Sie auf "Produkt und Beschaffung".
2. Klicken Sie auf "Bedarfsverursacherstruktur anzeigen".
    * Beachten Sie, dass ein Kanban mit derselben Menge wie die Auftragsposition erstellt wird. Sie können außerdem die Materialabgänge sehen, die erforderlich sind, um L0050 zu erzeugen. Dies ist der letzte Schritt in diesem Verfahren.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]