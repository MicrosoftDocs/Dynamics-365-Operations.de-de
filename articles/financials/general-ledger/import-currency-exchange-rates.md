---
title: "Währungswechselkurse importieren"
description: "Wenn eine juristische Person Rechnungen in Fremdwährungen erhalten hat, ist es erforderlich, die Fremdwährung in der lokalen Währung umgerechnet. Das bedeutet, dass aktueller Wechselkurse für unterschiedliche Währungen erforderlich sind. Dieses Thema enthält einen Überblick der erforderlichen Einstellungen und der Verarbeitung für den Import von Devisenkursreferenzsätzen der Daten, die über das Internet bei den Wechselkursanbietern, wie der Europäischen Zentralbank Zentralbank und der der russischer Föderation veröffentlicht werden."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: df07066371cb7d9c69976c9714b6d2fe456a0308
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="import-currency-exchange-rates"></a>Währungswechselkurse importieren

[!include[banner](../includes/banner.md)]


Wenn eine juristische Person Rechnungen in Fremdwährungen erhalten hat, ist es erforderlich, die Fremdwährung in der lokalen Währung umgerechnet. Das bedeutet, dass aktueller Wechselkurse für unterschiedliche Währungen erforderlich sind. Dieses Thema enthält einen Überblick der erforderlichen Einstellungen und der Verarbeitung für den Import von Devisenkursreferenzsätzen der Daten, die über das Internet bei den Wechselkursanbietern, wie der Europäischen Zentralbank Zentralbank und der der russischer Föderation veröffentlicht werden.

Die folgenden Abschnitte beschreiben den allgemeinen Informationsfluss, der für die Einrichtung und Verwaltung von Wechselkursen verwendet wird.

## <a name="configure-an-exchange-rate-provider"></a>Wechselkursanbieter konfigurieren
Bevor Sie Wechselkurse importieren können, müssen Sie die Informationen einrichten, die von den Anbietern erforderlich ist, die die Wechselkurse anbieten. Auf der **Konfigurieren von Wechselkursanbietern** Seite, um die Wechselkursanbieter auszuwählen. Einige Wechselkursanbieter sind mit den Demodaten in Microsoft Dynamics 365 for Finance and Operations enthalten. Die folgende Tabelle enthält Beschreibungen der Steuerelemente in diesem Seite.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Feld** | **Beschreibung**                                                                                                                                                                                                             |
| **Name**  | Der Name des Wechselkursanbieters.                                                                                                                                                                                     |
| **Schlüssel**   | Der eindeutige Bezeichner für jede Konfigurationsinformation, die vom Anbieter benötigt wird. Diese Informationen werden automatisch für jeden Wechselkursanbieter hinzugefügt, den Sie hinzufügen, indem Sie auf die Schaltfläche **Hinzufügen** klicken. |
| **Wert** | Informationen für jeden Schlüssel. Diese Informationen werden für jeden Wechselkursanbieter hinzugefügt, den Sie hinzufügen, indem Sie auf die Schaltfläche **Hinzufügen** klicken.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Währungswechselkurse importieren
Sie können Wechselkurse der Wechselkursanbieterquelle importieren und setzen sie in der **Währungswechselkurse** Seite festgelegt. Verwenden Sie die **Importwährungswechselkurse** Seite, um Kurse zu importieren. Die folgende Tabelle enthält Beschreibungen die Felder, die erforderlich sind, um den Importvorgang erfolgreich ausgeführt.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Feld**                              | **Beschreibung**                                                                                                                                                                                                                                                                                                                                                             |
| **Wechselkurstyp**                 | Ein Wechselkurstyp                                                                                                                                                                                                                                                                                                                                                      |
| **Wechselkursanbieter**             | Eine Wechselkursanbieterkennung                                                                                                                                                                                                                                                                                                                                                  |
| **Importieren ab**                       | Dieser Parameter verwaltet, ob zum heutigen Datum oder einen Datumsbereich importiert. Geben Sie ein Start- und Enddatum ein, falls Sie einen Zeitraum nutzen möchen.                                                                                                                                                                                                                |
| **Erforderliche Währungspaare erstellen**    | Dieses Kontrollkästchen verwaltet die automatische Erstellung von Währungspaaren, wenn die Währungspaare, die zu importieren sind, sind nicht zulässig. Diese Option kann möglicherweise nicht für mehrere Anbieter verfügbar.                                                                                                                                                                                               |
| **Vorhandene Wechselkurse überschreiben**   | Dieses Kontrollkästchen verwaltet die Aktualisierung des vorhandenen Wechselkurs für ein Währungspaar, wenn der Wechselkurs für ein bestimmtes Datum bereits vorhanden ist. Wenn Sie dieses Kontrollkästchen nicht aktivieren, wird der Wechselkurs für das spezifische Datum nicht importiert, wenn ein anderer Wechselkurs bereits vorhanden ist.                                                                                       |
| **Import an Feiertagen verhindern** | Dieses Kontrollkästchen verwaltet den Import des Wechselkurses für ein Datum, das einen von Feiertag ist. Wenn Sie z.B. dieses Kontrollkästchen aktivieren und die Zentralbank europäische als der Wechselkursanbieter verwenden, das Feld nicht den Wechselkurs an einem gesetzlichen Feiertag, der der aktuellen juristischen Person zugeordnet ist. Diese Option kann möglicherweise nicht für mehrere Anbieter verfügbar. |






