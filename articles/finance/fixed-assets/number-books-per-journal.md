---
title: Anzahl der Bücher pro Erfassung
description: In diesem Thema wird die Beziehung zwischen Erfassungen und Anlagenbüchern beschrieben, wenn Sie einen Vorschlag zur Anschaffung oder zur Abschreibung von Anlagen über einen Batch-Auftrag erstellen. Sie können die maximale Anzahl von Büchern definieren, die für jede Anschaffung und für jede Abschreibung enthalten sind.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c56b5a333854c9a95fdc74b8f98a3552ff0f7719
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944800"
---
# <a name="number-of-books-per-journal"></a>Anzahl der Bücher pro Erfassung

[!include [banner](../includes/banner.md)]

In diesem Thema wird die Beziehung zwischen Erfassungen und Anlagenbüchern beschrieben, wenn Sie einen Vorschlag zur Anschaffung oder zur Abschreibung von Anlagen über einen Batch-Auftrag erstellen. Sie können die maximale Anzahl von Büchern definieren, die für jede Anschaffung und für die Abschreibung enthalten sind, indem Sie die Felder im Abschnitt **Anzahl der Bücher pro Erfassung** in der **Allgemeines**-Registerkarte der **Anlagenparameter**-Seite (**Anlage \> Einrichten \> Anlageparameter**) verwenden. In diesen Feldern können Sie die Anzahl der Anlagenbücher pro Anschaffungs- und Abschreibungserfassung verteilen.

Für einen Anschaffungsvorschlag beträgt der Standardwert mindestens 10.000 Bücher. Für einen Abschreibungsvorschlag beträgt der Standardwert mindestens 2.000 Bücher.

Wenn beispielsweise 4.000 Anlagen vorhanden sind und jeder Anlage zwei Bücher zugeordnet sind, wird ein Buch in der aktuelle Ebene und das andere Buch in der Steuerebene gebucht. Wenn Sie 4.000 Anlagen durch Stapelverarbeitung erwerben, enthält der Batch-Auftrag der eine Erfassung von Anlageanschaffung erstellt, 4.000 Anlagenbücher.

> [!NOTE]
> Die erstellte Erfassung wird weiterhin verwendet, bis der Batch-Auftrag abgeschlossen ist.
>
> Die abgeleiteten Bücher sind nicht in der maximalen Anzahl von Büchern pro Erfassung enthalten.

Sie können die Stapelverarbeitung verwenden, um Abschreibungen für denselben Satz erworbener Anlagen durchzuführen. Ein Batch-Auftrag erstellt beispielsweise zwei Abschreibungserfassungen, die jeweils aus 2.000 Anlagenbüchern bestehen. Die erste Erfassung enthält Bücher, die dem Anlagevermögen zugeordnet sind und die Nummern 1 bis 2.000 haben. Die zweite Erfassung enthält dann Bücher, die dem Anlagevermögen zugeordnet sind und die Nummern 2.001 bis 4.000 haben.

Der Stapelverarbeitungsjob schließt geschlossene Bücher aus. Beispielsweise werden in einem Batch-Auftrag zur Abschreibung 10 der ersten 2.000 Bücher geschlossen. In diesem Fall enthält die erste Erfassung Bücher, die dem Anlagevermögen zugeordnet sind und die Nummern 1 bis 2.011 haben. Die zweite Erfassung enthält dann Bücher, die dem Anlagevermögen zugeordnet sind und die Nummern 2.012 bis 4.000 haben.

> [!NOTE]
> Wenn Sie Anlagen-IDs mit unterschiedlichen Trennzeichen (z. B. – oder /) haben und Anlagen-Transaktionen in Batchaufträgen erstellen, müssen Sie für jeden Trennzeichentyp einen separaten Batchauftrag ausführen. Das System kann nicht verschiedene Trennzeichen innerhalb desselben Batchauftrags verarbeiten.

Die Begrenzung der Anzahl der Bücher wird angewendet, wenn in derselben Erfassung keine doppelten Anlagen-IDs vorhanden sind. Wenn die Anlagen-ID jedoch mit der Buch-ID übereinstimmt, kann die Anzahl der Bücher pro Erfassung überschritten werden, um die Anlagen-ID in derselben Erfassung zu belassen.

Beispielsweise gibt es 5.001 Anlagen-IDs, jeder Anlagen-ID sind drei Bücher zugeordnet, und jedes Anlagenbuch wird auf derselben Buchungsebene gebucht. Sie führen drei aufeinanderfolgende Monate lang eine Abschreibung ohne Zusammenfassung durch.  Die Abschreibungserfassung wird über einen Batch-Auftrag erstellt, und das System erstellt sieben Erfassungen mit 667 Anlagen-IDs und drei Büchern für jede Anlagen-ID. Das Ergebnis werden 2.001 Bücher sein. Daher werden in drei Monaten 6.003 Erfassungszeilen vorhanden sein, um dieselben Anlagen-IDs in derselben Erfassung zu verwalten. Das System erstellt außerdem eine Erfassung mit 332 Anlagen-IDs und drei Büchern für jede Anlage-ID. In drei Monaten wird es 2.988 Zeilen geben.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
