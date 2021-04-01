---
title: Gebuchte Erfassungseinträge journalisieren
description: Diese Verfahren zeigt, wie gebuchte Journaleinträge journalisiert werden.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca1aed3a77da66ef336942b2c178abdd425d3c25
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240665"
---
# <a name="journalize-posted-journal-entries"></a>Gebuchte Erfassungseinträge journalisieren

[!include [banner](../../includes/banner.md)]

Diese Verfahren zeigt, wie gebuchte Journaleinträge journalisiert werden. Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.

1. Wechseln Sie im **Navigationsbereich** auf **Module > Hauptbuch > Sachkonto-Einstellungen > Hauptbuchparameter**.
2. Das Feld **Erstellte Journale erweitern** kann auf Ja oder Nein festgelegt werden. Bei Ja unterscheidet sich die Berichtsausgabe.
3. Wählen Sie aus, ob die Periode abgeschlossen werden kann, wenn der journalisierende Prozess nicht ausgeführt wurde. Ist die Option auf "Ja" festgelegt ist, kann der Zeitraum nicht abgeschlossen werden, bis der Erfassungsprozess für diesen Zeitraum abgeschlossenen wurde.  
4. Schließen Sie die Seite.
5. Wechseln Sie im **Navigationsbereich** zu **Module > Hauptbuch > Periodische Aufgaben > Journalisierung**.
6. Klicken Sie auf **Filter**.
7. Markieren Sie die Zeile mit den Filterkriterien, die Sie definieren möchten.
8. Geben Sie im Feld **Kriterien** Filterkriterien ein oder wählen Sie sie aus.
9. Klicken Sie zum Schließen der Filterseite auf **OK**.
10. Klicken Sie zum Starten des Journalisierungsprozesses auf **OK**. Ein Bericht wird generiert, nachdem der Vorgang abgeschlossen ist.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]