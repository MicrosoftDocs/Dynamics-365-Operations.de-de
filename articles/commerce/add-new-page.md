---
title: Neue Seite hinzufügen
description: In diesem Thema wird beschrieben, wie Sie eine neue Websiteseite in Microsoft Dynamics 365 Commerce hinzufügen.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b0f1e290526c25aa6e6300c65e24044a325bee53
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269957"
---
# <a name="add-a-new-site-page"></a>Neue Seite hinzufügen


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine neue Websiteseite in Microsoft Dynamics 365 Commerce hinzufügen.

## <a name="overview"></a>Übersicht

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
1. Wählen Sie **Fluid Container**und wählen Sie dann die Ellipsen-Schaltfläche und wählen **Modul hinzufügen**.
1. Wählen Sie **Umfangreicher Inhaltsblock** und wählen Sie **OK** aus.
1. Wählen Sie **Umfangreicher Inhaltsblock**und wählen Sie dann die Ellipsen-Schaltfläche und wählen dann **Modul hinzufügen**.
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

[Füllen einer Kategorie-Landingpage](enrich-category-page.md)

[Überprüfen der Zugänglichkeit des Seiteninhalts](verify-accessibility.md)
