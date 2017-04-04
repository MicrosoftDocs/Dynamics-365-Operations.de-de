---
title: Abschluss des Hauptbuchs am Ende der Periode
description: "In diesem Thema werden die Aufgaben beschrieben, die in der Regel ausgeführt werden, wenn ein Periodenabschluss für Hauptbuch ausgeführt wird."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: a7b72dfa98758b14d303d09890bd46729b1cdbe9
ms.lasthandoff: 03/31/2017


---

# <a name="close-the-general-ledger-at-period-end"></a>Abschluss des Hauptbuchs am Ende der Periode

In diesem Thema werden die Aufgaben beschrieben, die in der Regel ausgeführt werden, wenn ein Periodenabschluss für Hauptbuch ausgeführt wird. 

Im Hauptbuch können Sie Abschlussprozeduren für eine Periode oder ein Jahr ausführen. Abschlussvorgänge bereiten das System auf eine neue Periode vor. Um das System für ein neues Jahr erstellen, müssen Sie den Schließenprozess mit unterschiedlichen Geschäftsjahresenddaten ausführen. Jede Organisation gelten unterschiedliche Verfahren und Schritte, die sie für das Ende einer Periode ausgeführt wird. Nachfolgend sind einige Schritte für optionale Periodenenden:

-   Schließen Sie alle Aufgaben für alle anderen Module ab, z. B. Debitoren, Kreditoren und Bestand.
-   Überprüfen Sie, ob alle Erfassungen gebucht werden.
-   Führen Sie die Neubewertung der Fremdwährung aus, um alle unrealisierten Gewinn- oder Verlustbeträge zu generieren.
-   Gleichen Sie Buchungen für jedes Sachkonto aus.
-   Verarbeiten Sie alle erforderlichen Zuteilungen.
-   Buchen Sie manuelle Regulierungen für das Ende der Periode.
-   Journalisieren Sie Transaktionen und überprüfen Sie den **Sachkontoerfassungs** Bericht.
-   Führen Sie eine Konsolidierung aus, indem Sie ein Konsolidierungsunternehmen oder eine Finanzberichterstellung verwenden.
-   Generieren Sie Finanzaufstellungen zum Periodenende, indem Sie Finanzberichterstellung verwenden.
-   Legen Sie Sachkontoperioden auf **Gesperrt** fest, damit keine weitere Buchung stattfindet. Sie können für bessere Kontrolle eine Periode auf eine bestimmte Benutzergruppe begrenzen, wenn Aktivitäten zum Periodenende auftreten. Es ist keine der Entlassung, Perioden auf festzulegen ** dauerhaft geschlossen **, da Sie eine Frist nicht erneut geöffnet werden können, die abgeschlossen wurde.

Der Finanzperiodenschließenarbeitsbereich kann verwendet werden, um Aufgaben zum Organisieren und verfolgen, die für verschiedene Periodenendenprozesse erforderlich sind. Siehe Finanzperiodenschließenarbeitsbereich [] () und das financial-period-close-workspace.md Jahresabschluss [] () Year-end-close.md Themen unter. 




