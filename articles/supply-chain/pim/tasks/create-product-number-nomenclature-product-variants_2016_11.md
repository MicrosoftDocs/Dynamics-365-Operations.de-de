---
title: Produktnummernbezeichnung für konfigurierte Produktvarianten erstellen
description: Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für konfigurierte Produktvarianten eingerichtet wird und sie einem konfigurierbaren Produktmaster zugeordnet werden kann.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da52385f60b2522cf358e0ceb70448479a1e5dc714ef15ba361611ed404ed852
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726824"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Produktnummernbezeichnung für konfigurierte Produktvarianten erstellen

[!include [banner](../../includes/banner.md)]

Diese Verfahren zeigt, wie eine Produktnummerenbezeichnung für konfigurierte Produktvarianten eingerichtet wird und sie einem konfigurierbaren Produktmaster zugeordnet werden kann. Dieses Verfahren beschreibt auch, wie eine Konfigurationsbezeichnung für eine Produktkonfigurationsmodellkomponente erstellen wird. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Die neue Produktnummernbezeichnung wird dem Produktmaster D0004 zugewiesen. Diese Aufgabe erfolgt in der Regel durch einen Produktdesigner.

## <a name="create-a-product-number-nomenclature"></a>Erstellen eine Produktnummerbezeichnung

1. Wechseln Sie zu **Produktinformationsmanagement \> Einrichten \> Produktbezeichnung**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Geben Sie im Feld **Beschreibung** einen Wert ein.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Produktstammnummer**.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Textkonstante** aus.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Text** einen Wert ein.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Konfiguration**.
1. Schließen Sie die Seite.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Zuweisen der Produktnummernbezeichnung zu einem Produktmaster

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Produktmaster**.
1. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie zum Beispiel auf das Feld **Produktnummer** mit dem Wert 'D'.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Wählen Sie **Bearbeiten** aus.
1. Wählen Sie *Ja* im Feld **Bezeichnungen verwenden** aus.
1. Geben Sie im Feld **Produktvariantennummerbezeichnung** einen Wert ein oder wählen Sie einen Wert aus.
1. Schließen Sie die Seite.
1. Schließen Sie die Seite.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Erstellen einer Bezeichnung für eine Produktkonfigurationsmodellkomponente

1. Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Wählen Sie **Bearbeiten** aus.
1. Wählen Sie *Ja* im Feld **Konfigurationsnomenklatur verwenden**.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Attributwert**.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Attribut** einen Wert ein oder wählen Sie einen Wert aus.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Textkonstante** aus.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Text** einen Wert ein.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Attributwert**.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Attribut** einen Wert ein oder wählen Sie einen Wert aus.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Textkonstante** aus.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Text** einen Wert ein.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Attributwert**.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Attribut** einen Wert ein oder wählen Sie einen Wert aus.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Textkonstante** aus.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Text** einen Wert ein.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Attributwert**.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Attribut** einen Wert ein oder wählen Sie einen Wert aus.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Textkonstante** aus.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Text** einen Wert ein.
1. Wählen Sie **Hinzufügen** aus.
1. Wählen Sie **Nummernkreis Wert**.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Geben Sie im Feld **Nummernkreis** einen Wert ein oder wählen Sie einen aus.
1. Schließen Sie die Seite.
1. Schließen Sie die Seite.
1. Schließen Sie die Seite.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]