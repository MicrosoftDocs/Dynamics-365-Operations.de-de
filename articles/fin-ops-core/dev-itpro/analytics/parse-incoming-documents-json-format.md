---
title: Analysieren eingehender Dokumente im JSON-Format
description: In diesem Thema wird erläutert, wie Sie elektronische Berichterstattungsformate (ER) einrichten, um eingehende Dokumente im JavaScript Object Notation (JSON) Format zu analysieren.
author: kfend
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4e598dc15b619c2f6a0525ea18c371484ca26fa4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755153"
---
# <a name="parse-incoming-documents-in-json-format"></a>Analysieren eingehender Dokumente im JSON-Format

[!include[banner](../includes/banner.md)]

Sie können elektronische Berichterstattungsformate (ER) entwerfen, um eingehende elektronische Dokumente zu analysieren, die Daten in einem Textformat darstellen, das auf JavaScript basiert (das heißt, Dateien in JavaScript Object Notation \[JSON\] Format).

Um mehr über diese Funktion zu erfahren, laden Sie die Dateien in die folgende Tabelle, und führen Sie den ER Konfigurationsformat erstellen aus, um Daten aus externen JSON-Dateiaufgabenleitfaden zu importieren. Dieser Aufgabenleitfaden veranschaulicht, wie ein ER-Format verwendet werden kann, um eine eingehende JSON-Datei zu analysieren, um Bewerbungsdaten zu aktualisieren.

| Titel                                  | Dateiname |
|----------------------------------------|-----------|
| ER-Formatkonfiguration                | [Format zum Importieren des trans_JSON.xml der Kreditoren](https://go.microsoft.com/fwlink/?linkid=874111) |
| Beispiel einer eingehenden Datei im .csv-Format | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Anforderungen

Bevor Sie den ER Formatkonfiguration abschließen, um Daten aus einem externen JSON-Dateiaufgabenleitfaden zu importieren, muss die folgende Anforderungen erfüllt sein:

- Übergeordnete Elemente in der JSON-Datei können nur Objektelemente sein.
- Geschachtelte Elemente für ein Objekt sollen Eigenschaftenelemente sein, damit eine gültige JSON-Struktur erstellt wird.
- JSON-Arrays können nur geschachtelte Elemente der Eigenschaftenelemente eines Objekts sein.
- JSON-Arrays können nur JSON-Objekte enthalten. Sie können keine direkte Zeichenfolge / numerische Werte und geschachtelte Arrays enthalten. Elemente in diesen Arrays werden in der Reihenfolge analysiert, in der sie im Format angegeben werden. Vielfältige Einstellungen in jedem JSON-Objekt werden berücksichtigt.

Zusätzlich müssen Sie die erforderlichen Konfigurationen erstellen, um [Daten aus einer externen Datei zu importieren ](tasks/er-required-configurations-import-data.md) Aufgabenanleitung, wenn Sie diese noch nicht abgeschlossen haben. Laden Sie die folgende Datei herunter, um den Aufgabenleitfaden ausführen.

| Titel                  | Dateiname |
|------------------------|-----------|
| ER Modellkonfiguration | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]