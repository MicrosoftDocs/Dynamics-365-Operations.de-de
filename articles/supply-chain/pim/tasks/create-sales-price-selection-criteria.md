---
title: Verkaufspreisauswahlkriterien erstellen
description: Dieses Verfahren zeigt, wie ein Verkaufspreisauswahlkriterium für attributbasierte Verkaufspreismodelle erstellt wird.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a616dcfdd755efc9bf0473e9239acb9127f11f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818156"
---
# <a name="create-sales-price-selection-criteria"></a>Verkaufspreisauswahlkriterien erstellen

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie ein Verkaufspreisauswahlkriterium für attributbasierte Verkaufspreismodelle erstellt wird. Dieses Verfahren erfordert, dass mindestens ein Verkaufspreismodell vorhanden ist. Dieses Beispiel verwendet das Preismodell für das Lautsprecherlösungs-Verkaufspreismodell im USMF-Demodatunternehmen. Normalerweise wird ein Produktmanager dieses Verfahren durchführen.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Hinzufügen eines neuen Kriteriums für ein vorhandenes Verkaufspreismodell
1. Klicken Sie auf "Produktvariantenmodell-Definition".
2. Klicken Sie auf "Produktkonfigurationsmodelle".
3. In der LIste wählen Sie die Zeile für das Lautsprecherlösungsproduktmodell aus, aber klicken Sie nicht auf den Link für den Modellnamen.
4. Klicken Sie im Aktivitätsbereich auf "Modell".
5. Klicken Sie auf Preismodellkriterien.
6. Klicken Sie auf Neu.
7. Geben Sie im Feld Typ „Debitorengruppe 10“ ein.
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]