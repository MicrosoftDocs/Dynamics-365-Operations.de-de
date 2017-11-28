---
title: Statistische Grundplanung generieren
description: "Dieser Artikel enthält Informationen zu den Parametern und Filtern, die in der Berechnung der Bedarfsplanung verwendet werden."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c71d7632cfdafe48eee49c848982dfa85116df75
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="generate-a-statistical-baseline-forecast"></a>Statistische Grundplanung generieren

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zu den Parametern und Filtern, die in der Berechnung der Bedarfsplanung verwendet werden. 

Wenn Sie eine Grundplanung erstellen, müssen Sie zunächst die Parameter und die Filter angeben, die bei der Berechnung verwendet werden. So können Sie z. B. eine Grundplanung erstellen, die Bedarf basierend auf Buchungsdaten vom letzten Jahr für ein bestimmtes Unternehmen, für den kommenden Monat und für eine ausgewählte Gruppe von Artikeln einschätzt. 

Um eine Bedarfsplanung zu generieren, wechseln Sie zu **Produktprogrammplan &gt;Planung &gt; Bedarfsplanung &gt;Statistische Grundplanung generieren**. 

Der Planungszeitrahmen kann zum Zeitpunkt der Planunsgenerierung ausgewählt werden. Die verfügbaren Werte sind Tag, Woche und Monat. 

Die Anzahl von Planungszeitrahmen, für die die Planung generiert wird, wird im Feld **Planungshorizont** festgelegt. 

Wenn die Planungsstrategie auf **Über historischen Bedarf kopieren** festgelegt ist, wird das Ende des historischen Horizonts ignoriert. Das System kopiert die Anzahl der Zeitrahmen, die im Feld **Planungshorizont** angegeben ist, in den Planungsbedarf, beginnend ab dem Startdatum im Feld **Von Datum** unter **Historischer Horizont**. Indem historischer Bedarf von einem bestimmten Datum in ein zukünftiges Datum kopiert wird, können Produktionsplaner den Plan für die nächsten Quartale auf zwei Arten erstellen:

-   Durch Kopieren des Bedarfs aus demselben Quartal im letzten Jahr
-   Durch Kopieren des Bedarfs aus vorherigen Quartal

Um Unklarheiten in den Produktionsplänen zu verhindern, können mehrere Planungszeitrahmen eingefroren werden. Diese Zahl wird im Feld **Nichtplanungszeitraum** festgelegt. Auf der Seite **Angepasste Bedarfsplanung** werden die Zellen für die fixierten Zeitrahmen deaktiviert, um optisch anzugeben, dass diese Werte nicht geändert werden sollen. 

Das Startdatum für die Grundbedarfsplanung muss nicht das aktuelle Datum oder ein Datum in der Zukunft sein. Um ein anderes Startdatum festzulegen, verwenden Sie das Feld **Startdatum für statistische Grundplanung - Von Datum**. So können Benutzer im Juni beispielswseise eine Planung für das nächste Jahr generieren. Da die Planungszeitrahmen zwischen dem Ende des historischen Bedarfs und dem Beginn der Grundbedarfs fehlen, sind die Vorhersagen nicht genau. Wenn Sie den Microsoft Dynamics 365 for Finance and Operations -Bedarfsplanungsdienst verwenden, gibt es vier Arten, auf die Sie die fehlenden Lücken ausfüllen können. Sie können die Methode auswählen, die Sie wünschen, indem Sie den MISSING\_VALUE\_SUBSTITUTION-Parameter auf der Seite **Bedarfsplanungsparameter** festlegen. 

Das Feld **Startdatum für statistische Grundplanung** - **Von Datum** muss auf den Beginn eines Planungszeitrahmens festgelegt werden, beispielsweise in den USA ein Sonntag, wenn der Planungszeitrahmen die Woche ist. Das System reguliert automatisch das Feld **Startdatum für statistische Grundplanung** - **Von Datum**, um den Beginn eines Planungszeitrahmens abzugleichen. 

Das Feld **Startdatum für statistische Grundplanung** - **Von Datum** kann auf ein Datum in der Vergangenheit gesetzt werden. Das bedeutet, es ist möglich, eine Bedarfsplanung in der Vergangenheit zu generieren. Dies ist hilfreich, da Benutzer die Planungsdienstparameter ändern können, damit die statistische Planung, die in der Vergangenheit generiert wurde, mit dem tatsächlichen historischen Bedarf übereinstimmt. Benutzer können mithilfe dieser Parametereinstellungen dann fortfahren, um eine statistische Grundplanung für die Zukunft zu erstellen. 

Die manuellen Anpassungen, die in den vorherigen Bedarfsplanungsiterationen vorgenommen wurden, können automatisch in die neue Grundplanung übernommen werden, wenn das Kontrollkästchen **Manuelle Anpassungen auf Bedarfsplanung übertragen** aktiviert ist. Wenn das Kontrollkästchen deaktiviert ist, werden die manuellen Anpassungen nicht zur Grundplanung hinzugefügt, sie werden jedoch nicht gelöscht. Die manuellen Anpassungen, die an einer Planung vorgenommen werden, können nur zum Zeitpunkt des Planungsimports gelöscht werden, indem das Kontrollkästchen **Manuelle Anpassungen der Grundbedarfsplanung speichern** deaktiviert wird. Manuelle Anpassungen werden zum Zeitpunkt der Autorisierung gespeichert. Wenn ein Benutzer manuelle Anpassungen an der Planung vornimmt, aber die Planung nicht in Dynamics 365 for Finance and Operations autorisiert, gehen die Änderungen daher verloren. Weitere Informationen zu manuellen Anpassungen und dazu, wie sie arbeiten, finden Sie unter [Autorisieren der angepassten Planung](authorize-adjusted-forecast.md). 

Eine Bedarfsplanungsgenerierung kann einen Namen und Kommentare haben, damit Benutzer die Planung erkennen können, die generiert wurde. Diese Werte werden im Generierungsverlauf der Planung auf der Seite **Generierungsverlauf statistische Grundplanung** angezeigt. 

Die Intercompany-Planungsgruppe, die Artikelverteilungsschlüssel und andere Filter können zum Zeitpunkt der Planungsgenerierung angewendet werden. Sie können verwendet werden, um die Leistung zu verbessern oder die Daten in überschaubare Blöcke aufzuteilen. Beachten Sie jedoch, dass keine Bedarfsplanung für die Mitglieder eines Artikelverteilungsschlüssels generiert wird, der keiner Intercompany-Planungsgruppe zugeordnet ist, auch wenn der Artikelverteilungsschlüssel in der Abfrage ausgewählt wird. 

**Tipp**: Manchmal erhalten Benutzer Fehler, während sie eine Bedarfsplanung generieren oder die Planungsgenerierung wird ohne Sitzungsprotokoll abgeschlossen. Dies kann aufgrund der übrigen Daten in der Abfrage auftreten, die zuvor für die Planungsgenerierung verwendet wurde. Um dieses Problem zu beheben, klicken Sie auf **Auswählen**, um die Seite **Abfrage** zu öffnen, klicken Sie auf **Zurücksetzen**, und generieren Sie die Grundplanung neu. 

Wenn die Planung nicht für einen großen Satz Artikel generiert wird, sondern beispielsweise jeweils für einen Artikel oder einen Artikelverteilungsschlüssel, dann können Sie für eine bessere Leistung das Kontrollkästchen **Anforderungsantwortmodus verwenden** auf der Registerkarte **Produktprogrammplan - Einstellungen - Bedarfsplanung**  -  **Bedarfsplanungsparameter - Azure Machine Learning** aktivieren.

<a name="see-also"></a>Siehe auch
--------

[Einrichten einer Bedarfsplanung](demand-forecasting-setup.md)

[Manuelle Anpassungen an die Grundplanung](manual-adjustments-baseline-forecast.md)

[Autorisieren der angepassten Planung](authorize-adjusted-forecast.md)




