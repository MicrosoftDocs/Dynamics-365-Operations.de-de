---
title: "Währungswechselkurse importieren"
description: "Wenn eine juristische Person Rechnungen in Fremdwährungen erhalten hat, ist es erforderlich, die Fremdwährung in der lokalen Währung umgerechnet. Das bedeutet, dass aktueller Wechselkurse für unterschiedliche Währungen erforderlich sind. Dieses Thema enthält einen Überblick der erforderlichen Einstellungen und der Verarbeitung für den Import von Devisenkursreferenzsätzen der Daten, die über das Internet bei den Wechselkursanbietern, wie der Europäischen Zentralbank Zentralbank und der der russischer Föderation veröffentlicht werden."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>Währungswechselkurse importieren

Wenn eine juristische Person Rechnungen in Fremdwährungen erhalten hat, ist es erforderlich, die Fremdwährung in der lokalen Währung umgerechnet. Das bedeutet, dass aktueller Wechselkurse für unterschiedliche Währungen erforderlich sind. Dieses Thema enthält einen Überblick der erforderlichen Einstellungen und der Verarbeitung für den Import von Devisenkursreferenzsätzen der Daten, die über das Internet bei den Wechselkursanbietern, wie der Europäischen Zentralbank Zentralbank und der der russischer Föderation veröffentlicht werden.

In den folgenden Abschnitten wird den Informationsfluss, die für das Einrichten und die Verarbeitung des Imports der ausländischen Wechselkurse verwendet wird.

## <a name="configure-an-exchange-rate-provider"></a>Konfigurieren eines Wechselkursanbieter
Bevor Sie Wechselkurse importieren können, müssen Sie die Informationen einrichten, die von den Anbietern erforderlich ist, die die Wechselkurse anbieten. Auf der ** konfigurieren Sie Wechselkursanbieter ** Seite, um die Wechselkursanbieter auszuwählen. Einige sind mit den Wechselkursanbieter Demodaten in Microsoft Dynamics 365 für Arbeitsgänge einbezogen. Die folgende Tabelle enthält Beschreibungen der Steuerelemente auf dieser Seite an.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | Der Name des Wechselkursanbieters.                                                                                                                                                                                     |
| ** Schlüssel **   | Der eindeutige Bezeichner für jede Konfigurationsinformation, die vom Anbieter benötigt wird. Diese Information wird automatisch für jeden Wechselkursanbieter hinzugefügt, den Sie hinzufügen, wenn Sie auf die ** Hinzufügen ** Schaltfläche klicken. |
| **Value** | Informationen für jeden Schlüssel. Diese Informationen werden für jeden Wechselkursanbieter hinzugefügt, den Sie hinzufügen, wenn Sie auf die ** Hinzufügen ** Schaltfläche klicken.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Währungswechselkurse importieren
Sie können Wechselkurse der Wechselkursanbieterquelle importieren und setzen sie in der ** Währungswechselkurse ** Seite festgelegt. Verwenden Sie die Importwährungswechselkurse ** ** Seite, um Kurse zu importieren. Die folgende Tabelle enthält Beschreibungen die Felder, die erforderlich sind, um den Importvorgang erfolgreich ausgeführt.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | Ein Wechselkurstyp.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | Ein Wechselkursanbieter.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | Dieser Parameter verwaltet, ob zum heutigen Datum oder einen Datumsbereich importiert. Wenn Sie einen Datumsbereich verwenden möchten, geben können Sie das Start- und Enddatum aus.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | Dieses Kontrollkästchen verwaltet die automatische Erstellung von Währungspaaren, wenn die Währungspaare, die zu importieren sind, sind nicht zulässig. Diese Option kann z nicht für mehrere Anbieter verfügbar.                                                                                                                                                                                               |
| **Override existing exchange rates**   | Dieses Kontrollkästchen verwaltet die Aktualisierung des vorhandenen Wechselkurs für ein Währungspaar, wenn der Wechselkurs für ein bestimmtes Datum bereits vorhanden ist. Wenn Sie dieses Kontrollkästchen nicht aktivieren, wird der Konvertierungskurs für das spezifische Datum nicht importiert, wenn ein anderer Wechselkurs bereits vorhanden ist.                                                                                       |
| **Prevent import on national holiday** | Dieses Kontrollkästchen verwaltet den Import des Wechselkurses für ein Datum, das einen von Feiertag ist. Wenn Sie z dieses Kontrollkästchen aktivieren und die Zentralbank europäische als der Wechselkursanbieter verwenden, das Feld nicht den Wechselkurs an einem gesetzlichen Feiertag, der der aktuellen juristischen Person zugeordnet ist. Diese Option kann z nicht für mehrere Anbieter verfügbar. |




