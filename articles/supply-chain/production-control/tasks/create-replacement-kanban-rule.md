---
title: Ersatz-Kanban-Regel erstellen
description: Diese Prozedur konzentriert sich auf das Ersetzen einer vorhandenen Kanban-Regel durch eine neue Kanban-Regel an einem bestimmten Datum.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2db44c1b43a6dc5e0ab37a7756c4eecaab468e15
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570056"
---
# <a name="create-a-replacement-kanban-rule"></a>Ersatz-Kanban-Regel erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur konzentriert sich auf das Ersetzen einer vorhandenen Kanban-Regel durch eine neue Kanban-Regel an einem bestimmten Datum. Dies ist hilfreich, wenn Änderungen im Produktionsfluss oder bei den Auffüllungsregeln koordiniert und geplant werden müssen. Das Demodatenunternehmen in der Prozedur ist USMF. Diese Prozedur ist für den Fertigungsplaner oder den Wertstrommanager vorgesehen, wenn dieser die Produktion für einen geänderten Produktionsfluss oder eine neue Auffüllungsregel vorbereitet. Diese Aufgabe ersetzt Kanban-Regel 000022 durch eine neue Regel und erhöht die Höchstmenge von 48 auf 100 für die neue Regel.


## <a name="select-a-kanban-rule-to-replace"></a>Wählen Sie eine Kanban-Regel aus, die ersetzt werden soll.
1. Wechseln Sie zu Kanban-Regeln.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie Kanban-Regel "000022" aus.  

## <a name="create-a-replacement-kanban-rule"></a>Ersatz-Kanban-Regel erstellen
1. Klicken Sie auf "Kanban-Regel ersetzen".
2. Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.
    * Wählen Sie ein Datum in der Zukunft aus, wie in einer Woche ab jetzt. Dies ist das Datum und die Uhrzeit, zu der die neue Kanban-Regel aktiv wird und die alte Kanban-Regel ersetzt.  
    * Wenn die Kanban-Regel den Pfad des Produktionsflusses ändert, kann eine andere Aktivität ausgewählt werden.  In dieser Prozedur halten wir die Aktivität nicht betroffen.  
3. Klicken Sie auf "OK".
    * Beachten Sie, dass eine neue Kanban-Regel erstellt wird, um Kanban-Regel 000022 zu ersetzen.  
    * Das Gültigkeitsdatum wird gemäß dem ausgewählten Datum festgelegt, wenn Sie die Kanban-Regel ersetzen.  
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die ersetzte Kanban-Regel "000022" aus.  
    * Beachten Sie, dass die ersetzte Kanban-Regel dasselbe Datum wie das "Ablaufdatum" hat, da dies das Datum ist, an dem sie abläuft.  
5. Wählen Sie in der Liste die Zeile "1" aus.
    * Wählen Sie die neue Kanban-Regel über der Liste aus. Dies ist die Kanban-Regel mit der höchsten Kanban-Regel-Nummer.  
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Klicken Sie auf die Kanban-Regel-Nummer, um die Kanban-Regel zu öffnen.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Ändern Sie "Höchstmenge" für die Ersatz-Kanban-Regel
1. Legen Sie "Höchstmenge" auf "100" fest.
    * Erweitern Sie das Inforegister "Mengen", um das Feld "Höchstmenge" anzuzeigen. Das Ändern der Höchstmenge auf 100 ermöglicht es, dass bis zu 100 Kanbans verarbeitet werden können.    Dies ist der letzte Schritt in dieser Aufgabe.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]