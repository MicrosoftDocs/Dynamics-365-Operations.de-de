---
title: Produktionsauftrag beenden
description: Diese Prozedur zeigt, wie ein Produktionsauftrag beendet wird.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fade659c320e0ea1059644324859c9a3cb273c96
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207070"
---
# <a name="end-a-production-order"></a>Produktionsauftrag beenden

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie ein Produktionsauftrag beendet wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dies ist die abschließende Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.


## <a name="end-a-production-order"></a>Produktionsauftrag beenden
1. Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".
    * Wählen Sie einen Produktionsauftrag aus, der den Status "Fertig gemeldet" hat.  
2. Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".
3. Klicken Sie auf "Beenden".
    * Auf dieser Seite können Sie das Beenden des Produktionsauftrags bestätigen.  
4. Klicken Sie auf die Registerkarte "Allgemein".
5. Geben Sie ein Datum in das Feld "Datum" ein.
6. Wählen Sie im Feld "Ausschussmethode" "Zuordnung" aus.
    * Wenn Sie die Zuordnungsmethode auswählen, werden die Kosten des Ausschusses zu den Fertigerzeugnissen hinzugefügt.  
7. Klicken Sie auf "OK".

## <a name="validate-calculation-results"></a>Berechnungergebnisse überprüfen
1. Klicken Sie im Aktivitätsbereich auf "Kosten verwalten".
2. Klicken Sie auf "Kostenvergleich anzeigen".
    * Nachdem Sie den Produktionsauftrag abgeschlossen haben, können Sie den vorkalkulierten Einstandspreis mit dem realisierten Einstandspreis vergleichen, um einen Überblick über die Produktionsabweichungen zu erhalten.  
