---
title: Ausgleichen eines vordatierten Schecks für einen Kreditor
description: Gleichen Sie einen vordatierten Scheck aus, der an einen Kreditor ausgestellt wurde, wenn die Bank die Scheckbuchung ausgeglichen hat, nachdem der Scheck überfällig war und von der Bank verrechnet wurde.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e3816a2f1c95d568a173cb07daad0473703da9c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779500"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>Ausgleichen eines vordatierten Schecks für einen Kreditor

[!include [banner](../../includes/banner.md)]

Gleichen Sie einen vordatierten Scheck aus, der an einen Kreditor ausgestellt wurde, wenn die Bank die Scheckbuchung ausgeglichen hat, nachdem der Scheck überfällig war und von der Bank verrechnet wurde. 

Schließen Sie folgende Prozeduren ab, bevor Sie diese starten:

1) Einrichten von vordatierten Schecks

2) Erfassen und Buchen eines vordatierten Schecks für einen Kreditor



Die Rolle dieser Prozedur ist "Finanzverwalter". Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Kreditoren > Zahlungen > Vordatierte Schecks von Händler**.
2. Klicken Sie auf **Ausgleichen**.
3. Klicken Sie auf **Verrechnungsposten ausgleichen**.
    * Das Kreditorenkonto für Scheck-Transaktionen ausgleichen.  
4. Schließen Sie die Seite.
5. Wechseln Sie zu **Hauptbuch > Journaleinträge > Allgemeine Erfassungen**.
6. Wählen Sie im Feld **Anzeigen** die Option **Alle** aus.
7. Aktivieren oder deaktivieren Sie das vom **Benutzer erstellte Kontrollkästchen Nur Anzeigen**.
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Klicken Sie auf **Positionen**.
10. Klicken Sie auf **Beleg**.
11. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
