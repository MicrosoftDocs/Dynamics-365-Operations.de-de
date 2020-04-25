---
title: Gemischtes Kennzeichen – Empfang
description: In diesem Thema wird beschrieben, wie das Empfangen eines gemischten Ladungsträgers verwendet wird, um Arbeit für mehrere Artikel mit einem Mobilgerät zu erfassen und zu erstellen.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15c058887da33b522c5d9a1a8d2c45a5d1566a5d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215768"
---
# <a name="mixed-license-plate-receiving"></a>Gemischtes Kennzeichen – Empfang

[!include [banner](../includes/banner.md)]

Das Empfangen eines gemischten Ladungsträgers ermöglicht Ihnen, einen Ladungsträger zu erstellen, der aus mehreren Artikeln besteht, ehe Sie eine Einlagerungsarbeit erstellen und erfassen. 

Ein Ladungsträger, der aus mehreren Artikeln besteht, muss an der empfangenden Rampe nicht aufgeteilt werden, damit jeder Artikel erfasst werden kann. 

Wenn Sie eines Artikel-bezogenen Fluss verwenden, um die Quelldokumentpositionen zu identifizieren, können Sie Barcodes im Artikelsteuerelement scannen. Wenn der Strichcode eine Menge und eine Maßeinheit (UOM) hat, werden Artikel und Menge automatisch zum gemischten Ladungsträger hinzugefügt und Sie kehren zum Bildschirm zurück, um einen weiteren Artikel zu scannen. Dies ermöglicht Ihnen, schnell alle Artikel zu scannen, ohne jeden Schritt bestätigen zu müssen. 

Im Fluss für das Empfangen gemischter Ladungsträger können Sie die Liste der Artikel anzeigen, die bereits für den Ladungsträger gescannt wurden. Von hier können Sie die Menge eines Artikel ändern oder korrigieren.

## <a name="where-it-applies"></a>Wofür es angewendet wird

Der Empfang gemischter Ladungsträger ist ein Empfangsfluss eines Mobilgeräts, um gleichzeitig Arbeit für mehrere Positionen/Artikel zu erfassen und zu erstellen. Dies ist nützlich, wenn Sie eingehende Ladungsträger mit mehreren Artikel empfangen. 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>So richten Sie den Empfang gemischter Ladungsträger ein:
Der Empfang gemischter Ladungsträger wird als Menüoption des mobilen Geräts eingerichtet.

Sie müssen eine neue Menüoption mit Modusarbeit erstellen, die keine vorhandene Arbeit nutzt, und eine der folgenden Methoden verwenden:

- Gemischtes Kennzeichen – Empfang
- Empfang und Einlagerung gemischter Kennzeichen

Die Optionen zum Identifizieren der Quelldokumentpositionen sind Bestellungsartikel, Bestellpositionen, Rücklieferungen, Umlagerungsaufträge und Umlagerungsauftragspositionen. Diese Optionen können den eingehenden Auftrag für einen einzelnen Ladungsträger ändern. Die letzte Option ist per Ladungsartikel. Sie können mehrere Artikel zu einem Ladungsträger hinzufügen, können aber nicht zwischen Ladungen wechseln.
