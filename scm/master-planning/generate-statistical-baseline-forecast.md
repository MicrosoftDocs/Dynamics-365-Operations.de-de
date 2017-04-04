---
title: Generieren einer statistische Grundplanung
description: "Dieser Artikel enthält Informationen zu den Parametern und Filtern, die in der Berechnung der Bedarfsplanung verwendet werden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c0c918b94fe96d123bb6c25c42fe168a026cd8a9
ms.lasthandoff: 03/31/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Generieren einer statistische Grundplanung

Dieser Artikel enthält Informationen zu den Parametern und Filtern, die in der Berechnung der Bedarfsplanung verwendet werden. 

Wenn Sie eine Grundplanung erstellen, müssen Sie zunächst die Parameter und die Filter angeben, die bei der Berechnung verwendet werden. So können Sie z. B. eine Grundplanung erstellen, die Bedarf basierend auf Buchungsdaten vom letzten Jahr für ein bestimmtes Unternehmen, für den kommenden Monat und für eine ausgewählte Gruppe von Artikeln einschätzt. 

Um eine Bedarfsplanung zu generieren, fahren Sie Produktprogrammplanungs-Planungs-Bedarfsplanung &gt; ** generieren statistische Grundplanung **. 

Der Planungszeitrahmen kann zum Zeitpunkt der Planunsgenerierung ausgewählt werden. Die verfügbaren Werte sind Tag, Woche und Monat. 

Die Anzahl von Planungszeitrahmen, für die die Planung generiert wird, wird im Feld **Planungshorizont** festgelegt. 

Wenn die Planungsstrategie auf **Über historischen Bedarf kopieren** festgelegt ist, wird das Ende des historischen Horizonts ignoriert. Das System kopiert die Anzahl von den Buckets, die, die im Feld angegeben sind Planungshorizont ** ** Feld z Planungsbedarf und vom Datum abgeglichen wird, das im Feld festgelegt ist ** Von-Datum ** Feld unter ** historischer Horizont **. Indem historischer Bedarf von einem bestimmten Datum in ein zukünftiges Datum kopiert wird, können Produktionsplaner den Plan für die nächsten Quartale auf zwei Arten erstellen:

-   Durch Kopieren des Bedarfs aus demselben Quartal im letzten Jahr
-   Durch Kopieren des Bedarfs aus vorherigen Quartal

Um Unklarheiten in den Produktionsplänen zu verhindern, können mehrere Planungszeitrahmen eingefroren werden. Diese Zahl wird im Feld **Nichtplanungszeitraum** festgelegt. Auf der Seite **Angepasste Bedarfsplanung** werden die Zellen für die fixierten Zeitrahmen deaktiviert, um optisch anzugeben, dass diese Werte nicht geändert werden sollen. 

Das Startdatum für die Grundbedarfsplanung muss nicht das aktuelle Datum oder ein Datum in der Zukunft sein. Um ein anderes Startdatum festzulegen, verwenden Sie das Feld **Startdatum für statistische Grundplanung - Von Datum**. So können Benutzer im Juni beispielswseise eine Planung für das nächste Jahr generieren. Da die Planungszeitrahmen zwischen dem Ende des historischen Bedarfs und dem Beginn der Grundbedarfs fehlen, sind die Vorhersagen nicht genau. Wenn Sie das Microsoft Dynamics 365 für Arbeitsgangs-Bedarfsplanungs-Service verwenden, gibt es vier Arten, die Sie die fehlenden Lücken in ausgefüllt werden kann. Sie können die Methode auswählen, die Sie wünschen, indem Sie den FEHLENDEN \_WERT\_ERSETZUNGSparameter auf der Seite Bedarfsplanungsparameter ** ** festlegen. 

** Basis geplante Startdatum ** - ** Von-Datum ** Feld muss auf den Beginn eines Planungsbuckets beispielsweise in den USA festgelegt werden, ein Sonntag, wenn der Planungsbucket die Woche beträgt. Das System automatisch angepasst ** Basisplanungsstartdatum ** - ** Von-Datum ** das Feld, um den Anfangs- eines Planungsbuckets abzugleichen. 

** Basis geplante Startdatum ** - ** Von-Datum ** Feld kann auf ein Datum in der Vergangenheit gelegt werden. Das bedeutet, es ist möglich, eine Bedarfsplanung in der Vergangenheit zu generieren. Dies ist hilfreich, da Benutzer die Planungsdienstparameter ändern können, damit die statistische Planung, die in der Vergangenheit generiert wurde, mit dem tatsächlichen historischen Bedarf übereinstimmt. Benutzer können mithilfe dieser Parametereinstellungen dann fortfahren, um eine statistische Grundplanung für die Zukunft zu erstellen. 

Die manuellen Anpassungen, die in den vorherigen Bedarfsplanungsiterationen vorgenommen wurden, können automatisch in die neue Grundplanung übernommen werden, wenn das Kontrollkästchen **Manuelle Anpassungen auf Bedarfsplanung übertragen** aktiviert ist. Wenn das Kontrollkästchen deaktiviert ist, werden die manuellen Anpassungen nicht zur Grundplanung hinzugefügt, sie werden jedoch nicht gelöscht. Die manuellen Anpassungen, die an einer Planung vorgenommen werden, können nur zum Zeitpunkt des Planungsimports gelöscht werden, indem das Kontrollkästchen **Manuelle Anpassungen der Grundbedarfsplanung speichern** deaktiviert wird. Manuelle Anpassungen werden zum Zeitpunkt der Autorisierung gespeichert. Wenn ein Benutzer die manuelle Anpassungen der Planung vorgenommen, aber über die Planung nicht in Dynamics 365 für Arbeitsgänge, die verloren Änderungen sind. Weitere Informationen zum manuellen Regulierungen und wie sie arbeiten, finden Sie die angepasste Planung [] (authorize-adjusted-forecast.md) autorisierend. 

Eine Bedarfsplanungsgenerierung kann einen Namen und Kommentare haben, damit Benutzer die Planung erkennen können, die generiert wurde. Diese Werte werden im Generierungsverlauf der Planung auf der Seite **Generierungsverlauf statistische Grundplanung** angezeigt. 

Die Intercompany-Planungsgruppe, die Artikelverteilungsschlüssel und andere Filter können zum Zeitpunkt der Planungsgenerierung angewendet werden. Sie können verwendet werden, um die Leistung zu verbessern oder die Daten in überschaubare Blöcke aufzuteilen. Beachten Sie jedoch, dass keine Bedarfsplanung für die Mitglieder eines Artikelverteilungsschlüssels generiert wird, der keiner Intercompany-Planungsgruppe zugeordnet ist, auch wenn der Artikelverteilungsschlüssel in der Abfrage ausgewählt wird. 

**Tipp**: Manchmal erhalten Benutzer Fehler, während sie eine Bedarfsplanung generieren oder die Planungsgenerierung wird ohne Sitzungsprotokoll abgeschlossen. Dies kann aufgrund der übrigen Daten in der Abfrage auftreten, die zuvor für die Planungsgenerierung verwendet wurde. Um dieses Problem zu beheben, klicken Sie auf **Auswählen**, um die Seite **Abfrage** zu öffnen, klicken Sie auf **Zurücksetzen**, und generieren Sie die Grundplanung neu. 

Wenn die Planung nicht für einen großen Gruppe von Artikeln, sondern, beispielsweise, für einen Artikel oder einen Artikelverteilungsschlüssel gleichzeitig generiert wird, dann, um eine bessere Leistung abzurufen, können Sie das verwenden Sie Anforderungswartemodus ** ** Kontrollkästchen auf der Produktprogrammplanung ** - Einstellungen aktivieren - Bedarfsplanung **** - - Azure Lernfähigkeit einer Maschine ** Registerkarte.

<a name="see-also"></a>Siehe auch
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)


