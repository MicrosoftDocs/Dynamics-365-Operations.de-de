---
title: Abschluss des Hauptbuchs am Ende der Periode
description: In diesem Thema werden die Aufgaben beschrieben, die in der Regel ausgeführt werden, wenn ein Periodenabschluss für Hauptbuch ausgeführt wird.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23d4b9b070a48e1964ecd6896afe071b564d1194
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "329297"
---
# <a name="close-the-general-ledger-at-period-end"></a>Abschluss des Hauptbuchs am Ende der Periode

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Aufgaben beschrieben, die in der Regel ausgeführt werden, wenn ein Periodenabschluss für Hauptbuch ausgeführt wird. 

Im Hauptbuch können Sie Abschlussprozeduren für eine Periode oder ein Jahr ausführen. Abschlussvorgänge bereiten das System auf eine neue Periode vor. Um das System auf ein neues Jahr vorzubereiten, müssen Sie den Jahresabschlussprozess ausführen. Jede Organisation hat unterschiedliche Verfahren und Schritte, die für das Ende einer Periode ausgeführt werden. Nachfolgend sind einige Schritte für optionale Periodenenden beschrieben:

-   Schließen Sie alle Aufgaben für alle anderen Module ab, z. B. Debitoren, Kreditoren und Bestand.
-   Überprüfen Sie, ob alle Erfassungen gebucht werden.
-   Führen Sie die Neubewertung der Fremdwährung aus, um alle unrealisierten Gewinn- oder Verlustbeträge zu generieren.
-   Gleichen Sie Buchungen für jedes Sachkonto aus.
-   Verarbeiten Sie alle erforderlichen Zuteilungen.
-   Buchen Sie manuelle Regulierungen für das Ende der Periode.
-   Journalisieren Sie Transaktionen und überprüfen Sie den **Sachkontoerfassungs** Bericht.
-   Führen Sie eine Konsolidierung aus, indem Sie ein Konsolidierungsunternehmen oder eine Finanzberichterstellung verwenden.
-   Generieren Sie Finanzaufstellungen zum Periodenende, indem Sie Finanzberichterstellung verwenden.
-   Legen Sie Sachkontoperioden auf **Gesperrt** fest, damit keine weitere Buchung stattfindet. Sie können für bessere Kontrolle eine Periode auf eine bestimmte Benutzergruppe begrenzen, wenn Aktivitäten zum Periodenende auftreten. Es ist nicht sinnvoll, Perioden auf **Ständig Geschlossen** festzulegen, da eine geschlossene Periode nicht erneut geöffnet werden kann.

Der Arbeitsbereich Finanzperioden schließen kann verwendet werden, um die Aufgaben, die für verschiedene Periodenendenprozesse erforderlich sind, zu organisieren und nachzuverfolgen. 


Weitere Informationen zu Workflows finden Sie unter den folgenden Themen:
- [Finanzperiodenabschluss-Arbeitsbereich](financial-period-close-workspace.md) 
- [Jahresabschluss](Year-end-close.md)  
- [Massen-Finanzperiodenabschluss](tasks/mass-financial-period-close.md)




