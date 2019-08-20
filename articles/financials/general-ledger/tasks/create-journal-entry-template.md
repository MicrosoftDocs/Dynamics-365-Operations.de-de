---
title: Erstellen von Journaleinträgen mithilfe einer Vorlage
description: Gebuchte Erfassungsbelege können als Belegvorlagen gespeichert und in einem neuen Erfassungsbeleg angewendet werden.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a3fb750e04fb134fc9ac38d9a47201803566113
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846630"
---
# <a name="create-a-journal-entry-using-template"></a>Erstellen von Journaleinträgen mithilfe einer Vorlage

[!include [task guide banner](../../includes/task-guide-banner.md)]

Gebuchte Erfassungsbelege können als Belegvorlagen gespeichert und in einem neuen Erfassungsbeleg angewendet werden. Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.

1. Hauptbuch > Journaleinträge > Allgemeine Erfassungen. Klicken Sie auf "Neu".
    * Diese Prozedur beginnt, indem Sie einen Erfassungsbeleg erstellen und buchen, aber jeder bereits gebuchte Erfassungsbeleg kann als Vorlage gespeichert werden.  
2. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie auf Positionen.
6. Geben Sie ein Konto für den Typ "Konto" ein.
7. Geben Sie im Feld "Beschreibung" einen Wert ein.
8. Geben Sie einen Betrag im Feld "Lastschrift" ein.
9. Klicken Sie auf Neu.
10. Geben Sie ein anderes Konto für den Typ "Konto" ein.
11. Geben Sie im Feld "Beschreibung" einen Wert ein.
12. Geben Sie einen Betrag im Feld "Lastschrift" ein.
13. Klicken Sie auf Neu.
14. Geben Sie im Feld "Konto" die gewünschten Werte an.
15. Geben Sie im Feld "Beschreibung" einen Wert ein.
16. Geben Sie einen Betrag in das Feld "Gutschrift" ein, um den Beleg auszugleichen.
17. Klicken Sie auf "Buchen".
18. Klicken Sie auf Funktionen.
19. Klicken Sie auf "Belegvorlage speichern".
20. Bei dieser Prozedur wird ein Typ "Prozentvorlage" angenommen. Klicken Sie auf "OK".
    * • Prozent: Die Beträge im Beleg werden in Prozentsatzfaktoren konvertiert, wodurch jeder Betrag angewendet werden kann, wenn die Vorlage "Beleg" ausgewählt ist.  • Betrag: Die tatsächlichen Beträge werden gespeichert und angewendet.  
21. Klicken Sie auf "Allgemeine Erfassungen".
22. Klicken Sie auf "Neu".
23. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
24. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
25. Klicken Sie auf "Positionen".
26. Klicken Sie auf Funktionen.
27. Klicken Sie auf "Belegvorlage auswählen".
28. Suchen Sie die Vorlage, die Sie zuvor erstellt haben. Klicken Sie auf "OK".
    * Sie müssen möglicherweise auf "Vorheriger Schritt" klicken und dann die richtige Vorlage auswählen, wenn andere Vorlagen vorhanden sind.  
29. Geben Sie im Feld "Betrag" den Betrag ein, der auf den Beleg angewendet wird.
    * Das Betragsfeld wird nur angezeigt, wenn die Belegvorlage vom Typ "Prozent" ist.  
30. Klicken Sie auf "OK".

