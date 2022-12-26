---
title: Auszugsbuchungsfehler aufgrund von nicht verfügbarem Inventar oder Aktualisierungskonflikten
description: Dieser Artikel bietet mögliche Problemumgehungen für bestandsbezogene Probleme während der Kontoauszugsbuchung in Microsoft Dynamics 365 Commerce.
author: Shajain
ms.date: 12/19/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: cebb890b42def6e9b002b01be63266b88bfc35a4
ms.sourcegitcommit: 4ad87483ba0bfea3e04fdb7e578d8abc34e607a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2022
ms.locfileid: "9887628"
---
# <a name="statement-posting-errors-due-to-unavailable-inventory-or-update-conflicts"></a>Auszugsbuchungsfehler aufgrund von nicht verfügbarem Inventar oder Aktualisierungskonflikten

[!include [banner](../../includes/banner.md)]

Dieser Artikel bietet mögliche Problemumgehungen für bestandsbezogene Probleme während der Kontoauszugsbuchung in Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Description

Während der Buchung von Commerce-Transaktionen erhalten Sie möglicherweise Fehlermeldungen, die sich auf Bestandsprobleme oder Aktualisierungskonflikte beziehen.

### <a name="inventory-issues-error-message"></a>Inventar gibt Fehlermeldung aus

Wenn Inventarprobleme auftreten, ähnelt die Fehlermeldung, die Sie erhalten, diesem Beispiel:

> xx kann nicht entnommen werden, da nur yy im Lager verfügbar ist/sind.

### <a name="update-conflict-error-messages"></a>Konfliktfehlermeldungen aktualisieren

Ein Aktualisierungskonflikt kann auftreten, wenn als Bestandsbewertungsmethode entweder *Standardkosten* oder *Gleitender Durchschnitt* verwendet wird Da es sich bei diesen beiden Methoden um fortlaufende Kostenrechnungsverfahren handelt, werden die endgültigen Kosten zum Zeitpunkt der Buchung ermittelt.

Wenn Sie die Methode *Gleitender Durchschnitt* verwenden, ähnelt die Fehlermeldung zum Aktualisierungskonflikt, die Sie erhalten, diesem Beispiel:

> Bestandswert xx.xx wird nach Berechnung der anteiligen Ausgaben nicht erwartet

Wenn Sie die Methode *Standardkosten* verwenden, ähnelt die Fehlermeldung zum Aktualisierungskonflikt, die Sie erhalten, diesem Beispiel:

> Die Standardkosten stimmen nicht mit dem Wert des finanziellen Bestands nach der Aktualisierung überein. Wert = xx.xx, Menge = yy.yy, Standardkosten = zz.zz

## <a name="resolutions"></a>Auflösungen

### <a name="workaround-for-the-inventory-error"></a>Problemumgehung für den Inventarfehler

Sie können den Lagerbestandsfehler mindern, indem Sie entweder den Lagerbestand für den Artikel manuell aktualisieren oder indem Sie den physischen Negativbestand für die Artikelmodellgruppe aktivieren, die dem Artikel im Commerce headquarters zugeordnet ist.

Für eine einheitliche Buchungserfahrung empfiehlt Microsoft, dass Sie physischen negativen Bestand für die Artikelmodellgruppe aktivieren. In einigen Szenarien können Auszüge nur dann gebucht werden, wenn eine physische negative Inventur aktiviert ist.

Beispielsweise ist für einen Artikel kein Lagerbestand verfügbar, aber ein Kassierer gibt den Artikel zurück und fügt ihn dann derselben Transaktion zu einem reduzierten Preis hinzu, um eine Preisanpassung vorzutäuschen. In diesem Fall werden sowohl die Rückgabetransaktion als auch die Verkaufstransaktion in dieselbe Abrechnung der einzelnen Kundenbestellung gezogen. Da es jedoch keine Garantie dafür gibt, dass die Retourenposition (die den Bestand erhöht) gebucht wird, bevor die Verkaufsposition (die den Bestand verringert) gebucht wird, können Bestandsfehler auftreten. Wenn in diesem Szenario der physische negative Bestand eingeschaltet ist, wird die Transaktionsbuchung nicht negativ beeinflusst, und das System spiegelt den Bestand korrekt wider.

#### <a name="enable-negative-physical-inventory-for-an-item-model-group"></a>Aktivieren Sie einen negativen physischen Bestand für eine Artikelsteuerungsgruppe

Führen Sie die folgenden Schritte aus, um negativen physischen Bestand für eine Artikelmodellgruppe im Commerce headquarters zu aktivieren.

1. Wechseln Sie zu **Lagerverwaltung \> Einstellungen \> Lager**.
1. Wählen Sie im linken Navigationsbereich die Artikelmodellgruppe aus.
1. Wählen Sie im Abschnitt **Inventarrichtlinien** unter **Negatives Inventar** das Kontrollkästchen **Physisches negatives Inventar** aus.

![Physischer negativer Bestand aktiviert.](./media/Physical_Negative_Inventory.png)

### <a name="workaround-for-the-update-conflict-error"></a>Problemumgehung für den Aktualisierungskonfliktfehler

Mögliche Problemumgehungen zum Beheben des Aktualisierungskonfliktfehlers finden Sie unter [Ein Aktualisierungskonflikt tritt auf, wenn die Bestandsbewertungsmethode entweder Standardkosten oder gleitender Durchschnitt ist](/troubleshoot/dynamics-365/supply-chain/costing/update-conflict-standard-cost-moving-average-inventory-valuation).

> [!NOTE]
> Für den Aktualisierungskonflikt-Fehler müssen Sie die Kundenaufträge nicht löschen, die mit dem Aggregationsschritt der Buchung generiert wurden. Nachdem Sie die vorgeschlagenen Problemumgehungen implementiert haben, sollte der Auszug gebucht werden, wenn Sie erneut versuchen, Auszüge zu buchen.
