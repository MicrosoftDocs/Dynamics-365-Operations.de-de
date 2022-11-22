---
title: Einrichten von vordatierten Schecks
description: In diesem Artikel wird erläutert, wie angegeben wird, ob Journaleinträge für vordatierte Schecks gebucht werden sollen, und welche Erfassungen für das Verrechnen von Einträgen und von Kreditorenzahlungen verwendet werden sollen.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7172dd56113de23d841fe59ed9785471e90ed1f
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779608"
---
# <a name="set-up-postdated-checks"></a>Einrichten von vordatierten Schecks

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird erläutert, wie angegeben wird, ob Journaleinträge für vordatierte Schecks gebucht werden sollen, und welche Erfassungen für das Verrechnen von Einträgen und von Kreditorenzahlungen verwendet werden sollen. Sie können auch Verrechnungskonten für ausgestellte Schecks, erhaltene Schecks oder für die Quellensteuer angeben. Vordatierte Schecks sind Schecks, die ausgestellt werden, um Zahlungen zu einem späteren Datum leisten oder erhalten zu können. Sie können angeben, ob der Scheck vor seinem Fälligkeitsdatum in Ihren Kontoblättern widergespiegelt sein muss.



Die Rolle dieser Prozedur ist "Finanzverwalter". Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.


## <a name="set-up-postdated-checks"></a>Einrichten von vordatierten Schecks
1. Wechseln Sie zu **Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung**.
2. Klicken Sie auf die Registerkarte **Vordatierte Schecks**.
3. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen **Vordatierte Schecks aktivieren**.
4. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen **Beitragsjournaleinträge für der vordatierten Schecks buchen**.
5. Geben Sie im Feld **Verrechnungskonto** die gewünschten Werte an.
6. Geben Sie im Feld **Verrechnungskonto für erhaltene Schecks** die gewünschten Werte an.
7. In der **allgemeinen Erfassung für das Vorbereiten des Eintrags** felds, geben Sie einen Wert ein.
8. Geben Sie im Feld **Vordatierte Schecks in diese Kreditoren-Zahlungserfassung übertragen** einen Wert ein.
9. Geben Sie im Feld **Verrechnungskonto für Quellensteuer** die gewünschten Werte an.
10. Klicken Sie auf **Speichern**.
11. Schließen Sie die Seite.
12. Wechseln Sie zu **Kreditoren > Zahlungseinstellungen > Zahlungsmethoden**.
13. Klicken Sie auf **Neu**.
14. Geben Sie im Feld **Zahlungsmethode** einen Wert ein.
15. Markieren Sie das Kontrollkästchen , um anzugeben, dass der **Scheckbetrag zu einem Verrechnungskonto gebucht** wird.
16. Wählen Sie im Feld **Kontotyp** **Bank** aus.
    * Das Gegenkonto der Zahlungsmethode ist eine Bank.  
17. Geben Sie im Feld **Zahlungskonto** die gewünschten Werte an.
    * Wählen Sie das Bankkonto aus, das zum Abziehen des Rechnungsbetrags verwendet wird.  
18. Klicken Sie auf **Speichern**.
19. Schließen Sie die Seite.
> [!NOTE]
> Um einen vordatierten Scheck auf ein Bankkonto buchen zu können, wenn das Sitzungsdatum höher oder gleich dem Fälligkeitsdatum ist, müssen Sie die Funktion **Validierung des Fälligkeitsdatums der Buchung der Zahlungserfassung mit vordatiertem Schecks auf das Bankkonto**. Mit dieser Funktion können Sie Zahlungserfassungen für Kreditoren und Debitoren mit vordatierten Schecks buchen, wenn das Sitzungsdatum höher oder gleich dem Fälligkeitsdatum ist.
> 
> Füllen Sie beim Festlegen der **Zahlungmethode** (**Kreditorenkonto > Zahlungssetup > Zahlungsmethoden**) **Transferkonto** nicht aus. In diesem Fall wird als Gegenkonto das Bankkonto eingetragen, das unter **Zahlungsmethode** angegeben ist.
>  
> Wenn die Funktion aktiviert ist und das Sitzungsdatum niedriger ist als das Fälligkeitsdatum, wird beim Buchen einer Zahlungserfassung die folgende Fehlermeldung angezeigt: **Das Fälligkeitsdatum muss niedriger oder gleich dem Sitzungsdatum sein, wenn der Gegenkontotyp die Bank ist**. Wenn die Funktion nicht aktiviert ist, können Sie eine Zahlungserfassung mit einem vordatierten Scheck buchen, wenn das Sitzungsdatum niedriger ist als das Fälligkeitsdatum.
> Diese Funktion ist ab Version 10.0.21 und höher verfügbar.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
