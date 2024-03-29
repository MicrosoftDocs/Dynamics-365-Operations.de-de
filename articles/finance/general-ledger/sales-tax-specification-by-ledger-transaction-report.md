---
title: Bericht „Mehrwertsteuerspezifikation nach Sachkontobuchungen“
description: In diesem Artikel wird erläutert, wie der Bericht „Mehrwertsteuerspezifikation nach Sachkontobuchungen“ verwendet wird, um Informationen zu Sachkontobuchungen anzuzeigen und zu drucken, für die Mehrwertsteuer berechnet wird.
author: EricWang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: c96f457a0ea24aef1769f370c3c0657ada31eebf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898090"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>Bericht „Mehrwertsteuerspezifikation nach Sachkontobuchungen“
[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie der Bericht **Mehrwertsteuerspezifikation nach Sachkontobuchungen** verwendet wird, um Informationen zu Sachkontobuchungen anzuzeigen und zu drucken, für die Mehrwertsteuer berechnet wird.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Steuerkonto für Nicht-Steuerkonten

Der Bericht **Mehrwertsteuerspezifikation nach Sachkontobuchungen** enthält Steuerbuchungen für Steuerkonten und Nicht-Steuerkonten. Diese Konten werden folgendermaßen kategorisiert:

- **Steuerkonto** – Es wird ein Konto als ein Steuerkonto angesehen, wenn eine Steuerbuchung gebucht wird, und das Hauptkonto in der Erfassungsposition **Mehrwertsteuer** ein Steuerkonto ist, wie z. B. ein Konto für Mehrwertsteuer oder Vorsteuer.
- **Nicht-Steuerkonto** – Es wird ein Konto als ein Nicht-Steuerkonto angesehen, wenn eine Steuerbuchung gebucht wird, und das Hauptkonto in der ursprünglichen Transaktion ein Nicht-Steuerkonto ist, wie z. B. ein Konto für Umsatzerlös oder Ausgaben.

Für Steuerkonten zeigen die Spalten **Buchungsgrundlage**, **Vorsteuer** und **Mehrwertsteuer** im Bericht **0** (null) an. Für Nicht-Steuerkonten zeigen die Spalten Beträge an.

## <a name="filtering-the-data-on-the-report"></a>Filtern der Daten im Bericht

Wenn dieser Bericht generiert wird, werden die folgenden Felder verfügbar. Sie können mithilfe dieser Felder die Daten filtern, die im Bericht angezeigt werden.

| Feld                      | Beschreibung |
|----------------------------|-------------|
| Datum                       | Verwenden Sie die Felder in den Abschnitten **Von** und **Bis**, um für die Steuerbuchungen einen Datumsbereich zu definieren. |
| Hauptkonto               | Verwenden Sie die Felder in den Abschnitten **Von** und **Bis**, um für die Hauptkonten einen Bereich zu definieren. |
| Mehrwertsteuercode             | Verwenden Sie die Felder in den Abschnitten **Von** und **Bis**, um einen Bereich von Mehrwertsteuercodes zu definieren. |
| Gruppieren                   | Wählen Sie aus, ob der Bericht nach Sachkonto oder Mehrwertsteuercode gruppiert werden soll. |
| Zwischensumme nach Mehrwertsteuercode | Legen Sie diese Option auf **Ja** fest, um Zwischensummen nach Mehrwertsteuercode anzuzeigen. |
| Nur Summen                | Legen Sie diese Option auf **Ja** fest, um nur Summen anzuzeigen. |
| Nur Hauptkonten         | Legen Sie diese Option auf **Ja** fest, um nur Hauptkonten im Bericht einzubeziehen. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Ausschließliches Anzeigen von Nicht-Steuerkonten im Bericht

Um nur Nicht-Steuerkonten im Bericht anzuzeigen, richten Sie eine Filterbedingung ein, wie z. B. Sternchen (\*), wie in der folgenden Abbildung dargestellt.

![Bericht mit Nicht-Steuerkonten.](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
