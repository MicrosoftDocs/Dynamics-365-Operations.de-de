---
title: Ausgleichen eines vordatierten Schecks von einem Debitor
description: Sie können einen vordatierten Scheck ausgleichen, nachdem der Scheck von der Bank verrechnet wurde.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f714e41f47a31bce16424de18878d2f5acb5028d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834547"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>Ausgleichen eines vordatierten Schecks von einem Debitor

[!include [banner](../../includes/banner.md)]

Sie können einen vordatierten Scheck ausgleichen, nachdem der Scheck von der Bank verrechnet wurde. Bei dieser Finanzbuchung wird auch die Übergangskontobuchung für den vordatierten Scheck ausgeglichen. 

Schließen Sie folgende Prozeduren ab, bevor Sie diese starten:

1) Einrichten von vordatierten Schecks

2) Einen vordatierten Scheck für einen Debitor erfassen und buchen 



Die Rolle dieses Aufgabenleitfadens ist "Finanzverwalter".



Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu Kredit und Inkasso > Abfragen und Berichte > Zahlungen > Vordatierte Schecks.
2. Klicken Sie auf "Ausgleichen".
3. Klicken Sie auf Verrechnungsposten ausgleichen.
    * Gleichen Sie das Debitorenkonto für die Scheck-Transaktionen aus.  
4. Schließen Sie die Seite.
5. Wechseln Sie zu "Hauptbuch" > "Journaleinträge" > "Allgemeine Erfassungen".
6. Wählen Sie im Feld 'Anzeigen:' eine Option aus.
7. Aktivieren oder deaktivieren Sie das vom Benutzer erstellte Kontrollkästchen Nur Anzeigen.
8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
9. Klicken Sie auf Positionen.
10. Klicken Sie auf Beleg.
11. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]