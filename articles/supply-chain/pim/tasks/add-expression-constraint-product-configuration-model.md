--- 
title: "Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen"
description: "Im folgenden Verfahren sehen Sie, wie Sie einen neuen Einschränkungsausdruck einem Produktkonfigurationsmodell hinzufügen können."
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2016
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
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Im folgenden Verfahren sehen Sie, wie Sie einen neuen Einschränkungsausdruck einem Produktkonfigurationsmodell hinzufügen können. Es zeigt, wie Sie vorgeben, dass der "Eckschutz" an einem Lautsprecher angebracht werden muss, wenn der Benutzer einen vorderen Metallgrill ausgewählt hat. Das Verfahren verwendet die Komponente "High end speaker" im Vorführungsunternehmen USMF.


## <a name="create-an-expression-constraint"></a>Erstellen einer Ausdruckseinschränkung
1. Klicken Sie auf "Produktvariantenmodell-Definition".
2. Klicken Sie auf "Produktkonfigurationsmodelle".
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Diese Beispiel verwendet das Spitzenlautsprechermodell.  
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Erweitern Sie den Abschnitt "Einschränkungen".
6. Klicken Sie auf Hinzufügen.
7. Klicken Sie auf "Erstellen".
8. Geben Sie im Feld "Name" einen Wert ein.

## <a name="enter-expression"></a>Ausdruck eingeben
1. Klicken Sie auf "Ausdruck bearbeiten".
    * Wenn Sie die Benutzeroberfläche in der Aufgabe "Aufzeichung" in dieser Phase entsperren, können Sie IntelliSense und die Liste der Symbole verwenden, um die "Ausdruckseinschränkung" zu erstellen.  
2. Geben Sie im Feld "ConstraintBody" "Implies[FrontGrill=="Metal", CornerProtection] " ein.
    * Dieser logische Ausdruck besagt: Wenn der vordere Grill aus Metall ist, muss die Option "Eckschutz" ausgewählt werden.  
3. Klicken Sie auf "Überprüfen".
    * Die Validierungsfunktion wird durch den Einschränkungsausdruck und Überprüfungen auf Syntaxfehler ausgeführt.  
4. Klicken Sie auf "Schließen".
5. Klicken Sie auf "OK".


