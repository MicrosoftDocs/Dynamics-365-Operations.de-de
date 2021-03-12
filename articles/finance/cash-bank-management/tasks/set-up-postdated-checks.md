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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b677056f11a8733bf90f18110b8ee47f6447503b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976290"
---
# <a name="set-up-postdated-checks"></a>Einrichten von vordatierten Schecks

[!include [banner](../../includes/banner.md)]

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
18. Klicken Sie auf Speichern.
19. Schließen Sie die Seite.

