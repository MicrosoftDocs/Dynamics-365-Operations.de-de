---
title: Eingehende Dokumente im Excel-Format analysieren
description: In diesem Thema finden Sie Informationen über den Entwurf von Elektronischen Berichtsformaten (ER) zum Analysieren von Inhalten in eingehenden Microsoft Excel-Dateien.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "367477"
---
# <a name="parse-incoming-documents-in-excel-format"></a>Analysieren eingehender Dokumente im Excel-Format

[!include[banner](../includes/banner.md)]

Sie können Elektronische Berichtsformate (ER) erstellen, um eingehende Microsoft Excel-Dateien zu analysieren, die Daten in Microsoft Excel-Arbeitsmappen darstellen (Dateien im XLSX-Format). Sie können den Inhalt aus diesen Dateien dann verwenden, um Anwendungsdaten zu aktualisieren. Dies ist hilfreich, wenn Sie:

- Ein neues Modell und Format entwerfen und diese zur Laufzeit testen wollen. In diesem Fall simuliert Excel die eigentlichen Anwendungsdaten.
- Verwalten Sie Daten außerhalb Ihrer Anwendung in Excel und importieren Sie diese Daten, um einen bestimmten Bericht zu erstellen.

Um mehr über diese Funktion zu erfahren, führen Sie die Aufgabenleitfäden **ER Daten aus einer Microsoft Excel-Datei importieren (Teil 1: Entwerfen des Formats)** und **ER Daten aus einer Microsoft Excel-Datei importieren (Teil 2: Daten importieren)** aus (Teile des 7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)-Geschäftsprozesses). Diese Aufgabenleitfäden zeigen, wie die eingehende Excel-Datei analysiert werden kann, indem das ER-Format verwendet wird, um Informationen aus eingehenden Dokumenten zu importieren und Anwendungsdaten zu aktualisieren. Sie können die Dateien des Aufgabenleitfaden im [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) herunterladen.

Laden Sie die folgenden Dateien herunter, um die oben genannten Aufgabenleitfäden auszuführen.

| Inhaltsbeschreibung                         | Datei                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Eingehende Datei im .XLSX-Format - Vorlage    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Eingehende Datei im .XLSX-Format - Beispieldaten | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Wenn Sie den Aufgabenleitfaden [ER Erstellen der erforderlichen Konfigurationen, um Daten aus einer externen Datei zu importieren](./tasks/er-required-configurations-import-data.md) in der aktuellen Dynamics 365 for Finance and Operation-Anwendung noch nicht abgespielt haben, laden Sie die folgende Datei herunter.

| Inhaltsbeschreibung    | Datei                                                            |
|------------------------|-----------------------------------------------------------------|
| ER Modellkonfiguration | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |
