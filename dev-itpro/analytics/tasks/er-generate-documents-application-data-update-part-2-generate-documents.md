--- 
title: "Generieren von Dokumenten mit Anwendungsdatenupdate für elektronische Berichterstellung (ER)"
description: "Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, \"ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 1 - Importkonfigurationen)."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f10faaaffeb7df5be0b37a9b8dbfa5db5c24d2a2
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Generieren von Dokumenten mit Anwendungsdatenupdate für elektronische Berichterstellung (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 1: Importkonfigurationen).



Die Schritte in dieser Prozedur erläutern, wie elektronische Berichtskonfigurationen (ER) erstellt werden, um elektronische Dokumente zu generieren. In diesem Beispiel erstellen Sie die erforderlichen ER-Konfigurationen für das Beispielunternehmen Litware, Inc., um elektronische Dokumentd zu erstellen.



Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Die Schritte können abgeschlossen werden, indem Sie den DEMF-Datensatz verwenden. 



Bevor Sie beginnen, ändern Sie den Landkontext für das DEMF-Unternehmen DEU (Deutschland) zu BEL (Belgien). Klicken Sie auf Organisationsverwaltung >Organisation >Juristische Personen, um den Ländercode in der primären Adresse der juristischen Person DEMF zu aktualisieren. Starten Sie Ihre Anwendung neu.


## <a name="run-imported-er-format"></a>Führen Sie das importierte ER-Format aus
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie 'Intrastatmodell' (Modell) in der Struktur.
3. Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Format)" aus.
4. Klicken Sie auf "Ausführen".
    * Führt die Entwurfsversion der ER-Formatkonfiguration aus, um den Intrastat-Bericht zu generieren.  
5. Geben Sie im Feld Tabelle den Typ Intrastat.xml ein.
    * Namen der Datei angeben.  
6. Klicken Sie auf "OK".
    * Erstellte XML Datei überprüfen.  
7. Schließen Sie die Seite.
8. Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".
    * Öffnen Sie dieses Formular, das die Intrastat-Buchungen enthält, die im generierten elektronischen Dokument enthalten sind.  
9. Intrastat-Archivkennung anklicken.
    * Da das ausgeführte ER-Format nur Einstellungen für Anwendungsdatenenaktualisierungen enthält, wurden die Details des abgeschlossenen Intrastat-Bericht archiviert.  
10. Schließen Sie die Seite.
11. Schließen Sie die Seite.


