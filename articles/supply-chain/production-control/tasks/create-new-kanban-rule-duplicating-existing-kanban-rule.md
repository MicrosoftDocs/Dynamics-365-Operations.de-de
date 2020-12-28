---
title: Neue Kanban-Regel durch Duplizieren einer vorhandenen Kanban-Regel erstellen
description: Ziel dieser Prozedur ist es, ein Duplikat einer vorhandenen Kanban-Regel zu erstellen.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84a0093d95c2f7084c7a0ed17f8b2f86d654b5d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428423"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a>Neue Kanban-Regel durch Duplizieren einer vorhandenen Kanban-Regel erstellen

[!include [banner](../../includes/banner.md)]

Ziel dieser Prozedur ist es, ein Duplikat einer vorhandenen Kanban-Regel zu erstellen. Dies ist hilfreich, wenn Sie neue Kanban-Regeln basierend auf vorhandenen Kanban-Regeln erstellen möchten. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Vorgehensweise ist für den Verfahrenstechniker oder den Wertstrom-Manager vorgesehen, da dieser die Produktion für einen geänderten Produktionsfluss oder eine neue Auffüllungsregel vorbereitet.


## <a name="select-a-kanban-rule"></a>Kanban-Regel auswählen
1. Wechseln Sie zu Kanban-Regeln.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Kanban-Regel 000017 für Produkt M0006 aus.  

## <a name="duplicate-a-kanban-rule"></a>Kanban-Regel duplizieren
1. Klicken Sie auf das Formular "Kanban-Regel duplizieren"
    * Wird eine Kanban-Regel dupliziert, ist es möglich, Typ, Datum, Aktivitäten und die Produktauswahl zu ändern. Ändern Sie das Produkt für diese Prozedur im nächsten Schritt.  
2. Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie M0007 aus.  
3. Klicken Sie auf "OK".
    * Beachten Sie, dass ein Duplikat von Kanban-Regel 000017 erstellt wird.    

