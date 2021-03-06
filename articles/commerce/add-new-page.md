---
title: Neue Seite hinzufügen
description: In diesem Thema wird beschrieben, wie Sie eine neue Websiteseite in Microsoft Dynamics 365 Commerce hinzufügen.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797550"
---
# <a name="add-a-new-site-page"></a>Neue Seite hinzufügen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine neue Websiteseite in Microsoft Dynamics 365 Commerce hinzufügen.

Nachdem Sie Vorlagen und Fragmente für Ihre Site erstellt haben, besteht der nächste Schritt darin, die Seiten zu erstellen, von denen die Kategorien verwendet werden. Um anzufangen, müssen Sie eine Vorlage oder ein Layout, einen Seitenname und eine URL Seite auswählen.

## <a name="template-or-layout"></a>Vorlage oder Layout

Sie können entweder eine ursprüngliche Vorlage oder ein Layout für die neue Seite nutzen. Weitere Informationen finden Sie unter [Vorlagen und Layouts Überblick](templates-layouts-overview.md).

## <a name="page-name"></a>Seitenname

Der Seitenname muss für die Seite eindeutig sein. Er sollte beschreibend sein, sodass Sie ihn einfach finden können und andere Personen wissen, für was die Seite ist. Wählen Sie den Seitennamen sorgfältig aus, da sie später nicht geändert werden kann.

## <a name="page-url"></a>Seiten-URL

Sie können die Option haben, eine URL für die neue Seite einzugeben. Wenn Sie eine Seite erstellen, können Sie eine Zeichenfolge eingeben, die verwendet wird, um die URL zu vervollständigen. Diese Zeichenfolge ist als relative URL oder URL-Typ bekannt. Eine vollständige URL wird anschließend auf Basis des URL-Typs generiert, und die neue Seite wird zugeordnet. Sie können den URL-Typ später ändern, bevor Sie die Seite veröffentlichen. Weitere Informationen finden Sie unter [Erstellen einer URL-Seite](create-page-URL.md).

> [!NOTE]
> Dynamics 365 Commerce entkoppelt URLs und Inhalt. Das bedeutet, eine Seite kann erstellt werden, die keiner URL zugeordnet ist, und eine URL kann erstellt werden, die keiner Seite zugeordnet ist. Daher kann Inhalt-Auslagerung für eine URL erfolgen und erfordert keine Ausfallzeit und die Umleitungen sind einfacher zu verwalten.

## <a name="add-a-new-page"></a>Eine neue Seite hinzufügen

Um eine neue Seite Ihrer Site hinzufügen, führen Sie die folgenden Schritte aus.

1. Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.
1. Wählen Sie **Neue Seite** aus.
1. Wählen Sie im Dialogfeld **Neue Seite** eine Vorlage und wählen dann **OK**.
1. Wählen Sie im Feld **Seitenname** einen Seitennamen (z.B. **Meine neue Seite**).
1. Wählen Sie das Feld **URL** und geben Sei eine Zeichenfolge ein (URL-Typ) um die URL abzuschließen (beispielsweise **mynewpage**).
1. Wählen Sie **OK**. Der Seiteneditor wird angezeigt. Beachten Sie, dass eine Kopf- und eine Fußzeile automatisch der Seite hinzugefügt werden, basierend auf der Vorlage, die Sie ausgewählt haben.
1. Auf dem Seitenüberblick wählen Sie den Slot (**Haupt**) und wählen die Ellipsen-Schaltfläche **...** und wählen Sie **Modul hinzufügen**.
1. Wählen Sie **Container** und dann **OK** aus
1. Wählen Sie **Fluid Container** und wählen Sie dann die Ellipsen-Schaltfläche und wählen **Modul hinzufügen**.
1. Wählen Sie **Umfangreicher Inhaltsblock** und wählen Sie **OK** aus.
1. Wählen Sie **Umfangreicher Inhaltsblock** und wählen Sie dann die Ellipsen-Schaltfläche und wählen dann **Modul hinzufügen**.
1. Wählen Sie **Umfangreiches Inhaltsblockelement** und wählen Sie **OK** aus.
1. Im Eigenschaftenbereich auf der rechten Seite, wählen Sie, **Absatz** und dann geben Sie im Feld **Mein Prüftext** ein.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Geben Sie im Feld **Kommentare** **Neue Seite hinzufügen** ein und wählen Sie dann **OK** aus.
1. Wählen Sie **Vorschau** aus, um Ihre Seite in der Vorschau anzuzeigen. Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.
1. Wählen Sie **Veröffentlichen** aus.
1. Im Navigationspfad (Breadcrumbs) wählen Sie **Fabrikam** (oder den Namen der Site).
1. Wählen Sie im linken Navigationsbereich **URLs** aus.
1. Suchen Sie Ihre URL und wählen Sie sie aus in der Liste (**mynewpage**).
1. Wählen Sie **Veröffentlichen** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Bestehende Seite einer Website ändern](modify-existing-page.md)

[Auswählen von Seitenlayouts](select-page-layouts.md)

[Verwalten von SEO-Metadaten](manage-seo-metadata.md)

[Speichern, Vorschau und Veröffentlichung einer Seite](save-preview-publish-page.md)

[Erweitern einer Produktseite](enrich-product-page.md)

[Kategoriezielseite erweitern](enrich-category-page.md)

[Überprüfen der Zugänglichkeit des Seiteninhalts](verify-accessibility.md)

[Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
