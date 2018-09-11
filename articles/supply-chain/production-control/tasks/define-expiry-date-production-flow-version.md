--- 
title: "Ablaufdatum für eine Produktionsflussversion definieren"
description: "Um die Gültigkeitsdauer und die Verarbeitung einer Produktionsflussversion an einem bestimmten Datum zu beenden, oder den Ersatz einer aktiven Version mit einer neuen Version zu planen, müssen Sie ein Ablaufdatum für die Version festgelegt."
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6fabeb31720a60bf97d08dabf8ed87ac6af7cbf7
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Ablaufdatum für eine Produktionsflussversion definieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Um die Gültigkeitsdauer und die Verarbeitung einer Produktionsflussversion an einem bestimmten Datum zu beenden, oder den Ersatz einer aktiven Version mit einer neuen Version zu planen, müssen Sie ein Ablaufdatum für die Version festgelegt. Es ist nicht erforderlich, die Version zu deaktivieren.


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>Wählen Sie ein Ablaufdatum, um eine Produktionsflussversion zu beenden
1. Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen einen Produktionsfluss aus, der eine Version aufweist, die bereits definiert ist.  
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie auf "Bearbeiten".
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.
    * Zum Ablaufdatum wird keine neue Version gestartet oder aktiviert. Es ist nicht mehr möglich, Einzelvorgänge für den Produktionsfluss zu erstellen oder zu starten. Können Sie gestartete Einzelvorgänge nach Ablaufdatum noch ausführen.  


