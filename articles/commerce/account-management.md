---
title: Kontoverwaltungsseiten und Module
description: In diesem Thema werden Kundenbetreuungsseiten und Module in Microsoft Dynamics 365 Commerce behandelt.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c465b8883438eee886b177274bf89ddb86aa00b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980555"
---
# <a name="account-management-pages-and-modules"></a>Kontoverwaltungsseiten und Module

[!include [banner](includes/banner.md)]

In diesem Thema werden Kundenbetreuungsseiten und Module in Microsoft Dynamics 365 Commerce behandelt.

## <a name="overview"></a>Übersicht

Kundenbetreuung bezieht sich auf eine Gruppe von Seiten, die benötigt wird, um Konto-zugeordnete Benutzerinformationen in Dynamics 365 Commerce zu verwalten. Zu den Kontoverwaltungsseiten gehören die Startseite, die Benutzerprofilseite, die Benutzeradressenseite, der Bestellverlauf, die Bestelldetailseite, Treuepunkteseite und die Wunschlistenseite.

### <a name="account-management-landing-page"></a>Kontenverwaltungsseite-Landingpage

Die Kundenbetreuungsangebotsseite verwendet die folgenden Module:

- **Container** – Alle Zielseitenmodule für die Kontoverwaltung sollten sich in einem Container befinden. 
- **Konto-Begrüßungskachel** – Dieses Modul wird verwendet, um eine Begrüßungsmeldung auf der Kontoverwaltungsseite bereitzustellen. Es enthält Eigenschaften für die Überschrift.
- **Generische Kachel für Konto** – Dieses Modul kann verwendet werden, um Überschriften und Links für Kontoverwaltungsseiten bereitzustellen, z. B. die Seiten „Bestellverlauf“ oder „Mein Profil“. Mit dem allgemeinen Kachelmodul kann eine Kachel für eine beliebige Seite konfiguriert werden. In Fabrikam wird dieses Modul für die Seitenlinks „Bestellverlauf“ und „Mein Profil“ auf der Zielseite der Kontoverwaltung verwendet.
- **Wunschlistenkachel für Konto** – Dieses Modul wird verwendet, um eine Übersicht der Artikel auf der Wunschliste des Debitors anzuzeigen. Beispielsweise kann stehen, „Sie hat 10 Artikel auf Ihrer Wunschliste.“ Es umfasst Eigenschaften für die Überschrift und den Link „Details anzeigen“. Der Link „Details anzeigen“ muss konfiguriert werden, um die Wunschlistenseite umzuleiten. 
- **Adresskachel für Konto** – Dieses Modul wird verwendet, um eine Zusammenfassung der Benutzeradressen bereitzustellen. Beispielsweise kann stehen „Sie haben 2 Adressen Ihrem Konto hinzugefügt.“ Es umfasst Eigenschaften für die Überschrift und den Link „Details anzeigen“. Der Link „Details anzeigen“ muss konfiguriert werden, um die Benutzeradressseite umzuleiten.
- **Loyalitätskachel für Konto** – Dieses Modul wird verwendet, um zu die Treueprogramminformationen darzustellen und zu verknüpfen. Diese Kachel hat zwei Status: In einem Status werden Links angezeigt, über die einem Treueprogramm beigetreten werden kann, wenn der Benutzer noch kein Mitglied ist. Der andere Status zeigt Links zum Anzeigen der Treuedetailseite an, wenn der Benutzer bereits Mitglied ist. Zu den Eigenschaften gehören die Überschrift, der Link „Anmelden“ und der Link „Treueprogramm anzeigen“. Der Link „Treueprogramm anzeigen“ muss konfiguriert werden, um auf die Treueprogrammseite umzuleiten. Der Link „Anmelden“ sollte konfiguriert werden, um zu einer Seite umzuleiten, auf der der Benutzer dem Treueprogramm beitreten kann. 

### <a name="order-history-page"></a>Bestellverlaufseite

Die Auftragsverlaufseite verwendet das Auftragsarchivierungsmodul, um alle neuen Aufträge zu zeigen, die der Benutzer erteilt hat.

### <a name="order-details-page"></a>Auftragsdetailseite

Die Bestelldetailseite stellt Detailinformationen zu jedem Auftrag bereit und wird über die Auftragsverlaufsseite abgerufen. Es verwendet das Bestelldetailmodul, das die Vertriebs-ID oder -Transaktions-ID erfordert, um die Auftragsdetails abzurufen.

### <a name="user-profile-page"></a>Benutzerprofilseite

Die Benutzerprofilseite zeigt die Benutzerkontodetails, beispielsweise den Benutzernamen und die E-Mail-Adresse an. Es verwendet die Benutzerprofildetails und Benutzerprofilbearbeitungsmodule. Obwohl die E-Mail-Adresse nicht entfernt werden kann, kann sie bearbeitet werden. Auf der Benutzerprofilseite werden auch Benutzereinstellungen angezeigt, mit denen ein Benutzer bestimmte Funktionen wie die Personalisierung von Empfehlungslisten aktivieren oder deaktivieren kann. 

### <a name="user-address-page"></a>Adressenseite des Benutzers

Die Benutzeradressenseite zeigt die Liste der Adressen, die dem Benutzerkonto zugeordnet sind. Der Benutzer stellt entweder diese Adressen für das Auschecken bereit oder fügt diese direkt dieser Seite hinzu. Das Benutzeradressenmodul wird verwendet, um Adressen hinzuzufügen und zu bearbeiten, die primäre Adresse festzulegen und vorhandenen Adressen auf der Seite zu rendern.

### <a name="wish-list-page"></a>Wunschlistenseite

Die Seite Wunschliste zeigt eine Liste von Elementen, die der Kunde seiner Wunschliste hinzugefügt hat. Es verwendet das Wunschlistenmodul, um Wunschlistenartikel zu rendern.

### <a name="loyalty-page"></a>Treueseite

Die Treueprogrammseite ermöglicht es einem Debitor, ihre Programmdetails anzuzeigen, wenn er bereits Treueprogrammmitglied ist. Sie können auch die Punkte anzeigen, die sie für kürzliche Transaktionen erworben haben. Die Seite verwendet das Modul „Treuedetails“, um die Treuedetails anzuzeigen. 

Um dem Treueprogramm beizutreten, kann eine Marketingseite mit Modulen für die Registrierung von Treueprogrammen- und Treueprogrammbedingungen erstellt werden. Wenn der Benutzer kein Mitglied eines Treueprogramms ist, kann der Benutzer sich mit diesen Modulen anmelden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kauffeldmodul](add-buy-box.md)

[Einkaufswagenmodul](add-cart-module.md)

[Auschecken-Modul](add-checkout-module.md)

[Auftragsbestätigungsmodul](order-confirmation-module.md)

[Kopfzeilenmodul](author-header-module.md)

[Fußzeilenmodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]