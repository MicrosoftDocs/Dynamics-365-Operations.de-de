---
title: Umfangreiches Inhaltsblockmodul
description: Dieses Thema enthält umfangreiche Inhaltsblockmodule und beschreibt, wie sie den Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785420"
---
# <a name="content-rich-block-module"></a>Umfangreiches Inhaltsblockmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält umfangreiche Inhaltsblockmodule und beschreibt, wie sie den Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Ein umfangreiches Inhaltsblockmodul ist ein spezieller Container, der eines oder mehrere umfangreichen Inhaltsblockmodule aufnimmt. Umfangreiche Inhaltsblockmodule werden für Textinhalt auf einer Seite verwendet. Dieser Inhalt kann entweder zu Informations- oder Werbezwecke verwendet werden.

Umfangreiche Inhaltsblockmodule werden von Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite verwendet werden. Es sind jedoch Module, die nicht von Seiteninhalt oder anderen Modulen abhängen.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>Beispiele für umfangreiche Inhaltsblockmodule in E-Commerce

Umfangreiche Inhaltsblockmodule können folgendermaßen verwendet werden:

* Um weitere Produktfunktionen auf einer Produktdetailseite zu zeigen.
* Für Informationszwecke auf einer beliebigen Seite. So können beispielsweise die Vorteile der Treueprogrammen erklären, Versand- und Rückgaberichtlinien erläutern oder häufig gestellte Fragen umfassen oder Inhalt zu „…über uns“ bereitstellen.
* Um benutzerdefinierte Nachrichten in einer Produktdetailseite hinzufügen. (beispielsweise „kostenloser Versand für Aufträge über $50“).
* Für Haftungsausschlüsse und Kontaktdetails auf Produktdetailseiten, Einkaufswagenseiten, Auscheckenseiten und anderen Seiten, (beispielsweise „Versand und Retouren hängen von den Shoprichtlinien ab“).

## <a name="content-rich-block-module-properties"></a>Umfangreiche Inhaltsblockmoduleigenschaften

| Eigenschaftenname     | Wert                                 | Eigenschaft |
|-------------------|---------------------------------------|----------|
| Spaltenanzahl | Eine Nummer aus **1** bis **4**     | Die Anzahl der Spalten in umfangreichen Inhaltsblockmodulen Es kann bis zu vier Spalten geben. |
| Breite             | **Container ausfüllen** oder **Bildschirm ausfüllen** | Wenn der Wert auf **Container ausfüllen** festgelegt ist, wird der Container auf die Breite des Containers beschränkt. Wenn der Wert auf **Bildschirm ausfüllen** gesetzt wird, werden die Elemente nicht auf die Containerbreite eingeschränkt und können den Bildschirm ausfüllen. Sie können den Wert ändern, um das gewünschte Layout zu erreichen. |

## <a name="content-rich-block-item-module-properties"></a>Umfangreiche Inhaltsblockelementmoduleigenschaften

| Eigenschaftenname | Wert          | Beschreibung |
|---------------|----------------|-------------|
| Absatz     | Absatztext | Der Text, der jeden umfangreichen Inhaltsblockmoduls begleiten soll. Einige grundlegende umfangreiche Inhaltsblockmodule werden unterstützt wie Fettformatierung und Kursivformattierung. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Hinzufügen eines umfangreichen Inhaltsblockmoduls zu einer Seite

Um ein umfangreiches Inhaltsblockmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Erstellen Sie eine Seitenvorlage, die mit **Inhaltvorlage** bezeichnet ist.
1. Im **Haupt-** Slot der Standardseite fügen Sie ein umfangreiches Inhaltsblockmodul hinzu.
1. Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.
1. Verwenden Sie die Inhaltvorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Inhaltseite** hat.
1. Im **Haupt-** Slot der neuen Seite fügen Sie ein umfangreiches Inhaltsblockmodul hinzu.
1. In den Eigenschaften des umfangreichen Inhaltsblockmoduls legen Sie die Zahl der Spalten auf **2** fest.
1. Im umfangreichen Inhaltsblockmodul wählen Sie **Modul hinzufügen** und fügen ein umfangreiches Inhaltsblockmodulelement hinzu (zum Beispiel **item1**).
1. In einem neuen umfangreiches Inhaltsblockmodul fügen Sie den Absatztext hinzu.
1. Im umfangreichen Inhaltsblockmodul wählen Sie **Modul hinzufügen** und fügen ein umfangreiches Inhaltsblockmodulelement hinzu (zum Beispiel **item2**).
1. In einem neuen umfangreiches Inhaltsblockmodul fügen Sie den Absatztext hinzu.
1. Seite speichern und Änderungen in der Vorschau anzeigen. Sie sollten zwei Rich-Text-Textblöcke in einer Zwei-Spaltenansicht sehen.
1. Laden Sie die Seite hoch und veröffentlichen Sie sie.

> [!NOTE]
> Wenn Sie einen dritten umfangreichen Inhaltsblock hinzufügen, wird er unter den zwei Elementen angeordnet, die Sie zuvor hinzugefügt haben. Wenn Sie die Anzahl und Artikel im Container ändern, können Sie unterschiedliche Layouts für Textinhalt erreichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Warnmmodul](add-alert.md)

[Karussellmodul](add-carousel.md)

[Inhaltsplatzierungsmodul](add-content-placement-modules.md)

[Funktionsmodul](add-feature-module.md)

[Hero-Modul](add-hero-module.md)

[Video-Player-Modul](add-video-player.md)

