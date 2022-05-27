---
title: Nachkalkulationsversionen – Übersicht
description: Dieser Artikel enthält Informationen zu Nachkalkulationsversionen, deren Verwaltung und die Datentypen, die Sie darin einschließen können. Der Hauptzweck einer Nachkalkulationsversion besteht in der Speicherung von Kostendatensätzen für Artikel sowie von Kostenkategorien und Berechnungsformeln für indirekte Kosten.
author: JennySong-SH
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "54532"
- intro-internal
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f83c35872c769ffd14894aaacc729b031d76504
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670495"
---
# <a name="costing-versions-overview"></a>Nachkalkulationsversionen – Übersicht

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Nachkalkulationsversionen, deren Verwaltung und die Datentypen, die Sie darin einschließen können. Der Hauptzweck einer Nachkalkulationsversion besteht in der Speicherung von Kostendatensätzen für Artikel sowie von Kostenkategorien und Berechnungsformeln für indirekte Kosten.

Abhängig von den in einer Nachkalkulationsversion enthaltenen Daten kann eine Nachkalkulation einen oder auch mehrere Zwecke erfüllen. Der Hauptzweck einer Nachkalkulationsversion besteht in der Speicherung von Kostendatensätzen für Artikel sowie von Kostenkategorien und Berechnungsformeln für indirekte Kosten. Eine Nachkalkulationsversion kann eine Gruppe von Standardkostendatensätzen oder eine Gruppe von Datensätzen mit geplanten Kosten enthalten, die auf dem der Nachkalkulationsversion zugewiesenen Nachkalkulationstyp basieren.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Nachkalkulationsversionen für Standardkosten oder geplante Kosten
### <a name="standard-costs"></a>Standardkosten

Von einer Nachkalkulationsversion kann für Artikel ein Lagermodell vom Typ "Standardkosten" unterstützt werden. In diesem Fall enthält die Nachkalkulationsversion eine Gruppe von Standardkostendatensätzen für Artikel und Fertigungsprozesse. Die Kostendaten für Fertigungsprozesse werden in Bezug auf die Kostenkategorien für Arbeitsgänge des Arbeitsplans sowie in Bezug auf die Berechnungsformeln für Produktionsgemeinkosten ausgedrückt.

### <a name="planned-costs"></a>Geplante Kosten

Eine Nachkalkulationsversion kann eine Gruppe von Datensätzen mit geplanten Kosten für Artikel und Fertigungsprozesse enthalten. Nachkalkulationsversionen, die geplante Kosten enthalten, werden häufig zur Unterstützung von Nachkalkulationssimulationen (wie der Simulation der Auswirkungen von Kostenänderungen auf eingekauftes Material oder der Auswirkungen von Fertigungsprozessen auf die berechneten Kosten produzierter Artikel) eingesetzt. Die Artikelkostendatensätze für geplante Kosten können auch zur Unterstützung eines Lagermodells vom Typ "Istkosten" verwendet werden. Zu diesem Zweck werden die Ausgangswerte für Artikelkosten bereitgestellt. Diese Werte enthalten die Berechnung geplanter Kosten für produzierte Artikel.

## <a name="entering-costs"></a>Eingeben von Kosten
Die Datenverwaltung von Kostendatensätzen in einer Nachkalkulationsversion erfordert die Eingabe von Kosten für eingekaufte Artikel sowie für Artikel, die von einem Standort an einen anderen umgelagert werden. Die zusätzliche Datenverwaltung für Hersteller erfordert die Eingabe von Kosten für Kostenkategorien, die den Arbeitsgängen des Arbeitsplans zugeordnet sind, die Eingabe von Formeln zur Berechnung der indirekten Kosten für Produktionsgemeinkosten sowie die Berechnung der Kosten für produzierte Artikel. 

Die Artikelkostendaten in einer Nachkalkulationsversion setzen sich aus einem oder mehreren Kostendatensätzen für jeden Artikel zusammen. Bei der Eingabe erhält ein Artikelkostendatensatz zunächst den Status **Ausstehend** sowie ein gewünschtes Gültigkeitsdatum. Bei Aktivierung des Artikelkostendatensatzes wird der Status zu **Aktiv** und das Gültigkeitsdatum in das Aktivierungsdatum aktualisiert. Unterschiedliche Artikelkostendatensätze können für unterschiedliche Standorte, Gültigkeitsdaten oder Statusinformationen stehen. Beim Berechnen der Kosten produzierter Artikel für ein in der Zukunft liegendes Datum werden für die Herstellkostenkalkulation Kostendatensätze mit dem entsprechenden Gültigkeitsdatum verwendet – unabhängig davon, ob sie den Status **Ausstehend** oder den Status **Aktiv** besitzen. Der derzeit aktive Kostendatensatz eines Artikels wird zur Vorkalkulation der Produktionsauftragskosten sowie zur Bewertung der Lagerbuchungen in Rahmen eines Lagermodells vom Typ "Standardkosten" verwendet. Die Verwaltung von Kostendatensätzen für Kostenkategorien und Berechnungsformeln für indirekte Kosten gleicht der Verwaltung von Artikelkostendatensätzen. 

Anhand zweier Sperrrichtlinien für Nachkalkulationen wird bestimmt, ob ausstehende Kosten verwaltet und ob die ausstehenden Kosten aktiviert werden können. Ermöglichen Sie mithilfe der Sperrrichtlinien die Verwaltung von Daten, und sperren Sie damit anschließend die Datenverwaltung für Kostendatensätze in einer Nachkalkulationsversion. 

Nachkalkulationsversionen können für die Herstellkostenkalkulation auch Daten zu Artikelverkaufspreisen oder Artikeleinkaufspreisen enthalten.

## <a name="item-sales-prices-for-bom-calculations"></a>Artikelverkaufspreise für Herstellkostenkalkulationen
Der wichtigste Grund zum Einschließen von Daten zu den Verkaufspreisen ist die Beibehaltung des berechneten Verkaufspreises eines produzierten Artikels. Der berechnete Verkaufspreis kann anschließend analysiert werden, um zu bestimmen, wie Komponenten, Arbeitsplanvorgänge und Gemeinkosten zu den Kosten und zum Verkaufspreis beitragen. 

Ein sekundärer Grund zum Einschließen von Daten zu Verkaufspreisen ist, die Verkaufspreisdatensätze für Komponentenartikel zu definieren. Diese Datensätze können dann verwendet werden, um den Verkaufspreis produzierter Artikel zu berechnen. Sie definieren zuerst das Verkaufspreismodell, das in eine Herstellkostenkalkulationsgruppe eingebettet wird, und weisen die Herstellkostenkalkulationsgruppe den eingekauften Artikeln zu. Wenn Sie anschließend Herstellkostenkalkulationen mit geplanten Kosten ausführen, wählen Sie das Einstandspreismodell der Herstellkostenkalkulationsgruppe. 

Ansonsten werden die Verkaufspreisdatensätze für Artikel lediglich zu Referenzzwecken verwendet – unabhängig davon, ob die Datensätze manuell eingegeben oder berechnet wurden. Wenn Sie den Verkaufspreisdatensatz eines Artikels aktivieren, können Sie den Basisverkaufspreis des Artikels aktualisieren. Der Basiseinkaufspreis ist jedoch nicht standortspezifisch und kann manuell außer Kraft gesetzt werden. Der Basisverkaufspreis des Artikels wird als Standardverkaufspreis für Aufträge und Verkaufsangebote verwendet.

## <a name="item-purchase-prices-for-bom-calculations"></a>Artikeleinkaufspreise für Herstellkostenkalkulationen
Der Hauptgrund zum Aktivieren von Einkaufspreisdaten besteht im Definieren von Einkaufspreisdatensätzen für Komponentenartikel, die dann zum Berechnen der Kosten produzierter Artikel verwendet werden können. Die Artikeleinkaufspreisdatensätze müssen manuell eingegeben werden. 

Zum Aktivieren von Einkaufspreisinformationen definieren Sie zunächst eine Herstellkostenkalkulationsgruppe mit dem Einstandspreismodell für den Einkaufspreis des Artikels, und weisen Sie die Herstellkostenkalkulationsgruppe eingekauften Artikeln zu. Daraufhin verwenden Sie ein Einstandspreismodell für die Herstellkostenkalkulationsgruppe, wenn Herstellkostenkalkulationen mit geplanten Kosten ausgeführt werden, um den Verkaufspreis produzierter Artikel zu berechnen. 

Die Einkaufspreisdatensätze für Artikel dienen auch zu Referenzzwecken. Durch Ändern des Status des Einkaufspreisdatensatzes eines Artikels von **Ausstehend** zu **Aktiv** kann der Basiseinkaufspreis des Artikels aktualisiert werden. Der Basiseinkaufspreis ist jedoch nicht standortspezifisch und kann manuell außer Kraft gesetzt werden. Der Basiseinkaufspreis des Artikels wird als Standardeinkaufspreis für Bestellungen genutzt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]