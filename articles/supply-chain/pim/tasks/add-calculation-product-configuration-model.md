---
title: Berechnung zu einem Produktkonfigurationsmodell hinzufügen
description: Im folgenden Verfahren sehen Sie, wie Sie einen neuen Berechnung zu einem Produktkonfigurationsmodell hinzufügen können.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268baa4b518f6df52d4393f7278a79cbe1733844
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812672"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Berechnung zu einem Produktkonfigurationsmodell hinzufügen

[!include [banner](../../includes/banner.md)]

Im folgenden Verfahren sehen Sie, wie Sie einen neuen Berechnung zu einem Produktkonfigurationsmodell hinzufügen können. Darin wird angezeigt, wie Sie einen logischen Ausdruck unter Verwendung des "If"-Operators erstellen können, um eine Lautsprecherhöhe bis 10 für weiße Lautsprecher und 15 für alle anderen Gehäusefarben festzulegen. Das Verfahren verwendet die Komponente "High end speaker" im Vorführungsunternehmen USMF.


## <a name="add-a-calculation"></a>Eine Berechnung hinzufügen

## <a name="create-calculation-expression"></a>Berechnungsausdruck erstellen
1. Klicken Sie auf "Ausdruck bearbeiten".
2. Geben Sie im Feld "ConstraintBody" "If[CabinetFinish== "White", 10, 15]" ein.
3. Klicken Sie auf "Überprüfen".
4. Klicken Sie auf "Schließen".
5. Klicken Sie auf "OK".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]