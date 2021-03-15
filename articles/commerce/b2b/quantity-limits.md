---
title: Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites
description: In diesem Thema wird beschrieben, wie Sie Produktmengenbeschränkungen für B2B-E-Commerce-Websites (Business-to-Business) einrichten.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e70648da2cc1c526625b6e34fd0867d40abb5a85
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035912"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Produktmengenbeschränkungen für B2B-E-Commerce-Websites (Business-to-Business) einrichten.

Die meisten Produkte haben eine Maßeinheit, die ihre Gruppierung definiert. Die Gruppierung beeinflusst, wie die Produkte verkauft werden können. Einige Produkte haben möglicherweise eine zusätzliche Gruppierung für Mengen. Diese Gruppierung bestimmt, ob die Produkte als einzelne Einheiten oder als Vielfache verkauft werden können und ob ein Mindest- oder Höchstbestellmengenlimit eingehalten werden muss.

Die Mengenbegrenzungsfunktion stellt sicher, dass die Mindest-, Höchst-, Mehrfach- und Standardmengen, die in Microsoft Dynamics 365 Commerce konfiguriert sind (in den Standardeinstellungen für Bestellungen oder in den Site-Einstellungen für den Commerce-Website-Generator). auf Kundenbestellungen angewendet werden, die auf einer E-Commerce-Site aufgegeben werden. Produktmengenbeschränkungen werden derzeit für Point of Sale (POS) und Call Center nicht unterstützt.

Viele Einzelhändler bieten die Option der Debitorenaufträge (auch Sonderaufträge), um die verschiedenen Produkt- und Erfüllungsbedingungen zu erfüllen. Nachfolgend sind einige typische Szenarios:

- Ein Kunde möchte, dass Produkte bestimmter Varianten in Vielfachen von wenigen Artikeln verkauft werden.
- Ein Debitor möchte Produkte von einem Shop oder einem Lagerplatz aufheben, der aus Filiale oder vom Lagerplatz abweicht, an dem der Debitor die Produkte gekauft hat. Die Verpackungsstandards für die Geschäfte unterscheiden sich jedoch von den Verpackungsstandards für den Online-Vertrieb.
- Ein Kunde möchte ein Produkt in limitierter Auflage kaufen, das ein maximales Mengenlimit für Artikel hat, die gekauft werden können.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>Die Funktion für Standardbestelleinstellung in der Commerce-Zentralverwaltung aktivieren

Bevor Sie Produktmengenlimits festlegen können, muss die Standardfunktion für Bestelleinstellungen in der Commerce-Zentralverwaltung aktiviert werden.

Führen Sie diese Schritte aus, um die Funktion Standardbestelleinstellungen zu aktivieren.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.
1. Suchen Sie die **Die Einstellungen für Website und Standardbestellung in der Kundenbestellung unterstützen** Funktion und wählen Sie sie aus.
1. Wählen Sie unten im rechten Bereich die Option **Jetzt aktivieren** aus. 

## <a name="define-quantity-settings"></a>Mengeneinstellungen festlegen 

Sie können die Mengeneinstellungen auf der Seite **Standardauftragseinstellungen** definieren.

Gehen Sie zum Festlegen der Mengeneinstellungen folgendermaßen vor. 

1. Navigieren Sie zu Produkt **Einzelhandel und Handel \> Produkte und Kategorien \> Freigegebene Produkte nach Kategorie**.
1. Wählen Sie ein freigegebenes Produkt.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Auftragseinstellungen** die Option **Standardauftragseinstellungen** aus. 
1. Legen Sie auf der **Standardbestelleinstellungen**-Seite, im Inforegister **Auftrag** im **Verkaufsmenge**-Abschnitt die Produktverkaufsmengen fest:

    - **Mehrere** – die Menge, in deren Vielfachen das Produkt gekauft werden kann.
    - **Mindestbestellmenge** – die Mindestanzahl der Produkte, die gekauft werden müssen.
    - **Maximalbestellmenge** – die Maximalanzahl der Produkte, die gekauft werden kann.
    - **Standardbestellmenge** – die Standardmenge, die bei Auswahl des Produkts automatisch eingegeben wird.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Aktivieren Sie die Funktion für B2B-Bestellmengenbeschränkungen im Commerce-Website-Generator

Führen Sie diese Schritte aus, um die Funktion für B2B-Bestellmengenbeschränkungen im Commerce-Website-Generator zu aktivieren.

1. Gehen Sie zu **Site-Einstellungen \> Erweiterungen**
1. Unter **Bestellmengenlimits aktivieren** wählen Sie im Dropdown-Menü **Für B2B-Kunden aktiviert**. 

> [!NOTE] 
> Aktualisierte Einstellungen für den Site Builder werden erst wirksam, nachdem die Datei App.settings.json aktualisiert wurde. Weitere Informationen finden Sie unter [SDK- und Modulbibliothek-Updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine B2B-E-Commerce-Website einrichten](set-up-b2b-site.md)

[Erstellen von Organisationsmodellierungshierarchien für B2B-Organisationen](org-model.md)

[Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten](manage-b2b-users.md)

[Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]