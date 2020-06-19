---
title: Textblock-Modul
description: Dieses Thema enthält Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 93ad09a05d188a30b099b9a44c35e15839be80a7
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411134"
---
# <a name="text-block-module"></a>Textblock-Modul


[!include [banner](includes/banner.md)]

Dieses Thema enthält Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein Textblockmodul ist ein Modul, mit dem Textinhalte hinzugefügt werden. Dieser Inhalt kann entweder zu Informations- oder Werbezwecken verwendet werden.

Textblock-Module werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden. Es sind jedoch Module, die nicht von Seiteninhalt oder anderen Modulen abhängen.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Beispiele für Textblockmodule in E-Commerce

Textblockmodule können folgendermaßen verwendet werden:

* Um weitere Produktfunktionen auf einer Produktdetailseite zu zeigen.
* Für Informationszwecke auf einer beliebigen Seite. So können beispielsweise die Vorteile der Treueprogrammen erklären, Versand- und Rückgaberichtlinien erläutern oder häufig gestellte Fragen umfassen oder Inhalt zu „…über uns“ bereitstellen.
* Um benutzerdefinierte Nachrichten in einer Produktdetailseite hinzufügen. (beispielsweise „kostenloser Versand für Aufträge über $50“).
* Für Haftungsausschlüsse und Kontaktdetails auf Produktdetailseiten, Einkaufswagenseiten, Auscheckenseiten und anderen Seiten, (beispielsweise „Versand und Retouren hängen von den Shoprichtlinien ab“).

Das folgende Bild zeigt ein Beispiel eines Textblockmoduls, das auf einer Homepage verwendet wird.

![Beispiel eines Textblockmoduls](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Eigenschaften des Textblock-Moduls

| Eigenschaftenname     | Wert                                            | Beschreibung |
|-------------------|--------------------------------------------------|-------------|
| Rich-Text         | Rich-Text                                        | Absatztext. Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung. |
| Benutzerdefinierter Klassenname | Ein Cascading Style Sheets ( CSS) Klassenname        | Der Name einer benutzerspezifischen CSS Klasse, die ein Entwickler zum Formatieren dieses Moduls bereitstellt. Der Klassenname sollte im Theme Pack definiert werden. |
| Schriftgröße         | **Klein**, **Mittel**, **Groß** oder **Sehr groß** | Die Schriftgröße des aktuellen Inhalts. |

## <a name="add-a-text-block-module-to-a-page"></a>Hinzufügen eines Textblockmoduls zu einer Seite

Um ein Textblockmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie einen Namen für die **Inhaltvorlage** ein und wählen OK.
1. Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die Vorlage **Inhalt-Vorlage** aus. Unter **Seitenname** geben Sie **Inhalt-Seite** ein und wählen dann **OK** aus.
1. Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.
1. Legen Sie im Eigenschaftsfenster für das Containermodul die Eigenschaft **Breite** auf **Container füllen** fest.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Textblock** und dann **OK** aus. 
1. Fügen Sie im Eigenschaftenbereich des Textblockmoduls Text zum Feld **Rich Text** hinzu.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Starterkit](starter-kit-overview.md)

[Werbebannermodul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Inhaltsblockmodul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)

