---
title: Berichtigung einer Freitextrechnung
description: In diesem Artikel wird beschrieben, wie eine Freitextrechnung, die gebucht wurde, korrigiert und als korrekte Rechnung erfasst wird.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: ab16c517abfd3fa2b59625fff04b7427ee3471bb
ms.lasthandoff: 03/31/2017


---

# <a name="correct-a-free-text-invoice"></a>Berichtigung einer Freitextrechnung

[!include[banner](../includes/banner.md)]


In diesem Artikel wird beschrieben, wie eine Freitextrechnung, die gebucht wurde, korrigiert und als korrekte Rechnung erfasst wird.

Um eine Freitextrechnung zu korrigieren, die bereit gebucht wurde, öffnen Sie die gebuchte Freitextrechnung. Auf der Seite **Rechnung**  wählen Sie **Abbrechen**, und dann **Rechnung korrigieren**. Wählen Sie einen Ursachencode aus, und geben Sie Kommentare ein, und wählen Sie Datum für die korrigierte Rechnung ein. Sie können die berichtigte Rechnung bearbeiten und buchen. 

Wenn Sie die berichtigte Rechnung buchen, wird eine Stornorechnung für einen Habenbetrag erstellt, der mit dem ursprünglichen Rechnungsbetrag übereinstimmt. Dadurch wird der kombinierte Saldo der ursprünglichen Rechnung und der Stornierung auf 0 gesetzt. Die Stornorechnung wird mit der ursprünglichen Rechnung ausgeglichen. 

Nachdem Sie die berichtigte Rechnung buchen, haben Sie drei Rechnungen:

-   **Ursprüngliche Rechnung** – Die Rechnung mit den zu korrigierenden Informationen.
-   **Stornorechnung** – Die vom System generierte Ausgleichsrechnung, die zur Stornierung der zuletzt berichtigten Rechnung erstellt wurde.
-   **Korrigierte Rechnung** – Die Rechnung mit den korrigierten Rechnungsinformationen.

Sie können Storno- und Korrekturrechnungen auf zwei Arten identifizieren:

-   Die **Alle Freitextrechnungen**-Seite umfasst eine **Korrektur**-Spalte, in der Sie sehen können, welche Rechnungen Stornorechnungen und berichtigte Rechnungen sind.
-   Der Kopf der Freitextrechnung zeigt den Status **Rechnung stornieren **\[Rechnungsnummer\]oder**korrekte Rechnungsnummer '\[Rechnungsnummer\]'**.

> [!NOTE]
> Diese Funktion ist nur verfügbar, wenn der Konfigurarionsschlüsse **Freitext-Rechnungskorrektur** ausgewählt ist.




