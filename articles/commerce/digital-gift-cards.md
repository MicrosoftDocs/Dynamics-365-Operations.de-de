---
title: Digitale E-Commerce-Geschenkkarten
description: In diesem Thema wird erläutert, wie digitale Geschenkkarten in der E-Commerce-Implementierung von Microsoft Dynamics 365 Commerce funktionieren. Zudem bietet es einen Überblick über wichtige Konfigurationsschritte.
author: anupamar-ms
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 6c4cf4e94e6271843d55b4ca7a0fb3ffaffc9542
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344394"
---
# <a name="e-commerce-digital-gift-cards"></a>Digitale E-Commerce-Geschenkkarten

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In diesem Thema wird erläutert, wie digitale Geschenkkarten in der E-Commerce-Implementierung von Microsoft Dynamics 365 Commerce funktionieren. Zudem bietet es einen Überblick über wichtige Konfigurationsschritte.

In Dynamics 365 Commerce folgt der Kauf digitaler Geschenkkarten demselben Flow wie der Kauf anderer Produkte im System. Es müssen keine zusätzlichen Module konfiguriert werden. Wenn dem Warenkorb mehrere Geschenkkarten hinzugefügt werden, werden die Geschenkkartenartikel nicht in einer einzigen Verkaufsposition aggregiert. Dieses Verhalten ist erforderlich, da jede Verkaufsposition mithilfe einer separaten Geschenkkartennummer fakturiert wird.

Der Kauf digitaler Geschenkkarten wird in der Dynamics 365 Commerce-Version 10.0.16 und höher unterstützt.

Die folgende Abbildung zeigt ein Beispiel für die Produktdetailseite (PDP) für eine digitale Geschenkkarte auf der Fabrikam-E-Commerce-Website.

![Beispiel einer PDP für digitale Geschenkkarten auf der Fabrikam-E-Commerce-Website.](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Die Funktion für digitale Geschenkkarten in der Commerce-Zentralverwaltung aktivieren

Damit der Kaufflow für digitale Geschenkkarten in Dynamics 365 Commerce funktioniert, muss die Funktion **Kauf einer Geschenkkarte über die E-Commerce-Funktion** in der Commerce-Zentralverwaltung aktiviert sein. Sie finden die Funktion im Arbeitsbereich **Funktionsverwaltung** in der Commerce-Zentralverwaltung, wie in der folgenden Abbildung dargestellt.

![Arbeitsbereich für die Funktionsverwaltung in der Commerce-Zentralverwaltung.](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Eine digitale Geschenkkarte in der Commerce-Zentralverwaltung konfigurieren

Digitale Geschenkkartenprodukte sollten in der Commerce-Zentralverwaltung konfiguriert werden. Der Vorgang ähnelt dem Vorgang für andere Produkte. Die folgenden wichtigen Schritte gelten jedoch speziell für die Konfiguration von Geschenkkarten für den Kauf. Weitere Informationen zum Erstellen und Konfigurieren von Produkten finden Sie unter [Ein neues Produkt in Commerce erstellen](create-new-product-commerce.md).

- Wenn Sie digitale Geschenkkartenprodukte im Dialogfeld **Neues Produkt** konfigurieren, setzen Sie das Feld **Produkttyp** auf **Service**. (Um das Dialogfeld zu öffnen, rufen Sie **Einzelhandel und Handel \> Produkte und Kategorien \> Produkte nach Kategorie** auf, und wählen Sie **Neu** aus.) Produkte des Typs **Service** werden nicht auf verfügbaren Bestand geprüft, bevor ein Auftrag erteilt wird. Weitere Informationen finden Sie unter [Ein neues Produkt erstellen](create-new-product-commerce.md#create-a-new-product).
- Auf der Registerkarte **Buchung** der Seite **Commerce-Parameter** muss das Feld **Geschenkkartenprodukt** auf **Digitale Geschenkkarte** gesetzt sein, wie in der folgenden Abbildung dargestellt. Wenn es sich bei dem Produkt um eine externe Geschenkkarte handelt, finden Sie weitere Informationen unter [Unterstützung für externe Geschenkkarten](./dev-itpro/gift-card.md).

    ![Geschenkkartenprodukt-Feld in der Commerce-Zentralverwaltung.](./media/PostGiftcard.png)

- Wenn eine Geschenkkarte mehrere vordefinierte Beträge unterstützen muss (z. B. 25, 50 und 100 US-Dollar), sollte die Dimension **Größe** verwendet werden, um diese vordefinierten Beträge einzurichten. Jeder vordefinierte Betrag ist eine Variante. Weitere Informationen finden Sie unter [Produktdimensionen](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json).
- Wenn Kunden in der Lage sein müssen, einen benutzerdefinierten Betrag für eine Geschenkkarte zu bestimmen, richten Sie zunächst eine Variante ein, die einen benutzerdefinierten Betrag zulässt. Öffnen Sie anschließend das Produkt über die Seite **Freigegebene Produkte in Kategorie**, und setzen Sie dann im Inforegister **Commerce** das Feld **Preis eingeben** auf **Neuer Preis muss eingegeben werden**, wie in der folgenden Abbildung dargestellt. Diese Einstellung stellt sicher, dass Kunden einen Preis eingeben können, wenn sie nach dem Produkt auf einer PDP suchen.

    ![„Preis eingeben“-Feld in der Commerce-Zentralverwaltung.](./media/KeyInPrice.png)

- Die Lieferart für eine digitale Geschenkkarte muss auf **Elektronisch** eingestellt sein. Wählen Sie auf der Seite **Lieferarten** (**Einzelhandel und Handel \> Kanaleinstellung \> Lieferarten**) die Lieferart **Elektronisch** im Listenbereich aus, und fügen Sie dann das digitale Geschenkkartenprodukt dem Raster im Inforegister **Produkte** hinzu, wie in der folgenden Abbildung dargestellt. Weitere Informationen finden Sie unter [Lieferarten einrichten](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

    ![Digitale Geschenkkartenprodukte auf der „Lieferart“-Seite in der Commerce-Zentralverwaltung.](./media/ElectronicMode.PNG)

- Vergewissern Sie sich, dass ein Onlinefunktionsprofil erstellt und Ihrem Onlineshop in der Commerce-Zentralverwaltung zugeordnet wurde. Stellen Sie im Funktionsprofil die Option **Aggregierte Produkte** auf **Ja** ein. Diese Einstellung stellt sicher, dass alle Artikel außer Geschenkkarten aggregiert werden. Weitere Informationen finden Sie unter [Ein Onlinefunktionsprofil erstellen](online-functionality-profile.md).
- Erstellen Sie einen neuen E-Mail-Benachrichtigungstyp auf der Seite **E-Mail-Benachrichtigungsprofile**, und setzen Sie das Feld **E-Mail-Benachrichtigungstyp** auf **Geschenkkarte ausstellen**, um sicherzustellen, dass Kunden eine E-Mail erhalten, nachdem eine Geschenkkarte fakturiert wurde. Weitere Informationen finden Sie unter [Einen E-Mail-Benachrichtigungstyp einrichten](email-notification-profiles.md).

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Der Medienbibliothek des Commerce-Website-Generators Produktbilder hinzufügen

Sie müssen der Medienbibliothek des Commerce-Website-Generators Produktbilder für digitale Geschenkkartenprodukte hinzufügen. Vergewissern Sie sich, dass die Dateinamen der Geschenkkarten-Bilddateien den Namenskonventionen Ihrer Website für Produktbilder entsprechen. Weitere Informationen finden Sie unter [Bilder hochladen](dam-upload-images.md).

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Im Commerce-Website-Generator einen benutzerdefinierten Betrag für eine digitale Geschenkkarte konfigurieren

Wenn die Konfiguration einer digitalen Geschenkkarte einen benutzerdefinierten Betrag zulässt, muss dieses Verhalten auch im [Kauffeldmodul](add-buy-box.md), das auf den PDPs Ihrer Website verwendet wird, aktiviert werden. Das Kauffeldmodul unterstützt die Modulkonfiguration, um benutzerdefinierte Beträge zu ermöglichen. Sie können auch die minimalen und maximalen Beträge definieren, die für benutzerdefinierte Beträge zulässig sind.

Führen Sie folgende Schritte aus, um im Commerce-Website-Generator einen benutzerdefinierten Betrag für eine digitale Geschenkkarte zu konfigurieren.

1. Rufen Sie das Kauffeldmodul auf, das auf den PDPs Ihrer Website verwendet wird. Dieses Kauffeldmodul kann in einem Fragment, in einer Vorlage oder auf einer Seite implementiert sein.
1. Wählen Sie **Bearbeiten** aus.
1. Wählen Sie im Eigenschaftenbereich rechts das Kontrollkästchen **Benutzerdefinierten Preis zulassen** aus.
1. Optional: Geben Sie Beträge unter **Minimaler Preis** und **Maximaler Preis** ein, um für benutzerdefinierte Beträge minimale und maximale Beträge zu definieren.
1. Wählen Sie **Bearbeiten beenden** und anschließend **Veröffentlichen** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Kauffeldmodul](add-buy-box.md)

[Auschecken-Modul](add-checkout-module.md)

[Einkaufswagenmodul](add-cart-module.md)

[Neues Produkt in Commerce erstellen](create-new-product-commerce.md)

[Lieferarten einrichten](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Produktdimensionen](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json)

[E-Mail-Benachrichtigungsprofil einrichten](email-notification-profiles.md)

[Ein Onlinefunktionsprofil erstellen](online-functionality-profile.md)

[Unterstützung für externe Geschenkgutscheine](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]