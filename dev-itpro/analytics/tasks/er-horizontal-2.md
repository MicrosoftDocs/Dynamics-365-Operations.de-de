--- 
title: "Ausführen eines Formats, das horizontal erweiterbarer Bereiche zum dynamischen Hinzufügen von Spalten in Excel-Berichten für elektronische Berichterstellung verwendet"
description: "In den folgenden Schritten wird erläutert, wie einem Benutzer mit der Rolle Systemadministrator oder elektronischer Berichterstellungsentwickler ein Elektronische Berichterstellung-Format (ER) zur Generierung von Berichten als OPENXML-Arbeitsblätter (Excel) konfigurieren kann, in dem die erforderlichen Spalten als horizontal erweiterbare Bereiche erstellt werden können."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4b859151edd28e39c1f97b2f600da6e304b1d065
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Ausführen eines Formats, das horizontal erweiterbarer Bereiche zum dynamischen Hinzufügen von Spalten in Excel-Berichten für elektronische Berichterstellung verwendet

[!include[task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie einem Benutzer mit der Rolle Systemadministrator oder elektronischer Berichterstellungsentwickler ein Elektronische Berichterstellung-Format (ER) zur Generierung von Berichten als OPENXML-Arbeitsblätter (Excel) konfigurieren kann, in dem die erforderlichen Spalten als horizontal erweiterbare Bereiche erstellt werden können. Diese Schritte können im DEMF-Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie die Schritte in "ER - Verwendung von horizontal erweiterbaren Bereichen zum dynamischen Hinzufügen von Spalten zu Excel-Berichten (Teil 1: Designformat)" ausführen.

Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


## <a name="find-created-format"></a>Erstelltes Format suchen
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie in der Struktur "Finanzdimensions-Beispielmodell".
3. Wählen Sie in der Strukturdarstellung "Finanzdimensionsbeispielmodell\Beispielbericht mit horizontal erweiterbaren Bereichen" aus.

## <a name="execute-format-to-create-excel-output"></a>Format für Excel-Ausgabe ausführen
1. Klicken Sie auf "Ausführen".
2. Geben Sie im Feld "Dimensionsnamen" "BusinessUnit;CostCenter;Department" ein.
    * Geben Sie im Feld 'Dimensionsname' einen Wert ein, oder wählen Sie einen Wert aus.  Um alle Dimensionen für das aktuelle Unternehmen auszuwählen, geben Sie Folgendes ein: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
4. Klicken Sie auf "Filter".
5. Wählen Sie die Zeile für die Sachkontoerfassungstabelle und das Feld Erfassungschargennummer aus.
6. Geben Sie im Feld "Kriterien" den Wert '00057..00058' ein.
    * 00057..00058  
7. Klicken Sie auf "OK".
8. Klicken Sie auf "OK".
    * Prüfen Sie das generierte Ergebnis. Beachten Sie, dass die neu erstellte Excel-Datei dieselbe Anzahl von Spalten enthält, die für Finanzdimensionen ausgewählt wurden. Der in Berichtskopf in diesen Spalten enthält die Namen der Finanzdimensionen. Die Transaktionszeilen in diesen Spalten enthalten die Finanzdimensionen. Führen Sie diesen Bericht aus und wählen Sie unterschiedliche Dimensionen aus, um zu sehen, dass der Bericht nicht von der Anzahl der ausgewählten Dimensionen oder aus der Anzahl der Dimensionen abhängt, die in Dynamics 365 for Finance and Operations, Enterprise Edition für diese Instanz konfiguriert werden.  


