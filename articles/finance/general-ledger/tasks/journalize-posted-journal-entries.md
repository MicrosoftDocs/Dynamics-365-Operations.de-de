---
title: Gebuchte Erfassungseinträge journalisieren
description: Diese Verfahren zeigt, wie gebuchte Journaleinträge journalisiert werden.
author: aprilolson
ms.date: 03/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8fca167563b14c825ebe29874c6488ddfb4d9a
ms.sourcegitcommit: 06acdfbccd7bd213a2397ea7b85d104f01914437
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2022
ms.locfileid: "8400874"
---
# <a name="journalize-posted-journal-entries"></a>Gebuchte Erfassungseinträge journalisieren

[!include [banner](../../includes/banner.md)]

Der Journalisierungsprozess im Hauptbuch bietet eine Möglichkeit, gebuchte Belegposten für Ihr Hauptbuch zu gruppieren und zu melden. Basierend auf den von Ihnen angegebenen Kriterien generiert die Verarbeitung eine Liste von Belegen, die eine eindeutige Nummernfolge verwenden und die den Wert **Erfassungsnummer** im Hauptbuch als Referenz haben.

Führen Sie diese Schritte aus, um gebuchte Journaleinträge zu journalisieren. Für diese Prozedur wird das Demo-Datenunternehmen **USMF** verwendet.

1. Gehen Sie zu **Hauptbuch** \> **Hauptbuch einrichten** \> **Hauptbuch-Parameter**.
2. In dem **Erweiterte Journalisierung**-Feld wählen Sie einen Wert aus. Bei Auswahl von **Ja** unterscheidet sich die Berichtsausgabe.
3. Wählen Sie aus, ob die Periode abgeschlossen werden kann, wenn der journalisierende Prozess nicht ausgeführt wurde. Wenn Sie **Ja** auswählen, kann der Zeitraum nicht abgeschlossen werden, bis der Journalisierungsprozess für diesen Zeitraum abgeschlossenen wurde.
4. Schließen Sie die Seite.
5. Gehen Sie zu **Hauptbuch** \> **Periodische Aufgaben** \> **Journalisierung**, und wählen Sie **Filter** aus.
6. Wählen Sie die Zeile für die Filterkriterien aus, die Sie definieren möchten.
7. Geben Sie im Feld **Kriterien** Filterkriterien ein oder wählen Sie sie aus.
8. Klicken Sie auf **OK**, um die Seite zu schließen.
9. Wählen Sie zum Starten des Journalisierungsprozesses **OK** aus. Ein Bericht wird generiert, nachdem der Vorgang abgeschlossen wurde.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
