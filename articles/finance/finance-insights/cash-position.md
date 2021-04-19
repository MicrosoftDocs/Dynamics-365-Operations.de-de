---
title: Bargeldposition (Vorschau)
description: In diesem Thema wird beschrieben, wie die Funktion zur Cashflow-Planung die Bargeldposition eines Unternehmens für bestimmte Zeiten vorhersagt. Außerdem werden die Optionen beschrieben, mit denen Prognosen für verschiedene Zeiträume angezeigt werden können.
author: ShivamPandey-msft
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 36eb939d2539653fdcde78a6044cf1a87e8e3280
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811386"
---
# <a name="cash-position-preview"></a>Bargeldposition (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Die Bargeldposition ist die Projektion des Cashflows, die für die nahe Zukunft prognostiziert wird. Sie basiert auf der Projektion von Geldeingängen von Debitoren, die ausstehende Rechnungen und Bestellungen bezahlen, sowie auf der Projektion von Barauszahlungen, die an Kreditoren für Kaufrechnungen und Bestellungen gezahlt werden.

Wenn das System Debitorenzahlungen vorhersagt, verwendet es die Zahlungsvorhersagen aus der Funktion zur Vorhersage von Debitorenzahlungen. Ohne Zahlungsvorhersagen wird die durchschnittliche Zeit, die erforderlich ist, um eine Debitorenrechnung in eine Zahlung für jeden Debitor umzuwandeln, zur Berechnung eines Zahlungsdatums verwendet. Bei offenen Debitorenbestellungen berechnet das System das Rechnungsdatum anhand der durchschnittlichen Anzahl von Tagen für die Rechnungsstellung der Auftragspositionen pro Debitor. Anschließend wird das Rechnungsdatum als Eingabe für die Zahlungsvorhersagefunktion verwendet. Die Funktion zur Vorhersage der Debitorenzahlung berechnet für jede Bestellposition ein Zahlungsdatum. 

<*Text von Jarek oder Dave darüber erforderlich, wie Zahlungsvorhersagen in ein Datum umgewandelt werden*> Der Zahlungstermin für ausstehende Rechnungen ist ungefähr [*geschätzt*] aus den Zahlungsvorhersagen durch Auswahl eines Datums, das dem fünfzigsten Perzentil der kumulativen Verteilungsfunktion entspricht, die aus den Wahrscheinlichkeiten des vorhergesagten Buckets stammen.

Ein ähnlicher Ansatz wird verwendet, um Zahlungen an Kreditoren vorherzusagen. Für jeden Kreditor berechnet das System die durchschnittliche Zeit, die erforderlich ist, um eine Kreditorenrechnung in eine Zahlung umzuwandeln. Diese Anzahl von Tagen wird dann dazu verwendet, das Zahlungsdatum zu berechnen. Bei offenen Kreditorenbestellungen berechnet das System das Rechnungsdatum unter Berücksichtigung der durchschnittlichen Anzahl von Tagen, die erforderlich sind, um Auftragspositionen für jeden Kreditor in eine Rechnung umzuwandeln. Das System berechnet dann das Zahlungsdatum unter Verwendung der durchschnittlichen Zeit, die erforderlich ist, um eine Zahlung für jeden Kreditor umzuwandeln.

Der obere Teil der **Bargeldposition**-Registerkarte enthält ein Bargeldpositionsdiagramm. Dieses Diagramm zeigt die Geldeingänge und -abgänge sowie deren Auswirkungen auf die gesamte Liquiditätsbilanz. Die Details im Bargeldpositionsdiagramm können in täglichen, wöchentlichen, monatlichen oder vierteljährlichen Zeiträumen angezeigt werden. Wenn Sie **Täglich** auswählen, können Sie Prognosen für die nächsten 21 Tage anzeigen. Wenn Sie **Wöchentlich** auswählen, können Sie Prognosen für die nächsten 20 Wochen anzeigen. Wenn Sie **Monatlich** auswählen, können Sie Prognosen für die nächsten 12 Monate anzeigen. Wenn Sie **Vierteljährlich** auswählen, können Sie Prognosen für die nächsten 12 Quartale anzeigen. Sie können das Diagramm ausblenden, wenn Sie zusätzlichen Platz auf Ihrem Bildschirm benötigen, um Inhalte auf der Registerkarte **Bargeldposition** anzuzeigen.

Der untere Teil der Registerkarte **Bargeldposition** zeigt Details zur Position, zum Cashflow, zu geplanten Zahlungen und zum Bankkonto.

- Informationen im Raster **Positionsdetails** werden in drei Abschnitten dargestellt: einer Liste der Liquiditätskonten, einer Liste der Dokumente, aus denen sich die Geldzugänge zusammensetzen, und einer Liste der Dokumente, aus denen sich die Geldabgänge zusammensetzen. Das Raster zeigt auch eine Bilanz der Bargeldposition an. Für den ersten Zeitraum, den Sie anzeigen, ist der Saldo für die Liquiditätskonten der Eröffnungssaldo. Für Folgeperioden werden die Salden für die Liquiditätskonten auf der Grundlage der Summierung von Geldzugängen und der Subtraktion von Geldabgängen aus früheren Perioden berechnet. Um Details zu den Transaktionen anzuzeigen, aus denen der Saldo besteht, wählen Sie die Verknüpfung **Bilanz** aus.
- Das **Cashflow**-Raster zeigt die Geldeingänge, die pro Periode aggregierten Geldabgänge und ihre Auswirkungen auf die Liquiditätskontensalden an. Für den ersten Zeitraum, ist der Saldo für die Liquiditätskonten der Eröffnungssaldo. Für Folgeperioden werden die Salden für die Liquiditätskonten auf der Grundlage der Summierung von Geldzugängen und der Subtraktion von Geldabgängen aus früheren Perioden berechnet.
- Das **Projizierter Banksaldo**-Raster zeigt die erwarteten Geldabgänge und ihre Auswirkungen auf die Liquiditätskonten.
- Das **Bankkonto**-Raster zeigt die Auswirkungen der erwarteten Geldein- und -abgänge auf den Banksaldo.

Erstellen Sie eine Momentaufnahme, um die Bargeldposition zu speichern und zu bearbeiten. Weitere Informationen zum Arbeiten mit Momentaufnahmen, finden Sie unter [Übersicht über Momentaufnahmen](payment-snapshots.md).

#### <a name="privacy-notice"></a>Datenschutzhinweis
Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]