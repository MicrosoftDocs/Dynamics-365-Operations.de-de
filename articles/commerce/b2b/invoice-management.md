---
title: Rechnungsverwaltung für B2B-E-Commerce-Websites
description: In diesem Thema werden die Funktionen der Rechnungsverwaltung von Microsoft Dynamics 365 Commerce Business-to-Business-(B2B-)E-Commerce-Websites beschrieben.
author: shajain
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 60cb0c8aaede4a0eaeed80cf5ebe41068da57836
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686299"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>Rechnungsverwaltung für B2B-E-Commerce-Websites

[!include [banner](../../includes/banner.md)]

In diesem Thema werden die Funktionen der Rechnungsverwaltung von Microsoft Dynamics 365 Commerce Business-to-Business-(B2B-)E-Commerce-Websites beschrieben.

Es ist eine gängige Praxis für Unternehmen, die B2B-Transaktionen abwickeln, Aufträge auf Debitorenkredit anzunehmen und dann eine Rechnung an die Kunden zu senden, nachdem der Auftrag ausgeführt wurde. Zahlungsbedingungen werden für Kunden festgelegt und es kann einige Rabatte geben, um Kunden zu motivieren, pünktlich oder vorzeitig zu zahlen. Um die Wahrscheinlichkeit zu erhöhen, dass Zahlungen pünktlich eingehen, können Kunden auf B2B-E-Commerce-Websites alle ihre Rechnungen einsehen. Der Kunde kann die Rechnungen einfach filtern, um sich bezahlte, unbezahlte und teilweise bezahlte Rechnungen zusammen mit den Fälligkeitsdaten anzeigen zu lassen.

![Rechnungsseite auf einer B2B-Website.](../media/ViewInvoices.png)

> [!NOTE]
> Ein angemeldeter Benutzer kann nur seine eigenen Rechnungen anzeigen und bezahlen. Wenn ein Organisationskonto im Dropdownmenü **Rechnungskonto** im Inforegister **Rechnung und Lieferung** des Kundendatensatzes in der Commerce-Zentralverweisung konfiguriert ist, kann der Benutzer Rechnungen für das Organisationskonto anzeigen und bezahlen.

Auf der Seite **Rechnungen** einer B2B-Website kann ein Benutzer eine unbezahlte oder teilweise bezahlte Rechnung und dann **Rechnung bezahlen** auswählen. Die ausgewählte Rechnung wird dem Warenkorb hinzugefügt und der Benutzer kann mit der Zahlung fortfahren. Der Benutzer kann dann entscheiden, ob er den vollen Rechnungsbetrag oder einen Teilbetrag bezahlen möchte. Der Benutzer kann die Auf-Rechnung-Zahlungsmethode nicht zum Bezahlen von Rechnungen verwenden.

> [!NOTE]
> Rechnungen können nur dann zum Warenkorb hinzugefügt werden, wenn sich derzeit keine Artikel darin befinden. Artikel können umgekehrt nur dann zum Warenkorb hinzugefügt werden, wenn sich derzeit keine Rechnungen darin befinden. Microsoft plant, diese Einschränkung in zukünftigen Commerce-Versionen zu entfernen.

![Warenkorbseite auf einer B2B-Website.](../media/PayInvoice.png)

Auf der Seite **Rechnungen** kann ein Benutzer auch neben der Rechnung **Rechnung anfordern** auswählen. Auf diese Weise kann der Benutzer verlangen, dass die Details der Rechnung an seine registrierte E-Mail-Adresse gesendet werden.

![Dialogfeld „Rechnung anfordern“.](../media/RequestInvoice2.png)

Nachdem ein Benutzer eine Rechnung angefordert hat, wird die Anforderung in den Abschnitt **B2B-Anforderungen** der Seite **Mein Konto** verschoben. Nachdem die Aufträge **P-0001** und **Aufträge und Kanalanforderungen synchronisieren** in der Commerce-Zentralverwaltung ausgeführt wurden, wird die Rechnungs-E-Mail ausgelöst und der Status der B2B-Anforderung als abgeschlossen gekennzeichnet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
