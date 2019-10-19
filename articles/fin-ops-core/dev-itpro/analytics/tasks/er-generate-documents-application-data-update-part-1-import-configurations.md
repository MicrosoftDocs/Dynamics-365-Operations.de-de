---
title: Importieren von Konfigurationen, um Dokumente zu generieren, die Anwendungsdaten haben
description: Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd7a07d041373b266103f313df1bf2810e9c858
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182346"
---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>Importieren von Konfigurationen, um Dokumente zu generieren, die Anwendungsdaten haben

[!include [task guide banner](../../includes/task-guide-banner.md)]

Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.

Die Schritte in dieser Prozedur erläutern, wie elektronische Berichtskonfigurationen (ER) erstellt werden, um elektronische Dokumente zu generieren. In diesem Verfahren importieren Sie eine geänderte Excel-Vorlage in eine ER-Formatkonfigurationen, die für das Beispielunternehmen, Litware, Inc. erstellt wurde, und erstellen dann die elektronischen Dokumente. Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Die Schritte können abgeschlossen werden, indem Sie den DEMF-Datensatz verwenden. Bevor Sie beginnen, laden Sie die Dateien herunter und speichern Sie jene, die im Hilfethema "Generieren Sie elektronische Dokumente und Aktualisierungsbewerbungsdaten mit ER-Tool" (generate-electronic-documents-update-application-data/) aufgeführt sind. Die Dateien sind Intrastat (model).xml, Intrastat (mapping).xml, und Intrastat (format).xml.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
    * Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren” abschließen.  
    * Die Schritte in diesem Verfahren zeigen, wie ER-Funktionen verwendet werden, um Anwendungsdaten zu vervollständigen und wie ein Intrastat-Bericht zu erstellt wird. Die Details des Generieren eines Berichts werden in den Bewerbungstabellen archiviert. Wenn zurzeit der Intrastat-Berichts-Prozess im Intrastat-Formular aktiviert ist, wird das Archivieren auf Grundlage der Logik ausgeführt, die im vorhandenen Quellcode programmiert wird. In diesem Verfahren konfigurieren Sie eine ähnliche jedoch vereinfachte Logik von Anwendungsdaten nur mithilfe des ER-Frameworks. Es werden keine Änderungen am Quellcode vorgenommen.   

## <a name="import-er-configurations"></a>ER Konfigurationen importieren
1. Klicken Sie auf "Berichterstellungskonfigurationen".
2. Klicken Sie auf „Austauschen”.
3. Klicken Sie auf „Aus XML-Datei laden”.
    * Wir fügen eine neue ER-Modellkonfiguration hinzu, die das Datenmodell enthält, das entwickelt wurde, die als Datenquelle für das Generieren des Intrastat-Berichts verwendet werden. Später erweitern Sie diese Datenmodelldefinition, um sie für eine Bewerbungsdatenenaktualisierung zu verwenden, um Details des Intrastat-Berichts-Prozesses zu archivieren.   
    * Navigieren klicken und Intrastat (Modell).xml Datei wäheln.  
4. Klicken Sie auf "OK".
5. Erweitern Sie 'Intrastatmodell' in der Struktur (Modell).
6. Klicken Sie auf Designer.
7. Wählen Sie in der Struktur erweitern 'Für ausgehende Dokumente'.
8. Wählen Sie in der Struktur erweitern 'Für ausgehende Dokumente\Transaktionen.
    * Überprüfe Sie die Struktur des importierten Datenmodells. Beachten Sie, dass der Stammartikel "für ausgehendes Dokument" definiert wird, um dem Datenfluss zum Abrufen der Daten von der Anwendung zu definierten und als Datenquelle verwendet wird, um den Intrastat-Bericht zu generieren. Die "Buchungen (Belegliste)" werden verwendet, um die Liste von Intrastat-Buchungen zu repräsentieren, die gemeldet werden müssen. Da Sie gemeldete Warencodes archivieren, wird die eindeutige Kennung des einzelnen Warencodes "Waren Rec ID (Int64)" in diesem Datenfluss erforderlich.   
9. Schließen Sie die Seite.
10. Klicken Sie auf „Austauschen”.
11. Klicken Sie auf „Aus XML-Datei laden”.
    * Importieren Sie die ER-Zuordnungskonfiguration, die den Datenfluss zum Abrufen der Daten von der Anwendung abruft und dann verwendet, um den Intrastat-Bericht zu generieren. Später erweitern Sie diese Datenmodelldefinition, um sie für eine Bewerbungsdatenenaktualisierung zu verwenden, um Details des Intrastat-Berichts-Prozesses zu archivieren.   
    * Klicken Sie auf Navigieren und wählen Sie die Intrastat (Verknüfpungs).xml Datei.  
12. Klicken Sie auf "OK".
13. Erweitern Sie 'Intrastatmodell' (Modell) in der Struktur.
14. Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Zuordnung)" aus.
15. Klicken Sie auf Designer.
    * Beachten Sie, dass die aktuelle Modellzuordnung den Wert "Zum Modell" im Richtungsfeld enthält. Das bedeutet, dass die Modellzuordnung zum Abrufen der Daten von der Anwendung und das Speichern im Datenmodell erfolgt ist.  
16. Klicken Sie auf Designer.
17. Erweitern Sie in der Struktur Liste.
18. Erweitern Sie in der Struktur Transaktion=Liste.
    * Wiederholen Sie die Struktur der Zuordnung, die das Datenmodell verwendet, das auf der Basis des Stammartikel gefiltert wird, "für ausgehendes Dokument." Beachten Sie, dass die Datenquelle hinzugefügte "Liste" Zugang zu den erforderlichen Anwendungsdaten bietet, die die Liste der Datensätze in der Intrastat-Tabelle ist.  
19. Schließen Sie die Seite.
20. Schließen Sie die Seite.
21. Klicken Sie auf „Austauschen”.
22. Klicken Sie auf „Aus XML-Datei laden”.
    * Importieren Sie die ER-Formatkonfiguration, die den Layout des Intrastat-Berichts und das Auffüllens des Prozesses von Daten im Bericht angegeben. Später erweitern Sie diese Datenmodelldefinition, um sie für eine Bewerbungsdatenenaktualisierung zu verwenden, um Details des Intrastat-Berichts-Prozesses zu archivieren.   
    * Klicken Sie auf Navigieren und wählen Sie die Intrastat (Format).xml Datei.  
23. Klicken Sie auf "OK".
24. Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Format)" aus.
25. Klicken Sie auf Designer.
26. Klicken Sie „Erweitern/reduzieren”.
27. Wählen Sie in der Struktur Datei\Erklärung.
28. Klicken Sie auf die Registerkarte Zuordnung.
29. Wählen Sie in der Struktur Datei
    * Wiederholen Sie die Struktur des Formats, das verwendet wird, um den Intrastat-Bericht zu generieren. Beachten Sie, dass er entwickelt wurde, um damti eine XML-Datei zu generieren, indem Daten vom Datenmodell aufgefüllt, die auf der Basis des Stammartikel "für ausgehendes Dokument" basiert.. Stellen Sie sicher, dass der Name für die enerierte Datei im Benutzerdialogfeldformular definiert wurde (" FN" Datenquelle wird dafür verwendet).   
30. Schließen Sie die Seite.

