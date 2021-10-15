---
title: Produktkonfigurationsmodell erstellen
description: Im folgenden Verfahren wird gezeigt, wie ein Produktkonfigurationsmodell erstellt wird und grundlegende Informationen wie Attribute und Unterkomponenten eingegeben werden.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca99c0346a3f982164076167c3429587aac18be6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568423"
---
# <a name="create-a-product-configuration-model"></a>Produktkonfigurationsmodell erstellen

[!include [banner](../../includes/banner.md)]

Im folgenden Verfahren wird gezeigt, wie ein Produktkonfigurationsmodell erstellt wird und grundlegende Informationen wie Attribute und Unterkomponenten eingegeben werden. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="create-a-product-model"></a>Erstellen eines Produktmodells

1. Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Geben Sie im Feld **Beschreibung** einen Wert ein.
1. Wählen Sie im Feld **Löserstrategie** eine Option aus.
    * Die Solver-Strategie bestimmt, wie die Einschränkungen in einem einschränkungsbasierten Produktkonfigurationsmodell verarbeitet werden. Diese Auswahl kann Auswirkungen auf die Leistung des Produktkonfigurationsmodells haben.  
1. Geben Sie im Feld **Name** einen Wert ein.
    * Die Stammkomponente stellt das Produktkonfigurationsmodell dar, kann jedoch auch in anderen Produktmodellen verwendet werden.  
1. Wählen Sie **OK**.
1. Wählen Sie im Feld **Konfigurationen wiederverwenden** eine Option.
    * Wenn der Parameter "Konfigurationen wiederverwenden" auf "Ja" festgelegt wird, prüft das System nach jeder Konfigurationssitzung auf identische Konfigurationen und verwendet sie erneut , wenn eine komplette Übereinstimmung gefunden wird.  

## <a name="add-attributes"></a>Attribute hinzufügen

1. Erweitern Sie den Abschnitt **Attribute**.
2. Wählen Sie **Hinzufügen** aus.
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Geben Sie in das Feld **Lösername** einen Wert ein.
    * Der Solver-Name wird vom Constraint-Solver des Produktkonfigurators verwendet. Er darf keine Leerzeichen oder Sonderzeichen mit Ausnahme von _ (Unterstrich) enthalten.  
6. Geben Sie im Feld **Beschreibung** einen Wert ein.
    * Der Beschreibungstext wird dem Konfigurationsbenutzer angezeigt und kann somit als Hilfe im Auswählen des richtigen Attributwerts dienen.  
7. Geben Sie in das Feld **Attribut-Typ** einen Wert ein oder wählen Sie einen Wert aus.
    * Der Attributtyp bestimmt, welche Werte für das Attribut verfügbar sind.  
8. Aktivieren Sie das Kontrollkästchen **Bei Wiederverwendung einbeziehen**.
    * Diese Option ist nur verfügbar, wenn die Option "Konfigurationen wiederverwenden" ausgewählt wurde. Wenn Sie die Attribute für das Kontrollkästchen "In Wiederverwendung einbeziehen" aktivieren, wird dieses Attribut berücksichtigt, wenn das System nach einer kompletten Übereinstimmung sucht.  

## <a name="add-subcomponents"></a>Unterkomponenten hinzufügen

1. Erweitern Sie den Abschnitt **Unterkomponenten**.
2. Wählen Sie **Hinzufügen** aus.
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Geben Sie in das Feld **Lösername** einen Wert ein.
6. Geben Sie im Feld **Beschreibung** einen Wert ein.
7. Geben Sie im Feld **Komponente** einen Wert ein oder wählen Sie einen aus.
    * Jede Unterkomponente muss auf eine Komponentendefinition verweisen. Dieser Entwurf unterstützt wiederverwendbare Komponenten und stellt sicher, dass eine Komponente, nachdem sie einmal definiert wurde, in vielen Produktmodellen verwendet werden kann.  
8. Wählen Sie **Speichern** aus.
9. Wählen Sie **Stücklisten-Zeilen-Details**.
    * Das Formular "Stücklistenpositionsdetail"ermöglicht dem Benutzer, die erforderlichen Eigenschaften für die Unterkomponente auszuwählen. Jeder Eigenschaft kann ein fester Wert oder ein Attribute zugewiesen werden. Die Zuordnung zu einem Attribut führt dazu, dass der Stücklistenabrechnungscode, verschiedene Werte abhängig von der Konfigurationsauswahl abruft.  
10. Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.
    * Jede Unterkomponente stellt einen konfigurierbaren Produktmaster mit einschränkungsbasierten Konfigurationtechnologie dar. Die Referenz wird durch die Artikelnummer vorgenommen.  
11. Aktivieren Sie das Kontrollkästchen **Setzen**.
12. Wählen Sie **Ja** im Feld **Berechnung**.
    * Das Festlegen der Berechnungsoption stellt sicher, dass das Produkt enthalten ist, wenn eine Kostenberechnung für das Produkt ausgeführt wird.  
13. Wählen Sie die Registerkarte **Einrichten**.
14. Aktivieren Sie das Kontrollkästchen **Setzen**.
15. Geben Sie im Feld **Menge** eine Zahl ein.
    * Das Feld "Menge" bestimmt, wie viel von diesem Produkt im konfigurierten Produkt verbraucht wird.  
16. Aktivieren Sie das Kontrollkästchen **Setzen**.
17. Geben Sie in das Feld **Per Serie** eine Zahl ein.
18. Wählen Sie **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]