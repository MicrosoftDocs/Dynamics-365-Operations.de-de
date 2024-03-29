---
title: Berichtigung einer Freitextrechnung
description: In diesem Artikel wird beschrieben, wie eine Freitextrechnung, die gebucht wurde, korrigiert und als korrekte Rechnung erfasst wird.
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3cc07a1f0ba444250eddcf892681e2ca63e9c1a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780520"
---
# <a name="correct-a-free-text-invoice"></a>Berichtigung einer Freitextrechnung

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie eine Freitextrechnung, die gebucht wurde, korrigiert und als korrekte Rechnung erfasst wird.

Zum Korrigieren einer bereits gebuchten Freitextrechnung: 
1. Öffnen Sie die gebuchte Freitextrechnung. 
2. Auf der Seite **Rechnung**  wählen Sie **Abbrechen**, und dann **Rechnung korrigieren**. 
3. Wählen Sie einen Ursachencode aus, und geben Sie Kommentare ein, und wählen Sie Datum für die korrigierte Rechnung ein.
4. Sie können die berichtigte Rechnung bearbeiten und buchen. 

Wenn Sie die berichtigte Rechnung buchen, wird eine Stornorechnung für einen Habenbetrag erstellt, der mit dem ursprünglichen Rechnungsbetrag übereinstimmt. Dadurch wird der kombinierte Saldo der ursprünglichen Rechnung und der Stornierung auf 0 gesetzt. Die Stornorechnung wird mit der ursprünglichen Rechnung ausgeglichen. 

Nachdem Sie die berichtigte Rechnung buchen, haben Sie drei Rechnungen:

-   **Ursprüngliche Rechnung** – Die Rechnung mit den zu korrigierenden Informationen.
-   **Stornorechnung** – Die vom System generierte Ausgleichsrechnung, die zur Stornierung der zuletzt berichtigten Rechnung erstellt wurde.
-   **Korrigierte Rechnung** – Die Rechnung mit den korrigierten Rechnungsinformationen.

Sie können Storno- und Korrekturrechnungen auf zwei Arten identifizieren:

-   Die **Alle Freitextrechnungen**-Seite umfasst eine **Korrektur**-Spalte, in der Sie sehen können, welche Rechnungen Stornorechnungen und berichtigte Rechnungen sind.
-   Der Kopf der Freitextrechnung zeigt den Status **Rechnung stornieren**\[Rechnungsnummer\]oder **korrekte Rechnungsnummer '\[Rechnungsnummer\]'**.

> [!NOTE]
> Diese Funktion ist nur verfügbar, wenn der Konfigurarionsschlüsse **Freitext-Rechnungskorrektur** ausgewählt ist. Weitere Informationen dazu, wie Sie Konfigurationsschlüssel aktivieren, finden Sie im Abschnitt zum Aktivieren (oder Deaktivieren) von Konfigurationsschlüsseln im Artikel [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md). 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
