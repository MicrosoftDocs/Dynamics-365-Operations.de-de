---
title: Bestehende Seite einer Website ändern
description: In diesem Artikel wird beschrieben, wie Sie eine vorhandene Websiteseite in Microsoft Dynamics 365 Commerce ändern.
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
ms.openlocfilehash: ceffb07afc8287e975f48696a059d3cd4ad20ffa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848862"
---
# <a name="modify-an-existing-site-page"></a>Bestehende Seite einer Website ändern

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie eine vorhandene Websiteseite in Microsoft Dynamics 365 Commerce ändern.

Wenn Sie eine Seite ändern müssen, müssen Sie sie zunächst im Seiteneditor öffnen. Gehen Sie zu der Site, die Ihre Seite enthält, und suchen Sie dann in der Liste der Seiten die gewünschte Seite. Wenn Sie die Seite nicht finden können, können Sie die umfangreiche Suchfunktion des Erstellungstools verwenden. Geben Sie entweder den genauen Seitennamen oder die ersten Buchstaben und dann ein Sternchen ein (\*). Eine gefilterte Liste der Seiten wird angezeigt. Sie können diese Liste verwenden, um die gewünschte Seite zu finden. Nachdem Sie die richtige Seite gefunden haben, wählen Sie den Seitennamen aus, um die Seite im Seiteneditor zu öffnen.

> [!TIP]
> Wenn Ihre Seite im Seiteninspektor angezeigt wird, können Sie **Bearbeiten** auswählen und sie auschecken, bevor Sie sie im Seiteneditor öffnen. Auf diese Weise können Sie mehrere Seiten gleichzeitig auschecken.

Nachdem die Seite im Seiteneditor geöffnet wurde, müssen Sie sicherstellen, dass sie für Sie ausgecheckt ist. Die Befehlsleiste im Erstellungstools ist dynamisch, kontextbezogen und statusabhängig. Daher werden nur die Aktionen angezeigt, die Sie derzeit auf der Seite ausführen können. Wenn die Seite beispielsweise nicht für Sie ausgecheckt wurde, werden die Schalflächen **Speichern** und **Bearbeiten beenden** nicht in der Befehlsleiste angezeigt. Der Status der Seite wird auch auf der rechten Seite des Fensters angezeigt.

Wenn die Seite noch nicht für Sie ausgecheckt wurde, wählen Sie **Bearbeiten** in der Befehlsleiste aus. Die Befehlsleiste ändert sich, um den neuen Status der Seite widerzuspiegeln. Sie erhalten auch eine Benachrichtigung, die besagt, dass die Seite für Sie ausgecheckt wurde.

Der nächste Schritt besteht darin, Ihre tatsächlichen Änderungen vorzunehmen. Häufig verwenden Sie die Seitengliederungsstruktur auf der linken Seite, um das zu ändernde Modul zu suchen und auszuwählen, und nehmen dann im Eigenschaftsfenster auf der rechten Seite Änderungen vor. 

Ihre Änderung kann jedoch manchmal das Hinzufügen oder Entfernen von Modellen oder Fragmenten umfassen. Um ein Fragment oder Modul hinzuzufügen, suchen Sie in der Seitenstruktur den Slot, dem Sie das Modul oder Fragment hinzufügen möchten, und klicken Sie dann auf die Schaltfläche mit den Auslassungspunkten (**...**) für diesen Slot. Ein Menü mit Befehlen zum Hinzufügen eines Moduls oder Fragments wird angezeigt. Um ein Modul oder Fragment zu entfernen, suchen Sie es und wählen Sie es in der Seitenstruktur aus, klicken Sie auf die Schaltfläche mit den Auslassungspunkten und wählen Sie dann den Befehl zum Löschen des Moduls oder Fragments aus.

> [!TIP]
> Sie können auch die Eigenschaften für jedes Modul anzeigen und bearbeiten, das in der Visual Page Builder-Vorschau angezeigt wird, indem Sie es direkt auswählen.

Nachdem Sie Ihre Änderungen vorgenommen und eine Vorschau des Effekts angezeigt haben, sollten Sie die Seite durch Auswahl von **Bearbeiten beenden** auf der Befehlsleiste einchecken. 

Um Ihre Änderungen umgehend zu veröffentlichen, wählen Sie **Veröffentlichen** in der Befehlsleiste aus. Die zuletzt eingecheckte Version der Seite, die Sie geändert haben, wird veröffentlicht und steht externen Benutzern zur Verfügung, die Ihre Website anzeigen. 

## <a name="example-change-the-video-on-the-home-page"></a>Beispiel: Das Video auf der Startseite ändern

Das folgende Beispiel zeigt, wie Sie die Startseite ändern, indem Sie das im Video-Player-Modul angezeigte Video ändern.

1. Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.
1. Wählen Sie im Navigationsbereich links **Seiten** aus.
1. Suchen Sie die Startseite und wählen Sie sie aus, um sie im Seiteneditor zu öffnen.
1. Wählen Sie in der Befehlsleiste **Bearbeiten** aus.
1. Wählen Sie in der Seitengliederung den **Haupt**-Slot aus.
1. Erweitern Sie unter dem **Haupt**-Slot alle flüssigen Containermodule.
1. Suchen Sie das Video-Player-Modul und wählen Sie es aus.
1. Wählen Sie im Eigenschaftenbereich rechts die Eigenschaft **Video** aus. Die Anlagen-Auswahl wird angezeigt.
1. Wählen Sie in der Anlagen-Auswahl eine verfügbare Videoanlage oder **Neue Anlage hochladen** aus, um eine neue Videoanlage hochzuladen.
1. Wählen Sie **OK**.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Geben Sie im Feld **Kommentare** **Video geändert** ein und wählen Sie dann **OK** aus.
1. Wählen Sie **Vorschau** aus, um die aktualisierte Seite in der Vorschau anzuzeigen. Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.
1. Wählen Sie **Veröffentlichen** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Neue Seite hinzufügen](add-new-page.md)

[Auswählen von Seitenlayouts](select-page-layouts.md)

[Verwalten von SEO-Metadaten](manage-seo-metadata.md)

[Speichern, Vorschau und Veröffentlichung einer Seite](save-preview-publish-page.md)

[Erweitern einer Produktseite](enrich-product-page.md)

[Kategoriezielseite erweitern](enrich-category-page.md)

[Überprüfen der Zugänglichkeit des Seiteninhalts](verify-accessibility.md)

[Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
