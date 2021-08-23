---
title: Ändern von elektronisches Berichterstellungsformaten, indem Excel-Vorlagen erneut angewendet werden
description: In diesem Thema wird beschrieben, wie Sie das Format der elektronischen Berichterstellung (EB) ändern können, das verwendet wird, um Geschäftsdokumente zu generieren, indem eine geänderte Excel-Tabelle erneut angewendet wird.
author: NickSelin
ms.date: 06/01/2017
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
ms.openlocfilehash: 57f0db12657878fa34c86c55925d62100c26cad8799e5e6ace7e7dd81d91cd9f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737874"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Elektronische Berichterstellungsformate ändern, indem Microsoft Excel-Vorlagen erneut angewendet werden

[!include [banner](../includes/banner.md)]

Das elektronische Meldung (ER)- Tool wird verwendet, um Geschäftsdokumente in einem elektronischen Format zu generieren. Um ein Geschäftsdokument zu generieren, müssen Sie ein ER-Format erstellen und verwenden dann den ER-Designe, um das Layout des Geschäftsdokuments zu definieren und die Daten anzugeben, die im Modul implementierten einbezogen werden sollen. Sie können das ER-Format anschließend ausführen, um das Geschäftsdokument zu generieren.

Das EB-Tool kann verwendet werden, um Geschäftsdokumente als Microsoft Excel-Dateien zu generieren. Sie können ein Excel-Dokument als Vorlage für diese Dokumente verwenden. Um das Dokumentlayout im ER-Designer zu definieren, können Sie den Inhalt des Excel-Dokuments importieren das als Vorlage für das festgelegte ER-Format verwenden möchten. Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Design einer Konfiguration zur Generierung von Berichten im OPENXML-WORD-Format** (Teil des 7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)-Geschäftsprozesses) wieder.

Wenn Sie das Excel-Dokument bearbeiten, das als Vorlage für ein Geschäftsdokument verwendet wird, wenn neue ER-Funktionen Sie die aktualisierte Vorlage für den ER-Format erneut verwenden. Das ER-Format wird dann aktualisiert, damit sie die aktualisierte Vorlage verwendet werden soll. Weitere Informationen zu diesen Funktionen, siehe Aufgabenleitfaden **Ein elektronisches Berichterstellungsformat ändern, indem eine Microsoft Excel-Vorlage erneut angewendet wird** (Gehört zum 7.5.5.3 Acquire/Develop IT service/solution components (10683) Geschäftsprozess). Als Teil des Schritts für das Importieren einer aktualisierten Vorlage im Aufgabenleitfaden, verwenden Sie die geänderte Vorlage des Zahlungsberichts SampleVendPaymWsReport2-Excel-Datei als Vorlage.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]