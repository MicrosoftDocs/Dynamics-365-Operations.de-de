---
title: Barrierefreiheit von Seiteninhalten prüfen
description: In diesem Artikel wird beschrieben, wie Sie die Barrierefreiheit von Seiteninhalten in Microsoft Dynamics 365 Commerce überprüfen.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 686ec37f24cf68902c4dd918c0ca8aea7612e1a9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291972"
---
# <a name="verify-page-content-accessibility"></a>Barrierefreiheit von Seiteninhalten prüfen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie die Barrierefreiheit von Seiteninhalten in Microsoft Dynamics 365 Commerce überprüfen.

Wenn Sie mit dem Ändern einer Seite fertig sind, sollten Sie sicherstellen, dass der Inhalt für alle im Web zugänglich ist. In den Commerce-Authoring-Tools können Sie mithilfe des integrierten Dienstes [Microsoft Accessibility Insights](https://accessibilityinsights.io/) auf einfache Weise die Zugänglichkeit von Seiteninhalten überprüfen. Dieser Dienst überprüft Ihren Seiteninhalt anhand der neuesten Richtlinien zur [World Wide Web Consortium (W3C Zugänglichkeit)](https://www.w3.org/standards/webdesign/accessibility).

Die [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-Integration muss auf Mandanten- oder Site-Ebene aktiviert sein, bevor Sie sie verwenden können.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Aktivieren Sie Microsoft Accessibility Insights für alle Websites in Ihrem Mandanten

Um [Microsoft Accessibility Insights](https://accessibilityinsights.io/) zu aktivieren, führen Sie die folgenden Schritte aus, um alle Commerce-Sites in Ihrem Mandanten zu integrieren.

> [!NOTE]
> Um auf Mandanteneinstellungen zuzugreifen, müssen Sie als Systemadministrator bei Commerce angemeldet sein.

1. Melden Sie sich bei Commerce als Systemadministrator an.
1. Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.
1. Wählen Sie unter **Mandanteneinstellungen** die Option **Funktionen** aus.
1. Legen Sie die Option **Zugänglichkeitsprüfung** auf **Ein** fest.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Aktivieren Sie Microsoft Accessibility Insights für eine einzelne Site

Um die [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-Integration für eine einzelne Commerce-Site zu aktivieren, führen Sie die folgenden Schritte aus.

1. Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.
1. Wählen Sie im linken Navigationsbereich **Site-Einstellungen** aus, um den Bereich zu erweitern.
1. Wählen Sie unter **Site-Einstellungen** die Option **Funktionen** aus.
1. Legen Sie die Option **Zugänglichkeitsprüfung** auf **Ein** fest.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Überprüfen Sie die Zugänglichkeit des Inhalts auf der Homepage

Um den integrierten [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-Dienst zu verwenden und so den Inhalt Ihrer Startseite in Commerce zu scannen und zu prüfen, gehen Sie folgendermaßen vor.

1. Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.
1. Wählen Sie im linken Navigationsbereich die Option **Seiten** aus.
1. Suchen Sie die Startseite und wählen Sie sie aus, um sie im Seiteneditor zu öffnen.
1. Wählen Sie in der Befehlsleiste die Option **Zugänglichkeit prüfen** aus. Die Seite **Zugänglichkeit prüfen** wird angezeigt.
1. Überprüfen Sie nach Abschluss des Scans den Inhalt des Berichts.
1. Wenn Prüfungen fehlgeschlagen sind, wählen Sie jedes fehlgeschlagene Prüfelement aus, um es zu erweitern und weitere Details anzuzeigen.
1. Um den Bericht zu schließen, nachdem Sie ihn geprüft haben, scrollen Sie zur Seite **Zugänglichkeit prüfen**, und wählen Sie **OK** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Bestehende Seite einer Website ändern](modify-existing-page.md)

[Neue Seite hinzufügen](add-new-page.md)

[Auswählen von Seitenlayouts](select-page-layouts.md)

[Verwalten von SEO-Metadaten](manage-seo-metadata.md)

[Speichern, Vorschau und Veröffentlichung einer Seite](save-preview-publish-page.md)

[Erweitern einer Produktseite](enrich-product-page.md)

[Füllen einer Kategorie-Landingpage](enrich-category-page.md)

[Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
