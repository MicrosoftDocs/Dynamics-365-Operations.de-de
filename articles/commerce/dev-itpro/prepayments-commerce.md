---
title: Vorauszahlungen in Dynamics 365 Commerce
description: Dieser Artikel bietet einen Überblick über die Verarbeitung für Vorauszahlungsbuchungen in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780360"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Vorauszahlungen in Dynamics 365 Commerce

[!include[banner](../includes/banner.md)]

Dieser Artikel bietet einen Überblick über die Verarbeitung für Vorauszahlungsbuchungen in Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce verarbeitet Vorauszahlungstransaktionen für die folgenden Zahlungsarten, die in der Debitorenbuchhaltung oder im Handel verwendet werden:

- **Anzahlung auf Kundenkonto** – Ein Kunde zahlt am Point of Sale (POS) ein Pfand. Der Handel wickelt die Kautionszahlung als Vorauszahlungstransaktion ab. Wenn Sie die Transaktion buchen, wird ein Zahlungsjournal erstellt und auf der **Alle Journale** Seite in Commerce headquarters. Das **Erfassungsbeleg für Vorauszahlung** Kontrollkästchen auf der **Zahlung** Registerkarte wird automatisch für das Zahlungsjournal ausgewählt. Weitere Informationen, einschließlich Vorauszahlungs- und steuerspezifischer Informationen, die für die Zielregion relevant sind, finden Sie unter [Globalisierungsressourcen – Länder-/regionsspezifische Hilfeinhalte](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content).
- **Kundenauftrag mit Anzahlung** – Ein Kunde erstellt am POS eine Kundenbestellung. Der Kunde kann eine Anzahlung für die Bestellung leisten, basierend auf dem standardmäßigen Anzahlungsprozentsatz, der auf der **Kundenbestellungen** Seite in Commerce headquarters (**Handelsparameter \> Kundenbestellungen**) konfiguriert ist. Der Handel wickelt die Kautionszahlung für den Kundenauftrag als Vorauszahlungstransaktion ab. Wenn Sie die Transaktion buchen, wird ein Zahlungsjournal erstellt und auf der **Alle Journale** Seite. Das **Erfassungsbeleg für Vorauszahlung** Kontrollkästchen auf der **Zahlung** Registerkarte wird automatisch für das Zahlungsjournal ausgewählt. Die Zahlung wird beglichen und die Kundenrechnung wird automatisch bei Abholung oder Lieferung der Bestellung erstellt.
- **Call-Center-Verkaufsauftrag** – Ein Call-Center-Kundendienstmitarbeiter erstellt einen Verkaufsauftrag im Namen eines Kunden und das **Vorauszahlung** Attribut ist auf **Ja** während der Zahlungserfassung festgelegt.

Commerce führt die folgenden Aufgaben aus, um eine Vorauszahlung zu verarbeiten:

- **Verarbeiten Sie eine Anzahlung für ein Kundenkonto** – Eine Anzahlung, die ein Kunde leistet, wird mithilfe eines Dienstes, der Daten synchronisiert, an Commerce übertragen. Commerce erstellt eine Einzelhandelszahlungstransaktion für die Zahlung. Wenn Sie die Einzelhandelstransaktion buchen, wird ein Kassenbuch oder Debitorenzahlungsbuch gebucht. Das **Erfassungsbeleg für Vorauszahlung** Kontrollkästchen auf der **Zahlung** Registerkarte der **Alle Journale** Seite in Commerce headquarters wird automatisch für das Zahlungsjournal ausgewählt. Vorauszahlungen können nicht verarbeitet werden, wenn der Zahlungsbetrag negativ ist.
- **Bearbeiten Sie eine Kundenbestellung oder einen Verkaufsauftrag mit einer Anzahlung** – Ein Kunde zahlt eine erforderliche Anzahlung für eine Kundenbestellung, indem er Commerce Data Exchange: Echtzeitdienst verwendet. Commerce erstellt entweder ein Debitorenzahlungsjournal oder ein Kassenbuch, abhängig von der Zahlungsmethode, die der Kunde verwendet. Das **Erfassungsbeleg für Vorauszahlung** Kontrollkästchen auf der **Zahlung** Registerkarte der **Alle Journale** Seite wird automatisch für das Zahlungsjournal in Commerce headquarters ausgewählt. Wenn ein Kunde mehrere Zahlungsmethoden für Teilzahlungen verwendet, verarbeitet Commerce jede Teilzahlung basierend auf der verwendeten Zahlungsmethode.

Für Kreditkarten und digitale Geldbörsen, denen Kreditkartenzahlungsmethoden zugrunde liegen, sendet Commerce nach erfolgreicher Autorisierung eine „Capture“-Anfrage. (Beträge werden erfasst, bevor der Verkaufsauftrag fakturiert wird.)

Wenn Sie eine Kundenbestellung stornieren, wird der Vorauszahlungsbetrag zurückerstattet und eine Rückerstattungszahlungserfassung für den Anzahlungsbetrag gebucht. Der Erstattungsbetrag wird basierend auf der Zahlungsmethode berechnet und gebucht, die Sie beim Buchen der Erstattungszahlung angegeben haben. Commerce erhebt möglicherweise eine Stornogebühr, basierend auf dem Prozentsatz, den Sie auf der **Handelsparameter** Seite in Commerce headquarters festgelegt haben.

Wenn Sie eine Kundenbestellung zurücksenden, werden eine Rücksendebestellung und eine Erstattungszahlungserfassung erstellt. Wenn Sie die Reklamation buchen, erstellt Commerce abhängig von der Zahlungsmethode, die der Kunde für die ursprüngliche Transaktion verwendet hat, entweder eine Debitorenzahlungserfassung oder eine Kassenerfassung.
