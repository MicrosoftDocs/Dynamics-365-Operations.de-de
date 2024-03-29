---
title: Erstellen einer betrieblichen Ressource
description: Eine betriebliche Ressource führt die Aktivitäten eines Projekts oder eines Produktionsprozesses aus.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90535d3a6cf58fc10309cf035bc74143a96c2add
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576855"
---
# <a name="create-an-operations-resource"></a>Erstellen einer betrieblichen Ressource

[!include [banner](../../includes/banner.md)]

Eine betriebliche Ressource führt die Aktivitäten eines Projekts oder eines Produktionsprozesses aus. Diese Prozedur zeigt Ihnen an, wie eine betriebliche Ressource definiert wird. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.

1. Wechseln Sie zu "Ressourcen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Ressource" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.

## <a name="define-capacity-and-consumption-parameters"></a>Kapazitäts- und Verbrauchsparameter definieren
1. Erweitern Sie den Abschnitt "Arbeitstang".
2. Geben Sie im Feld "Ausschuss" eine Zahl ein.
3. Geben Sie im Feld "Rüstkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie die Kostenkategorie an, die definiert, wie die Kosten der Einstellung berücksichtigt werden sollen.  
4. Geben Sie im Feld "Ausführungszeitkategorie" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie die Kostenkategorie an, die definiert, wie die Kosten der Laufzeit berücksichtigt werden sollen.  
5. Geben Sie im Feld "Stückkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie die Kostenkategorie an, die definiert, wie die Ressourcenkosten, basierend auf der Ausgabemenge, berücksichtigt werden sollen.  
6. Wählen Sie im Feld "Kapazitätseinheit" eine Option aus.
    * Geben Sie die Einheit an, in der die Kapazität der betrieblichen Ressource ausgedrückt wird.  
7. Geben Sie im Feld "Kapazität" eine Zahl ein.
8. Geben Sie im Feld "Effizienzgrad" eine Zahl ein.
    * Geben Sie die Effizienz an, die Sie von der betrieblichen Ressource erwarten. Mit dem Effizienzgrad wird der Durchsatz einer betrieblichen Ressource angepasst und er wirkt sich somit auch auf die für die Ressource reservierte Zeit aus.  
9. Geben Sie im Feld "Grobterminierungsprozentsatz" eine Zahl ein.
    * Geben Sie den maximalen Prozentsatz der Kapazität der betrieblichen Ressource an, die sie für die Grobterminierung verwendet möchten.  
10. Wählen Sie "Ja" im Feld "Begrenzte Kapazität" aus.
    * Legen Sie diese Option auf "Ja" fest, wenn die betriebliche Ressource auf Basis der tatsächlichen Kapazität, die verfügbar ist, geplant werden soll, und wenn vorhandene Kapazitätsreservierungen berücksichtigt werden sollen. Wenn die Option auf "Nein" festgelegt ist, wird angenommen, dass die betriebliche Ressource unbegrenzte Kapazität hat, und die Ressource kann möglicherweise überbucht werden.  
11. Wählen Sie "Ja" im Feld "Engpassressource" aus.

## <a name="define-working-times"></a>Arbeitszeiten definieren
1. Erweitern Sie den Abschnitt "Kalender".
2. Klicken Sie auf Hinzufügen.
3. Geben Sie im Feld "Kalender" einen Wert ein oder wählen Sie einen Wert aus.
    * Geben Sie den Arbeitszeitkalender an, der die Kapazität (in Stunden) der Ressource definiert.  
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="define-resource-capabilities"></a>Ressourcenfähigkeiten definieren
1. Erweitern Sie den Abschnitt "Funktionen".
2. Klicken Sie auf Hinzufügen.
    * Eine Funktion ist die Fähigkeit einer betrieblichen Ressource, eine bestimmte Aktivität auszuführen. Das Planungsmodul weist Ressourcen zu, indem die Ressourcenanforderungen jeder Aktivität mit den Funktionen der verfügbaren betrieblichen Ressourcen abgeglichen werden.  
3. Geben Sie im Feld "Funktion" einen Wert ein, oder wählen Sie einen Wert aus.
4. Geben Sie im Feld "Ebene" eine Zahl ein.
    * Geben Sie den Grad der Effizienz an, mit der die Ressource die Funktion verarbeitet.  
5. Geben Sie im Feld "Priorität" eine Zahl ein.
    * Geben Sie die Priorität der betrieblichen Ressource hinsichtlich der Funktion an. Bei der Planung nach Priorität, wird die betriebliche Ressource mit der höchsten Priorität (also mit dem niedrigsten numerischen Wert) zuerst ausgewählt.  

## <a name="assign-resource-to-resource-group"></a>Einer Ressourcengruppe eine Ressource zuweisen
1. Erweitern Sie den Abschnitt "Ressourcengruppen".
2. Klicken Sie auf Hinzufügen.
    * Die Ressourcengruppe definiert den Standort-, Produktionseinheits- und Lagerortkontext für betriebliche Ressourcen. Die betriebliche Ressource kann nur eingeplant werden, wenn sie einer Ressourcengruppe zugewiesen ist, und zwar nur an dem Standort, an dem sich die Ressourcengruppe befinden.  
3. Geben Sie im Feld "Ressourcengruppe" einen Wert ein oder wählen Sie einen Wert aus.
4. Geben Sie im Feld "Lagerplatz für Wareneingang" einen Wert ein, oder wählen Sie einen Wert aus.
    * Geben Sie den Lagerort an, von dem aus die betriebliche Ressource Material verbraucht.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]