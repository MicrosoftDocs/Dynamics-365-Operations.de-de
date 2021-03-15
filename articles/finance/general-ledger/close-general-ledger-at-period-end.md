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
ms.reviewer: roschlom
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 944f88e65c5dbbd2acf21ebfd96c28ce477798ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975990"
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
- [Arbeitsbereich für Abschluss der Finanzperiode](financial-period-close-workspace.md) 
- [Jahresendabschluss](Year-end-close.md)  
- [Massen-Finanzperiodenabschluss](tasks/mass-financial-period-close.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]