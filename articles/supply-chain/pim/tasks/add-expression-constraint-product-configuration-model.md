---
title: Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen
description: Im folgenden Verfahren sehen Sie, wie Sie einen neuen Einschränkungsausdruck einem Produktkonfigurationsmodell hinzufügen können.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77e8b991a2615a8f5d238acc4655f231edb6ca98
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569648"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen

[!include [banner](../../includes/banner.md)]

Im folgenden Verfahren sehen Sie, wie Sie einen neuen Einschränkungsausdruck einem Produktkonfigurationsmodell hinzufügen können. Es zeigt, wie Sie vorgeben, dass der "Eckschutz" an einem Lautsprecher angebracht werden muss, wenn der Benutzer einen vorderen Metallgrill ausgewählt hat. Das Verfahren verwendet die Komponente "High end speaker" im Vorführungsunternehmen USMF.

## <a name="create-an-expression-constraint"></a>Erstellen einer Ausdruckseinschränkung

1. Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Diese Beispiel verwendet das Spitzenlautsprechermodell.  
4. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
5. Erweitern Sie den Abschnitt **Einschränkungen**.
6. Wählen Sie **Hinzufügen** aus.
7. Wählen Sie **Erstellen** aus.
8. Geben Sie im Feld **Name** einen Wert ein.

## <a name="enter-expression"></a>Ausdruck eingeben

1. Wählen Sie **Ausdruck bearbeiten** aus.
    * Wenn Sie die Benutzeroberfläche in der Aufgabe "Aufzeichung" in dieser Phase entsperren, können Sie IntelliSense und die Liste der Symbole verwenden, um die "Ausdruckseinschränkung" zu erstellen.  
2. Geben Sie im Feld **ConstraintBody** 'Implies[FrontGrill=="Metal", CornerProtection] ' ein.
    * Dieser logische Ausdruck besagt: Wenn der vordere Grill aus Metall ist, muss die Option "Eckschutz" ausgewählt werden.  
3. Wählen Sie **Überprüfen** aus.
    * Die Validierungsfunktion wird durch den Einschränkungsausdruck und Überprüfungen auf Syntaxfehler ausgeführt.  
4. Wählen Sie **Schließen** aus.
5. Wählen Sie **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]