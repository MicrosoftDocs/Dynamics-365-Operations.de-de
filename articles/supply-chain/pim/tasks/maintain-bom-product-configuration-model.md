---
title: Stückliste für ein Produktkonfigurationsmodell verwalten
description: Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921316"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Stückliste für ein Produktkonfigurationsmodell verwalten

[!include [banner](../../includes/banner.md)]

Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell. Das Spitzenlautsprechermodell im Vorführungsunternehmen USMF wird verwendet, um diese Prozedur zu erstellen.

## <a name="add-a-bom-line"></a>Hinzufügen einer Stücklistenposition

1. Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie den Spitzenlautsprecher für diese Prozedur aus.  
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Erweitern Sie den Abschnitt **Stücklisten**.
1. Wählen Sie **Hinzufügen** aus.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Geben Sie im Feld **Beschreibung** einen Wert ein.
1. Wählen Sie **Speichern** aus.

## <a name="add-bom-line-details"></a>Hinzufügen von Stücklistenpositionsdetails

1. Wählen Sie **Stücklisten-Zeilen-Details**.
2. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.
    * Sie können beispielsweise Artikel "M0055" auswählen.  
    * Für jede Stücklistenpositionseigenschaft können Sie festlegen, ob ein fester Wert oder ein Attribut zugeordnet ist.  
3. Aktivieren Sie das Kontrollkästchen **Setzen**.
4. Wählen Sie *Ja* im Feld **Berechnung**.
    * Das Festlegen der Eigenschaft **Berechnung** auf *Ja* stellt sicher, dass die Zeile der Stückliste in die Kalkulation einbezogen wird.  
5. Wählen Sie die Registerkarte **Einrichten**.
6. Aktivieren Sie das Kontrollkästchen **Setzen**.
7. Geben Sie im Feld **Menge** eine Zahl ein.
    * Das Feld "Menge" bestimmt die Menge des Artikels, der in der Stückliste enthalten ist. Dieser könnte ein offensichtlicher Kandidat für eine Attributzuordnung sein.  
8. Wählen Sie die Registerkarte **Dimension**.
    * Überprüfen Sie, ob vorhandene Produktdimensionen aktiv sind und daher ein Wert oder ein Attribut zugewiesen sein muss..  
9. Wählen Sie **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]