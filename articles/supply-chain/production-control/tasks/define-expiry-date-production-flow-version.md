---
title: Ablaufdatum für eine Produktionsflussversion definieren
description: Um die Gültigkeitsdauer und die Verarbeitung einer Produktionsflussversion an einem bestimmten Datum zu beenden, oder den Ersatz einer aktiven Version mit einer neuen Version zu planen, müssen Sie ein Ablaufdatum für die Version festgelegt.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97ac33d28a49ad0f2a3956ad65b159e4ec4785c7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428408"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Ablaufdatum für eine Produktionsflussversion definieren

[!include [banner](../../includes/banner.md)]

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

