---
title: Einstellungen „Produkt in den Warenkorb legen“ anwenden
description: Dieses Thema behandelt die Einstellungen „Produkt in den Warenkorb leben“ und beschreibt, wie sie in Microsoft Dynamics 365 Commerce angewendet werden.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6299a1c815978ab9f748b6110980e673e1fbae927ed08a5e2e080f89ef063115
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712813"
---
# <a name="apply-add-product-to-cart-settings"></a>Einstellungen „Produkt in den Warenkorb legen“ anwenden

[!include [banner](includes/banner.md)]

Dieses Thema behandelt die Einstellungen **Produkt in den Warenkorb leben** und beschreibt, wie sie in Microsoft Dynamics 365 Commerce angewendet werden.

Es werden verschiedene Workflows unterstützt, wenn ein Produkt auf einer Dynamics 365 Commerce-E-Commerce-Site in den Warenkorb gelegt wird. Der Site-Benutzer kann beispielsweise zur Warenkorbseite weitergeleitet werden. Alternativ kann der Benutzer auf der aktuellen Seite bleiben, aber eine Benachrichtigung erhalten, die bestätigt, dass das Produkt in den Warenkorb gelegt wurde.

Um die verschiedenen Workflows zu unterstützen, steht das Feld **Produkt in den Warenkorb legen** unter **Einstellungen \> Erweiterungen** im Commerce-Website-Generator zur Verfügung. Wählen Sie eine der folgenden Einstellungsoptionen, um den entsprechenden Workflow zu implementieren:

- **Zur Warenkorbseite navigieren** – Benutzer werden zur Warenkorbseite weitergeleitet, wenn sie dem Warenkorb einen Artikel hinzufügen.
- **Benachrichtigung anzeigen** – Benutzern wird eine Bestätigungsbenachrichtigung angezeigt, wenn sie dem Warenkorb einen Artikel hinzufügen, und sie können weiter auf der Produktdetailseite (PDP) browsen.
- **Mini-Warenkorb anzeigen** – Wenn Benutzer einen Artikel in den Warenkorb legen, wird der Inhalt des Mini-Warenkorbs angezeigt. Benutzer können alle Artikel im Warenkorb überprüfen und zur Kasse gehen, wenn sie soweit sind.
- **Benachrichtigung mit dem Benachrichtigungsmodul anzeigen** – Wenn Benutzer einen Artikel in den Warenkorb legen, wird das Benachrichtigungsmodul verwendet, um eine Bestätigungsbenachrichtigung anzuzeigen. Damit diese Einstellungsoption funktioniert, muss das Benachrichtigungsmodul zum Seitenkopf hinzugefügt werden.
- **Nicht zur Warenkorbseite navigieren** – Benutzer bleiben auf der aktuellen Seite, wenn sie dem Warenkorb einen Artikel hinzufügen.

Die folgende Abbildung zeigt ein Beispiel für die Einstellungsoptionen **Produkt in den Warenkorb legen** im Website-Generator.

![Beispiel für die Einstellungsoptionen „Produkt in den Warenkorb legen“ im Website-Generator](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - Die Website-Einstellungen **Produkt in den Warenkorb legen** mit Stand der Dynamics 365 Commerce-Version 10.0.11. Wenn Sie eine Aktualisierung von einer älteren Version von Dynamics 365 Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren. Informationen zum Aktualisieren der Datei appsettings.json finden Sie unter [SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - Die Einstellungsoption **Mini-Warenkorb anzeigen** ist ab der Dynamics 365 Commerce-Version 10.0.20 verfügbar. Wenn Sie eine Aktualisierung von einer älteren Version von Dynamics 365 Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren. Informationen zum Aktualisieren der Datei appsettings.json finden Sie unter [SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

Das folgende Darstellung zeigt ein Beispiel einer Benachrichtigung „Zum Warenkorb hinzugefügt“ auf der Fabrikam-Site.

![Beispiel einer Benachrichtigung „Zum Warenkorb hinzugefügt“ auf der Fabrikam-Site](./media/ecommerce-addtocart-notifications.PNG)

Das folgende Darstellung zeigt ein Beispiel einer Benachrichtigung „Zum Warenkorb hinzugefügt“ auf der Adventure Works-Site.

![Beispiel einer Benachrichtigung „Zum Warenkorb hinzugefügt“ auf der Adventure Works-Site](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Kauffeldmodul](add-buy-box.md)

[Shopauswahlmodul](store-selector.md)
