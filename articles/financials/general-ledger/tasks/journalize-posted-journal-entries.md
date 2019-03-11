---
title: Gebuchte Erfassungseinträge journalisieren
description: Diese Verfahren zeigt, wie gebuchte Journaleinträge journalisiert werden.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b50809cf9eb59475856f91d9f1ddfe28ecfd8de6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "318533"
---
# <a name="journalize-posted-journal-entries"></a>Gebuchte Erfassungseinträge journalisieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Verfahren zeigt, wie gebuchte Journaleinträge journalisiert werden. Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.

1. Überprüfen Sie die Einstellungen für die Journalisierung unter Hauptbuch > Sachkontoeinrichtung > Hauptbuchparameter.
2. Das Feld "Erweiterte Journalisierung" kann auf Ja oder Nein festgelegt werden. Bei Ja unterscheidet sich die Berichtsausgabe.
3. Wählen Sie aus, ob die Periode abgeschlossen werden kann, wenn der journalisierende Prozess nicht ausgeführt wurde.
    * Ist die Option auf "Ja" festgelegt ist, kann der Zeitraum nicht abgeschlossen werden, bis der Erfassungsprozess für diesen Zeitraum abgeschlossenen wurde.  
4. Schließen Sie die Seite.
5. Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Journalisierung".
6. Klicken Sie auf "Filter".
7. Markieren Sie die Zeile mit den Filterkriterien, die Sie definieren möchten.
8. Geben Sie im Feld "Kriterien" einen Filterkriterien ein oder wählen Sie sie aus.
9. Klicken Sie zum Schließen der Filterseite auf OK.
10. Klicken Sie zum Starten des Journalisierungsprozesses auf "OK".
    * Ein Bericht wird generiert, nachdem der Vorgang abgeschlossen ist.  

