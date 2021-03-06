---
title: Sie können Masterplanungselemente nicht nach den zugehörigen Abdeckungsgruppenwerten filtern
description: Sie können Masterplanungselemente nicht nach den zugehörigen Abdeckungsgruppenwerten filtern.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049469"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Sie können Masterplanungselemente nicht nach den zugehörigen Abdeckungsgruppenwerten filtern

KB-Nummer: 4612572

## <a name="symptoms"></a>Symptome

Sie möchten die Elemente filtern, die in einem Masterplanungs-Chargeneinzelvorgang enthalten sind, basierend auf den Werten der zugehörigen Datensätze aus der Elementabdeckungstabelle. (Zum Beispiel möchten Sie Elemente nach ihrem Wert **Verkäufer** und/oder **Abdeckungsgruppe** filtern). Mit der Filter-Einrichtung für den Chargeneinzelvorgang können Sie eine Verknüpfung aus der Tabelle **Artikel** zur Tabelle **Artikelabdeckung** erstellen; geben Sie dann Feldwerte aus der Elementabdeckungstabelle in Ihrer Abfrage an. Nach Abschluss dieser Einrichtung erstellt das System jedoch weiterhin Planaufträge für die gesamte Artikelabdeckung, nicht nur für die Artikel, die den angegebenen Feldwerten aus der Artikelabdeckungstabelle entsprechen.

## <a name="resolution"></a>Lösung

Der Chargeneinzelvorgang kann nur nach Elementen filtern. Obwohl Sie der Tabelle **Artikelabdeckung** eine Verknüpfung hinzufügen können, werden Filtereinstellungen, die Sie für diese Tabelle vornehmen, sich nicht auf die Abfrageausgabe auswirken. Zur Laufzeit führt das System eine Planung für alle Abdeckungsgruppen und alle Variationen der gefilterten Elemente aus. Nachdem ein Artikel bereits im Lauf enthalten ist, wirken sich alle im Artikelfilter enthaltenen Abdeckungsgruppen nicht auf die Planungsausgabe aus.
