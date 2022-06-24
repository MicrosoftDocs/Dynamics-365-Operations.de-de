---
title: Arbeitszeitsteuerung
description: In diesem Artikel wird die Arbeitszeitsteuerung im Anlagenverwaltung erläutert.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f5f5dbb23c4d6c86bee7612c4ade65ef4b1cee8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869748"
---
# <a name="work-hour-control"></a>Arbeitszeitsteuerung

[!include [banner](../../includes/banner.md)]

 

Im Anlagenmanagement können Sie Stunden berechnen, um sich einen Überblick über die Iststunden im Vergleich zu den Budgetstunden auf Anlagen, Technischen Standorten oder Arbeitsaufträgen zu verschaffen. Die Ist-Stunden basieren auf gebuchten Transaktionen.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Arbeitszeitsteuerung für Anlagen, Technische Standorte und Arbeitsaufträge

Die Berechnungen für Anlagen, Technische Standorte und Arbeitsaufträge sind nahezu identisch. Der einzige Unterschied besteht darin, dass Sie bei Anlagen und Technischen Standorten auch Teilanlagen und Teilstandorte in Ihre Kalkulation einbeziehen können. Das Datum ist das Transaktionsdatum, an dem die Registrierung erfasst wurde.

1. Klicken Sie auf **Anlagenmanagement** > **Anfragen** > **Anlagen** > **Anlagenstundensteuerung** oder **Funktionsstandortsteuerung**, oder **Anlagenmanagement** > **Anfragen** > **Aufträge** > **Auftragsstundensteuerung**.

2. Im Dialog **Anlagenstundensteuerung**, .

3. Wählen Sie im Dialog **Assetstundensteuerung** / **Funktionsstandortsteuerung** / **Arbeitsauftragsstundensteuerung** in den Feldern **Ab Datum** und **Bis Datum** einen zu berechnenden Zeitraum aus.

4. Wählen Sie bei Bedarf ein **Finanzdimensionssatz**, das in die Berechnung einbezogen werden soll.

5. Wählen Sie „Ja“ auf der Schaltfläche **Null überspringen** umschalten, wenn Sie keine Ergebnisse mit Nullstunden anzeigen möchten.

6. Im Feld **Stufe** können Sie angeben, wie detailliert die Stundenkontrollzeilen zu Technischen Standorten sein sollen. 

    Wenn Sie z.B. die Zahl in das Feld einfügen und eine mehrstufige Technische Platzhierarchie haben, werden alle Stundensteuerzeilen für einen Technischen Standort auf der obersten Ebene angezeigt, so dass die Stunden auf einer Zeile von Technischen Standorten auf einer niedrigeren Ebene summiert werden können. 
    
    Wenn Sie die Zahl „0“ in das Feld **Ebene** eingeben, erhalten Sie ein detailliertes Ergebnis, das alle Stundenkontrollzeilen auf allen Ebenen des Technischen Standorts anzeigt, auf denen sie sich befinden.

7. Wählen Sie „Ja“ auf der Schaltfläche **Teilanlagen einbeziehen** Umschalten, um die mit Teilanlagen verbundenen Kosten als separate Zeilen anzuzeigen.

8. Wenn Sie die Suche einschränken möchten, können Sie bestimmte Anlagen / Technische Standorte / Arbeitsaufträge auf den **Sätzen auswählen, die mit** FastTab versehen werden sollen.

9. Klicken Sie auf **OK**, um die Berechnung zu starten.

10. Klicken Sie auf der Seite **Anlagenstundensteuerung** auf die **Gruppieren nach…**-Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen. Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben. Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.

## <a name="example"></a>Beispiel

Die Abbildung zeigt ein Beispiel für eine Berechnung der **Anlagenstundensteuerung**.

- Das Feld **Originalbudget** zeigt Budgetstunden aus der Arbeitsauftragsprognose. 
- Das Feld **Iststunden** zeigt gebuchte Stunden auf Arbeitsaufträgen. 
- Das Feld **Verpflichtete Stunden** zeigt die Gesamtzahl der Stunden, die Ihr Unternehmen in Bezug auf Arbeitsaufträge verpflichtet ist.

![Beispiel der Berechnung der Anlagenstundensteuerung.](media/04-controlling-and-reporting.png)

Eine weitere Möglichkeit, eine Stundenberechnung durchzuführen, besteht darin, Anlagen in **Alle Anlagen** oder **Aktive Anlagen** mehrfach auszuwählen. Dann klicken Sie auf die Schaltfläche **Stundensteuerung** auf dem Inforegister **Allgemein**. Die ausgewählten Anlagen werden automatisch in das Feld **Anlagen** auf der Seite **Einzubeziehende Anlagen** FastTab eingefügt. Klicken Sie im Dialog **Anlagenstundensteuerung** auf **OK**, und die Berechnung für die ausgewählten Anlagen wird angezeigt. Das gleiche Verfahren kann für Technische Standorte in **Alle Technischen Standorte** oder **Aktive Technische Standorte** und für Arbeitsaufträge in **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** durchgeführt werden.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]