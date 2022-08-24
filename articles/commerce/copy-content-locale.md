---
title: Kopieren Sie den Inhalt in ein anderes Gebietsschema
description: Dieser Artikel beschreibt, wie Sie in Microsoft Dynamics 365 Commerce bestehende Inhalte innerhalb einer Website in ein anderes Gebietsschema kopieren können.
author: josaw1
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6afa871048bde22133ae083b8d56b6e99e49c401
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269260"
---
# <a name="copy-content-to-another-locale"></a>Kopieren Sie den Inhalt in ein anderes Gebietsschema

[!include[banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie in Microsoft Dynamics 365 Commerce bestehende Inhalte innerhalb einer Website in ein anderes Gebietsschema kopieren können.

Wenn Sie Inhalte in Commerce Site Builder erstellen, werden diese immer mit einer Gebietsschema-Kennung wie „en-us“ verknüpft. Sie können einzelne Seiten und Assets in ein anderes Gebietsschema innerhalb derselben E-Commerce-Website kopieren, indem Sie das Gebietsschema wechseln, wenn Sie einen Artikel bearbeiten und dann eine neue Variante des Artikels erstellen. In manchen Fällen, z.B. wenn Sie ein völlig neues Gebietsschema für Ihren Shop einführen, ist es sinnvoll, alle Inhaltsartikel eines bestehenden Gebietsschemas in das neue Gebietsschema zu duplizieren. Wenn das neue Gebietsschema dieselbe Basissprache hat wie eines der vorhandenen Gebietsschemata, können Sie das vorhandene Gebietsschema als Quellgebietsschema für den Vorgang des Kopierens des Gebietsschemas verwenden. (Zum Beispiel verwenden die Gebietsschemata „en-us“ und „en-au“ beide die englische Sprache.) Auf diese Weise helfen Sie, den Aufwand für die Lokalisierung des Inhalts im neuen Gebietsschema zu verringern.

Die folgenden Vorgehensweisen erklären, wie Sie einem bestehenden Channel ein neues Gebietsschema hinzufügen, alle Inhaltsartikel eines bestehenden Gebietsschemas in ein neues Gebietsschema kopieren und den Status eines Gebietsschema-Kopiervorgangs überwachen.

## <a name="add-a-new-locale"></a>Fügen Sie ein neues Gebietsschema hinzu

So fügen Sie in Commerce Site Builder ein neues Gebietsschema hinzu.

1. Gehen Sie im Website-Builder zu Ihrer Website.
1. Wählen Sie im linken Navigationsbereich **Site-Einstellungen** und dann **Kanäle**.
1. Wählen Sie unter **Kanal** den Kanal aus, dem Sie das neue Gebietsschema hinzufügen möchten.
1. Wählen Sie im Dialogfeld Kanal, das rechts erscheint, **Ein Gebietsschema hinzufügen**.
1. Wählen Sie in der Dialogbox **Ein Gebietsschema hinzufügen** im Feld **Zu unterstützendes Gebietsschema** ein Gebietsschema aus.
1. Stellen Sie sicher, dass der Wert **Domäne** korrekt ist.
1. Geben Sie unter **Pfad** einen eindeutigen URL-Pfad ein (zum Beispiel **de-us** oder **english-us**).
1. Wählen Sie **OK** aus.
1. Schließen Sie das Dialogfeld Kanal.
1. Überprüfen Sie unter **Kanal**, ob das neue Gebietsschema neben dem richtigen Kanal aufgeführt ist.
1. Wählen Sie **Speichern und veröffentlichen** aus.

> [!NOTE]
> Bevor das neue Gebietsschema im Site Builder konfiguriert werden kann, muss es in der Commerce headquarters dem zugehörigen Online Store-Kanal hinzugefügt werden.

## <a name="copy-all-content-items-to-a-new-locale"></a>Kopieren Sie alle Artikel des Inhalts in ein neues Gebietsschema

Gehen Sie folgendermaßen vor, um alle Artikel in Commerce Site Builder in ein neues Gebietsschema zu kopieren.

1. Gehen Sie im Website-Builder zu Ihrer Website.
1. Wählen Sie im linken Navigationsbereich **Site-Einstellungen** und dann **Kanäle**.
1. Wählen Sie in der Befehlsleiste **Lokalkopie erstellen von**.
1. Bestätigen Sie im Dialogfenster **Lokalkopie erstellen**, das rechts erscheint, unter **Quellseite**, dass die richtige Seite ausgewählt ist.
1. Wählen Sie im Feld **Quellkanal** den Quellkanal.
1. Wählen Sie im Feld **Zielkanal** denselben Quellkanal.
1. Wählen Sie im Feld **Quellgebietsschema** das Quellgebietsschema aus.
1. Wählen Sie im Feld **Zielgebietsschema** das neue Gebietsschema aus.
1. Wählen Sie **Gebietsschema kopieren**. Eine Benachrichtigung bestätigt, dass der Vorgang des Kopierens von Gebietsschemata begonnen hat.

> [!NOTE]
> Sie können auch Inhalte zwischen verschiedenen Kanälen kopieren.

## <a name="monitor-the-status-of-the-locale-copy"></a>Überwachen Sie den Status der Gebietsschema-Kopie

Um den Status eines Vorgangs zum Kopieren eines Gebietsschemas zu überwachen, folgen Sie diesen Schritten.

1. Gehen Sie im Website-Builder zu Ihrer Website.
1. Wählen Sie im linken Navigationsbereich **Site-Einstellungen** und dann **Aufträge**.
1. Wählen Sie unter **Aktuelle Aufträge** den zu überwachenden Auftrag. Die Auftragsdetails werden in dem rechts angezeigten Dialogfeld angezeigt.
