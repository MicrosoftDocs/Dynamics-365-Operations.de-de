---
title: Erstellen von Schichtmodellen
description: Schichtmodelle definieren die Arbeitsstunden in einer Woche und werden verwendet, um die Arbeitszeiten für einen bestimmten Zeitraum zu generieren.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ef913777c8e2aa14af21e28ed56362e31b3d70a1a52e988a90ad94f59b77b70
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741260"
---
# <a name="create-working-time-templates"></a>Erstellen von Schichtmodellen

[!include [banner](../../includes/banner.md)]

Schichtmodelle definieren die Arbeitsstunden in einer Woche und werden verwendet, um die Arbeitszeiten für einen bestimmten Zeitraum zu generieren. Dieses Verfahren zeigt Ihnen, wie ein Schichtmodell mithilfe der Arbeitszeit-Planungseigenschaften für die Kategorisierung von Arbeitszeitintervallen definiert wird. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.

1. Wechseln Sie zu **Arbeitsbereiche > Ressourcenlebenszyklusverwaltung**.
1. Wählen Sie **Arbeitszeitvorlagen**.

## <a name="create-working-time-template"></a>Erstellen von Schichtmodellen

1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Arbeitszeitvorlage** einen Wert ein.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Erweitern Sie den Abschnitt **Montag**.
1. Wählen Sie **Hinzufügen** aus.
1. Geben Sie im Feld **Von** eine Uhrzeit ein.
    * Geben Sie die Uhrzeit an, zu der die Arbeit am Morgen beginnt.  
1. Geben Sie im Feld **Bis** eine Uhrzeit ein.
    * Geben Sie die Uhrzeit an, zu der Arbeitskräfte zum Mittagessen gehen.  
1. Wählen Sie **Hinzufügen** aus.
1. Geben Sie im Feld **Von** eine Uhrzeit ein.
    * Geben Sie die Uhrzeit an, zu der die Arbeitskräfte vom Mittagessen kommen.  
1. Geben Sie im Feld **Bis** eine Uhrzeit ein.
    * Geben Sie das Ende des Arbeitstages an.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikation von Arbeitszeiten auf alle Wochentage

1. Wählen Sie **Kopieren Tag**.
    * Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Dienstag.  
1. Wählen Sie **OK**.
1. Wählen Sie **Kopieren Tag**.
    * Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Mittwoch.  
1. Wählen Sie im Feld **Bis Wochentag** eine Option aus.
1. Wählen Sie **OK**.
1. Wählen Sie **Kopieren Tag**.
    * Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Donnerstag.  
1. Wählen Sie im Feld **Bis Wochentag** eine Option aus.
1. Wählen Sie **OK**.
1. Wählen Sie **Kopieren Tag**.
    * Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Freitag.  
1. Wählen Sie im Feld **Bis Wochentag** eine Option aus.
1. Wählen Sie **OK**.

## <a name="define-time-slots-for-special-operations"></a>Definieren von Zeitrahmen für spezielle Vorgänge

1. Erweitern Sie den Abschnitt **Freitag**.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
1. Geben Sie in das Feld **Eigenschaft** einen Wert ein oder wählen Sie einen Wert aus.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
1. Geben Sie in das Feld **Eigenschaft** einen Wert ein oder wählen Sie einen Wert aus.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Markieren von Wochenendentagen als "Keine Abholung"

1. Erweitern Sie den Abschnitt **Samstag**.
1. Wählen Sie *Ja* im Feld **Zur Abholung geschlossen**.
1. Erweitern Sie den Abschnitt **Sonntag**.
1. Wählen Sie *Ja* im Feld **Zur Abholung geschlossen**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]