--- 
title: "Plan mit Einschränkungen erstellen"
description: "Diese Prozedur zeigt, wie ein Plan erstellt wird, der sowohl Material- als auch Kapazitätsengpässe berücksichtigt."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6735f0287e7a61ff494a48c97c44480c6038097c
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="generate-a-constrained-plan"></a>Plan mit Einschränkungen erstellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie ein Plan erstellt wird, der sowohl Material- als auch Kapazitätsengpässe berücksichtigt. Der Plan stellt sicher, dass die Herstellung nicht beginnt, bevor das Material verfügbar ist und die Ressourcen nicht überbucht werden. 

Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Prozedur ist für den Produktionsplaner vorgesehen.


## <a name="set-up-a-constrained-plan"></a>Einen eingeschränkten Plan einrichten
1. Klicken Sie auf "Produktprogrammplanung".
2. Klicken Sie auf "Produktprogrammpläne".
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Beispiel: StaticPlan  
4. Wählen Sie "Ja" im Feld "Begrenzte Kapazität" aus.
5. Geben Sie im Feld "Begrenzte Kapazität" den Wert "30" ein.
6. Erweitern Sie die Planungszeiträume im Tage-Abschnitt.
7. Wählen Sie "Ja" im Feld "Kapazität" aus.
8. Geben Sie im Feld "Zeitraum für Kapazitätsplanung (Tage)" eine Zahl ein.
    * Beispiel: 60  
9. Wählen Sie "Ja" im Feld "Berechnete Verzögerungen" aus.
10. Geben Sie im Feld "Planungszeitraum für Verzögerungen berechnen (Tage)" eine Zahl ein.
    * Beispiel: 60  
11. Erweitern Sie den Abschnitt "Berechnete Verzögerungen".
12. Wählen Sie "Ja" im Feld "Die berechnete Verzögerung dem Bedarfsdatum hinzufügen".
13. Wählen Sie "Ja" im Feld "Die berechnete Verzögerung dem Bedarfsdatum hinzufügen".
14. Wählen Sie "Ja" im Feld "Die berechnete Verzögerung dem Bedarfsdatum hinzufügen".
15. Schließen Sie die Seite.

## <a name="create-a-constrained-plan"></a>Einen Plan mit Einschränkungen erstellen
1. Klicken Sie auf "Ausführen".
2. Geben Sie im Feld "Produktprogrammplan" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie den Plan aus, für den Sie Einschränkungen eingerichtet haben.  
3. Klicken Sie auf "OK".
    * Dies kann einige Zeit in Anspruch nehmen.  
4. Klicken Sie auf "Bestellvorschläge".


