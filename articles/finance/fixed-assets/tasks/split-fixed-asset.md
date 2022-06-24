---
title: Eine Anlage splitten
description: In diesem Artikel wird erläutert, wie Sie einen Prozentsatz eines Anlagenbuchs in ein neues Anlagenbuch aufteilen.
author: moaamer
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d7fe30702717f960a42fb2a118e0d12587024f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880787"
---
# <a name="split-a-fixed-asset"></a>Eine Anlage splitten

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie einen Prozentsatz eines Anlagenbuchs in ein neues Anlagenbuch aufteilen. 

## <a name="create-a-new-fixed-asset"></a>Neue Anlage erstellen

1. Wechseln Sie im Navigationsbereich zu **Module \> Anlagen \> Anlagen \> Anlagen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Anlagengruppe** einen Wert ein oder wählen Sie einen Wert aus. Notieren Sie sich die Anlagennummer, die später im Teilungsprozess zu verwenden ist.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Schließt das Formular.

## <a name="split-a-fixed-asset"></a>Anlage teilen

Bevor ein vollständig abgeschriebener Vermögenswert aufgeteilt wird, sollte der Status des Anlagenbuchs manuell von **Geschlossen** auf **Öffnen** geändert werden. Dieser Schritt ist erforderlich, da der Buchstatus **offen** sein muss, wenn Sie Transaktionen für den Vermögenswert buchen müssen (z. B. für einen Veräußerungsverkauf). Sie müssen auch die **Mehrere Transaktionen innerhalb eines Belegs erlauben**-Parameter auf der **Allgemeines**-Registerkarte der **Hauptbuchparameter**-Seite aktivieren. Führen Sie die folgenden Schritte aus, um die Anlage zu teilen, nachdem der Status des Anlagenbuches geändert wurde und mehrere Transaktionen innerhalb eines Belegs zulässig waren.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
