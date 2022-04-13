---
title: Plan mit Einschränkungen erstellen
description: Dieses Thema zeigt, wie ein Plan erstellt wird, der sowohl Material- als auch Kapazitätsengpässe berücksichtigt.
author: t-benebo
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8372f4e35b34ff66ef55c0961b867a1aff7a5e6
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468943"
---
# <a name="generate-a-constrained-plan"></a>Plan mit Einschränkungen erstellen

[!include [banner](../../includes/banner.md)]

Dieses Thema zeigt, wie ein Plan erstellt wird, der sowohl Material- als auch Kapazitätsengpässe berücksichtigt. Der Plan stellt sicher, dass die Herstellung nicht beginnt, bevor das Material verfügbar ist und die Ressourcen nicht überbucht werden. 

Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Diese Prozedur ist für den Produktionsplaner vorgesehen.


## <a name="set-up-a-constrained-plan"></a>Einen eingeschränkten Plan einrichten
1. Auf der Startseite wählen Sie den Arbeitsbereich **Produktprogrammplanung** aus.
2. Wählen Sie **Produktprogrammpläne** in der Liste mit Links ganz rechts im Arbeitsbereich aus.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Beispiel: **StaticPlan**  
4. Wählen Sie **Ja** im Feld **Begrenzte Kapazität** aus.
5. Geben Sie im Feld **Planungszeitraum für begrenzte Kapazität** den Wert `30` ein.
6. Erweitern Sie den Abschnitt **Planungszeitraum in Tagen**.
7. Wählen Sie **Ja** im Feld **Kapazität** aus.
8. Geben Sie im Feld **Zeitraum für Kapazitätsplanung (Tage)** eine Zahl ein. Beispiel: `60`  
9. Wählen Sie **Ja** im Feld **Berechnete Verzögerungen** aus.
10. Geben Sie im Feld **Planungszeitraum für Verzögerungen berechnen (Tage)** eine Zahl ein. Beispiel: `60` 
11. Erweitern Sie den Abschnitt **Berechnete Verzögerungen**.
12. Wählen Sie **Ja** in allen Feldern **Die berechnete Verzögerung dem Bedarfsdatum hinzufügen**.
13. Schließen Sie die Seite.

## <a name="create-a-constrained-plan"></a>Einen Plan mit Einschränkungen erstellen
1. Wählen Sie **Ausführen** aus.
2. Geben Sie im Feld **Produktprogrammplan** den Plan ein oder wählen Sie den Plan aus, für den Sie Einschränkungen eingerichtet haben.  
3. Wählen Sie **OK**.
4. Wählen Sie **Bestellvorschläge** aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]