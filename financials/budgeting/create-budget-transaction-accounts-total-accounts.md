---
title: "Erstellen Sie ein Budget für Buchungs- und Summenkonten"
description: "Dieser Artikel gibt einen Überblick über den Prozess für das Erstellen von Budgets basierend auf Summenkonten. Er erläutert auch, wie die Budgetsteuerung für Summenkonten aktiviert wird, wenn die Budgetsteuerung erforderlich ist."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: af9b6a5ebb25c0054704b60c84057eee609ffab7
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Erstellen Sie ein Budget für Buchungs- und Summenkonten

Dieser Artikel gibt einen Überblick über den Prozess für das Erstellen von Budgets basierend auf Summenkonten. Er erläutert auch, wie die Budgetsteuerung für Summenkonten aktiviert wird, wenn die Budgetsteuerung erforderlich ist.

Sowohl mit Haushaltsplan- als auch mit Budgetregistereintragsdokumenten können Hauptkonten budgetiert werden, deren Hauptkontotyp **Summe** lautet. Istwerte können nur den buchungsbezogenen Hauptkonten gebucht werden. 

Für den periodischen Prozess zum **Generieren eines Budgetplans aus dem Hauptbuch** auf der Registerkarte **Quelle** können Sie den Hauptkontotyp **Summe** als Kriterium angeben. In diesem Fall ist jedes Gesamthauptkonto im Ziel-Haushaltsplan einbezogen, und der Betrag entspricht dem Gesamtbetrag des Bereichs der ausgewählten Hauptkonten. 

Sie können die Budgetsteuerung für Hauptkonten vom **Summe**-Typ aktivieren. Diese Funktionalität wird durch die Verwendung von Budgetgruppen unterstützt. Für jedes Hauptkonto das gesamte Budget muss, das für eine Budgetgruppe gesteuert werden soll, auf der Seite ** Budgetsteuerungskonfiguration ** erstellt werden. Die Kriterien, die Sie angeben, müssen das gesamte Hauptkonto und des Bereichs der Konten umfassen. Um den Prozess der Erstellung von Budgetgruppen zu beschleunigen, können Sie die Datenentität Budgetsteuerungsgruppen nutzen. 

Wenn ein Budget für die Berichterstellung, also beispielsweise in einer Finanzaufstellung, verwendet wird, setzt sich die Budgetsumme für das Summenkonto wie folgt zusammen:

-   Aus den Budgets, die auf jedem Buchungssachkonto innerhalb des Intervalls des Summenkontos erstellt werden.
-   Aus dem Budgetbetrag, der direkt auf dem Summenkonto gebucht wird

Auf diese Weise können also separate Budgets für die wichtigsten Buchungskonten im Intervall des Summenkontos erstellt und kann der verbleibende Budgetbetrag dem Summenkonto hinzugefügt werden.


