---
title: Erweiterte Regeln für Erfassungen erstellen
description: Dieses Verfahrens zeigt das Erstellen von erweiterten Regeln für Erfassungen.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3eb34ac419aeab3663a8931d022abf7bcbfddd37
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916143"
---
# <a name="create-advanced-rules-for-journals"></a>Erweiterte Regeln für Erfassungen erstellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahrens zeigt das Erstellen von erweiterten Regeln für Erfassungen. Hierzu zählen die Einrichtung Erfassungssteuerungs- und Benutzerbuchungseinschränkungen. Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.


## <a name="set-up-journal-control"></a>Einrichten der Erfassungskontrolle
1. Wechseln Sie im **Navigationsbereich** zu **Module > Hauptbuch > Erfassungseinstellungen > Journale**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie im **Aktivitätsbereich** auf **Erfassungssteuerung**.
4. Klicken Sie im Inforegister **Welche Kontenarten können gebucht werden** auf **Hinzufügen**.
5. Klicken Sie im Feld **Unternehmenskonten** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie im Inforegister **Welche Segmentwerte sind für diese Erfassung gültig** auf **Hinzufügen**.
9. Klicken Sie im Feld **Kontostruktur** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
10. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
12. Klicken Sie im Feld **Segment** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
13. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
14. Klicken Sie im Feld **Von Wert** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
15. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
16. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
17. Klicken Sie im Feld **Bis Wert** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
18. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
19. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.

## <a name="set-up-posting-restrictions"></a>Einrichten von Buchungseinschränkungen
1. Schließen Sie die Seite.
2. Klicken Sie auf **Buchungseinschränkungen**.
3. Wählen Sie im Feld **Wie möchten Sie Buchungseinschränkungen einrichten?** die Option 'Nach Benutzergruppe' aus.
4. In der Struktur überprüfen Sie die Gruppe, der Sie die Buchung für diesen Erfassungsnamen gestatten möchten.
5. Klicken Sie auf **OK**.

