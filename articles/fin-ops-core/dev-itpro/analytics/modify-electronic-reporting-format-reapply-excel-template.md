---
title: Ändern von elektronisches Berichterstellungsformaten, indem Excel-Vorlagen erneut angewendet werden
description: In diesem Artikel wird beschrieben, wie Sie das Format der elektronischen Berichterstellung (EB) ändern können, das verwendet wird, um Geschäftsdokumente zu generieren, indem eine geänderte Excel-Tabelle erneut angewendet wird.
author: NickSelin
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50b115448bc89bba7e9abeb8062d03d31a163b64
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906730"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Elektronische Berichterstellungsformate ändern, indem Microsoft Excel-Vorlagen erneut angewendet werden

[!include [banner](../includes/banner.md)]

Das elektronische Meldung (ER)- Tool wird verwendet, um Geschäftsdokumente in einem elektronischen Format zu generieren. Um ein Geschäftsdokument zu generieren, müssen Sie ein ER-Format erstellen und verwenden dann den ER-Designe, um das Layout des Geschäftsdokuments zu definieren und die Daten anzugeben, die im Modul implementierten einbezogen werden sollen. Sie können das ER-Format anschließend ausführen, um das Geschäftsdokument zu generieren.

Das EB-Tool kann verwendet werden, um Geschäftsdokumente als Microsoft Excel-Dateien zu generieren. Sie können ein Excel-Dokument als Vorlage für diese Dokumente verwenden. Um das Dokumentlayout im ER-Designer zu definieren, können Sie den Inhalt des Excel-Dokuments importieren das als Vorlage für das festgelegte ER-Format verwenden möchten. Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Design einer Konfiguration zur Generierung von Berichten im OPENXML-WORD-Format** (Teil des 7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)-Geschäftsprozesses) wieder. In dem Schritt der Anleitung, in dem Sie eine Excel-Vorlage importieren, verwenden Sie die ursprüngliche Vorlage der Excel-Datei Payment Report, [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx).

Wenn Sie das Excel-Dokument bearbeiten, das als Vorlage für ein Geschäftsdokument verwendet wird, wenn neue ER-Funktionen Sie die aktualisierte Vorlage für den ER-Format erneut verwenden. Das ER-Format wird dann aktualisiert, damit sie die aktualisierte Vorlage verwendet werden soll. Weitere Informationen zu diesen Funktionen, siehe Aufgabenleitfaden **Ein elektronisches Berichterstellungsformat ändern, indem eine Microsoft Excel-Vorlage erneut angewendet wird** (Gehört zum 7.5.5.3 Acquire/Develop IT service/solution components (10683) Geschäftsprozess). In dem Schritt der Anleitung, in dem Sie eine aktualisierte Vorlage importieren, verwenden Sie die geänderte Vorlage der Excel-Datei Payment Report, [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Vorlage aktualisieren](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
