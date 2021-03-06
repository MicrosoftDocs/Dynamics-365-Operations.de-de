---
title: 'ER – Horizontal erweiterbare Bereiche zum dynamischen Hinzufügen von Spalten in Excel-Berichten nutzen (Teil 2: Format ausführen)'
description: In diesem Thema wird beschrieben, wie Sie ein EB-Format (elektronische Berichterstellung) konfigurieren, um Berichte als Excel-Dateien (OPENXML-Arbeitsblätter) zu generieren. (Teil 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a62bad6ca241a2372a72e312ec5a707008a5fc09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744986"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER – Horizontal erweiterbare Bereiche zum dynamischen Hinzufügen von Spalten in Excel-Berichten nutzen (Teil 2: Format ausführen)

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie einem Benutzer mit der Rolle Systemadministrator oder elektronischer Berichterstellungsentwickler ein Elektronische Berichterstellung-Format (ER) zur Generierung von Berichten als OPENXML-Arbeitsblätter (Excel) konfigurieren kann, in dem die erforderlichen Spalten als horizontal erweiterbare Bereiche erstellt werden können. Diese Schritte können im DEMF-Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie die Schritte in „ER - Verwendung von horizontal erweiterbaren Bereichen zum dynamischen Hinzufügen von Spalten zu Excel-Berichten (Teil 1: Designformat)“ ausführen.

Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


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
    * Prüfen Sie das generierte Ergebnis. Beachten Sie, dass die neu erstellte Excel-Datei dieselbe Anzahl von Spalten enthält, die für Finanzdimensionen ausgewählt wurden. Der in Berichtskopf in diesen Spalten enthält die Namen der Finanzdimensionen. Die Transaktionszeilen in diesen Spalten enthalten die Finanzdimensionen. Führen Sie diesen Bericht aus und wählen Sie unterschiedliche Dimensionen aus, um zu sehen, dass der Bericht nicht von der Anzahl der ausgewählten Dimensionen oder aus der Anzahl der Dimensionen abhängt, die für diese Instanz konfiguriert werden.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]