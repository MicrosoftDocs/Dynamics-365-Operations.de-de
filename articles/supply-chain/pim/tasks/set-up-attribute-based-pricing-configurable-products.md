---
title: Eine Attribut-basierte Preiskalkulation für konfigurierbare Produkte einrichten
description: In diesem Thema wird erläutert, wie Sie eine attributive Preisgestaltung einrichten.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4acd7b423396124dd1059602f5aa6460ec5e259
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578151"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Eine Attribut-basierte Preiskalkulation für konfigurierbare Produkte einrichten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie eine attributive Preisgestaltung einrichten. Als Voraussetzung müssen Sie ein Produktkonfigurationsmodell haben, das eine oder mehrere Komponenten und Attribute besitzt. Dieses Beispiel verwendet das High-End-Lausprecherproduktmodell im Demodatenunternehmen USMF. Normalerweise wird ein Produktmanager dieses Verfahren durchführen.


## <a name="create-a-new-price-model"></a>Erstellen eines neuen Preismodellkriteriums

1. Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.
1. Wählen Sie in der Liste die Zeile **High-End-Lautsprecher**, aber nicht den Link für den Namen.
1. Wählen Sie im Aktionsbereich **Modell**.
1. Wählen Sie **Preismodelle**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Preismodellname** einen Wert ein. Verwenden Sie einen Namen, mit dem das Modell einfach zu identifizieren ist.  
1. Geben Sie im Feld **Beschreibung** einen Wert ein.
1. Wählen Sie **Speichern**.

## <a name="add-price-elements"></a>Hinzufügen von Preiselementen

1. Wählen Sie **Bearbeiten** aus. Jede Komponente in einem Produktmodell kann ein Basispreiselement und eine beliebige Anzahl Preisausdrucksregeln haben. Sie können die Preise in den verschiedenen Währungen hinzufügen.  
2. Geben Sie im Feld **Basispreisausdruck** einen Wert ein. Geben Sie beispielsweise "100" ein. Ein Basispreisausdruck kann ein numerischer Wert sein, oder er kann aus einer arithmetischen Berechnung mit einem oder mehreren Attribute zusammensetzen.  
3. Wählen Sie **Hinzufügen** aus.
4. Geben Sie im Feld **Name** `Rosewood` ein. Die Preisausdruckname erleichtert die Erkennung des Preiselements. In diesem Beispiel wird ein Preiselement für die Rosenholzlautsprechergehäuse-Option erstellt.  
5. Wählen Sie **Bedingung bearbeiten**. Eine Preisbedingung stellt sicher, dass ein Preisausdruckselement nur dann in den Verkaufspreis einbezogen wird, wenn eine bestimmte Kombination von Attributen vorhanden ist.  
6. Geben Sie im Feld **ConstraintBody** `CabinetFinish=="Rosewood"` ein.
7. Wählen Sie **OK**.
8. Geben Sie in das Feld **Ausdruck** einen Wert ein. Geben Sie z.B. `50` ein. 
9. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]