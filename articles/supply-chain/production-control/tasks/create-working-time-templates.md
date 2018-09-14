--- 
title: Erstellen von Schichtmodellen
description: "Schichtmodelle definieren die Arbeitsstunden in einer Woche und werden verwendet, um die Arbeitszeiten für einen bestimmten Zeitraum zu generieren."
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2df37747601618fc3d45734152a05aedd39500a6
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-working-time-templates"></a>Erstellen von Schichtmodellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Schichtmodelle definieren die Arbeitsstunden in einer Woche und werden verwendet, um die Arbeitszeiten für einen bestimmten Zeitraum zu generieren. Dieses Verfahren zeigt Ihnen, wie ein Schichtmodell mithilfe der Arbeitszeit-Planungseigenschaften für die Kategorisierung von Arbeitszeitintervallen definiert wird. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.

1. Wechseln Sie zu "Alle Arbeitsbereiche" > "Ressourcenlebenszyklusverwaltung".
2. Klicken Sie auf "Schichtmodelle".

## <a name="create-working-time-template"></a>Erstellen von Schichtmodellen
1. Klicken Sie auf "Neu".
2. Geben Sie im Feld "Schichtmodell" einen Wert ein.
3. Geben Sie im Feld "Name" einen Wert ein.
4. Erweitern Sie den Abschnitt "Montag".
5. Klicken Sie auf Hinzufügen.
6. Geben Sie im Feld "Von" eine Uhrzeit ein.
    * Geben Sie die Uhrzeit an, zu der die Arbeit am Morgen beginnt.  
7. Geben Sie im Feld "Bis" eine Uhrzeit ein.
    * Geben Sie die Uhrzeit an, zu der Arbeitskräfte zum Mittagessen gehen.  
8. Klicken Sie auf Hinzufügen.
9. Geben Sie im Feld "Von" eine Uhrzeit ein.
    * Geben Sie die Uhrzeit an, zu der die Arbeitskräfte vom Mittagessen kommen.  
10. Geben Sie im Feld "Bis" eine Uhrzeit ein.
    * Geben Sie das Ende des Arbeitstages an.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikation von Arbeitszeiten auf alle Wochentage
1. Klicken Sie auf "Tag kopieren".
    * Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Dienstag.  
2. Klicken Sie auf "OK".
3. Klicken Sie auf "Tag kopieren".
    * Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Mittwoch.  
4. Wählen Sie im Feld "Bis Wochentag" eine Option aus.
5. Klicken Sie auf "OK".
6. Klicken Sie auf "Tag kopieren".
    * Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Donnerstag.  
7. Wählen Sie im Feld "Bis Wochentag" eine Option aus.
8. Klicken Sie auf "OK".
9. Klicken Sie auf "Tag kopieren".
    * Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Freitag.  
10. Wählen Sie im Feld "Bis Wochentag" eine Option aus.
11. Klicken Sie auf "OK".

## <a name="define-time-slots-for-special-operations"></a>Definieren von Zeitrahmen für spezielle Vorgänge
1. Erweitern Sie den Abschnitt "Freitag".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Geben Sie im Feld "Eigenschaft" einen Wert ein, oder wählen Sie einen Wert aus.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Geben Sie im Feld "Eigenschaft" einen Wert ein, oder wählen Sie einen Wert aus.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Markieren von Wochenendentagen als "Keine Abholung"
1. Erweitern Sie den Abschnitt "Samstag".
2. Wählen Sie "Ja" im Feld "Keine Abholung" aus.
3. Erweitern Sie den Abschnitt "Sonntag".
4. Wählen Sie "Ja" im Feld "Keine Abholung" aus.


