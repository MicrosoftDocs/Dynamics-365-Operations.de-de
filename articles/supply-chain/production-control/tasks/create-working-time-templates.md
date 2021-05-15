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
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920928"
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