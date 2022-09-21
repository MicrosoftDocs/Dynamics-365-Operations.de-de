---
title: Versionsverlauf anzeigen, um Seiten und Fragmente wiederherzustellen
description: Dieser Artikel beschreibt, wie Sie den Versionsverlauf für eine Seite oder ein Fragment anzeigen und zu einer älteren Version in Microsoft Dynamics 365 Commerce Site Builder zurückkehren können.
author: phinneyridge
ms.date: 06/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c4d78103a3c08ee4052290fccf6750aba7eecf4a
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474098"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>Versionsverlauf anzeigen, um Seiten und Fragmente wiederherzustellen

[!include [banner](includes/banner.md)]

Dieser Artikel beschreibt, wie Sie den Versionsverlauf für eine Seite oder ein Fragment anzeigen und zu einer älteren Version in Microsoft Dynamics 365 Commerce Site Builder zurückkehren können.

Mit dem Site Builder von Commerce können Sie den Versionsverlauf einer Seite oder eines Fragments einsehen und bei Bedarf zu einer bestimmten früheren Version eines Belegs zurückkehren. Während ein Beleg geöffnet ist, können Sie in der Befehlsleiste **Verlauf anzeigen** wählen, um ein Dialogfeld **Versionsverlauf** zu öffnen, in dem auf der Registerkarte **Version** der Verlauf aller Versionen und Speicheraktivitäten für die Seite oder das Fragment aufgelistet ist. Sie können dann eine frühere Version des Belegs in der Liste auswählen, eine Vorschau davon anzeigen und sie als aktuelle Version wiederherstellen. Die Registerkarte **Aktivität** des Dialogfelds listet den gesamten Aktivitätsverlauf des Belegs auf, einschließlich aller Ereignisse zum Speichern, Veröffentlichen und Entöffentlichen.

> [!NOTE]
> Eine neue Version eines Belegs wird jedes Mal erstellt, wenn ein Site-Autor Änderungen vornimmt und dann **Bearbeitung abgeschlossen** für den Beleg wählt. 

Um den Versionsverlauf für eine Seite oder ein Fragment einzusehen und zu einer früheren Version zurückzukehren, gehen Sie wie folgt vor.

1. Öffnen Sie im Site Builder die Seite oder das Fragment, für das Sie den Versionsverlauf anzeigen möchten.
1. Wählen Sie in der Befehlsleiste **Historie anzeigen**.

    ![Schaltfläche „Verlauf anzeigen“.](./media/version-history-1.png)

1. Wählen Sie im Dialogfeld **Versionsverlauf** auf der Registerkarte **Version** eine frühere Version des Belegs aus. Der Eigenschaftsbereich auf der rechten Seite zeigt eine Miniaturvorschau der ausgewählten Version sowie Informationen darüber, wer sie wann geändert hat.

    ![Listenansicht der Versionsverwaltung.](./media/version-history-2.png)

1. Um eine vollständig gerenderte Vorschau der ausgewählten Version des Belegs anzuzeigen, wählen Sie **Vorschau**. Um die Vorschau zu schließen und zum Dialogfeld **Versionsverlauf** zurückzukehren, wählen Sie **Vorschau beenden**.
1. Um eine frühere Version eines Belegs wiederherzustellen, markieren Sie ihn in der Liste auf der Registerkarte **Version** und wählen Sie dann **Wiederherstellen**. Ein Nachrichtenfeld **Version \<version number\>** wiederherstellen erscheint und fordert Sie auf, die Wiederherstellungsaktion zu bestätigen. 

    ![Schaltfläche „Wiederherstellen“ und Nachricht zur Bestätigung.](./media/version-history-3.png)

1. Um mit der Wiederherstellungsaktion fortzufahren, wählen Sie **Wiederherstellen**. Der Site Builder wird aktualisiert und zeigt die wiederhergestellte Version der Seite oder des Fragments an.
1. Um die wiederhergestellte Version zu veröffentlichen, wählen Sie **Bearbeitung abschließen** und dann **Veröffentlichen**.
