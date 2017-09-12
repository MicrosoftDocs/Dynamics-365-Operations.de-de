--- 
title: Sicherheitsbestandserfassung verwenden, um die Mindestdeckung zu aktualisieren
description: "Diese Prozedur zeigt, wie man die Vorschläge zur Mindestdeckung berechnet, basierend auf früheren Transaktionen, und dann die Artikeldeckung mit dem Vorschlag aktualisiert."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d278b20724006ec3b3aa557738e8b130ca2bba15
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# Sicherheitsbestandserfassung verwenden, um die Mindestdeckung zu aktualisieren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie man die Vorschläge zur Mindestdeckung berechnet, basierend auf früheren Transaktionen, und dann die Artikeldeckung mit dem Vorschlag aktualisiert. Dieses wird unter Verwendung der Sicherheitsbestandserfassung getan. Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF. Diese Aufgabe ist für den Produktionsplaner bestimmt, um mithilfe davon die Mindestdeckung beizubehalten.


## Einen neuen Sicherheitsbestands-Erfassungsname erstellen
1. Wechseln Sie zu Sicherheitsbestands-Erfassungsnamen.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" die Bezeichnung "Material" ein.
4. Geben Sie im Feld "Beschreibung" die Bezeichnung "Material" ein.
5. Schließen Sie die Seite.

## Eine Sicherheitsbestandserfassung erstellen
1. Wechseln Sie zu Sicherheitsbestandsberechnung.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie den Sicherheitsbestands-Erfassungsname aus, den Sie erstellt haben, zum Beispiel "Material".  
4. Klicken Sie auf "Positionen erstellen".
5. Geben Sie in das Feld "Von Datum" ein Datum ein.
    * Legen Sie das Datum auf "02.01.2015" fest.  
6. Geben Sie in das Feld "Bis Datum" ein Datum ein.
    * Legen Sie das Datum auf "30.12.2015" fest.  
7. Klicken Sie auf "OK".
    * Dadurch werden Positionen für Dimensionen erstellt, die Bestandstransaktionen haben.  

## Vorschlag ermitteln
1. Klicken Sie auf "Vorschlag berechnen".
2. Wählen Sie die Option "Durchschnittliche Abgänge während Lieferzeit verwenden".
3. Legen Sie den Multiplikationsfaktor auf "10" fest.
    * Der Faktor "Multiplizieren" wird verwendet, um den Vorschlag anzupassen. Weil Demodaten nur einige, wenige Transaktionen haben, müssen Sie den Faktor festlegen, um einen realistischen Vorschlag zu erhalten.  
4. Klicken Sie auf "OK".
    * Führen Sie einen Bildlauf nach unten durch, um M0002 und M0003 zu suchen. Zeigen Sie die Spalte "Berechnete Mindestmenge" an.   

## Mindestmenge aktualisieren
1. Geben Sie im Feld "Neue Mindestmenge" eine Zahl ein.
    * Aktualisieren Sie die "Neue Mindestmenge", damit sie dem Wert in der "Berechneten Mindestmenge" entspricht. Wenn das "Berechnete Minimum" null ist, können Sie den gewünschten zukünftigen Wert eingeben. Zum Beispiel können Sie die "Berechnete Mindestmenge" in diesem Feld für M0002 eingeben, die den Lagerort 12 hat.  
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Zum Beispiel können Sie M0002 auswählen, der Lagerort 12 hat.  
3. Geben Sie im Feld "Neue Mindestmenge" eine Zahl ein.
    * Aktualisieren Sie die "Neue Mindestmenge", damit sie dem Wert in der "Berechneten Mindestmenge" entspricht. Wenn das "Berechnete Minimum" null ist, können Sie den gewünschten zukünftigen Wert eingeben.  

## Buchen Sie die neue Mindestmenge und überprüfen Sie das Ergebnis
1. Klicken Sie auf "Buchen".
2. Klicken Sie auf "OK".
3. Klicken Sie, um dem Link im Feld "Artikelnummer" zu folgen.
4. Klicken Sie, um dem Link im Feld "Artikelnummer" zu folgen.
5. Klicken Sie im Aktivitätsbereich auf "Plan".
6. Klicken Sie auf "Artikeldeckung".
    * Beachten Sie, dass die "Mindestmenge" mit der neuen Mindestmenge aus der Sicherheitsbestandserfassung aktualisiert wurde.  


