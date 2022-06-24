---
title: Dashboard für die Nutzungsverwaltung
description: In diesem Artikel wird erläutert, wie Sie das Dashboard für die Nutzungsverwaltung verwenden, um die Nutzung des Dienstes für die elektronische Rechnungsstellung zu überwachen und konform zu bleiben.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3fad2acea373e96092208ce06edb31f1a862912d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875970"
---
# <a name="usage-management-dashboard"></a>Dashboard für die Nutzungsverwaltung

[!include [banner](../includes/banner.md)]

Das Dashboard für die **Nutzungsverwaltung** hilft Ihnen bei der Überwachung der Nutzung des elektronischen Rechnungsstellungsdienstes und hilft somit Ihrem Unternehmen, die monatlichen Nutzungsbedingungen einzuhalten. Die Compliance wird durch die Berechnung des Einreichungsvolumens und den Vergleich mit dem erfassten Einreichungsvolumen festgestellt, um Abweichungen zwischen dem erfassten Volumen und dem verbrauchten Volumen zu erkennen.

Das Dashboard enthält die folgenden Indikatoren:

- Ein Kostenindikator, den Sie verwenden können, um den Verbrauch für Lizenzierungs-Compliance-Zwecke zu überwachen:

    - Verbrauch pro Monat (Export)

- Drei Betriebsindikatoren, die Sie verwenden können, um die Nutzung des elektronischen Rechnungsstellungsdienstes für Verwaltungszwecke zu verfolgen:

    - Verbrauch nach Funktion
    - Verbrauch nach Umgebung
    - Verbrauch pro Monat (Import)

## <a name="measurement-scope"></a>Messbereich

- Maßeinheit: 

    Das **Nutzungsverwaltung**-Dashboard zählt die Einreichung von Geschäftsdokumenten und importierten elektronischen Rechnungen.

- Organisation: 

    Die Zählung wird nach der Mandanten-ID Ihrer Organisation zusammengefasst, unabhängig von der Anzahl der Instanzen von Microsoft Dynamics 365 Finance oder Dynamics 365 Supply Chain Management, oder der Anzahl der juristischen Personen, für die der Dienst für die elektronische Rechnungsstellung aktiviert ist.


## <a name="indicator-usage-per-month-export"></a>Indikator: Verbrauch pro Monat (Export)

Dieses Kennzeichen liefert Details zu den elektronischen Rechnungen, die Ihre Organisation während eines definierten Zeitraums ausstellt.

### <a name="scope"></a>Bereich
- Die Anzahl der Geschäftsdokumente, die von Finance and Supply Chain Management an den Dienst für die elektronische Rechnungsstellung gesendet werden, unabhängig von der Anzahl der Zeilen, die diese Geschäftsdokumente enthalten.
- Die Anzahl der eingereichten Geschäftsdokumente, die erfolgreich vom elektronischen Rechnungsdienst verarbeitet wurden. Ein Dokument gilt als erfolgreich verarbeitet, wenn der Aktionsfluss, der in der Funktionseinrichtung definiert ist, abgeschlossen ist.

> [!NOTE]
> Wenn eine elektronische Rechnung an einen externen Webdienst gesendet wird, erfolgt die Zählung unabhängig von den Ergebnissen der Webdienst-Verarbeitung (akzeptiert, abgelehnt oder Schemavalidierungsfehler). Wenn der Webdienst die Anfrage des elektronischen Rechnungsdienstes erhalten und darauf geantwortet hat, gilt die Einreichung als gültige Zählung.

- **Ausnahme:** Geschäftsdokumente werden nicht gezählt, wenn sie von Finance and Supply Chain Management erneut an den Dienst für die elektronische Rechnungstellung übermittelt werden, beispielsweise in Szenarien, in denen eine erneute Übermittlung desselben Geschäftsdokuments erforderlich ist, um den Status der elektronischen Rechnung zu ändern. Zum Beispiel wird die Ausstellung einer brasilianischen elektronischen Rechnung (Steuerdokument) als gültig gezählt, aber die Stornierungsanfrage dafür wird nicht gezählt.


### <a name="calculation"></a>Herstellkostenkalkulation

Die Berechnung des Saldos wird wie folgt berechnet:

Guthaben = Kostenlos + Gekauft – Gebraucht

Wobei:

- Frei:
  
    Ein kostenloser Umfang an Geschäftsunterlagen, den der Kunde pro Monat einreichen kann. Es enthält ein Paket von 100 Geschäftsdokumenten, die an den elektronischen Rechnungsdienst übermittelt werden können. Das freie Volumen ist nicht kumulativ und das verbleibende Guthaben wird nicht auf den nächsten Zeitraum übertragen.
  
- Eingekauft:
  
    Ein Paket von 1.000 Geschäftsdokumenten, die an den elektronischen Rechnungsdienst übermittelt werden können. Dieses Paket muss monatlich für Ihre Organisation erworben werden. Das gekaufte Volumen ist nicht kumulativ und das verbleibende Guthaben wird nicht auf den nächsten Zeitraum übertragen.
  
- Verwendet: 

    Die Anzahl der Übermittlungen von Geschäftsdokumenten an den elektronischen Rechnungsstellungsdienst nach definierten Kriterien.
   
> [!IMPORTANT]
> Wenn Ihre Organisation plant, das monatliche Volumen von 100 kostenlosen Übermittlungen zu überschreiten, kaufen Sie das Spitzenvolumen, um sicherzustellen, dass Sie die Microsoft-Lizenzierungsrichtlinie für den elektronischen Rechnungsdienst einhalten.
>
> Derzeit muss das gekaufte Volumen je nach Erwerbsdatum in mehreren Paketen von 1.000 Einreichungen manuell eingegeben werden.

## <a name="indicator-usage-by-feature"></a>Indikator: Nutzung nach Funktion

Dieser Indikator zeigt die Nutzung elektronischer Rechnungsfunktionen für die Ausstellung elektronischer Rechnungen während eines definierten Zeitraums an.

- Kalkulation:
  
    Verwendet = Die Anzahl, wie oft jede elektronische Rechnungsstellungsfunktion während der Übermittlung von Geschäftsdokumenten an den elektronischen Rechnungsstellungsdienst verwendet wurde.

## <a name="indicator-usage-by-environment"></a>Indikator: Nutzung nach Umgebung

Dieser Indikator zeigt die Nutzung von Service-Umgebungen für die elektronische Rechnungsstellung während eines definierten Zeitraums an.

- Kalkulation:
    
    Verwendet = Die Anzahl, wie oft jedeService-Umgebung für die elektronische Rechnungsstellung während der Übermittlung von Geschäftsdokumenten an den elektronischen Rechnungsstellungsdienst verwendet wurde.

## <a name="indicator-usage-per-month-import"></a>Indikator: Verbrauch pro Monat (Import)

Dieser Indikator zeigt das Importvolumen elektronischer Rechnungen durch den Dienst für die elektronische Rechnungserstellung in Finance und Supply Chain Management während eines definierten Zeitraums an.

- Bereich:

    Elektronische Rechnungen, die in Finance and Supply Chain Management importiert werden, unabhängig von der Anzahl der Zeilen, die diese elektronischen Rechnungen enthalten.

- Kalkulation:

    Eingegangen = Die Anzahl importierter elektronischer Rechnungen in Finance and Supply Chain Management.

## <a name="functions"></a>Funktionen
### <a name="purchase"></a>Kaufen

Wählen Sie auf der Registerkarte **Verbrauch pro Monat (Export)** die Option **Kauf**, um die Anzahl der erworbenen Einreichungen manuell zu registrieren.

Wählen Sie für ein bestimmtes Datum **Neu** und geben Sie die Anzahl der **Pakete** ein, die an diesem Tag erworben wurden.

Die **Menge** wird folgendermaßen berechnet:

Menge = Pakete * 1.000

Das berechnete **Menge** spiegelt sich in der **Gekauft** vom Indikator **Verbrauch pro Monat (Export)**.

### <a name="update"></a>Buchen

Wählen Sie im Aktivitätsbereich **Aktualisieren**, um die Berechnung zu aktualisieren und die auf der Seite und im Diagramm angezeigten Daten zu aktualisieren.

### <a name="reset-history-data"></a>Verlaufsdaten zurücksetzen

Wählen Sie im Aktivitätsbereich **Verlaufsdaten zurücksetzen**, um die Datenbank zu aktualisieren, aus der die Indikatoren berechnet werden.




> [!NOTE]
> Das **Nutzungsverwaltung**-Dashboard zeigt keine Geldbeträge an. Stattdessen wird nur das Volumen der gezählten Einreichungen und importierten Dokumente angezeigt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
