--- 
title: "Anlagenabschreibung über juristische Personen hinweg berechnen"
description: "Dieses Verfahren beschreibt, wie Sie den Abschreibungsprozess für mehrere juristische Personen einrichten und ausführen können."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: de-de
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Anlagenabschreibung über juristische Personen hinweg berechnen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Anlagenabschreibung kann über juristische Personen hinweg in einem Einzelschritt ausgeführt werden. Dieses Verfahren beschreibt, wie Sie den Prozess für mehrere juristische Personen einrichten und ausführen können. Es verwendet die Buchhalterrolle.  

Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.


Schritt(16) Unteraufgabe: Einrichten unternehmensübergreifender Abschreibungs-Ausführungserfassungen. 

1. Zunächst müssen Sie die in der unternehmensübergreifenden Abschreibung zu verwendenden Erfassungen einrichten, die in jeder juristischen Person ausgeführt wird. Wechseln Sie zu "Anlagen" > "Einstellungen" > "Anlagenparameter". 
2. Erweitern Sie den Anlagenvorschlagsabschnitt. 
3. Erstellen Sie einen Datensatz mit dem für jede Buchungsebene in der juristischen Person zu verwendenden Journal. Wenn Bücher nicht im Hauptbuch gebucht werden, sollte keine die Buchungsebene mit dem zugeordneten Journal ausgewählt werden. Klicken Sie auf Hinzufügen. 
4. Geben Sie im Feld 'Buchungsebene' einen Wert ein, oder wählen Sie einen Wert aus. 
5. Geben Sie im Feld 'Journal' einen Wert ein, oder wählen Sie einen Wert aus. 
6. Wiederholen die Erfassungseinrichtung auf der Anlagenparameterseite in jeder juristischen Person. 

Unteraufgabe: Abschreibung berechnen.

1. Verwenden Sie die Seite Abschreibungsvorschlag, um die Abschreibung zu starten, die zu den juristischen Personen ausgeführt wird. Wechseln Sie zu "Anlagen" > "Erfassungseinträge" > "Abschreibungsvorschlag" erstellen. 
2. Geben Sie im Feld 'Buchungsebene' einen Wert ein, oder wählen Sie einen Wert aus. 
3. Der Journalname ist standardmäßig von den Anlagenparametern. Er kann für die aktuelle juristische Person hier geändert werden. 
4. Geben Sie in das Feld "Bis Datum" ein Datum ein. 
5. Dient zum Auswählen der in der Abschreibungsausführung einzubeziehenden juristischen Personen. Nur juristische Personen mit Erfassungen, die für Anlagenvorschläge auf der Anlagenparameterseite eingerichtet werden, werden in der Liste angezeigt. 
6. Wenn dieser Schlüssel aktiviert ist, wird die Beitragserfassungsoption automatisch die Abschreibungserfassungen, wenn sie erstellt werden. Wenn sie nicht ausgewählt ist, werden Erfassungen erstellt, aber nicht gebucht, sodass Sie die Details prüfen, bevor sie gebucht wird. Wählen Sie "Ja" im Feld "Erfassungen buchen" aus. 
7. Filterungsfelder enthalten alle Anlagen und Bücher, Gruppen für die juristischen Personen, die für diese Abschreibungsausführung ausgewählt werden. 
8. Die Stapelverarbeitungsoption ist standardmäßig aktiviert. Wenn diese Option aktiviert ist, werden die Abschreibungserfassungserstellung und Buchung im Hintergrund ausgeführt. 
9. Klicken Sie auf "Erfassung erstellen". 
10. Sie müssen die Abschreibungserfassungen anzeigen, die in der entsprechenden juristischen Personen erstellt werden. Wechseln Sie zu "Anlagen" > "Journaleinträge" > "Anlagenerfassung".

