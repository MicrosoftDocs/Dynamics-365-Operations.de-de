---
title: Verarbeiten von Zuteilungen
description: "Dieser Artikel enthält Informationen zu Zuteilungen, die Optionen zur Verarbeitung in Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, und beschreibt, wie sie in der Budgetplanung verwendet werden können. Zuweisungen werden verwendet, um Beträge über mehrere Sachkontokombinationen zu verteilen. Sie unterstützen, um sicherzustellen, dass eine Ausgabe oder Umsatzerlös zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: e6d88503972850f6163aba6b45547a111f44abab
ms.contentlocale: de-de
ms.lasthandoff: 06/20/2017


---

# <a name="process-allocations"></a>Verarbeiten von Zuteilungen

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zu Zuteilungen, die Optionen zur Verarbeitung in Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, und beschreibt, wie sie in der Budgetplanung verwendet werden können. Zuweisungen werden verwendet, um Beträge über mehrere Sachkontokombinationen zu verteilen. Sie unterstützen, um sicherzustellen, dass eine Ausgabe oder Umsatzerlös zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird.

Microsoft Dynamics 365 for Finance and Operations enthält die folgenden Funktionen zur Unterstützung dieses Vorgangs:

-   Manuelle Zuteilung von Transaktionsbeträgen: Verwenden Sie dazu die Aktivität "Teilen" in den Buchhaltungsverteilungen oder wenden Sie Standardvorlagen für Finanzdimensionen auf ein Dokument an. Weitere Informationen finden Sie unter [Buchhaltungsverteilungen](../accounts-payable/accounting-distributions.md).
-   Automatische Zuteilung von Transaktionsbeträgen: Dies geschieht auf der Grundlage von Zuteilungsbedingungen, die für das jeweilige Hauptkonto definiert sind. Zuteilungskontoeinträge werden basierend auf dem Prozentsatz und dem Zielsachkonto für jede Erfassung generiert, wenn ein Buchhaltungseintrag die für das Quellsachkonto definierten Kriterien erfüllt.
-   Automatische Zuteilung von Sachkontosalden oder festen Beträgen auf der Grundlage von Sachkonto-Zuordnungsregeln. Die Sachkonto-Zuordnungsregeln werden periodisch mithilfe der Zuordnungserfassungen verarbeitet. 

###  <a name="allocations-in-budget-planning"></a>Zuteilungen bei der Budgetplanung

Sachkonto-Zuordnungsregeln können für Budgetpläne verwendet werden. Wenn Sie Sachkontozuordnungsregeln in der Budgetplanung verwenden, die arbeiten die Zuordnungsregeln nach der gleichen Methode wie im Sachkonto, aber die Quelldaten und die Zieldaten stammen aus dem Budgetplan. Sie können Sachkontozuordnungsregeln manuell auswählen, um sie für Budgetpläne zu verwenden. Alternativ können Sie einen Zuordnungszeitplan verwenden, der als Teil einer Workflowprozesses ausgeführt wird.

> [!NOTE]
> Sie können Intercompany-Sachkontozuordnungsregeln für Budgetplanung nicht verwenden.






