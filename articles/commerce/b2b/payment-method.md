---
title: Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites
description: In diesem Thema wird beschrieben, wie Sie die Zahlungsmethode für Kundenkonten für B2B-E-Commerce-Websites (Business-to-Business) konfigurieren.
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
ms.openlocfilehash: 82dfd6ac7e97d838ef442fd6ded4a4f165fc795b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211200"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die Zahlungsmethode für Kundenkonten für B2B-E-Commerce-Websites (Business-to-Business) konfigurieren.

Einzelhändler können für die von ihnen verkauften Produkte und angebotenen Dienstleistungen verschiedene Zahlungsformen in einem E-Commerce-Kanal akzeptieren. Jeder vom Einzelhändler akzeptierte Zahlungstyp muss beim Einrichten des Systems in Microsoft Dynamics 365 Commerce konfiguriert werden. Die Zahlungsmethode Kundenkonto (oder „Konto“) muss auf B2B-E-Commerce-Websites unterstützt werden. 

## <a name="prerequisites"></a>Voraussetzungen

1. Fügen Sie die Zahlungsmethode „Kundenkonto“ in der Commerce-Zentralverwaltung hinzu.
2. Verknüpfen Sie die Zahlungsmethode „Kundenkonto“ mit dem E-Commerce-Kanal.
3. Stellen Sie sicher, dass **Auf Konto zulassen** für den Kunden unter **Einzelhandel und Handel \> Kunden \> Alle Kunden \> Zahlungsstandards** in der Commerce-Zentralverwaltung aktiviert ist. Stellen Sie auch sicher, dass **Kreditlimit**-Parameter für den Kunden unter **Einzelhandel und Handel \> Kunden \> Alle Kunden \> Kredit und Inkasso** in der Commerce-Zentralverwaltung entsprechend eingestellt werden. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Aktivieren der Zahlungsmethode „Kundenkontos“ im Commerce-Website-Generator 

Führen Sie folgende Schritte aus, um die Zahlungsmethode „Kundenkontos“ im Commerce-Website-Generator zu aktivieren.

1. Gehen Sie zu **Seiteneinstellungen \> Erweiterungen**.
1. Stellen Sie die **Kundenkontenzahlungen aktivieren**-Eigenschaft auf **Für B2B-Kunden aktiviert**. 
1. Wählen Sie **Speichern und veröffentlichen**.

> [!NOTE]
> Die neuen Seiteneinstellungen werden erst wirksam, nachdem die Datei App.settings.json aktualisiert wurde. Weitere Informationen finden Sie unter [SDK- und Modulbibliothek-Updates](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Aktivieren der Zahlungsmethode „Kundenkonto“ auf der Auftragsabschlussseite für die B2B-E-Commerce-Website

Führen Sie diese Schritte aus, um die Zahlungsmethode „Kundenkonto“ auf der Auftragsabschlussseite für die B2B-E-Commerce-Website zu aktivieren.

1. Suchen und bearbeiten Sie im Commerce-Website-Generator die Auftragsabschlussseite oder das Fragment, das das Auftragsabschlussmodul für die B2B-E-Commerce-Website enthält.
1. Wählen Sie Im **Kassenbereichcontainer**-Slot **Modul hinzufügen** aus, und fügen Sie dann ein **Kundenkontozahlung**-Modul hinzu.
1. Positionieren Sie das **Kundenkontozahlung**-Modul durch Auswahl der Auslassungspunkte (**...**), und wählen Sie dann je nach Bedarf **Nach oben** oder **Nach unten**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Bestätigen, dass die Zahlungsmethode „Kundenkonto“ aktiviert und veröffentlicht wurde

Führen Sie diese Schritte aus, um zu bestätigen, dass die Zahlungsmethode „Kundenkonto“ aktiviert und veröffentlicht wurde.

1. Melden Sie sich bei der E-Commerce-Website an.
1. Fügen Sie ein Produkte zum Warenkorb hinzu.
1. Zur vorherigen Auftragsabschlussseite wechseln. Sie sollten die neue **Kundenkonto**-Zahlungsmethode sehen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine B2B-E-Commerce-Website einrichten](set-up-b2b-site.md)

[Erstellen von Organisationsmodellierungshierarchien für B2B-Organisationen](org-model.md)

[Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten](manage-b2b-users.md)

[Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites](quantity-limits.md)

[SDK- und Modulbibliothekupdates](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]