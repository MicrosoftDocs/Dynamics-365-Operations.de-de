---
title: Anlage teilen
description: In diesem Abschnitt wird erläutert, wie Sie einen Prozentsatz eines Anlagenbuchs in ein neues Anlagenbuch aufteilen.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000292"
---
# <a name="split-a-fixed-asset"></a>Anlage teilen

[!include [banner](../../includes/banner.md)]

In diesem Abschnitt wird erläutert, wie Sie einen Prozentsatz eines Anlagenbuchs in ein neues Anlagenbuch aufteilen. Dabei werden die "Buchhalterrolle" und die USMF-Demodaten verwendet.

## <a name="create-a-new-fixed-asset"></a>Neue Anlage erstellen

1. Wechseln Sie im Navigationsbereich zu **Module \> Anlagen \> Anlagen \> Anlagen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Anlagengruppe** einen Wert ein oder wählen Sie einen Wert aus. Notieren Sie sich die Anlagennummer, die später im Teilungsprozess zu verwenden ist.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Schließt das Formular.

## <a name="split-a-fixed-asset"></a>Anlage teilen

Bevor ein vollständig abgeschriebener Vermögenswert aufgeteilt wird, sollte der Status des Anlagenbuchs manuell von **Geschlossen** auf **Öffnen** geändert werden. Dieser Schritt ist erforderlich, da der Buchstatus **offen** sein muss, wenn Sie Transaktionen für den Vermögenswert buchen müssen (z. B. für einen Veräußerungsverkauf). Führen Sie die folgenden Schritte aus, um die Anlage zu teilen, nachdem der Status des Anlage-Buches geändert wurde.

1. Suchen und wählen Sie in der Liste die Verknüpfung der zu teilenden Anlage.
2. Wählen Sie **Bücher**. Wählen Sie das Buch aus, um die neue Anlage aufzuteilen.
3. Wählen Sie **Funktionen**.
4. Wählen Sie **Anlage teilen**.
5. Geben Sie im Feld **Zu Anlage** einen Wert ein oder wählen Sie ihn aus.
6. Wählen Sie im Feld **Zum Buch** die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Geben Sie im Feld **Transaktionsdatum** ein Datum ein.
8. Geben Sie im Feld **Prozent** eine Zahl ein.
9. Geben Sie im Feld **Journalname** einen Wert ein oder wählen Sie ihn aus.
10. Wählen Sie **OK**.

## <a name="post-the-journal-transaction"></a>Die Erfassungstransaktion buchen

1. Gehen Sie im Navigationsbereich zu **Module \> Anlage \> Journalbuchungen \> Anlagenbuchhaltung**.
2. Wählen Sie in der Liste die Erfassung aus, die mit dem Teilungsprozess erstellt wurde.
3. Wählen Sie **Positionen** aus.

    - Überprüfen Sie die erstellten Erfassungspositionen.
    - Eine "Anschaffungsänderungstransaktion" wird für die ursprüngliche Anlage erstellt, um den Wert um den Prozentsatz zu verringern, der im Teilungsprozess angegeben wird.
    - Eine "Anschaffungstransaktion" wird für die neue Anlage für denselben Betrag erstellt.

4. Wählen Sie **Buchen** aus.
