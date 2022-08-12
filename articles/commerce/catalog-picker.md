---
title: Modul für die Katalogauswahl
description: Dieser Artikel befasst sich mit den Modulen zur Katalogauswahl und beschreibt, wie Sie diese zu Microsoft Dynamics 365 Commerce Business-to-business (B2B) E-Commerce Websites hinzufügen können.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136943"
---
# <a name="catalog-picker-module"></a>Modul für die Katalogauswahl

[!include [banner](includes/banner.md)]

Dieser Artikel befasst sich mit den Modulen zur Katalogauswahl und beschreibt, wie Sie diese zu Microsoft Dynamics 365 Commerce Business-to-business (B2B) E-Commerce Websites hinzufügen können.

Ein Katalogauswahlmodul ist ein spezieller Container, der dazu dient, alle Produktkataloge aufzulisten, die den Benutzern der B2B-Website zum Einkaufen zur Verfügung stehen. Mehrere Kataloge werden derzeit nur für B2B-Websites unterstützt.

Die folgende Abbildung zeigt ein Beispiel für ein Katalog-Pickermodul.

![Beispiel für ein Katalog-Pickermodul, das drei Produktkataloge auflistet.](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Fügen Sie ein Katalogauswahlmodul zu Ihrer Website hinzu

Gehen Sie folgendermaßen vor, um Ihrer Website in Commerce Site Builder ein Katalogauswahlmodul hinzuzufügen.

### <a name="create-a-catalog-picker-page"></a>Erstellen Sie eine Katalog-Pickerseite

Erstellen Sie zunächst eine Katalogauswahlseite.

1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. Im Dialogfeld **Eine neue Seite erstellen** geben Sie unter **Seitenname** **Katalogpicker** ein.
1. Geben Sie unter **Seiten-URL** eine URL für die Seite ein und wählen Sie dann **Weiter**.

    ![Erstellen Sie ein Dialogfeld für eine neue Seite.](./media/Create-catalog-picker-page.png)

1. Wählen Sie unter **Wählen Sie eine Vorlage**, wählen Sie **Allgemeiner Inhalt** und wählen Sie dann **Weiter**.
1. Wählen Sie unter **Wählen Sie ein Layout** die Option **Flexibles Layout** und wählen Sie dann **Weiter**.
1. Unter **Prüfen und beenden** überprüfen Sie die Konfiguration der Seite. Wenn Sie die Seiteninformationen bearbeiten müssen, wählen Sie **Zurück**. Wenn die Seiteninformationen korrekt sind, wählen Sie **Seite erstellen**.
1. Wählen Sie unter **Katalogauswahl** die Option **Hauptplatz**, markieren Sie die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.

    ![Hinzufügen eines Moduls zur Zuteilung von Zeitfenstern unter Catalog picker.](./media/Author-web-page-catalog-picker-1.png)

1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Markieren Sie den Steckplatz **Container**, markieren Sie die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Katalog-Picker** und wählen Sie dann **OK**.
1. Wählen Sie im Bereich **Katalogauswahl** unter **Überschrift** die Option **Kataloge** und geben Sie dann eine Überschrift für die Katalogauswahlseite ein.
1. Wählen Sie unter **Überschriftsebene** eine Überschriftsebene und wählen Sie dann **OK**.
1. Geben Sie unter **Rich-Text** den Text ein, der oben auf der Katalogauswahlseite erscheinen soll.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

### <a name="add-a-link-on-your-account-page"></a>Fügen Sie einen Link auf Ihrer Kontoseite hinzu

Als nächstes fügen Sie auf Ihrer **Mein Konto** Seite einen Verweis auf Ihre Katalogauswahlseite hinzu.

1. Gehen Sie zu **Seiten**, suchen und wählen Sie die Seite **Mein Konto** Ihrer Website und wählen Sie dann **Bearbeiten**.
1. Wählen Sie unter dem **Hauptfenster** der Seite die **Generische Kachel für Konten**. 
1. Wählen Sie im Eigenschaftsbereich **Konto generische Kachel** unter **Verknüpfungen** die Option **Aktionsverknüpfung hinzufügen** und anschließend die Option **Aktionsverknüpfung**.
1. Geben Sie im Dialogfeld **Aktionslink** unter **Linktext** den Linktext für den Link zu Ihrer Katalogauswahlseite ein.
1. Wählen Sie unter **Verknüpfungsziel** die Option **Verknüpfung hinzufügen**.
1. Wählen Sie im Dialogfeld **Link hinzufügen** die Option **Benutzerdefinierte Seite** und wählen Sie dann **Weiter**.
1. Wählen Sie unter **Name** Ihre Katalogauswahlseite aus, wählen Sie **Anwenden** und wählen Sie dann **OK**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

Die folgende Abbildung zeigt ein Beispiel für eine Buchhaltungsseite mit einem Verweis auf die Katalogseite.

![Seite Meine Konten mit Link zum Katalog.](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Fügen Sie einen Link in der Kopfzeile hinzu

Fügen Sie schließlich einen Link von der Kopfzeile Ihrer Website zu Ihren Katalogen hinzu.

1. Gehen Sie zu **Fragmente**, suchen und markieren Sie das Kopfzeilenfragment Ihrer Website und wählen Sie dann **Bearbeiten**.
1. Wählen Sie den Slot **Kopf** aus. 
1. Wählen Sie im Eigenschaftenbereich **Kopfzeile** unter **Meine Kontoverknüpfungen** die Option **Aktionsverknüpfung hinzufügen** und dann **Aktionsverknüpfung**.
1. Geben Sie im Dialogfeld **Aktionslink** unter **Linktext** den Linktext für den Link zu Ihrer Katalogauswahlseite ein.
1. Wählen Sie unter **Verknüpfungsziel** die Option **Verknüpfung hinzufügen**.
1. Wählen Sie im Dialogfeld **Link hinzufügen** die Option **Benutzerdefinierte Seite** und wählen Sie dann **Weiter**.
1. Wählen Sie unter **Name** Ihre Katalogauswahlseite aus, wählen Sie **Anwenden** und wählen Sie dann **OK**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Kopffragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

Die folgende Abbildung zeigt ein Beispiel für die Kopfzeile einer E-Commerce-Website mit einem Verweis auf den B2B-Katalog.

![Kopfzeile der E-Commerce-Website mit Dropdown-Link zum Katalog.](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Zusätzliche Ressourcen 

[Commerce-Kataloge für B2B-Websites erstellen](catalogs-b2b-sites.md)

[Auswirkung der Erweiterbarkeit von Commerce-Katalogen auf B2B-Anpassungen](catalogs-b2b-sites-dev.md)

[FAQ zu Commerce-Katalogen für B2B](catalogs-b2b-sites-FAQ.md)

[Seiten und Module zur Kontenverwaltung](account-management.md)

[Kopfzeilenmodul](author-header-module.md)
