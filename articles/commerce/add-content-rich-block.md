---
title: Textblockmodul
description: Dieser Artikel behandelt Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 9e422c203d719b2e46620ce50b9d029e7ebd8d4c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270481"
---
# <a name="text-block-module"></a>Textblockmodul

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Ein Textblockmodul ist ein Modul, mit dem Textinhalte hinzugefügt werden. Dieser Inhalt kann entweder zu Informations- oder Werbezwecken verwendet werden.

Textblock-Module werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden. Es sind jedoch Module, die nicht von Seiteninhalt oder anderen Modulen abhängen.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Beispiele für Textblockmodule in E-Commerce

Textblockmodule können folgendermaßen verwendet werden:

* Um weitere Produktfunktionen auf einer Produktdetailseite zu zeigen.
* Für Informationszwecke auf einer beliebigen Seite. So können beispielsweise die Vorteile der Treueprogrammen erklären, Versand- und Rückgaberichtlinien erläutern oder häufig gestellte Fragen umfassen oder Inhalt zu „…über uns“ bereitstellen.
* Um benutzerdefinierte Nachrichten in einer Produktdetailseite hinzufügen. (beispielsweise „kostenloser Versand für Aufträge über $50“).
* Für Haftungsausschlüsse und Kontaktdetails auf Produktdetailseiten, Einkaufswagenseiten, Auscheckenseiten und anderen Seiten, (beispielsweise „Versand und Retouren hängen von den Shoprichtlinien ab“).

Das folgende Bild zeigt ein Beispiel eines Textblockmoduls, das auf einer Homepage verwendet wird.

![Beispiel eines Textblockmoduls.](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Eigenschaften des Textblock-Moduls

| Eigenschaftenname     | Wert                                            | Beschreibung |
|-------------------|--------------------------------------------------|-------------|
| Rich-Text         | Rich-Text                                        | Absatztext. Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung. |
| Benutzerdefinierter Klassenname | Ein Cascading Style Sheets (CSS) Klassenname        | Der Name einer benutzerspezifischen CSS Klasse, die ein Entwickler zum Formatieren dieses Moduls bereitstellt. Der Klassenname sollte im Theme Pack definiert werden. |
| Schriftgröße         | **Klein**, **Mittel**, **Groß** oder **Sehr groß** | Die Schriftgröße des aktuellen Inhalts. |

## <a name="add-a-text-block-module-to-a-page"></a>Hinzufügen eines Textblockmoduls zu einer Seite

Um ein Textblockmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie einen Namen für die **Inhaltvorlage** ein und wählen OK.
1. Markieren Sie im Slot **Hauptteil** die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie in der Dialogbox **Module auswählen** das Modul **Standardseite** und wählen Sie dann **OK**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. Im Dialogfeld **Neue Seite erstellen** unter **Seitenname** geben Sie **Inhalt-Seite** ein und wählen **Weiter**.
1. Unter **Vorlage auswählen** wählen Sie **Inhalt-Vorlage** und dann aus **Weiter**.
1. Wählen Sie unter **Wählen Sie ein Layout** ein Seitenlayout (z.B. **Flexibles Layout**) und wählen Sie dann **Weiter**.
1. Unter **Prüfen und beenden** überprüfen Sie die Konfiguration der Seite. Wenn Sie die Seiteninformationen bearbeiten müssen, wählen Sie **Zurück**. Wenn die Seiteninformationen korrekt sind, wählen Sie **Seite erstellen**. 
1. Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Legen Sie im Eigenschaftsfenster für das Containermodul die Eigenschaft **Breite** auf **Container füllen** fest.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Textblock** und dann **OK** aus. 
1. Fügen Sie im Eigenschaftenbereich des Textblockmoduls Text zum Feld **Rich Text** hinzu.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Werbebannermodul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Inhaltsblockmodul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
