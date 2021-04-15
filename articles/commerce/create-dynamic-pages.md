---
title: Dynamische E-Commerce-Seiten anhand von URL-Parametern erstellen
description: In diesem Thema wird erläutert, wie Sie eine E-Commerce-Seite in Microsoft Dynamics 365 Commerce einrichten, die basierend auf URL-Parametern dynamischen Inhalt bereitstellen kann.
author: StuHarg
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8f59b80880e6947e1b45c110df0e78d4bdd57c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795810"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Dynamische E-Commerce-Seiten anhand von URL-Parametern erstellen

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie eine E-Commerce-Seite in Microsoft Dynamics 365 Commerce einrichten, die basierend auf URL-Parametern dynamischen Inhalt bereitstellen kann.

Eine E-Commerce-Seite kann so konfiguriert werden, dass sie unterschiedliche Inhalte basierend auf einem Segment im URL-Pfad bereitstellt. Daher wird die Seite als dynamische Seite bezeichnet. Das Segment wird als Parameter zum Abrufen des Seiteninhalts verwendet. So wird beispielsweise eine Seite namens **Blog\_Zuschauer** erstellt und der URL `https://fabrikam.com/blog` zugeordnet. Diese Seite kann dann verwendet werden, um unterschiedliche Inhalte basierend auf dem letzten Segment im URL-Pfad anzuzeigen. Zum Beispiel ist das letzte Segment in der URL `https://fabrikam.com/blog/article-1` **Artikel-1**.

Separate benutzerdefinierte Seiten, die die dynamische Seite überschreiben, können auch Segmenten im URL-Pfad zugeordnet werden. So wird beispielsweise eine Seite namens **Blog\_Zusammenfassung** erstellt und der URL `https://fabrikam.com/blog/about-this-blog` zugeordnet. Wird diese URL angefordert, wird die Seite **Blog\_Zusammenfassung**, die dem Parameter **/über-diesen-Blog** zugeordnet ist, anstelle der Seite **Blog\_Zuschauer** zurückgegeben.

> [!NOTE]
> Die Funktionen zum Hosten, Abrufen und Anzeigen dynamischer Seiteninhalte werden mithilfe eines benutzerdefinierten Moduls implementiert. Weitere Informationen finden Sie unter [Onlinekanalerweiterbarkeit](e-commerce-extensibility/overview.md).

## <a name="set-up-a-dynamic-e-commerce-page"></a>Eine dynamische E-Commerce-Seite einrichten

Um eine dynamische E-Commerce-Seite einzurichten, müssen Sie die dynamische Seite sowie die Basis-URL erstellen und die Route zur dynamischen Seite konfigurieren.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>Die Seite, die dynamischen Inhalt bereitstellt, erstellen

Führen Sie die folgenden Schritte aus, um eine Seite zu erstellen, die dynamischen Inhalt bereitstellt [Eine neue Website-Seite hinzufügen](add-new-page.md). Für die von Ihnen erstellte Seite muss ein Modul implementiert werden, das das letzte Segment im URL-Pfad verwendet, um Inhalte aus einer externen Datenquelle abzurufen. Weitere Informationen zur Entwicklung benutzerdefinierter Module finden Sie unter [Onlinekanalerweiterbarkeit](e-commerce-extensibility/overview.md).

### <a name="create-the-base-url-for-the-dynamic-page"></a>Die Basis-URL für die dynamische Seite erstellen

Führen Sie die folgenden Schritte aus, um die Basis-URL für die dynamische Seite im Commerce-Website-Generator zu erstellen.

1. Rufen Sie **URLs** auf, und wählen Sie **Neu \> Neue URL** aus.
1. Wählen Sie im Dialogfeld **Neue URL erstellen** die Option **Interne Seite** aus. Egen Sie unter **URL-Pfad** den Pfad ein, der als Stamm für die dynamische Seite dient (in diesem Beispiel: **/Blog**). Wählen Sie dann **Weiter** aus.
1. Wählen Sie im Dialogfeld **Eine Seite auswählen** die Seite aus, die Sie zuvor als dynamische Seite erstellt haben, und wählen Sie dann **Speichern** aus.
1. Wählen Sie **Veröffentlichen** aus.

### <a name="configure-the-route-to-the-dynamic-page"></a>Die Route zur dynamischen Seite konfigurieren

Führen Sie die folgenden Schritte aus, um die Route zu der dynamischen Seite im Commerce-Website-Generator zu konfigurieren.

1. Gehen Sie zu **Seiteneinstellungen \> Erweiterungen**.
1. Wählen Sie unter **Parametrisierte URL-Pfade** die Option **Hinzufügen** aus. Geben Sie dann den URL-Pfad ein, den Sie beim Erstellen der URL eingegeben haben (in diesem Beispiel: **/Blog**).
1. Wählen Sie **Speichern und veröffentlichen** aus.

Sobald die Route konfiguriert wurde, geben alle Anfragen an den parametrisierten URL-Pfad die Seite zurück, die dieser URL zugeordnet ist. Wenn Anfragen ein zusätzliches Segment enthalten, wird die zugehörige Seite zurückgegeben und der Seiteninhalt mithilfe des Segments als Parameter abgerufen. Beispielsweise gibt `https://fabrikam.com/blog/article-1` die Seite **Blog\_Zusammenfassung** zurück, und der Seiteninhalt wird mithilfe des **/Artikel-1**-Parameters abgerufen.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Eine parametrisierte URL mit einer benutzerdefinierten Seite überschreiben

Führen Sie die folgenden Schritte aus, um eine parametrisierte URL mit einer benutzerdefinierten Seite im Commerce-Website-Generator zu überschreiben.

1. Rufen Sie **URLs** auf, und wählen Sie **Neu \> Neue URL** aus.
1. Wählen Sie im Dialogfeld **Neue URL erstellen** die Option **Interne Seite** aus. Geben Sie unter **URL-Pfad** den Pfad ein, der das zu überschreibende Segment enthält (in diesem Beispiel: **/Blog/über-diesen-Blog**). Wählen Sie dann **Weiter** aus.
1. Wählen Sie im Dialogfeld **Eine Seite auswählen** die benutzerdefinierte Seite und anschließend **Speichern** aus.
1. Wählen Sie **Veröffentlichen** aus.
1. Wenn die benutzerdefinierte Seite noch nicht veröffentlicht wurde, rufen Sie **Seiten** auf, wählen Sie die benutzerdefinierte Seite und anschließend **Veröffentlichen** aus.

Nachdem die benutzerdefinierte Seite veröffentlicht wurde, wird sie anstelle der dynamischen Seite mit parametrisiertem Inhalt bereitgestellt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Bestehende Seite einer Website ändern](modify-existing-page.md)

[Neue Seite hinzufügen](add-new-page.md)

[Auswählen von Seitenlayouts](select-page-layouts.md)

[Verwalten von SEO-Metadaten](manage-seo-metadata.md)

[Speichern, Vorschau und Veröffentlichung einer Seite](save-preview-publish-page.md)

[Erweitern einer Produktseite](enrich-product-page.md)

[Füllen einer Kategorie-Landingpage](enrich-category-page.md)

[Überprüfen der Zugänglichkeit des Seiteninhalts](verify-accessibility.md)

[Onlinekanalerweiterbarkeit](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
