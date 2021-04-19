---
title: Berichte erstellen, indem Sie Inhalt als unformatierten XML-Code hinzufügen
description: Sie können Elektronische Berichterstellung(ER)-Formate entwerfen, die ausgehende Dokumente im XML-Format generieren.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3e007b4feac612ecf74f60dd8a87d76efc7ab4c7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752791"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>Berichte erstellen, indem Sie Inhalt als unformatierten XML-Code hinzufügen

[!include[banner](../includes/banner.md)]

Mit dem neuen Formatelement **RAW XML** können Sie Elektronische Berichterstellung (ER)-Formate entwerfen, die ausgehende Dokumente im XML-Format erzeugen. In einigen Fällen möchten Sie aus einem oder mehreren der folgenden Gründe XML-Rohdaten zu diesen Berichten hinzufügen:

- Es ist bequemer, unformatierten XML-Code für den ursprünglichen Entwurf und die laufende Verwaltung eines Reports zu verwenden, da die XML-Struktur durch die Ausführung eines Laufzeit-Ausdrucks automatisch generiert werden kann. Daher müssen Mehrfachbindungen nicht für mehrere Formatelemente zur Entwurfszeit bestimmt werden. Es ist möglich, wenn die Datenquellen, die Sie verwenden, Informationen enthalten, die für die Erstellung von XML-Elementen während der Berichtserstellung verwendet werden können.
- Keine andere Methode kann verwendet werden, um den Bericht mit XML-Inhalten zu füllen, der zuvor im System empfangen und gespeichert wurde. Beispielsweise kann die XML-Antwort, die erzeugt wird, den Inhalt einer XML-Anforderung enthalten, die zuvor übermittelt wurde.
- Keine andere Methode kann verwendet werden, um Zeichen aufgrund ihrer numerischen Codes in das generierte Dokument einzufügen. Für einige Sprachen und Zeichen existieren solche Codes nicht. Beispiele sind der griechische Buchstabe rho (ρ) und HTML-Entitätscodes wie \&eacute; für ein *e*, das einen Akut (é) hat.

> [!NOTE]
> Beachten Sie, dass das Framework nicht kontrolliert, ob der XML-Inhalt, der mit Hilfe des Formatelements **RAW XML** in das generierte Dokument eingefügt wird, korrekt ist.

Um mehr über diese Funktion zu erfahren, spielen Sie die Aufgabenleitfäden **ER XML-Rohdaten verwenden, um XML-Berichte zu generieren (Teil 1: Entwerfen eines Datenmodells)** und **ER XML-Rohdaten verwenden, um XML-Berichte zu generieren (Teil 2: Bericht entwerfen und ausführen)** ab, die Teil des **7.5.4.3 Acquire/Develop IT-Service/Lösungskomponenten (10677)** Geschäftsprozesses sind und im [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) heruntergeladen werden können. Diese Aufgabenleitfäden führen Sie durch den Prozess der Konfiguration eines ER-Formats zum Einfügen von XML-Rohdaten in generierte Dateien.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]