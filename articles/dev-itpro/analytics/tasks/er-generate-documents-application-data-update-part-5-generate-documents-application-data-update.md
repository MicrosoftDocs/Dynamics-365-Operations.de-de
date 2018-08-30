--- 
title: Generieren von Dokumenten, die Anwendungsdaten haben
description: "Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, \"ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 4: Ändern Sie das Format)\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 90c6ebc456d3e137e43022fad7d59ce3ca2cdcab
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="generate-documents-that-have-application-data"></a>Generieren von Dokumenten, die Anwendungsdaten haben

[!include [task guide banner](../../includes/task-guide-banner.md)]

Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 4: Ändern Sie das Format)".



Die Schritte in dieser Prozedur erläutern, wie elektronische Berichtskonfigurationen (ER) erstellt werden, um elektronische Dokumente zu generieren. In diesem Verfahren führen Sie die ER-Formatkonfiguration aus, um die Intrastat-Berichts- und Aktualisierungsbewerbungsdaten für das Archivieren von Details des Generieren eines Berichts zu generieren.



Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Die Schritte können abgeschlossen werden, indem Sie den DEMF-Datensatz verwenden. Bevor Sie beginnen, stellen Sie sicher, dass der Landkontext für das DEMF-Unternehmen BEL (Belgien) ist.


## <a name="set-up-foreign-trade-parameters"></a>Außenhandelsparameter einrichten
1. Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Außenhandelsparameter".
2. Klicken Sie auf die Registerkarte "Nummernkreis".
    * Zum Archivieren der Details des Intrastat-Berichterstattungsprozess müssen wir Datensätze jedes Archivs, das wir erstellt haben identifizieren. Ein spezieller Nummernkreis muss konfiguriert werden.  
3. Wählen Sie die Intrastat-Archiv "ID-" Referenz aus.
4. Geben Sie im Feld "Nummernkreiscode" einen Wert ein.
    * Geben Sie im Feld "Nummernsequenzcode" einen Wert ein, oder wählen Sie einen Wert aus.  
5. ResolveChanges den Nummersequenzcode.
6. Klicken Sie auf "Speichern".
7. Schließen Sie die Seite.

## <a name="run-modified-er-format"></a>Führen Sie geändertes ER-Format aus
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie 'Intrastatmodell' (Modell) in der Struktur.
3. Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Format)" aus.
4. Klicken Sie auf "Ausführen".
5. Geben Sie im Feld Tabelle den Typ intrastat2.xml ein.
    * intrastat2.xml  
6. Klicken Sie auf "OK".

## <a name="review-er-format-executions-results"></a>Überprüfen Sie die Ergebnisse der ER-Formatausführung
    * Erstellte XML Datei überprüfen.  
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".
    * Öffnen Sie dieses Formular, das die Intrastat-Buchungen enthält, die im generierten elektronischen Dokument enthalten sind.  
3. Intrastat-Archivkennung anklicken.
    * Da das ausgeführte ER-Format nur Einstellungen für Anwendungsdatenenaktualisierungen enthält, wurden die Details des abgeschlossenen Intrastat-Bericht archiviert. In diesem Formular können Sie den Headerdatensatz des erstellten Dokumentarchivs finden.  
4. Klicken Sie auf Details.
    * In diesem Formular können Sie die Details für das erstellte Dokumentarchiv finden.  
5. Schließen Sie die Seite.
6. Schließen Sie die Seite.
7. Schließen Sie die Seite.


