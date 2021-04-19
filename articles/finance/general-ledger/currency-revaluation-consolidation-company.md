---
title: Neubewertung der Währung in einem Konsolidierungsunternehmen
description: In diesem Thema wird beschrieben, wie Währung in einem Konsolidierungsunternehmen neu bewertet werden.
author: roschlom
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c901d5ccd8c8b2146daa49752b7d8b70bbfca722
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818415"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Neubewertung der Währung in einem Konsolidierungsunternehmen

[!include [banner](../includes/banner.md)]

Wenn Sie Daten aus einer Buchhaltungswährung zu anderen konsolidieren, müssen Sie die Neubewertung der Währung noch durchführen, wenn es eine Änderung in den Wechselkursen gibt, damit die Kontosalden ordnungsgemäß neu bewertet werden. Wenn Sie ursprünglich die Daten konsolidieren, verwenden Sie die **Währungsumrechnung**-Registerkarte, um die ursprünglichen Wechselkurse für die Übersetzung während des Konsolidierungsprozesses auszuwählen. Nachdem ein neuer Wechselkurs eingegeben wurde (beispielsweise im nächsten Monat), müssen die Kontosalden neu bewertet werden. Die unrealisierten Gewinne oder Verluste werden dann entsprechend aktualisiert, basierend auf dem neuen Wechselkurs und -datum . Das folgende Beispiel veranschaulicht die Buchhaltungseinträge, die beim Ausführen des Prozesses erstellt werden.

## <a name="company-setup"></a>Unternehmenseinrichtung
-   **Quell-/Betreiberunternehmen (USMF)** – US-Dollar (USD) werden als Buchhaltungs- und Berichtswährung verwendet.
-   **Konsolidiertes Unternehmen (CON)** - Euro (EUR) werden als Buchhaltungs- und Berichtswährung verwendet.
    -   **Realisierter Gewinn** – Sachkonto 801500
    -   **Realisierter Verlust** – Sachkonto 801600
    -   **Unrealisierter Gewinn** – Sachkonto 801600
    -   **Unrealisierter Verlust** – Sachkonto 801400

## <a name="original-transactions"></a>Originalbuchungen
### <a name="cash-receipt-transactions-in-usmf"></a>Barbelegbuchungen in USMF

| Datum       | Sachkonto               | Währung | Betrag |
|------------|------------------------------|----------|--------|
| 11.10.2015 | 110110 – Bargeld                | USD      | 500    |
| 11.10.2015 | 130100 – Debitoren | USD      | ‑500   |

## <a name="exchange-rates"></a>Wechselkurse

| Ausgangswährung | Zielwährung | Startdatum | Kurs |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 01.10.2015  | 200           |
| EUR           | USD         | 01.11.2015  | 150           |
| EUR           | USD         | 01.12.2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>Die Konsolidierung für Oktober 2015 ausführen
### <a name="balances-in-the-consolidation-company"></a>Salden im Konsolidierungsunternehmen

| Sachkonto | Währung | Betrag | Herstellkostenkalkulation    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50 %  |
| 130100         | EUR      | ‑250   | ‑500 USD × 50 % |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>Ausführen einer Neubewertung der Währung für die Konten ab dem 1. Oktober 2015 bis zum 30. November 2015
### <a name="balances-in-the-consolidation-company"></a>Salden im Konsolidierungsunternehmen

| Sachkonto | Währung | Betrag  | Herstellkostenkalkulation                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333,33  | Ursprünglicher Betrag 500 × 66,6667 %  |
| 130100         | EUR      | ‑333,33 | Ursprünglicher Betrag -500 × 66,6667 % |
| 801400         | EUR      | 83,33   | 333,33 – 250                       |
| 801600         | EUR      | ‑83,33  | -333,33 – (-250)                   |

Sie finden zusätzliche Buchungen für die Berichtswährungsbeträge.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>Ausführen einer Neubewertung der Währung für die Konten ab dem 1. Oktober 2015 bis zum 31. Dezember 2015
### <a name="balances-in-the-consolidation-company"></a>Salden im Konsolidierungsunternehmen

| Sachkonto | Währung | Betrag  | Herstellkostenkalkulation                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Ursprünglicher Betrag 500 × 1                           |
| 130100         | EUR      | -500,00 | Ursprünglicher Betrag -500 × 1                          |
| 801400         | EUR      | 250     | 500 – 333,33 = 166,67 166,67 + 83,33 = 250           |
| 801600         | EUR      | ‑250    | -500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]