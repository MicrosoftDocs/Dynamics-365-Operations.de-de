---
title: Einrichten von vordatierten Schecks
description: In diesem Thema wird erläutert, wie angegeben wird, ob Journaleinträge für vordatierte Schecks gebucht werden sollen, und welche Erfassungen für das Verrechnen von Einträgen und von Kreditorenzahlungen verwendet werden sollen.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4b18ebe1388998b45e5ef38318b0ade9153f7c8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565948"
---
# <a name="set-up-postdated-checks"></a>Einrichten von vordatierten Schecks

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird erläutert, wie angegeben wird, ob Journaleinträge für vordatierte Schecks gebucht werden sollen, und welche Erfassungen für das Verrechnen von Einträgen und von Kreditorenzahlungen verwendet werden sollen. Sie können auch Verrechnungskonten für ausgestellte Schecks, erhaltene Schecks oder für die Quellensteuer angeben. Vordatierte Schecks sind Schecks, die ausgestellt werden, um Zahlungen zu einem späteren Datum leisten oder erhalten zu können. Sie können angeben, ob der Scheck vor seinem Fälligkeitsdatum in Ihren Kontoblättern widergespiegelt sein muss.



Die Rolle dieser Prozedur ist "Finanzverwalter". Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.


## <a name="set-up-postdated-checks"></a>Einrichten von vordatierten Schecks
1. Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.
2. Klicken Sie auf die Registerkarte "Vordatierte Schecks".
3. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Vordatierte Schecks aktivieren".
4. Aktivieren bzw. deaktivieren Sie die Beitragsjournaleinträge für Kontrollkästchen der vordatierten Schecks.
5. Geben Sie im Feld Verrechnungskonto die gewünschten Werte an.
6. Geben Sie im Feld Verrechnungskonto für erhaltene Schecks die gewünschten Werte an.
7. In der allgemeinen Erfassung für das Vorbereiten des Eintrags felds, geben Sie einen Wert ein.
8. Geben Sie im Feld "Vordatierte Schecks in diese Kreditoren-Zahlungserfassung übertragen" einen Wert ein.
9. Geben Sie im Feld Verrechnungskonto für Quellensteuer die gewünschten Werte an.
10. Klicken Sie auf "Speichern".
11. Schließen Sie die Seite.
12. Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".
13. Klicken Sie auf "Neu".
14. Geben Sie im Feld "Zahlungsmethode" einen Wert ein.
15. Markieren Sie das Kontrollkästchen , um anzugeben, dass der Scheckbetrag zu einem Verrechnungskonto gebucht wird.
16. Wählen Sie im Feld "Kontotyp" "Bank" aus.
    * Das Gegenkonto der Zahlungsmethode ist eine Bank.  
17. Geben Sie im Feld "Zahlungskonto" die gewünschten Werte an.
    * Wählen Sie das Bankkonto aus, das zum Abziehen des Rechnungsbetrags verwendet wird.  
18. Schließen Sie die Seite.
19. Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".
20. Klicken Sie auf "Neu".
21. Geben Sie im Feld "Zahlungsmethode" einen Wert ein.
22. Markieren Sie das Kontrollkästchen , um anzugeben, dass der Scheckbetrag zu einem Verrechnungskonto gebucht wird.
23. Wählen Sie im Feld "Kontotyp" "Bank" aus.
    * Das Gegenkonto der Zahlungsmethode ist eine Bank.  
24. Geben Sie im Feld "Zahlungskonto" die gewünschten Werte an.
    * Wählen Sie das Bankkonto aus, das zum Abziehen des Rechnungsbetrags verwendet wird.  
25. Schließen Sie die Seite.

