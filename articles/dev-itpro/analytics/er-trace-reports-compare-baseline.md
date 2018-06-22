---
title: Erstellte Berichtsergebnisse protokollieren und mit Ausgangswerten vergleichen
description: "Dieses Thema enthält Informationen dazu, wie Sie die Ergebnisse von generierten ER-Berichten mit Basisberichtswerten vergleichen können."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 1a598d0bd053c60c3f8df6b05ecb7ff15addfaa3
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2018

---

# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Erstellte Berichtsergebnisse protokollieren und mit Ausgangswerten vergleichen

[!include[banner](../includes/banner.md)]

Sie können die Ergebnisse von ER-Formaten protokollieren, die ausgehende elektronische Dokumente erstellen. Wenn die Protokollgenerierung eingeschaltet ist (ER-Benutzerparameter **Im Debugmodus ausführen**), wird bei jeder Ausführung eines ER-Reports ein neuer Protokolldatenatz im Ausführungsprotokoll des ER-Formats erzeugt. In jeder erzeugten Protokollierung werden die folgenden Details gespeichert:

- Alle Warnungen, die von Validierungsregeln generiert wurden
- Alle Fehler, die durch Validierungsregeln generiert wurden 
- Alle erzeugten Dateien, die als Anlagen des Protokolldatensatzes gespeichert sind.

Sie können einzelne Basisanwendungsdateien für jedes ER-Format speichern. Dateien gelten als Basisdateien, wenn sie die erwarteten Ergebnisse von Berichten beschreiben, die ausgeführt werden. Wenn eine Basisdatei für ein ER-Format verfügbar ist, das bei eingeschalteter Protokollgenerierung ausgeführt wurde, speichert die Protokollierung zusätzlich zu den bereits erwähnten Details das Ergebnis des Vergleichs des erzeugten elektronischen Dokuments mit der Basisdatei. Mit einem Klick erhalten Sie auch das generierte elektronische Dokument und seine Basisdatei in einer einzigen Zip-Datei. Sie können dann einen detaillierten Vergleich durchführen, indem Sie ein externes Tool wie Windiff verwenden.

Sie können die Protokollierung auswerten, um zu analysieren, ob die erzeugten elektronischen Dokumente den erwarteten Inhalt enthalten. Sie können diese Auswertung in einer UAT-Umgebung (User Acceptance Testing) durchführen, wenn die Codebasis geändert wurde (z. B. wenn Sie auf eine neue Instanz der Anwendung migriert, Hotfixpakete installiert oder Code-Änderungen implementiert haben). Auf diese Weise können Sie sicherstellen, dass die Auswertung keine Auswirkungen auf die Ausführung der verwendeten ER-Berichte hat. Bei vielen ER-Berichten kann die Auswertung im unbeaufsichtigten Modus erfolgen.

Um mehr über diese Funktion zu erfahren, spielen Sie die Aufgabenleitfäden **ER Berichte erstellen und Ergebnisse vergleichen (Teil 1)** und **ER Berichte erstellen und Ergebnisse vergleichen (Teil 2)** ab, die Teil des **7.5.4.3 Test IT-Services/Lösungen (10679)** Geschäftsprozess sind und im [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) heruntergeladen werden können. Diese Aufgabenleitfäden führen Sie durch den Prozess der Konfiguration des ER-Frameworks zur Verwendung von Basisdateien für die Auswertung generierter elektronischer Dokumente.

