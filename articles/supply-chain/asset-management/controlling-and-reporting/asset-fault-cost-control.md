---
title: Kostensteuerung für Anlagenfehler
description: In diesem Artikel wird die Kostensteuerung für Anlagenfehler in der Anlagenverwaltung erläutert.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 553b89a43b656669b7730b19898f3a5d81a3873a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889663"
---
# <a name="asset-fault-cost-control"></a>Kostensteuerung für Anlagenfehler

[!include [banner](../../includes/banner.md)]

 

In Anlagenmanagement können Sie Kosten für Anlagenfehlererfassungen berechnen, um sich so einen Überblick über die Istkosten im Vergleich zu den Budgetkosten zu verschaffen. Istkosten basieren auf gebuchten Transaktionen. Das Datum ist das Fehlerdatum, an dem das Symptom erfasst wurde.

1. Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagenfehler** > **Kostensteuerung für Anlagenfehler**.

2. Im Dialogfeld **Kostensteuerung für Anlagenfehler** wählen Sie eine Finanzdimension aus, die in die Berechnung einbezogen werden soll, falls erforderlich.

4. Wählen Sie „Ja“ auf der Umschaltfläche **Null überspringen** aus, wenn keine Ergebnisse mit Kosten von Null angezeigt werden sollen.

5. Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Kostensteuerungspositionen bezüglich funktionaler Standorte sein sollen. 

    Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Kostensteuerungspositionen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt. 
    
    Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Kostensteuerungspositionen von Anlagenfehlern für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.

6. Wenn Sie die Suche begrenzen möchten, können Sie bestimmte Anlagen, Fehlerdaten und Fehlerursachen auf dem Inforegister **Einzuschließende Datensätze** auswählen.

7. Klicken Sie auf **OK**, um die Berechnung zu starten.

8. Klicken Sie auf die **Gruppieren nach…**-Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen. Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben. Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.

## <a name="example"></a>Beispiel

In diesem Beispiel wird eine Anlagenfehler-Kostenkontrollberechnung angezeigt.

- Das Feld **Ursprüngliches Budget** zeigt Budgetkosten aus der Arbeitsauftragsplanung. 
- Das Feld **Istkosten** zeigt gebuchte Kosten auf Arbeitsaufträgen. 
- Das Feld **Zugesagte Kosten** zeigt die Gesamtkosten, zu denen Ihr Unternehmen in Bezug auf Arbeitsaufträge verpflichtet ist.

    ![Abbildung 1.](media/05-controlling-and-reporting.png)

Informationen zum Einrichten von Fehlern finden Sie im Artikel [Fehlermanagement](../setup-for-work-orders/fault-management.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]