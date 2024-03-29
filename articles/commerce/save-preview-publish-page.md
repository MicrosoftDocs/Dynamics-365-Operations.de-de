---
title: Speichern, Vorschau und Veröffentlichung einer Seite
description: In diesem Artikel wird beschrieben, wie eine Seite in Microsoft Dynamics 365 Commerce gespeichert, als Vorschau angezeigt und veröffentlicht wird.
author: josaw1
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: bf9cc4eb916976ed0c87f27cf8df7c0d52d07ef0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280213"
---
# <a name="save-preview-and-publish-a-page"></a>Speichern, Vorschau und Veröffentlichung einer Seite

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie eine Seite in Microsoft Dynamics 365 Commerce gespeichert, als Vorschau angezeigt und veröffentlicht wird.

## <a name="save-a-page"></a>Speichern einer Seite

Um eine Seite zu speichern, müssen Sie sie für sich selbst auschecken und im Seiteneditor öffnen. Um eine Seite auszuchecken, wählen Sie in der Befehlsleiste **Bearbeiten** aus. Nach dem Bearbeiten einer Seite sollten Sie diese umgehend speichern, um sicherzustellen, dass Ihre Änderungen beibehalten werden.

Wenn Sie eine Seite speichern, sind die Änderungen nur für Sie sichtbar. Der Speichervorgang dient hauptsächlich zum Speichern von Änderungen, während die Seite noch nicht zum Einchecken bereit ist. Nachdem Sie die Seite bearbeitet haben, wird empfohlen, sie einzuchecken, damit die Änderungen für andere sichtbar werden. Zu diesem Zeitpunkt kann die Seite auch von anderen Benutzern ausgecheckt werden, die sie ändern müssen.

## <a name="preview-a-page"></a>Eine Seite als Vorschau anzeigen

Das Dokumenterstellungstool bietet zwei Arten von Vorschaufunktionen: Visual Page Builder, was ein „What you see is what you get“ (WYSIWYG)-Vorschaubereich im Seiteneditor ist und ein separates Vorschaufenster.

Bei der Verwendung des Seiteneditors wird eine WYSIWYG-Vorschau (What you see is what you get) im mittleren Bereich angezeigt. Diese Vorschau wird automatisch aktualisiert, wenn Sie die Seite speichern. Sie können dies auch manuell aktualisieren, indem Sie **Aktualisieren** in der Befehlsleiste auswählen. In der Vorschau wird die Seite so gerendert, wie sie den Benutzern der Site angezeigt wird. Darüber werden jedoch Dokumenterstellungshilfen gerendert.

Wenn Sie die Seite geändert haben, möchten Sie möglicherweise eine Vorschau anzeigen, um zu sehen, was Kunden sehen werden. Um eine Seite als Vorschau anzuzeigen, wählen Sie **Vorschau** in der Befehlsleiste aus. Die Vorschau wird in einem separaten Browserfenster angezeigt. Die Seite im Vorschaufenster wird so gerendert, wie es der Benutzer der Site sieht. Sie können die Größe des Fensters ändern, um sicherzustellen, dass die reagierenden Module in allen Ansichtsports korrekt gerendert werden.

> [!NOTE]
> Authentifizierung und korrekte Berechtigungen sind erforderlich, um eine Vorschau des unveröffentlichten Inhalts anzuzeigen. Wenn Sie die URL der Vorschau für eine andere Person freigeben, muss diese Person über die richtigen Berechtigungen für den Zugriff auf den Inhalt verfügen.

## <a name="publish-a-page"></a>Eine Seite veröffentlichen

Wenn Ihre Seite fertig ist, besteht der nächste Schritt darin, sie zu veröffentlichen, damit externe Benutzer den Inhalt anzeigen können. Bevor Sie eine Seite veröffentlichen können, müssen Sie sie durch Auswählen von **Beenden Sie die Bearbeitung** in der Befehlsleiste einchecken.

Sie können Seiten entweder im Seiteninspektor oder im Seiteneditor veröffentlichen und deren Veröffentlichung aufheben. Der Seiteninspektor zeigt eine Liste der Seiten an und ermöglicht Massenvorgänge. Mit dem Seiteneditor können Sie nur die einzelne Seite, die dort geöffnet ist, veröffentlichen oder deren Veröffentlichung aufheben.

Um eine oder mehrere Seiten im Seiteninspektor zu veröffentlichen, wählen Sie die Seiten aus, stellen Sie sicher, dass sie eingecheckt sind, und wählen Sie dann **Veröffentlichen** in der Befehlsleiste aus. Die Seiten werden veröffentlicht, und Sie erhalten eine Benachrichtigung über den Vorgang im Authoring-Tool.

Um eine einzelne Seite aus dem Seiteneditor heraus zu veröffentlichen, verfahren Sie ähnlich. Stellen Sie, während die Seite im Seiteneditor geöffnet ist, sicher, dass sie eingecheckt wurde, und wählen Sie dann **Veröffentlichen** in der Befehlsleiste aus. Die Seite wird veröffentlicht und Sie erhalten eine Benachrichtigung über den Vorgang.

Wenn Sie eine Seite veröffentlichen, wird nur der Seiteninhalt veröffentlicht. Sie und andere Benutzer können die Seite nur dann aufrufen und anzeigen, wenn ihr eine URL zugeordnet ist. Die URL muss getrennt veröffentlicht werden.

> [!IMPORTANT]
> Bevor Sie eine Seite veröffentlichen können, müssen alle Bilder oder Fragmente, auf die die Seite verweist, bereits veröffentlicht sein.

## <a name="save-preview-and-publish-a-home-page"></a>Speichern, Vorschau und Veröffentlichen einer Startseite

Gehen Sie folgendermaßen vor, um eine Startseite zu speichern, in der Vorschau anzuzeigen und zu veröffentlichen.

1. Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.
1. Wählen Sie im Navigationsbereich links **Seiten** aus.
1. Suchen Sie die Startseite und wählen Sie sie aus, um sie im Seiteneditor zu öffnen.
1. Wählen Sie **Bearbeiten** aus.
1. Ändern Sie die Seite nach Bedarf.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Geben Sie im Feld **Kommentare** eine Notiz zu den Änderungen ein, die Sie vorgenommen haben, und wählen Sie dann **OK** aus.
1. Wählen Sie **Vorschau** aus, um Ihre Seite in der Vorschau anzuzeigen. Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.
1. Wählen Sie **Veröffentlichen** aus.

## <a name="publish-a-url"></a>Eine URL veröffentlichen

Führen Sie folgende Schritte aus, um eine URL zu veröffentlichen.

1. Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.
1. Wählen Sie im linken Navigationsbereich **URLs** aus.
1. Suchen und wählen Sie die zu veröffentlichende URL aus.
1. Wählen Sie in der Befehlsleiste **Veröffentlichen** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Bestehende Seite einer Website ändern](modify-existing-page.md)

[Neue Seite hinzufügen](add-new-page.md)

[Auswählen von Seitenlayouts](select-page-layouts.md)

[Verwalten von SEO-Metadaten](manage-seo-metadata.md)

[Erweitern einer Produktseite](enrich-product-page.md)

[Füllen einer Kategorie-Landingpage](enrich-category-page.md)

[Überprüfen der Zugänglichkeit des Seiteninhalts](verify-accessibility.md)

[Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
