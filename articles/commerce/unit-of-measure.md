---
title: Einstellungen für Maßeinheiten anwenden
description: Dieser Artikel behandelt die Einstellungen der Maßeinheit und beschreibt, wie sie auf Microsoft Dynamics 365 Commerce festgelegt werden.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 7a7be6395a8bfce38e84f850bd792f358941c18a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275569"
---
# <a name="apply-unit-of-measure-settings"></a>Einstellungen für Maßeinheiten anwenden

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt die Einstellungen der Maßeinheit und beschreibt, wie sie auf Microsoft Dynamics 365 Commerce festgelegt werden.

Ein Produkt kann in verschiedenen Einheiten verkauft werden, z. B. „pro Stück“, „Paar“ und „Dutzend“. In der Commerce headquarters kann die verkaufte Maßeinheit für ein Produkt definiert werden und auf einer E-Commerce-Seite angezeigt werden. Wenn zum Beispiel ein Einzelhändler ein Produkt sowohl einzeln als auch in Dutzenden verkauft, können die verfügbaren Maßeinheiten zusammen mit anderen Produktinformationen angezeigt werden.

Im Beispiel in der folgenden Abbildung wurde für ein Produkt in der Commerce headquarters eine Maßeinheit **ea** (pro Stück) konfiguriert.

![Beispiel für ein Produkt, das mit einer Maßeinheit in der Commerce-Zentralverwaltung konfiguriert ist.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Unterstützung für die Anwendung und Anzeige der Maßeinheit ist ab der Commerce-Version 10.0.19 verfügbar.

## <a name="unit-of-measure-settings"></a>Einstellungen für die Maßeinheit

Die Einstellungen für die Anzeige von Maßeinheiten werden im Commerce Site Builder festgelegt, und zwar unter **Site-Einstellungen \> Erweiterungen \> Anzeige der Maßeinheit für Produkte**. Es gibt drei unterstützte Einstellungen:

- **Nicht anzeigen** – Wenn diese Einstellung festgelegt ist, wird auf der E-Commerce-Seite die Maßeinheit für das Produkt nicht angezeigt. Dieses Verhalten ist das Standardverhalten.
- **Anzeigen in der Produkt-Kauferfahrung** – Wenn diese Einstellung festgelegt ist, wird die Maßeinheit auf den Produkt-Detailseiten, im Warenkorb, an der Kasse, in der Bestellhistorie und auf den Bestelldetailseiten angezeigt.
- **Anzeige in der Produktübersicht und beim Kauf** – Wenn diese Einstellung festgelegt ist, wird die Maßeinheit auf den Seiten der Produktübersicht und auch während der Produktübersicht angezeigt. Als Teil dieses Verhaltens werden Maßeinheiten in den Suchergebnissen und den Modulen der Produktsammlung angezeigt.

> [!IMPORTANT]
> Die Einstellungen für die Anzeige von Maßeinheiten sind ab der Commerce-Version 10.0.19 verfügbar. Wenn Sie ein Update von einer älteren Version von Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren. Anweisungen finden Sie unter [SDK- und Modulbibliotheks-Updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Module, die die Einstellungen für die Maßeinheit verwenden

Zu den Modulen, die die Einstellungen für die Maßeinheit verwenden, gehören die Module „Kaufbox“, „Wunschliste“, „Warenkorb“, „Warenkorb-Symbol“, „Suchergebnis-Container“, „Produktsammlung“, „Kasse“ und „Bestelldetails“.

Im Beispiel in der folgenden Abbildung zeigt eine Produkt-Detailseite (PDP) die Maßeinheit (**ea**) für ein Produkt an.

![Beispiel für ein PDP, das die Maßeinheit anzeigt.](./media/Productunit-PDP.png)

In dem Beispiel in der folgenden Abbildung zeigt ein Produktsammlungsmodul die Maßeinheit (**ea**) für ein Produkt an.

![Beispiel eines Produktsammlung-Moduls, das die Maßeinheit anzeigt.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Einkaufswagenmodul](add-cart-module.md)

[Kauffeldmodul](add-buy-box.md)

[Seiten und Module zur Kontenverwaltung](account-management.md)

[SDK- und Modulbibliotheksupdates](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
