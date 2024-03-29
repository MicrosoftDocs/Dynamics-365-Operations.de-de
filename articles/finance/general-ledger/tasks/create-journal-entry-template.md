---
title: Erstellen von Journaleinträgen mithilfe einer Vorlage
description: Gebuchte Erfassungsbelege können als Belegvorlagen gespeichert und in einem neuen Erfassungsbeleg angewendet werden.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05cb878b570c45a2f7358ad60e6e01c7af17dc90
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716482"
---
# <a name="create-a-journal-entry-using-template"></a>Erstellen von Journaleinträgen mithilfe einer Vorlage

[!include [banner](../../includes/banner.md)]

Gebuchte Erfassungsbelege können als Belegvorlagen gespeichert und in einem neuen Erfassungsbeleg angewendet werden. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.

1. Gehen Sie zu **Navigationsbereich > Module > Hauptbuch > Journaleinträge > Allgemeine Erfassungen**.
2. Klicken Sie im **Aktivitätsbereich** auf **Neu**. Diese Prozedur beginnt, indem Sie einen Erfassungsbeleg erstellen und buchen, aber jeder bereits gebuchte Erfassungsbeleg kann als Vorlage gespeichert werden.  
3. Klicken Sie im Feld **Name** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. Klicken Sie auf **Positionen**.
7. Geben Sie im Feld **Kontenart** einen Wert ein.
8. Geben Sie im Feld **Beschreibung** einen Wert ein.
9. Geben Sie im Feld **Soll** einen Wert ein.
10. Klicken Sie auf **Neu**.
11. Geben Sie im Feld **Kontenart** einen Wert ein.
12. Geben Sie im Feld **Beschreibung** einen Wert ein.
13. Geben Sie im Feld **Soll** einen Wert ein.
14. Klicken Sie auf **Neu**.
14. Geben Sie im Feld **Konto** die gewünschten Werte an.
15. Geben Sie im Feld **Beschreibung** einen Wert ein.
16. Geben Sie im Feld **Gutschrift** einen Wert ein, um den Beleg auszugleichen.
17. Klicken Sie im **Aktivitätsbereich** auf **Buchen**.
18. Klicken Sie auf **Funktionen**.
19. Klicken Sie auf **Belegvorlage speichern**.
20. Bei dieser Prozedur wird ein Typ **Prozentvorlage** angenommen. Klicken Sie auf "OK".
    - Prozent: Die Beträge im Beleg werden in Prozentsatzfaktoren konvertiert, wodurch jeder Betrag angewendet werden kann, wenn die Vorlage „Beleg“ ausgewählt ist.
    - Betrag: Die tatsächlichen Beträge werden gespeichert und angewendet.  
21. Klicken Sie auf **Allgemeine Erfassungen**.
22. Klicken Sie auf **Neu**.
23. Klicken Sie im Feld **Name** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
24. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
25. Klicken Sie auf **Positionen**.
26. Klicken Sie auf **Funktionen**.
27. Klicken Sie auf **Belegvorlage auswählen**.
28. Suchen Sie die Vorlage, die Sie zuvor erstellt haben. Klicken Sie auf **OK**. Sie müssen möglicherweise auf **Vorheriger Schritt** klicken und dann die richtige Vorlage auswählen, wenn andere Vorlagen vorhanden sind.  
29. Geben Sie im Feld **Betrag** den Betrag ein, der auf den Beleg angewendet wird. Das Feld **Betrag** wird nur angezeigt, wenn die Belegvorlage vom Typ „Prozent“ ist.  
30. Klicken Sie auf **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
