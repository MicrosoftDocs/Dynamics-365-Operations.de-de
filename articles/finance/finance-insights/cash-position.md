---
title: Bargeldposition
description: In diesem Artikel wird beschrieben, wie die Funktion zur Cashflow-Planung die Bargeldposition eines Unternehmens für bestimmte Zeiten vorhersagt. Außerdem werden die Optionen beschrieben, mit denen Prognosen für verschiedene Zeiträume angezeigt werden können.
author: ShivamPandey-msft
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7581142348d91b3a37cc75cf801e7bfc098cd604
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870248"
---
# <a name="cash-position"></a>Bargeldposition

[!include [banner](../includes/banner.md)]

Die Bargeldposition ist die Projektion des Cashflows, die für die nahe Zukunft prognostiziert wird. Sie basiert auf der Projektion von Geldeingängen von Debitoren, die ausstehende Rechnungen und Bestellungen bezahlen, sowie auf der Projektion von Barauszahlungen, die an Kreditoren für Kaufrechnungen und Bestellungen gezahlt werden.

Wenn das System Debitorenzahlungen vorhersagt, verwendet es die Zahlungsvorhersagen aus der Funktion zur Vorhersage von Debitorenzahlungen. Ohne Zahlungsvorhersagen wird die durchschnittliche Zeit, die erforderlich ist, um eine Debitorenrechnung in eine Zahlung für jeden Debitor umzuwandeln, zur Berechnung eines Zahlungsdatums verwendet. Bei offenen Debitorenbestellungen berechnet das System das Rechnungsdatum anhand der durchschnittlichen Anzahl von Tagen für die Rechnungsstellung der Auftragspositionen pro Debitor. Anschließend wird das Rechnungsdatum als Eingabe für die Zahlungsvorhersagefunktion verwendet. Die Funktion zur Vorhersage der Debitorenzahlung berechnet für jede Bestellposition ein Zahlungsdatum. 

Der Zahlungstermin für ausstehende Rechnungen ist ungefähr [geschätzt] aus den Zahlungsvorhersagen durch Auswahl eines Datums, das dem fünfzigsten Perzentil der kumulativen Verteilungsfunktion entspricht, die aus den Wahrscheinlichkeiten des vorhergesagten Buckets stammen.

Ein ähnlicher Ansatz wird verwendet, um Zahlungen an Kreditoren vorherzusagen. Für jeden Kreditor berechnet das System die durchschnittliche Zeit, die erforderlich ist, um eine Kreditorenrechnung in eine Zahlung umzuwandeln. Diese Anzahl von Tagen wird dann dazu verwendet, das Zahlungsdatum zu berechnen. Bei offenen Kreditorenbestellungen berechnet das System das Rechnungsdatum unter Berücksichtigung der durchschnittlichen Anzahl von Tagen, die erforderlich sind, um Auftragspositionen für jeden Kreditor in eine Rechnung umzuwandeln. Das System berechnet dann das Zahlungsdatum unter Verwendung der durchschnittlichen Zeit, die erforderlich ist, um eine Zahlung für jeden Kreditor umzuwandeln.

Der obere Teil der **Bargeldposition**-Registerkarte enthält ein Bargeldpositionsdiagramm. Dieses Diagramm zeigt die Geldeingänge und -abgänge sowie deren Auswirkungen auf die gesamte Liquiditätsbilanz. Die Details im Bargeldpositionsdiagramm können in täglichen, wöchentlichen, monatlichen oder vierteljährlichen Zeiträumen angezeigt werden. Wenn Sie **Täglich** auswählen, können Sie Prognosen für die nächsten 21 Tage anzeigen. Wenn Sie **Wöchentlich** auswählen, können Sie Prognosen für die nächsten 20 Wochen anzeigen. Wenn Sie **Monatlich** auswählen, können Sie Prognosen für die nächsten 12 Monate anzeigen. Wenn Sie **Vierteljährlich** auswählen, können Sie Prognosen für die nächsten 12 Quartale anzeigen. Sie können das Diagramm ausblenden, wenn Sie zusätzlichen Platz auf Ihrem Bildschirm benötigen, um Inhalte auf der Registerkarte **Bargeldposition** anzuzeigen.

Der untere Teil der Registerkarte **Bargeldposition** zeigt Details zur Position, zum Cashflow, zu geplanten Zahlungen und zum Bankkonto.

- Informationen im Raster **Positionsdetails** werden in drei Abschnitten dargestellt: einer Liste der Liquiditätskonten, einer Liste der Dokumente, aus denen sich die Geldzugänge zusammensetzen, und einer Liste der Dokumente, aus denen sich die Geldabgänge zusammensetzen. Das Raster zeigt auch eine Bilanz der Bargeldposition an. Für den ersten Zeitraum, den Sie anzeigen, ist der Saldo für die Liquiditätskonten der Eröffnungssaldo. Für Folgeperioden werden die Salden für die Liquiditätskonten auf der Grundlage der Summierung von Geldzugängen und der Subtraktion von Geldabgängen aus früheren Perioden berechnet. Um Details zu den Transaktionen anzuzeigen, aus denen der Saldo besteht, wählen Sie die Verknüpfung **Bilanz** aus.
- Das **Cashflow**-Raster zeigt die Geldeingänge, die pro Periode aggregierten Geldabgänge und ihre Auswirkungen auf die Liquiditätskontensalden an. Für den ersten Zeitraum, ist der Saldo für die Liquiditätskonten der Eröffnungssaldo. Für Folgeperioden werden die Salden für die Liquiditätskonten auf der Grundlage der Summierung von Geldzugängen und der Subtraktion von Geldabgängen aus früheren Perioden berechnet.
- Das **Projizierter Banksaldo**-Raster zeigt die erwarteten Geldabgänge und ihre Auswirkungen auf die Liquiditätskonten.
- Das **Bankkonto**-Raster zeigt die Auswirkungen der erwarteten Geldein- und -abgänge auf den Banksaldo.

Erstellen Sie eine Momentaufnahme, um die Bargeldposition zu speichern und zu bearbeiten. Weitere Informationen zum Arbeiten mit Momentaufnahmen, finden Sie unter [Übersicht über Momentaufnahmen](payment-snapshots.md).

## <a name="details-of-the-cash-position-capability"></a>Details zur Fähigkeit zur Cashflow-Position 

Die Cashflow-Positionsfunktion umfasst die folgenden Funktionen. 

- Die Bargeldpositionsfunktion zeigt den Cashflow basierend auf vorhandenen Dokumenten im System und aus externen Systemen importierten Zahlungsmittelzu- und -abflusslinien an.
- Erleichtert die Integration von Cashflow-Daten von externen Systemen in Dynamics 365 Finance. Bargeldposition kann das Framework für Datenimport-Export verwenden. Dieses Framework erleichtert die Integration in Excel OData. Sie können auch Daten aus mehreren Quellen kombinieren, um eine umfassende Bargeldpositions-Lösung zu erstellen.
- Führt eine intelligente Bargeldposition ein. Die Bargeldposition wird basierend auf dem Zahlungsverhalten des Debitors erstellt, um vorherzusagen, wann ein Unternehmen mit Bargeld auf seinen Konten rechnen kann.
- Für Kundenbestellungen und Rechnungen wird die KI-Funktion zur Vorhersage der Kundenzahlung verwendet, um das historische Zahlungsverhalten des Kunden zu bestimmen, wenn eine Bestellung oder Rechnung bezahlt wird.
- Bei Lieferantenbestellungen und Rechnungen verwenden wir die durchschnittliche Zeit zwischen Versand und Rechnung und Zahlung einer Rechnung pro Lieferant, um zu bestimmen, wann eine Lieferantenbestellung oder Rechnung bezahlt wird, um die Geldabflüsse genauer zu machen.

Dies schafft eine genauere Ansicht des Cashflows basierend auf dem historischen Zahlungsverhalten des Schatzmeisters. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
