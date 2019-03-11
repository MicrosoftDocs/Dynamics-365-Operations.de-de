---
title: Eine Attribut-basierte Preiskalkulation für konfigurierbare Produkte einrichten
description: Dieses Verfahren zeigt Ihnen, wie Sie attributbasierte Preis einrichten.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8568b5f4933ae58bc2d55a169c798668e03bed2a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "333782"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Eine Attribut-basierte Preiskalkulation für konfigurierbare Produkte einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt Ihnen, wie Sie attributbasierte Preis einrichten. Als Voraussetzung müssen Sie ein Produktkonfigurationsmodell haben, das eine oder mehrere Komponenten und Attribute besitzt. Dieses Beispiel verwendet das High-End-Lausprecherproduktmodell im Demodatenunternehmen USMF. Normalerweise wird ein Produktmanager dieses Verfahren durchführen.


## <a name="create-a-new-price-model"></a>Erstellen eines neuen Preismodellkriteriums
1. Klicken Sie auf "Produktvariantenmodell-Definition".
2. Klicken Sie auf "Produktkonfigurationsmodelle".
3. Wählen Sie in der Liste die Position "High-End-Lautsprecher" aus, aber klicken Sie nicht auf den Link für den Namen.
4. Klicken Sie im Aktivitätsbereich auf "Modell".
5. Klicken Sie auf Preismodelle.
6. Klicken Sie auf "Neu".
7. Geben Sie im Feld "Preismodellname" einen Wert ein.
    * Verwenden Sie einen Namen, mit dem das Modell einfach zu identifizieren ist.  
8. Geben Sie im Feld "Beschreibung" einen Wert ein.
9. Klicken Sie auf "Speichern".

## <a name="add-price-elements"></a>Hinzufügen von Preiselementen
1. Klicken Sie auf "Bearbeiten".
    * Jede Komponente in einem Produktmodell kann ein Basispreiselement und eine beliebige Anzahl Preisausdrucksregeln haben. Sie können die Preise in den verschiedenen Währungen hinzufügen.  
2. Geben Sie im Feld "Basispreisausdruck" einen Wert ein.
    * Geben Sie beispielsweise "100" ein.   Ein Basispreisausdruck kann ein numerischer Wert sein, oder er kann aus einer arithmetischen Berechnung mit einem oder mehreren Attribute zusammensetzen.  
3. Klicken Sie auf Hinzufügen.
4. Geben Sie im Feld "Name" 'Rosenholz' ein.
    * Die Preisausdruckname erleichtert die Erkennung des Preiselements. In diesem Beispiel wird ein Preiselement für die Rosenholzlautsprechergehäuse-Option erstellt.  
5. Klicken Sie auf "Bedingung bearbeiten".
    * Eine Preisbedingung stellt sicher, dass ein Preisausdruckselement nur dann in den Verkaufspreis einbezogen wird, wenn eine bestimmte Kombination von Attributen vorhanden ist.  
6. Geben Sie im Feld "ConstraintBody" "CabinetFinish=="Rosenholz"" ein.
7. Klicken Sie auf "OK".
8. Geben Sie im Feld 'Ausdruck' einen Wert ein.
    * Geben Sie beispielsweise "50" ein.  
9. Schließen Sie die Seite.
10. Schließen Sie die Seite.

