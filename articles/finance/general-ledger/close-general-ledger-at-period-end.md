---
title: Abschluss des Hauptbuchs am Ende der Periode
description: In diesem Thema werden die Aufgaben beschrieben, die in der Regel ausgeführt werden, wenn ein Periodenabschluss für Hauptbuch ausgeführt wird.
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 359e177e4ac2218c28ddd7c5ac3b71ee69e652e8
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717529"
---
# <a name="close-the-general-ledger-at-period-end"></a>Abschluss des Hauptbuchs am Ende der Periode

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Aufgaben beschrieben, die in der Regel ausgeführt werden, wenn ein Periodenabschluss für Hauptbuch ausgeführt wird. 

Im Hauptbuch können Sie Abschlussprozeduren für eine Periode oder ein Jahr ausführen. Abschlussvorgänge bereiten das System auf eine neue Periode vor. Als Vorbereitung auf ein neues Jahr müssen Sie den Jahresabschlussprozess ausführen. Jede Organisation hat unterschiedliche Verfahren und Schritte, die für das Ende einer Periode ausgeführt werden. Nachfolgend sind einige Schritte für optionale Periodenenden beschrieben:

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

Der Arbeitsbereich **Finanzperiodenabschluss** kann verwendet werden, um die Aufgaben, die für verschiedene Periodenabschlussprozesse erforderlich sind, zu organisieren und nachzuverfolgen. 


Weitere Informationen zu Workflows finden Sie unter den folgenden Themen:
- [Arbeitsbereich für Abschluss der Finanzperiode](financial-period-close-workspace.md) 
- [Jahresendabschluss](Year-end-close.md)  
- [Massen-Finanzperiodenabschluss](tasks/mass-financial-period-close.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
