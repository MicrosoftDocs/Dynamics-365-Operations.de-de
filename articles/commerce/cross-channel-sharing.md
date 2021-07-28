---
title: Die kanalübergreifende Freigabe aktivieren und verwenden
description: In diesem Thema wird beschrieben, wie Sie die kanalübergreifende Freigabefunktion von Microsoft Dynamics 365 Commerce Site Builder aktivieren und verwenden.
author: psimolin
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a5f35dc48dbdf89e963108e9e8ef6faec326f970
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349721"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Kanalübergreifende Freigabe aktivieren und verwenden

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die kanalübergreifende Freigabefunktion von Microsoft Dynamics 365 Commerce Site Builder aktivieren und verwenden.

Durch die kanalübergreifende Freigabe können Einzelhändler Inhalte wiederverwenden und zwischen mehreren Kanälen einer Website austauschen. Diese Funktion ist nützlich, wenn die Site-Kanäle eine kompatible Basissprache haben oder wenn sie zahlreiche gemeinsame Inhaltselemente haben.

Die kanalübergreifende Freigabe aktiviert einen Standardkanal, der nach verfügbaren Inhalten durchsucht wird, wenn keine kanalspezifische Version des angeforderten Inhalts gefunden wird. Inhalte, die für mehrere Kanäle freigegeben werden sollen, werden im Standardkanal erstellt. Dieser Inhalt kann für jedes Gebietsschema lokalisiert werden, das auf einem beliebigen Site-Kanal verwendet wird.

## <a name="when-to-use-cross-channel-sharing"></a>Verwenden der kanalübergreifenden Freigabe

Die kanalübergreifende Freigabe ist nützlich, wenn mehrere Kanäle auf einer Website Inhalte freigeben können. Beispielsweise kann ein Einzelhändler mit mehreren Marken und Ladenzeilen, die unter einer einzigen Website zusammengefasst sind, einige Inhalte für einige oder alle Ladenzeilen freigeben. Dieser freigegebene Inhalt kann Seiten mit allgemeinen Geschäftsbedingungen, Zahlungsbedingungen, Versandmethoden und häufig gestellten Fragen (FAQ) enthalten.

Die kanalübergreifende Freigabe unterstützt auch Fragmente. Daher kann eine Inhaltsseite, die kanalspezifische Fragmente enthält, als kanalübergreifender Inhalt erstellt werden. In diesem Fall werden kanalspezifische Fragmente auf einer kanalübergreifenden Seite nur dann gerendert, wenn sie vom entsprechenden Storefront-Kanal angefordert werden, obwohl der größte Teil des Inhalts von den Kanälen gemeinsam genutzt wird.

Websites mit nur einem Kanal oder Websites mit mehreren Kanälen, auf denen keine Inhalte freigegeben werden können, profitieren nicht von der kanalübergreifenden Freigabe.

## <a name="enable-cross-channel-sharing"></a>Aktivieren der kanalübergreifenden Freigabe

Die kanalübergreifende Freigabe wird auf Site-Ebene aktiviert. Diese Operation ist einseitig. Mit anderen Worten, nachdem die kanalübergreifende Freigabe aktiviert wurde, kann sie nicht deaktiviert werden.

Führen Sie die folgenden Schritte aus, um die kanalübergreifende Freigabe im Commerce Site Builder zu aktivieren.

1. Gehen Sie zu **Site-Einstellungen \> Funktionen**.
1. Stellen Sie die Option für die **kanalübergreifende** Freigabe-Funktion auf **Ein**.

    ![Die auf „Ein“ gesetzte Option „Kanalübergreifend“ im Commerce-Website-Generator.](./media/enabling-cross-channel-sharing.png)

Nachdem Sie die kanalübergreifende Freigabe aktiviert haben, werden kanalübergreifende Informationen im Abschnitt **Kanäle** bei **Site-Einstellungen \> Funktionen** angezeigt, wie das Beispiel in der folgenden Abbildung zeigt.

![Kanalinformationen, die nach der aktivierten kanalübergreifenden Freigabe sichtbar sind.](./media/channels-cross-channel.png)

Nachdem Sie die kanalübergreifende Freigabe aktiviert haben, enthält das Feld **Kanal** oben rechts im Commerce Site Builder eine Option **Kanalübergreifender Onlineshop**, mit der Sie kanalübergreifende Inhalte verwalten können, wie in der folgenden Abbildung dargestellt.

![Option „Kanalübergreifender Onlineshop“ im Feld „Kanäle“, nachdem die kanalübergreifende Freigabe aktiviert wurde.](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Erstellen und verwenden kanalübergreifender Inhalte

Sie können kanalübergreifende Inhalte auf verschiedene Arten erstellen und verwenden. Sie können beispielsweise kanalübergreifende Fragmente erstellen, kanalübergreifende Seiten erstellen, die kanalübergreifende und kanalspezifische Inhalte verwenden, und kanalübergreifende Fragmente mit kanalspezifischen Versionen von Fragmenten überschreiben.

### <a name="create-a-cross-channel-fragment"></a>Ein kanalübergreifendes Fragment erstellen

Führen Sie die folgenden Schritte aus, um kanalübergreifende Fragmente im Commerce Site Builder zu erstellen.

1. Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.
1. Wählen Sie im Dialogfeld **Neues Seitenfragment** das Modul **Werbebanner** aus, und geben Sie dann unter **Name des Seitenfragments** einen Namen ein (z. B. **Kanalübergreifendes Banner**). Wählen Sie dann **OK** aus.
1. Im Eigenschaftenbereich des **Werbebanner**-Moduls wählen Sie **Nachricht hinzufügen** und dann **Nachricht** aus.
1. In dem **Nachricht**-Dialogfeld unter **Text** geben Sie **Kanalübergreifend** ein und wählen **OK** aus. 
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

Dieses kanalübergreifende Fragment kann auf kanalübergreifenden oder kanalspezifischen Seiten verwendet werden, die auf einem beliebigen Site-Kanal erstellt werden.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Erstellen einer kanalübergreifenden Seite, die kanalübergreifenden Inhalt verwendet

Kanalübergreifende Seiten können auf jedem Kanal Ihrer Website verwendet werden. Daher können Sie eine Seite mit freigegebenen Inhalten einmal erstellen und alle nachfolgenden Aktualisierungen an einem einzigen Ort vornehmen. Zum Beispiel kann eine kanalübergreifende Seite **Geschäftsbedingungen** mit der URL `/toc` von allen Kanälen einer Site gemeinsam genutzt werden. Wenn die Basis-URLs für die Site-Kanäle `www.fabrikam.com/brand1` und `www.fabrikam.com/brand2` sind, ist die gleiche kanalübergreifende gemeinsam genutzte **Geschäftsbedingungen**-Seite unter beiden URLs des Site-Kanals `www.fabrikam.com/brand1/toc` bzw. `www.fabrikam.com/brand2/toc`, verfügbar. Wenn die **Geschäftsbedingungen**-Seite später aktualisiert werden muss, müssen Sie nur die einzelne, freigegebene Seite aktualisieren.

Führen Sie die folgenden Schritte aus, um im Commerce Site Builder eine kanalübergreifende Seite zu erstellen, die kanalübergreifenden Inhalt verwendet.

1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie eine Vorlage z. B. **Marketing** aus.
1. Geben Sie unter **Seitenname** einen Namen für die Seite ein (z. B. **Kanalübergreifende Seite**).
1. Unter **Seiten-URL** geben Sie eine Seiten-URL ein (z. B. **Beispielseite**), und wählen Sie dann **OK** aus.
1. Im Slot **Hauptseite** der neuen Seite wählen Sie die Ellipsen-Schaltfläche (**...**) und wählen Sie **Fragment hinzufügen**.
1. Im Dialogfeld **Fragment hinzufügen** wählen Sie das zuvor erstellte kanalübergreifende Fragment mit einem Werbebanner aus und wählen dann **OK**.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Sie sollten das Werbebanner mit der Aufschrift „Kanalübergreifend“ sehen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Erstellen einer kanalspezifischen Seite, die kanalübergreifenden Inhalt verwendet

Durch die Verwendung kanalübergreifender Inhalte auf kanalspezifischen Seiten können Sie ein freigegebenes Inhaltsfragment einmal erstellen und dann auf kanalspezifischen Seiten verwenden. Dieses „Single Sourcing“ ist nützlich für freigegebene Inhalte wie Geschäftsbedingungen, Zahlungsbedingungen oder Kontaktinformationen.

Führen Sie die folgenden Schritte aus, um im Commerce Site Builder eine kanalspezifische Seite zu erstellen, die kanalübergreifenden Inhalt verwendet.

1. Innerhalb eines bestimmten Kanals, wie z. B. **Fabrikam erweiterter Onlineshop**, gehen Sie zu **Seiten** und wählen dann **Neu** aus, um eine neue Seite zu erstellen.
1. In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie eine Vorlage z. B. **Marketing** aus.
1. Geben Sie unter **Seitenname** einen Namen für die Seite ein (z. B. **Kanalspezifische Seite**).
1. Unter **Seiten-URL** geben Sie eine Seiten-URL ein (z. B. **kanalspezifischeseite**), und wählen Sie dann **OK** aus.
1. Im Slot **Hauptseite** der neuen Seite wählen Sie die Ellipsen-Schaltfläche (**...**) und wählen Sie **Fragment hinzufügen**.
1. In dem Dialogfeld **Fragment hinzufügen** unter **Kanal** wählen Sie **Kanalübergreifender Online-Shop** aus. Das zuvor erstellte kanalübergreifende Fragment sollte in der Liste angezeigt werden. Wählen Sie es und dann **OK** aus.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Sie sollten das Werbebanner mit der Aufschrift „Kanalübergreifend“ sehen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Erstellen einer kanalspezifischen Version einer kanalübergreifenden Seite

Die kanalübergreifende Freigabe unterstützt das Überschreiben kanalübergreifender Inhalte. Beispielsweise teilen alle bis auf einen Ihrer Website-Kanäle denselben Inhalt. Dieser eine Site-Kanal erfordert unterschiedliche Inhalte. Um die verschiedenen Inhalte dafür zu implementieren, überschreiben Sie den kanalübergreifenden Inhalt mit kanalspezifischem Inhalt, indem Sie eine kanalspezifische Version der kanalübergreifenden Seite erstellen.

Führen Sie die folgenden Schritte aus, um im Commerce Site Builder eine kanalspezifische Version einer kanalübergreifenden Seite zu erstellen.

1. In dem Feld **Kanal** oben rechts wählen Sie **Kanalübergreifender Onlineshop** aus.
1. Öffnen Sie die zuvor erstellte kanalübergreifende Seite.
1. Wählen Sie im Feld **Kanal** oben rechts den Kanal aus, der einen bestimmten Inhalt haben soll. Der Seiteneditor zeigt eine Meldung an, in der Sie aufgefordert werden, eine neue Seitenvariante zu erstellen.
1. Wählen Sie **Seitenvariante erstellen** aus.
1. Im **Haupt**-Slot der Seitenvariante wählen Sie die Ellipse (**...**) und dann **Modul hinzufügen** aus.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Werbebanner** und dann **OK** aus.
1. Im Eigenschaftenbereich des **Werbebanner**-Moduls wählen Sie **Nachricht hinzufügen** und dann **Nachricht** aus.
1. In dem **Nachricht**-Dialogfeld unter **Text** geben Sie **Kanalspezifisch** ein und wählen **OK** aus.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Sie sollten das Werbebanner mit der Aufschrift „Kanalspezifisch“ sehen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

Wenn Sie nun die Basis-URL des Kanals verwenden und zur URL der kanalübergreifenden Seite auf dieser Site wechseln, wird der kanalspezifische Inhalt anstelle des kanalübergreifenden Inhalts angezeigt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Möglichkeiten zum Hinzufügen von Inhalten](add-manage-content.md)

[Seitenmodellglossar](page-elements-overview.md)

[Dokumentstatus und -Lebenszyklus](document-states-overview.md)

[Arbeiten mit Veröffentlichungsgruppen](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
