---
title: Währungswechselkurse importieren
description: Dieser Artikel enthält Informationen zu den Anforderungen für den Import von Fremdwährungsreferenzkursen, die von Wechselkursanbietern veröffentlicht werden.
author: EvgenyPopovMBS
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 27f9b06646d9ce948a6b4528c38c5df9784b24b2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894934"
---
# <a name="import-currency-exchange-rates"></a>Importieren von Währungswechselkursen

[!include [banner](../includes/banner.md)]

Wenn eine juristische Person Rechnungen in Fremdwährungen erhalten hat, ist es erforderlich, die Fremdwährung in der lokalen Währung umzurechnen. Das bedeutet, dass aktueller Wechselkurse für unterschiedliche Währungen erforderlich sind. Dieser Artikel enthält einen Überblick der erforderlichen Einstellungen und der Verarbeitung für den erforderlichen Import von Devisenkursreferenzsätzen der Daten, die über das Internet bei den Wechselkursanbietern, wie der Europäischen Zentralbank und der russischen Föderation veröffentlicht werden.

Die folgenden Abschnitte beschreiben den allgemeinen Informationsfluss, der für die Einrichtung und Verwaltung von Wechselkursen verwendet wird.

## <a name="configure-an-exchange-rate-provider"></a>Wechselkursanbieter konfigurieren
Bevor Sie Wechselkurse importieren können, müssen Sie die Informationen einrichten, die von den Anbietern erforderlich ist, die die Wechselkurse anbieten. Auf der **Konfigurieren von Wechselkursanbietern** Seite, um die Wechselkursanbieter auszuwählen. Einige Wechselkursanbieter sind mit den Demodaten in Dynamics 365 Finance enthalten. Die folgende Tabelle enthält Beschreibungen der Steuerelemente in diesem Seite.

| Feld | Beschreibung                   |
|-----------|-----------------------------------|
| **Name**  | Der Name des Wechselkursanbieters.                                                                                                                                                                                     |
| **Schlüssel**   | Der eindeutige Bezeichner für jede Konfigurationsinformation, die vom Anbieter benötigt wird. Diese Informationen werden automatisch für jeden Wechselkursanbieter hinzugefügt, den Sie hinzufügen, indem Sie auf die Schaltfläche Hinzufügen klicken. |
| **Value** | Informationen für jeden Schlüssel. Diese Informationen werden automatisch für jeden Wechselkursanbieter hinzugefügt, den Sie hinzufügen, indem Sie auf die Schaltfläche Hinzufügen klicken.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importieren von Währungswechselkursen
Sie können Wechselkurse der Wechselkursanbieterquelle importieren und sie in der **Währungswechselkurse** Seite festgelegt. Verwenden Sie die **Importwährungswechselkurse** Seite, um Kurse zu importieren. Die folgende Tabelle enthält Beschreibungen der Felder, die erforderlich sind, um den Importvorgang erfolgreich ausgeführt.

| Feld | Beschreibung                   |
|-----------|-----------------------------------|
| **Wechselkurstyp**                 | Ein Wechselkurstyp                                                                                                                                                                                                                                                                                                                                                      |
| **Wechselkursanbieter**             | Eine Wechselkursanbieterkennung                                                                                                                                                                                                                                                                                                                                                  |
| **Importieren ab**                       | Dieser Parameter verwaltet, ob zum aktuellen Datum oder für ein bestimmtes Datum importiert werden soll. Geben Sie ein Start- und Enddatum ein, oder wählen Sie ein Start- oder Enddatum.                                                                                                                                                                                                                |
| **Erforderliche Währungspaare erstellen**    | Dieses Kontrollkästchen verwaltet die automatische Erstellung von Währungspaaren, wenn die Währungspaare, die zu importieren sind, sind nicht zulässig. Diese Option kann möglicherweise nicht für mehrere Anbieter verfügbar.                                                                                                                                                                                               |
| **Vorhandene Wechselkurse überschreiben**   | Dieses Kontrollkästchen verwaltet die Aktualisierung des vorhandenen Wechselkurs für ein Währungspaar, wenn der Wechselkurs für ein bestimmtes Datum bereits vorhanden ist. Wenn Sie dieses Kontrollkästchen nicht aktivieren, wird der Wechselkurs für das spezifische Datum nicht importiert, wenn ein anderer Wechselkurs bereits vorhanden ist.                                                                                       |
| **Import an Feiertagen verhindern** | Dieses Kontrollkästchen verwaltet den Import des Wechselkurses für ein Datum, das ein Feiertag ist. Wenn Sie z.B. dieses Kontrollkästchen aktivieren und die Zentralbank europäische als der Wechselkursanbieter verwenden, das Feld nicht den Wechselkurs an einem gesetzlichen Feiertag, der der aktuellen juristischen Person zugeordnet ist. Diese Option kann möglicherweise nicht für mehrere Anbieter verfügbar. |
| **Kurs vom vorherigen Tag** | Dieses Kontrollkästchen ist verfügbar, wenn Sie die Funktion **EZB-Import zum aktuellen oder vorherigen Datum** auf der Seite **Funktionsverwaltung** aktivieren. Dieses Kontrollkästchen ist nur für den Anbieter verfügbar. *Europäische Zentralbank*. Aktivieren Sie dieses Kontrollkästchen, um den Währungswechselkurs zu importieren, der von der Europäischen Zentral Bank am vorangegangenen Arbeitstag um ca. 16:00 Uhr MEZ veröffentlicht wurde. Das Kontrollkästchen ist standardmäßig aktiviert. Deaktivieren Sie dieses Kontrollkästchen, um den am selben Arbeitstag veröffentlichten Wechselkurs zu importieren.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]