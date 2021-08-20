---
title: Sicherheitsbestandserfassung verwenden, um die Mindestdeckung zu aktualisieren
description: Diese Prozedur zeigt, wie man die Vorschläge zur Mindestdeckung berechnet, basierend auf früheren Transaktionen, und dann die Artikeldeckung mit dem Vorschlag aktualisiert.
author: ChristianRytt
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 022ec17d0fdc8b1ee204280ecaac40d75e9c1a44974f2bd4a9bb49fa0aa7878e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759430"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Sicherheitsbestandserfassung verwenden, um die Mindestdeckung zu aktualisieren

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie man die Vorschläge zur Mindestdeckung berechnet, basierend auf früheren Transaktionen, und dann die Artikeldeckung mit dem Vorschlag aktualisiert. Dieses wird unter Verwendung der Sicherheitsbestandserfassung getan. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF. Diese Aufgabe ist für den Produktionsplaner bestimmt, um mithilfe davon die Mindestdeckung beizubehalten.


## <a name="create-a-new-safety-stock-journal-name"></a>Einen neuen Sicherheitsbestands-Erfassungsname erstellen
1. Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Masterplanung > Einrichten > Sicherheitsbestand Journalnamen**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Name** den Text'Material' ein.
4. Geben Sie im Feld **Beschreibung** den Text'Material' ein.
5. Schließen Sie die Seite.

## <a name="create-a-safety-stock-journal"></a>Eine Sicherheitsbestandserfassung erstellen
1. Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Masterplanung > Masterplanung > Ausführen > Sicherheitsbestandsberechnung**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus. Wählen Sie den Sicherheitsbestands-Erfassungsname aus, den Sie erstellt haben, zum Beispiel "Material".  
4. Klicken Sie auf **Zeilen erstellen**.
5. Geben Sie im Feld **Von Datum** ein Datum ein.  
6. Geben Sie im Feld **Bis Datum** ein Datum ein.
7. Klicken Sie auf **OK**. Dadurch werden Positionen für Dimensionen erstellt, die Bestandstransaktionen haben.  

## <a name="calculate-proposal"></a>Vorschlag ermitteln
1. Klicken Sie auf **Angebotsberechnung**.
2. Wählen Sie die Option **Durchschnittliches Problem während der Vorlaufzeit** verwenden.
3. Setzen Sie **Multiplikationsfaktor** auf '10'. Der Faktor "Multiplizieren" wird verwendet, um den Vorschlag anzupassen. Weil Demodaten nur einige, wenige Transaktionen haben, müssen Sie den Faktor festlegen, um einen realistischen Vorschlag zu erhalten.  
4. Klicken Sie auf **OK**. Führen Sie einen Bildlauf nach unten durch, um M0002 und M0003 zu suchen. Betrachten Sie die Spalte **Berechnetes Minimum** Menge.   

## <a name="update-minimum-quantity"></a>Mindestmenge aktualisieren
1. Geben Sie im Feld **Neue Mindestmenge** eine Zahl ein. Aktualisieren Sie die "Neue Mindestmenge", damit sie dem Wert in der "Berechneten Mindestmenge" entspricht. Wenn das "Berechnete Minimum" null ist, können Sie den gewünschten zukünftigen Wert eingeben. Zum Beispiel können Sie die "Berechnete Mindestmenge" in diesem Feld für M0002 eingeben, die den Lagerort 12 hat.  
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Zum Beispiel können Sie M0002 auswählen, der Lagerort 12 hat.  
3. Geben Sie im Feld **Neue Mindestmenge** eine Zahl ein. Aktualisieren Sie die "Neue Mindestmenge", damit sie dem Wert in der "Berechneten Mindestmenge" entspricht. Wenn das "Berechnete Minimum" null ist, können Sie den gewünschten zukünftigen Wert eingeben.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Buchen Sie die neue Mindestmenge und überprüfen Sie das Ergebnis
1. Klicken Sie auf **Buchen**.
2. Klicken Sie auf **OK**.
3. Klicken Sie hier, um dem Link im Feld **Artikelnummer** zu folgen.
4. Klicken Sie hier, um dem Link im Feld **Artikelnummer** zu folgen.
5. Klicken Sie im Aktionsbereich **Action Pane** auf Plan.
6. Klicken Sie auf **Einzelteilabdeckung**. Beachten Sie, dass die **Mindestmenge** mit der neuen Mindestmenge aus dem Sicherheitsbestandsjournal aktualisiert wurde.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]