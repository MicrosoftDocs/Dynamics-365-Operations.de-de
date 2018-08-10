--- 
title: "Stückliste für ein Produktkonfigurationsmodell verwalten"
description: "Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell."
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c017d7719ac6af43b0c8a162080bb753587df030
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Stückliste für ein Produktkonfigurationsmodell verwalten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell. Das Spitzenlautsprechermodell im Vorführungsunternehmen USMF wird verwendet, um diese Prozedur zu erstellen.


## <a name="add-a-bom-line"></a>Hinzufügen einer Stücklistenposition
1. Klicken Sie auf "Produktvariantenmodell-Definition".
2. Klicken Sie auf "Produktkonfigurationsmodelle".
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie den Spitzenlautsprecher für diese Prozedur aus.  
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Erweitern Sie den Abschnitt "Stücklistenpositionen".
6. Klicken Sie auf Hinzufügen.
7. Geben Sie im Feld "Name" einen Wert ein.
8. Geben Sie im Feld "Beschreibung" einen Wert ein.
9. Klicken Sie auf "Speichern".

## <a name="add-bom-line-details"></a>Hinzufügen von Stücklistenpositionsdetails
1. Klicken Sie auf "Stücklistenpositionsdetails".
2. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Sie können beispielsweise Artikel "M0055" auswählen.  
    * Für jede Stücklistenpositionseigenschaft können Sie festlegen, ob ein fester Wert oder ein Attribut zugeordnet ist.  
3. Wählen Sie das Kontrollkästchen "Festlegen" aus.
4. Wählen Sie "Ja" im Feld "Berechnung" aus.
    * Das Festlegen der Berechnungseigenschaft auf "Ja" gewährleistet, dass die Stücklistenposition in die Kostenberechnungen einbezogen ist.  
5. Klicken Sie auf die Registerkarte "Einstellungen".
6. Wählen Sie das Kontrollkästchen "Festlegen" aus.
7. Geben Sie im Feld "Menge" eine Zahl ein.
    * Das Feld "Menge" bestimmt die Menge des Artikels, der in der Stückliste enthalten ist. Dieser könnte ein offensichtlicher Kandidat für eine Attributzuordnung sein.  
8. Klicken Sie auf die Registerkarte 'Dimensionen'.
    * Überprüfen Sie, ob vorhandene Produktdimensionen aktiv sind und daher ein Wert oder ein Attribut zugewiesen sein muss..  
9. Klicken Sie auf "OK".


