---
title: Ausgleichen eines vordatierten Schecks für einen Kreditor
description: Gleichen Sie einen vordatierten Scheck aus, der an einen Kreditor ausgestellt wurde, wenn die Bank die Scheckbuchung ausgeglichen hat, nachdem der Scheck überfällig war und von der Bank verrechnet wurde.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08cf4ec805e632470ef778f31beb87597e0ca096
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976190"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>Ausgleichen eines vordatierten Schecks für einen Kreditor

[!include [banner](../../includes/banner.md)]

Gleichen Sie einen vordatierten Scheck aus, der an einen Kreditor ausgestellt wurde, wenn die Bank die Scheckbuchung ausgeglichen hat, nachdem der Scheck überfällig war und von der Bank verrechnet wurde. 

Schließen Sie folgende Prozeduren ab, bevor Sie diese starten:

1) Einrichten von vordatierten Schecks

2) Erfassen und Buchen eines vordatierten Schecks für einen Kreditor



Die Rolle dieser Prozedur ist "Finanzverwalter". Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu Kreditoren > Zahlungen > Vordatierte Schecks von Händler.
2. Klicken Sie auf "Ausgleichen".
3. Klicken Sie auf Verrechnungsposten ausgleichen.
    * Das Kreditorenkonto für Scheck-Transaktionen ausgleichen.  
4. Schließen Sie die Seite.
5. Wechseln Sie zu "Hauptbuch" > "Journaleinträge" > "Allgemeine Erfassungen".
6. Wählen Sie im Feld "Anzeigen" die Option "Alle" aus.
7. Aktivieren oder deaktivieren Sie das vom Benutzer erstellte Kontrollkästchen Nur Anzeigen.
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Klicken Sie auf Positionen.
10. Klicken Sie auf Beleg.
11. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]