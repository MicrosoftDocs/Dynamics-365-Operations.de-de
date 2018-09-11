--- 
title: Verkaufspreisauswahlkriterien erstellen
description: "Dieses Verfahren zeigt, wie ein Verkaufspreisauswahlkriterium für attributbasierte Verkaufspreismodelle erstellt wird."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59f6a4131f6a27c0089a1259e3f849f91a47bc87
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-price-selection-criteria"></a>Verkaufspreisauswahlkriterien erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie ein Verkaufspreisauswahlkriterium für attributbasierte Verkaufspreismodelle erstellt wird. Dieses Verfahren erfordert, dass mindestens ein Verkaufspreismodell vorhanden ist. Dieses Beispiel verwendet das Preismodell für das Lautsprecherlösungs-Verkaufspreismodell im USMF-Demodatunternehmen. Normalerweise wird ein Produktmanager dieses Verfahren durchführen.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Hinzufügen eines neuen Kriteriums für ein vorhandenes Verkaufspreismodell
1. Klicken Sie auf "Produktvariantenmodell-Definition".
2. Klicken Sie auf "Produktkonfigurationsmodelle".
3. In Sie wählen der Liste die Zeile für das Lautsprecherlösungsproduktmodell aus, aber klicken Sie nicht auf den Link für den Modellnamen.
4. Klicken Sie im Aktivitätsbereich auf "Modell".
5. Klicken Sie auf Preismodellkriterien.
6. Klicken Sie auf "Neu".
7. Geben Sie im Feld "Name" "Debitorengruppe 10" ein.
    * Der Name des Preismodellkriteriums wird verwendet, um die zugrunde liegenden Auswahlkriterien zu ermitteln.  
8. Geben Sie im Feld 'Preismodell' einen Wert ein, oder wählen Sie einen Wert aus.
9. Wählen Sie im Feld "Auftragstyp" die Option "Bestellung" aus.
    * Der Auftragstyp bestimmt die Datenbankfelder, die für die Auswahlabfrage verfügbar sind.  
10. Geben Sie ein Datum in das Feld "Gültig ab" ein.
11. Geben Sie im Feld "Ablaufzeitpunkt" ein Datum ein.
12. Klicken Sie auf "Speichern".

## <a name="create-the-query-for-the-selection-criteria"></a>Erstellen einer Abfrage für die Auswahlkriterien
1. Klicken Sie auf "Bearbeiten".
2. Wählen Sie im Feld "Debitoren" eine Option aus. 
3. Wählen Sie im Feld "Feld" "Debitorengruppe" aus.
    * In diesem Beispiel verwenden wir eine bestimmte Debitorengruppe für die Auswahlkriterien.  
4. Wählen Sie im Feld "Kriterien" "Debitorengruppe 10" aus. 
5. Klicken Sie auf "OK".


