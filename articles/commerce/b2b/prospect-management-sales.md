---
title: Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites mit Dynamics 365 Sales verwalten
description: In diesem Artikel wird beschrieben, wie Sie Microsoft Dynamics 365 Sales zur Verwaltung von Geschäftspartnergenehmigungen für Dynamics 365 Commerce Business-to-Business-(B2B)-E-Commerce-Websites verwenden.
author: shajain
ms.date: 2/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ac4aa15f2c6e7f557105254c2c8ce743a9466985
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878620"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites mit Dynamics 365 Sales verwalten

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Microsoft Dynamics 365 Sales zur Verwaltung von Geschäftspartnergenehmigungen für Dynamics 365 Commerce Business-to-Business-(B2B)-E-Commerce-Websites verwenden. Unternehmen, die bereits in die Dynamics 365 Sales-Lösung investiert haben, können ihre Lead- und Verkaufschance-Konzepte für den Genehmigungsprozess von B2B-E-Commerce-Geschäftspartner nutzen.

Hintergrundinformationen zum Genehmigungsprozess für B2B-Geschäftspartner finden Sie unter [Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten](manage-b2b-users.md).

Potenzielle Geschäftspartner können den Onboarding-Prozess für eine B2B-E-Commerce-Website initiieren, indem sie eine Onboarding-Anfrage über einen Link auf der B2B-Website senden. Nachdem die Anforderung gesendet wurde und die relevanten Aufträge (wie z. B. **P-0001** und **Aufträge und Kanalanforderungen synchronisieren**) in der Commerce-Zentralverwaltung ausgeführt werden, wird die Onboardinganforderung auf der Seite **Alle Interessenten** in der Commerce-Zentralverwaltung gespeichert. Der Genehmigungsprozess für potenzielle Geschäftspartner kann dann in Sales abgeschlossen werden.

Nachdem die Integration zwischen Sales und Commerce aktiviert wurde, bewirkt die Erstellung eines potenziellen Geschäftspartners in Commerce die Erstellung eines *Leads* in Sales.

Die folgende Abbildung zeigt ein Beispiel einer Lead-Erstellungsseite für einen potenziellen Geschäftspartner in Sales.

![Lead-Erstellungsseite in Dynamics 365 Sales.](../media/LeadInSales.png)

In der Abbildung zeigt der Abschnitt **Kontakt** die Person an, welche die Onboardinganforderung eingereicht hat, und der Abschnitt **Unternehmen** zeigt die Organisation. Ein Hinweis im Abschnitt **Zeitskala** zeigt an, dass der Lead von der Infrastruktur für duales Schreiben generiert wurde. Da er von der Infrastruktur für duales Schreiben erstellt wurde, erscheint dieser Lead nicht in der Dropdownliste **Meine offenen Leads**. Stattdessen wird es in einer neuen Ansicht mit dem Namen **Alle E-Commerce-B2B-Leads** angezeigt.

Wenn gemäß dem standardmäßigen Leadqualifizierungsprozess in Sales ein Benutzer den Lead „qualifiziert“, wird ein *Verkaufschance*-Datensatz, ein *Kontakt*-Datensatz und ein *Konto*-Datensatz erstellt. Die Infrastruktur für duales Schreiben wird verwendet, um den Kontakt- und den Kontodatensatz in Commerce zu schreiben. Der Kontakt wird als Kunde vom Typ *Person* und das Unternehmen wird als Kunde vom Typ *Organisation* angelegt. Wenn ein Benutzer für die Verkaufschance **Als gewonnen schließen** auswählt, wird der Interessent in Commerce genehmigt. Die Genehmigung eines Interessenten bewirkt, dass eine Kundenhierarchie erstellt wird.

Alle übrigen Geschäftsprozesse finden in Commerce statt. Diese Prozesse umfassen das Senden von E-Mails an den Geschäftspartner, das Festlegen der Kreditlimitverwaltung für die Benutzer und das Hinzufügen weiterer Benutzer zur B2B-Site. Wenn ein Benutzer jedoch den Lead disqualifiziert oder die Verkaufschance als verloren kennzeichnet, anstatt den Lead zu qualifizieren, wird der Interessent in Commerce als abgelehnt gekennzeichnet, und der Anforderer erhält eine ablehnende Onboarding-E-Mail.

## <a name="enable-integration-between-sales-and-commerce"></a>Integration zwischen Sales und Commerce aktivieren

Die Integration zwischen Sales und Commerce basiert auf der Infrastruktur für duales Schreiben. Daher sollte duales Schreiben aktiviert sein und funktionieren, damit Kunden, die in einem System erstellt werden, in das andere System geschrieben werden. Weitere Informationen zur Infrastruktur für duales Schreiben finden Sie unter [Duales Schreiben – Übersicht](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Nachdem duales Schreiben eingerichtet wurde, kann der Implementierungspartner zu [Microsoft AppSource](https://appsource.microsoft.com/) gehen und nach der Lösung namens [Commerce-Lösungen für duales Schreiben](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview) suchen. Installieren Sie das Paket mithilfe des standardmäßigen Installationsassistenten und testen Sie es dann, indem Sie einen Interessenten auf einer B2B-Website erstellen. Nachdem der Interessent erstellt wurde, überprüfen Sie, ob die Anfrage in Commerce unter **Alle Interessenten** erscheint, und überprüfen Sie dann, ob der Interessent als Lead in Sales angezeigt wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
