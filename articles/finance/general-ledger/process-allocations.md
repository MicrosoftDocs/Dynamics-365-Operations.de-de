---
title: Verarbeiten von Zuteilungen
description: Dieser Artikel enthält Informationen zu Zuweisungen, die Optionen zum Verarbeitung in Microsoft Dynamics 365 Finance und wie sie in der Budgetplanung verwendet werden können. Zuweisungen werden verwendet, um Beträge über mehrere Sachkontokombinationen zu verteilen. Sie unterstützen, um sicherzustellen, dass Ausgaben oder Umsatzerlöse zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: kfend
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0629b32d39f4d74ec37eebe92b92e0b186b5fce2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877982"
---
# <a name="process-allocations"></a>Zuteilungen verarbeiten

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Zuweisungen, die Optionen zum Verarbeitung und wie sie in der Budgetplanung verwendet werden können. Zuweisungen werden verwendet, um Beträge über mehrere Sachkontokombinationen zu verteilen. Sie unterstützen, um sicherzustellen, dass Ausgaben oder Umsatzerlöse zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird.

Folgende Funktionen unterstützen diesen Prozesses:

-   Manuelle Zuteilung von Transaktionsbeträgen: Verwenden Sie dazu die Aktivität "Teilen" in den Buchhaltungsverteilungen oder wenden Sie Standardvorlagen für Finanzdimensionen auf ein Dokument an. Weitere Informationen finden Sie unter [Abrechnungsverteilungen](../accounts-payable/accounting-distributions.md).
-   Automatische Zuteilung von Transaktionsbeträgen: Dies geschieht auf der Grundlage von Zuteilungsbedingungen, die für das jeweilige Hauptkonto definiert sind. Zuteilungskontoeinträge werden basierend auf dem Prozentsatz und dem Zielsachkonto für jede Erfassung generiert, wenn ein Buchhaltungseintrag die für das Quellsachkonto definierten Kriterien erfüllt. Weitere Informationen finden Sie unter [Zuordnungserfassungen Hauptkonto](../general-ledger/main-account-allocation-terms.md)
-   Automatische Zuteilung von Sachkontosalden oder festen Beträgen auf der Grundlage von Sachkonto-Zuordnungsregeln. Die Sachkonto-Zuordnungsregeln werden periodisch mithilfe der Zuordnungserfassungen verarbeitet. Weitere Informationen finden Sie unter [Zuordnungsregeln](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Zuteilungen bei der Budgetplanung

Sachkonto-Zuordnungsregeln können für Budgetpläne verwendet werden. Wenn Sie Sachkontozuordnungsregeln in der Budgetplanung verwenden, die arbeiten die Zuordnungsregeln nach der gleichen Methode wie im Sachkonto, aber die Quelldaten und die Zieldaten stammen aus dem Budgetplan. Sie können Sachkontozuordnungsregeln manuell auswählen, um sie für Budgetpläne zu verwenden. Alternativ können Sie einen Zuordnungszeitplan verwenden, der als Teil einer Workflowprozesses ausgeführt wird.

> [!NOTE]
> Sie können Intercompany-Sachkontozuordnungsregeln für Budgetplanung nicht verwenden.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
