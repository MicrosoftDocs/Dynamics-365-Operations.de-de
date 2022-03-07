---
title: Verkaufspreisauswahlkriterien erstellen
description: Dieses Verfahren zeigt, wie ein Verkaufspreisauswahlkriterium für attributbasierte Verkaufspreismodelle erstellt wird.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568446"
---
# <a name="create-sales-price-selection-criteria"></a>Verkaufspreisauswahlkriterien erstellen

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie ein Verkaufspreisauswahlkriterium für attributbasierte Verkaufspreismodelle erstellt wird. Dieses Verfahren erfordert, dass mindestens ein Verkaufspreismodell vorhanden ist. Dieses Beispiel verwendet das Preismodell für das Lautsprecherlösungs-Verkaufspreismodell im USMF-Demodatunternehmen. Normalerweise wird ein Produktmanager dieses Verfahren durchführen.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Hinzufügen eines neuen Kriteriums für ein vorhandenes Verkaufspreismodell

1. Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.
1. Wählen Sie in der Liste die Zeile für das Produktmodell der Speaker-Lösung, aber wählen Sie nicht den Link für den Modellnamen.
1. Wählen Sie im Aktionsbereich **Modell**.
1. Wählen Sie **Preismodellkriterien**.
1. Wählen Sie **Neu** aus.
1. Im Feld **Name** geben Sie 'Kundengruppe 10' ein.
    * Der Name des Preismodellkriteriums wird verwendet, um die zugrunde liegenden Auswahlkriterien zu ermitteln.  
1. Geben Sie im Feld **Preismodell** einen Wert ein oder wählen Sie einen aus.
1. Wählen Sie im Feld **Auftragstyp** *Verkaufsauftrag*.
    * Der Auftragstyp bestimmt die Datenbankfelder, die für die Auswahlabfrage verfügbar sind.  
1. Geben Sie in das Feld **Gültig ab** ein Datum ein.
1. Geben Sie in das Feld **Ablaufen bis** ein Datum ein.
1. Wählen Sie **Speichern** aus.

## <a name="create-the-query-for-the-selection-criteria"></a>Erstellen einer Abfrage für die Auswahlkriterien

1. Wählen Sie **Bearbeiten** aus.
2. Wählen Sie im Feld **Tabelle** die Option *Kunden*.
3. Wählen Sie im Feld **Feld** die Option *Kundengruppe*.
    * In diesem Beispiel verwenden wir eine bestimmte Debitorengruppe für die Auswahlkriterien.  
4. Wählen Sie im Feld **Kriterium** die *Kundengruppe 10*.
5. Wählen Sie **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]