---
title: MwSt.-Rückerstattung in der Ausgabenverwaltung
description: In diesem Thema wird erläutert, wie Sie Rückerstattungen auf gemeinsamen Mehrwertsteuer (VAT)- Buchungen erhalten.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bc9e533de40aa8fe8ddfe422cfe0f4078a360c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568939"
---
# <a name="vat-recovery-in-expense-management"></a>MwSt.-Rückerstattung in der Ausgabenverwaltung

[!include [banner](../includes/banner.md)]

Um Rückerstattungen für die Buchungen von anrechenbarer Mehrwertsteuer zu erhalten, muss ein Unternehmen oder eine Organisation genaue Informationen erkennen, sammeln, überprüfen und übermitteln. Dieser Prozess umfasst mehrere Aufgaben und kann je nach Größe des Unternehmens mehrere Mitarbeiter oder Rollen einschließen.

Zur Mehrwertsteuerbeitreibung mithilfe von Ausgabenverwaltung müssen die folgenden Voraussetzungen erfüllt werden:

- Steuercodes müssen für Länder/Regionen erstellt werden, die Ausgabenkategorien zugeordnet sind.
- Für jeden Steuercode muss eine Mehrwertsteuergruppe erstellt werden.
- Für jede Mehrwertsteuergruppe muss ein Artikel-Mehrwertsteuercode erstellt werden.

Wenn diese Voraussetzungen erfüllt sind, können Mitarbeiter die Schritte ausführen, die zur Anforderung von Rückerstattungen für Mehrwertsteuerbuchungen erforderlich sind.

1. Geben Sie in einer Spesenabrechnung die Steuerinformationen zu Kreditkartenbuchungen ein, um anrechenbare Mehrwertsteuerrückerstattungen zu ermitteln.
2. Alle Steuerinformationen müssen vollständig sein, bevor eine Spesenabrechnung gebucht wird.
3. Anrechenbare Ausgaben für die Beitreibung von internationaler Mehrwertsteuer werden verarbeitet.
4. Daten über die Mehrwertsteuerbeitreibung werden an den Drittanbieter gesendet, um die Rückgabebeträge zu erfassen, die aus der Beitreibung der Steuern von internationalen Unternehmen resultieren.
5. Ausgaben für die Beitreibung von inländischer Mehrwertsteuer.

Die folgenden Abschnitte beinhalten Beispiele, die zeigen, wie Contoso-Mitarbeiter jeden Schritt abschließen.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Geben Sie in einer Spesenabrechnung die Steuerinformationen zu Kreditkartenbuchungen ein, um anrechenbare Mehrwertsteuerrückerstattungen zu ermitteln.

Nancy, eine in den USA tätige Verkäuferin bei Contoso, kehrte kürzlich von einer Geschäftsreise nach Großbritannien zurück. Während ihrer Reise sind einige Ausgaben für Mahlzeiten angefallen, die Sie mit ihrer persönlichen Kreditkarte beglichen hat. Nancy muss eine Spesenabrechnung erstellen, um die Ausgaben auszugleichen.

Wenn Nancy Informationen über ihre Spesenabrechnung eingibt, wählt sie **Vereinigtes Königreich** im Feld **Land/Region** auf der Seite **Spesenabrechnung bearbeiten** aus. Die Liste der Mehrwertsteuergruppen wird dann gefiltert, so dass nur die Gruppen angezeigt werden, die sich auf Großbritannien beziehen. Nancy wählt die Mehrwertsteuergruppe **001 für Großbritannien** und anschließend die Artikel-Mehrwertsteuergruppe **Mahlzeiten**. Sie fügt anschließend eine neue Buchung für ihre Unterkunft hinzu. Da für Unterkünfte in Großbritannien nur eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe vorhanden sind, werden diese Informationen automatisch in Nancys Spesenabrechnung eingetragen.

Pro Contoso-Richtlinie müssen für alle Ausgaben ein entsprechender Beleg vorhanden sein. Wenn Nancy ihre Spesenabrechnung speichert, erhält sie eine Meldung, die angibt, dass für jede Buchung, die in ihrer Spesenabrechnung aufgelistet ist, ein Beleg hinzugefügt werden muss. Nancy überprüft, ob sie an die Spesenabrechnung eine digitale Abbildung jedes Belegs angefügt hat und übermittelt anschließend ihre Abrechnung. Anschließend sendet sie die Papierbelege an das zuständige Back-Office-Team zur Verarbeitung. Das Team sendet die MwSt. über die Mehrwertsteuerrückerstattung an den Drittanbieter, der die  Rückerstattung von internationalen Mehrwertsteuerbuchungen für Contoso zurückgibt.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Alle Steuerinformationen müssen vollständig sein, bevor eine Spesenabrechnung gebucht wird.

April, die bei Contoso für die Kreditorenkonten zuständig ist, muss alle fehlenden Steuerinformationen in eine Spesenabrechnung eingeben, bevor die Abrechnung gebucht werden kann. Sie öffnet die Seite **Spesenabrechnungsdetails** und sieht die genehmigte Spesenabrechnung von Nancy. April öffnet die Spesenabrechnung, um die Details der Buchungen anzuzeigen. Sie stellt fest, dass Nancy für eine der Buchungen keine Artikel-Mehrwertsteuergruppe eingegeben hat. Da diese Informationen fehlen, kann April die Spesenabrechnung nicht buchen. April sieht im Formular im Modul **Steuerkonfigurationen** nach und sucht die erforderliche Artikel-Mehrwertsteuergruppe für das Land bzw. die Region und den Buchungstyp. April kann die Spesenabrechnung nun im Hauptbuch buchen.

Wenn April die Spesenabrechnung bucht, erstellt Sie eine Arbeitsaufgabe für rückerstattbare Mehrwertsteuer. Diese Arbeitsaufgabe wird einem Mitglied des Back-Office-Verarbeitungsteams zugewiesen. April erhält eine Meldung, mit der die Buchung erfolgreich bestätigt wurde. Diese Nachricht führt auch die Anzahl der Mehrwertsteuerbuchungen auf, die zur Rückerstattung erkannt wurden.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Anrechenbare Ausgaben für die Rückerstattung von internationaler Mehrwertsteuer werden verarbeitet.

Arnie, ein Mitarbeiter des Back-Office-Teams bei Contoso, muss überprüfen, ob alle erforderlichen Informationen für die Mehrwertsteuerbeitreibung in den Spesenabrechnungen enthalten sind. Arnie öffnet das Formular **Ausgaben-Steuerbeitreibung** und wählt die von Nancy übermittelte Spesenabrechnung aus. Arnie überprüft, ob alle erforderlichen Belege angefügt wurden und ob die richtige Mehrwertsteuergruppe und die richtigen Artikel-Mehrwertsteuergruppen eingegeben wurden.

Wenn Arnie die Papierbelege von Nancy erhält, gleicht er die Papierbelege mit den digitalen Belegen ab und ändert den Status der Spesenabrechnung in **Bereit für Beitreibung**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Daten über die Mehrwertsteuerbeitreibung werden an den Drittanbieter gesendet, um die Rückgabebeträge zu erfassen, die aus der Beitreibung der Steuern von internationalen Unternehmen resultieren.

Wenn Arnie bereit ist, die Daten aus der Spesenabrechnung an den Drittanbieter zu senden, der die Rückerstattungen der **Mehrwertsteuerbeitreibungen** angemeldet, öffnet er das Formular . Arnie filtert das Formular, damit nur die Spesenabrechnungen angezeigt werden, die als **Bereit für Beitreibung** markiert sind. Anschließend klickt Arnie auf **Datei** > &gt; **Nach Excel exportieren**. Die Mehrwertsteuerinformationen aus den Spesenabrechnungen werden in ein Microsoft Excel-Arbeitsblatt exportiert. Arnie übermittelt das Arbeitsblatt an den Drittanbieter und informiert diesen, dass die Papierbelege per Kurierdienst gesendet wurden.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Verarbeiten von Ausgaben für die Beitreibung von inländischer Mehrwertsteuer

Arnie muss überprüfen, ob die Spesenabrechnungsbuchungen auf die Mehrwertsteuerbeitreibung angerechnet werden können, und ob die digitalen Belege an die Abrechnungen angefügt werden. Um die Verarbeitung von anrechenbaren Ausgaben für die Beitreibung inländischer Steuern zu beginnen, öffnet Arnie das Formular **Ausgaben-Steuerbeitreibung** und wählt die zu überprüfende Spesenabrechnung aus. Sie überprüft, ob die Belege im Namen des Unternehmens und nicht des Mitarbeiters ausgestellt wurden. Die MwSt-Rückerstattung muss im Name des Unternehmens sein. Arnie überprüft anschließend, ob die richtige Mehrwertsteuergruppe und die richtigen Artikel-Mehrwertsteuercodes angewendet wurden.

Wenn Arnie die Papierbelege erhält, ändert er den Status der Spesenabrechnung in **Bereit für Beitreibung** Er kann dann die Rückerstattung bei der entsprechenden Steuerbehörde einreichen. In diesem Fall handelt es sich in den USA um den Internal Revenue Service (IRS).
