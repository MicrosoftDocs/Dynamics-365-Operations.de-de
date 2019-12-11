---
title: Kontoverwaltungsseiten und Module
description: In diesem Thema werden Kundenbetreuungsseiten und Module in Microsoft Dynamics 365 Commerce behandelt.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785378"
---
# <a name="account-management-pages-and-modules"></a>Kontoverwaltungsseiten und Module

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema werden Kundenbetreuungsseiten und Module in Microsoft Dynamics 365 Commerce behandelt.

## <a name="overview"></a>Übersicht

Kundenbetreuung bezieht sich auf eine Gruppe von Seiten, die benötigt wird, um Konto-zugeordnete Benutzerinformationen in Dynamics 365 Commerce zu verwalten. Zu den Kontoverwaltungsseiten gehören die Startseite, die Benutzerprofilseite, die Benutzeradressenseite, der Bestellverlauf, die Bestelldetailseite, Treuepunkteseite und die Wunschlistenseite.

### <a name="account-management-landing-page"></a>Kontenverwaltungsseite-Landingpage

Die Kundenbetreuungsangebotsseite verwendet die folgenden Module:

- **Inhalt-Platzierung** – Dieses Modul ist ein Containermodul, das alle Module in der Kundenbetreuungsangebotsseite enthält.
- **Konto-Begrüßungselement** – Dieses Modul wird verwendet, um eine Begrüßungsmeldung auf der Kontoverwaltungsseite bereitzustellen. Sie umfasst Eigenschaften für die Überschrift und die Kachelgröße. Die Eigenschaft **Kachelgröße** definiert die Breite des Moduls im Inhaltplatzierungsmodul. Die verfügbaren Werte sind von **1** bis zu **12**, wobei **12** für die volle Breite des Inhaltplatzierungscontainers steht.
- **Kontenauftrags-Platzierungsartikel** – Dieses Modul wird verwendet, um eine Zusammenfassung der Anzahl von Aufträgen verfügbar machen, die vom Benutzer im Konto platziert wurden. Sie umfasst Eigenschaften für die Überschrift, die Kachelgröße und den Link „Details anzeigen“. Der Link „Details anzeigen“  muss konfiguriert werden, um die Auftragsverlaufsseite umzuleiten.
- **Kundenprofil-Platzierungsartikel** – Dieses Modul wird verwendet, um eine Zusammenfassung des Benutzerprofils bereitzustellen. Sie umfasst Eigenschaften für die Überschrift, die Kachelgröße und den Link „Details anzeigen“. Der Link „Details anzeigen“ muss konfiguriert werden, um die Benutzerprofilseite umzuleiten.
- **Konto Wunschlistenartikel** – Dieses Modul wird verwendet, um eine Übersicht der Artikel auf der Wunschliste des Debitors anzuzeigen. Beispielsweise kann stehen, „Sie hat 10 Artikel auf Ihrer Wunschliste.“ Sie umfasst Eigenschaften für die Überschrift, die Kachelgröße und den Link „Details anzeigen“. Der Link „Details anzeigen“ muss konfiguriert werden, um die Wunschlistenseite umzuleiten.
- **Kundenprofil-Adressartikel** – Dieses Modul wird verwendet, um eine Zusammenfassung der Benutzeradressen bereitzustellen. Beispielsweise kann stehen „Sie haben 2 Adressen Ihrem Konto hinzugefügt.“ Sie umfasst Eigenschaften für die Überschrift, die Kachelgröße und den Link „Details anzeigen“. Der Link „Details anzeigen“ muss konfiguriert werden, um die Benutzeradressseite umzuleiten.
- **Kontoenloyalitätsartikel** – Dieses Modul wird verwendet, um zu die Treueprogramminformationen darzustellen und zu verknüpfen. Sie umfasst Eigenschaften für den Link für die Überschrift, die Kachelgröße und den Link „Details anzeigen“ und „Mitglied werden“. Der Link „Details anzeigen“ muss konfiguriert werden, um auf die Treueprogrammseite umzuleiten. Der Link „Mitglied werden“ sollte konfiguriert werden, um zu einer Seite umzuleiten, auf der der Benutzer dem Treueprogramm beitreten kann.

### <a name="order-history-page"></a>Bestellverlaufseite

Die Auftragsverlaufseite verwendet das Auftragsarchivierungsmodul, um alle neuen Aufträge zu zeigen, die der Benutzer erteilt hat.

### <a name="order-details-page"></a>Auftragsdetailseite

Die Bestelldetailseite stellt Detailinformationen zu jedem Auftrag bereit und wird über die Auftragsverlaufsseite abgerufen. Es verwendet das Bestelldetailmodul, das die Vertriebs-ID oder -Transaktions-ID erfordert, um die Auftragsdetails abzurufen.

### <a name="user-profile-page"></a>Benutzerprofilseite

Die Benutzerprofilseite zeigt die Benutzerkontodetails, beispielsweise den Benutzername und die E-Mail-Adresse an. Es verwendet das Benutzerprofilmodul. Obwohl die E-Mail-Adresse nicht entfernt werden kann, kann sie bearbeitet werden.

### <a name="user-address-page"></a>Adressenseite des Benutzers

Die Benutzeradressenseite zeigt die Liste der Adressen, die dem Benutzerkonto zugeordnet sind. Der Benutzer stellt entweder diese Adressen für das Auschecken bereit oder fügt diese direkt dieser Seite hinzu. Das Benutzeradressenmodul wird verwendet, um Adressen hinzuzufügen und zu bearbeiten, die primäre Adresse festzulegen und vorhandenen Adressen auf der Seite zu rendern.

### <a name="wish-list-page"></a>Wunschlistenseite

Die Seite Wunschliste zeigt eine Liste von Elementen, die der Kunde seiner Wunschliste hinzugefügt hat. Es verwendet das Wunschlistenmodul, um Wunschlistenartikel zu rendern.

### <a name="loyalty-page"></a>Treueseite

Die Treueprogrammseite ermöglicht es einem Debitor, einem Treueprogramm beizutreten oder die Programmdetails anzuzeigen, wenn er bereits Treueprogrammmitglied ist. Sie können auch die Punkte anzeigen, die sie für kürzliche Transaktionen erworben haben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Starterkit-Überblick](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)
