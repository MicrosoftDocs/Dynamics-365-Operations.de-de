---
title: Textblock-Modul
description: Dieses Thema enthält Textblockmodule und es wird beschrieben, wie diese Site-Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025596"
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

## <a name="text-block-module-properties"></a>Eigenschaften des Textblock-Moduls

| Eigenschaftenname     | Value                                            | Beschreibung |
|-------------------|--------------------------------------------------|-------------|
| Rich-Text         | Rich-Text                                        | Absatztext. Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung. |
| Benutzerdefinierter Klassenname | Ein Cascading Style Sheets ( CSS) Klassenname        | Der Name einer benutzerspezifischen CSS Klasse, die ein Entwickler zum Formatieren dieses Moduls bereitstellt. Der Klassenname sollte im Theme Pack definiert werden. |
| Schriftgröße         | **Klein**, **Mittel**, **Groß** oder **Sehr groß** | Die Schriftgröße des aktuellen Inhalts. |

## <a name="add-a-text-block-module-to-a-page"></a>Hinzufügen eines Textblockmoduls zu einer Seite

Um ein Textblockmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine Seitenvorlage, die mit **Inhaltvorlage** bezeichnet ist. 
1. Fügen Sie im Slot **Text** das Modul **Standardseite** hinzu.
1. Beenden Sie die Bearbeitung der Vorlage und veröffentlichen Sie sie.
1. Verwenden Sie die Inhaltvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Inhaltseite** hat.
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu.
1. Legen Sie im Eigenschaftsfenster für das Containermodul die Eigenschaft **Breite** auf **Container füllen** fest.
1. Fügen Sie dem Containermodul ein Textblockmodul hinzu. 
1. Fügen Sie im Eigenschaftenbereich des Textblockmoduls Text zum Feld **Rich Text** hinzu.
1. Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie sie.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Übersicht](starter-kit-overview.md)

[Werbebanner-Modul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Inhaltsblockmodul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)

