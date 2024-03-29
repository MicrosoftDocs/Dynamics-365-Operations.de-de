---
title: Geschenkkartenmodul
description: Dieser Artikel behandelt Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 93e2a6608b6d3190df7df1d8f85fd9d7e1c18692
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280557"
---
# <a name="gift-card-module"></a>Geschenkkartenmodul

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt Geschenkkartenmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Geschenkkartenmodule können in Checkout-Modulen verwendet werden, um Geschenkkarten zu akzeptieren, eine übliche Zahlungsmethode, die für E-Commerce-Transaktionen genutzt wird. Das Geschenkkartenmodul unterstützt Dynamics 365-, SVS- und Givex-Geschenkkarten. SVS- und Givex-Geschenkkarten werden über den Adyen-Zahlungsanbieter eingelöst. Weitere Informationen zur Unterstützung externer Geschenkkarten wie SVS und Givex finden Sie unter [Unterstützung für externe Geschenkkarten](./dev-itpro/gift-card.md).

> [!NOTE]
> Hilfe für das Einlösen von SVS- und Givex-Geschenkkarten während des Checkout-Flows finden Sie in Dynamics 365 Commerce 10.0.11. 

Es stehen zwei Geschenkkartenmodule zur Verfügung:

- **Geschenkkarte** – Dieses Modul kann auf einer Kassenseite verwendet werden, um eine Geschenkkarte als Angebot einzulösen. 
- **Überprüfung des Guthabens einer Geschenkkarte** – Dieses Modul kann auf jeder Seite verwendet werden, um den Saldo einer Geschenkkarte zu prüfen. Dieses Modul ist in Commerce Version 10.0.14 und höher verfügbar.

> [!NOTE]
> Hilfe für das Modul „Guthabenüberprüfung der Geschenkkarte“ finden Sie in Dynamics 365 Commerce 10.0.14.

Das folgende Bild zeigt ein Beispiel eines Geschenkkartenmoduls, das auf einer Auschecken-Seite verwendet wird.

![Beispiel eines Geschenkkarten-Moduls.](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Moduleigenschaften

- **Zusätzliche Felder anzeigen** – Diese Eigenschaft definiert, welche Felder bei Geschenkkarten zusätzlich zur Geschenkkartennummer angezeigt werden sollen, die standardmäßig immer angezeigt wird. Beispielsweise unterstützen einige Geschenkkarten die Anzeige einer persönlichen Identifikationsnummer (PIN), andere die Anzeige einer PIN und eines Ablaufdatums. Alternativ könnte diese Eigenschaft auf Keine gesetzt werden, wodurch nur die Geschenkkartennummer und keine zusätzlichen Felder angezeigt werden.

    Folgende Werte werden unterstützt:

    - PIN
    - Ablaufdatum
    - Pin und Ablaufdatum festlegen 
    - Ohne

- **Für Gastbenutzer aktivieren**: Wenn diese Eigenschaft aktiviert ist, können Gastbenutzer Guthaben auf Geschenkkarten einlösen oder überprüfen. Diese Eigenschaft erfordert, dass der anonyme (Gast-)Zugriff für Geschenkkarten in der Commerce-Zentralverwaltung aktiviert ist. Weitere Informationen finden Sie unter [Aktivieren von Geschenkkarten-Zahlungen für Bezahlung als Gast](#enable-gift-card-payments-for-guest-checkout).

> [!IMPORTANT]
> Die Eigenschaft **Für Gastbenutzer aktivieren** ist ab der Commerce-Version 10.0.21 verfügbar. Es erfordert, dass das Commerce-Modulbibliothekspaket in der Version 9.31 installiert ist.

## <a name="site-settings-for-gift-card-modules"></a>Site-Einstellungen für Geschenkkartenmodule

Im Commerce Site Builder unter **Seiteneinstellungen \> Erweiterungen** gibt es eine Geschenkkartenmoduleinstellung namens **Unterstützter Geschenkkartentyp**. Diese Einstellung unterstützt drei Werte:
- **Dynamics 365 Geschenkkarte** – Wenn diese Einstellung angewendet wird, lässt das Geschenkkartenmodul nur die Einlösung von Dynamics 365 Geschenkkarten zu. Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.
- **SVS- und Givex-Geschenkkarten** – Wenn diese Einstellung angewendet wird, lässt das Geschenkkarten-Modul nur das Einlösen von Givex- und SVS-Geschenkkarten zu. Diese Einstellung wird nur für angemeldete und anonyme Benutzer auf der E-Commerce-Site unterstützt.
- **Dynamics 365-, SVS- und Givex-Geschenkkarten** – Wenn diese Einstellung angewendet wird, lässt das Geschenkkartenmodul das Einlösen von Dynamics 365-, Givex- und SVS-Geschenkkarten zu. Diese Einstellung wird nur für angemeldete Benutzer auf der E-Commerce-Site unterstützt.

> [!IMPORTANT]
> Diese Einstellungen sind in Dynamics 365 Commerce 10.0.11 verfügbar und sind nur erforderlich, wenn Sie Hilfe für SVS- oder Givex-Geschenkkarten benötigen. Wenn Sie eine Aktualisierung von einer älteren Version von Dynamics 365 Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren. Anweisungen zum Aktualisieren der Datei appsettings.json finden Sie unter [SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>Erweitern Sie interne Geschenkkarten für die Verwendung in E-Commerce-Storefronts

Standardmäßig sind interne Geschenkkarten nicht für die Verwendung in E-Commerce-Storefronts optimiert. Bevor Sie also die Verwendung von internen Geschenkkarten zur Zahlung zulassen, sollten Sie diese mit Erweiterungen konfigurieren, die sie sicherer machen. Hier sind die Geschenkkartenbereiche, die Sie erweitern sollten, bevor Sie die Verwendung interner Geschenkkarten in der Produktion zulassen:

- **Geschenkkartennummer** – Nummernkreise werden verwendet, um Geschenkkartennummern für interne Geschenkkarten zu generieren. Da Nummernkreise leicht vorhergesagt werden können, sollten Sie die Generierung von Geschenkkartennummern so erweitern, dass zufällige, kryptografisch sichere Zeichenfolgen für die ausgegebenen Geschenkkartennummern verwendet werden.
- **GetBalance** – Die **GetBalance** API wird verwendet, um den Kontostand von Geschenkkarten nachzuschlagen. Standardmäßig ist diese API öffentlich. Wenn für die Abfrage von Geschenkkarten-Salden keine PIN erforderlich ist, besteht das Risiko, dass Brute-Force-Angriffe die **GetBalance**-API verwenden, um zu versuchen, Geschenkkarten-Nummern abzufragen, die Salden haben. Durch die Implementierung von PIN-Anforderungen für interne Geschenkkarten und API-Drosselung können Sie das Risiko beheben.
- **PIN** – Standardmäßig unterstützen die internen Geschenkkarten keine PINs. Sie sollten interne Geschenkkarten so erweitern, dass eine PIN erforderlich ist, um den Kontostand abzurufen. Diese Funktionalität kann auch verwendet werden, um Geschenkkarten nach aufeinanderfolgenden falschen Versuchen, die PIN einzugeben, zu sperren.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>Aktivieren von Geschenkkarten-Zahlungen für das Einchecken von Gästen

Standardmäßig sind Geschenkkarten-Zahlungen für die (anonyme) Gast-Kasse nicht aktiviert. Um sie zu aktivieren, führen Sie diese Schritte aus.

1. Gehen Sie in der Commerce-Zentrale zu **Retail und Commerce \> Kanal einrichten \> POS einrichten \> POS \> POS Vorgänge**.
1. Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) die Kopfzeile des Rasters und wählen Sie dann **Spalten einfügen**.
1. Aktivieren Sie in der Dialogbox **Spalten einfügen** das Kontrollkästchen **Anonymen Zugriff zulassen**.
1. Wählen Sie **Aktualisieren**.
1. Legen Sie für die Vorgänge **520** (Geschenkkarten-Saldo) und **214** den Wert **AllowAnonymousAccess** auf **1** fest.
1. Wählen Sie **Speichern** aus.
1. Führen Sie den Job **1090** aus, um Änderungen mit der Kanaldatenbank zu synchronisieren. 

## <a name="add-a-gift-card-module-to-a-page"></a>Hinzufügen eines Geschenkkartenmoduls zu einer Seite

Anweisungen zum Hinzufügen eines Geschenkkartenmoduls zu einer Checkout-Seite und zum Festlegen der erforderlichen Eigenschaften finden Sie unter [Checkout-Modul](add-checkout-module.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einkaufswagenmodul](add-cart-module.md)

[Modul für Einkaufswagensymbol](cart-icon-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Zahlungsmodul](payment-module.md)

[Versandadressenmodul](ship-address-module.md)

[Lieferoptionenmodul](delivery-options-module.md)

[Abholinformationsmodul](pickup-info-module.md)

[Auftragsdetailmodul](order-confirmation-module.md)

[Unterstützung für externe Geschenkgutscheine](./dev-itpro/gift-card.md)

[SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
