---
title: Anlage als Ausschuss veräußern
description: Das Thema beschreibt den Prozess des Beseitigens von Transaktionen für eine Anlage, die als Ausschuss veräußert wurde.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 4dee4468079a9ad500f513900cec090acf6026ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969127"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Anlage als Ausschuss veräußern

[!include [banner](../includes/banner.md)]

Das Thema beschreibt den Prozess des Beseitigens von Transaktionen für eine Anlage, die als Ausschuss veräußert wurde. Die Transaktionsarten, die beseitigt werden können, enthalten die Anschaffung einer Anlage und kumulierte Abschreibungsbuchungen sowie andere Anlagentransaktionen. Die Beseitigung dieser Transaktionen wirkt sich auf Bilanzkonten aus, beispielsweise Anschaffungsänderungs-, Abschreibungsänderungs-, Neubewertungs-, Höherbewertungs- und Niedrigerbewertungskonten.

| Buchung                                         | Soll (S) | Haben (H) |
|-----------------------------------------------------|-------------|--------------|
| Soll – kumulierte Abschreibung                        | X           |              |
| H – Anlagengewinn/-verlust                          |             | X            |
| S – Anlagengewinn/-verlust                          | X           |              |
| H – Konto für Anlagenerwerb                 |             | X            |
| S – Anlagengewinn/-verlust (Nettobuchwert \[NBW\]) | X           |              |
| H – Anlagengewinn/-verlust (NBW)                    |             | X            |

> [!NOTE]
> Wir empfehlen Ihnen, eng mit dem Leiter der Finanzabteilung (CFO) oder Controller Ihres Unternehmens zusammenzuarbeiten, um die korrekten Konten zu ermitteln, die für die einzelnen Transaktionstypen verwendet werden sollten, und sicherzustellen, dass bei dem Veräußerungsprozess und den dabei generierten Transaktionen diese Konten korrekt aktualisiert werden.

Bevor eine Anlage als Ausschuss veräußert werden soll, müssen Sie Sachkonten erstellen, die mit dem Anschaffungswert der Anlage, der Abschreibung für das aktuelle Jahr, der Abschreibung für vorherige Jahre und dem NBW der Anlage verknüpft sind. Die Anlagentransaktionsarten werden auf der Seite **Anlagenbuchungsprofile** angezeigt. Gehen Sie zu **Anlagen \> Einstellungen \> Anlagenbuchungsprofile** und wählen Sie dann im Inforegister **Veräußerung** die Option **Ausschuss** im Feld über dem Raster aus. Die folgende Abbildung zeigt die Liste der Anlagentransaktionsarten auf der Seite **Anlagenbuchungsprofile**.


[![Veräußern einer Anlage als Ausschuss, Abb. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

Im folgenden Beispiel wurde eine Anlage am 1. Januar 2018 erworben und sie wird am 31. März 2019 zu Ausschuss veräußert.

- **Anschaffungspreis:** 24.000,00 US-Dollar (USD)
- **Nutzungsdauer:** Zwei Jahre
- **Abschreibungsmethode:** Lineare Nutzungsdauer
- **Abschreibungsbetrag:** 1.000,00 USD pro Monat

Der NBW einer Anlage wird mithilfe der folgenden Formel berechnet:

Nettobuchwert = Anschaffungspreis – Abschreibung

In diesem Beispiel wurde die Anlage erworben und wurde für 15 Monate abgeschrieben, von Januar 2018 bis März 2019. Daher ist der NBW der Anlage 9.000,00 USD (24.000,00 USD - 15.000,00 USD).

[![Abschreibungsbeispiel für eine Anlage](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Um eine Anlagenentsorgung zu erstellen, gehen Sie zu **Anlagen \> Journaleinträge \> Anlagenerfassung**, und wählen Sie dann im Aktivitätsbereich die Option **Positionen** aus. Wählen Sie **Verschrottung** und dann eine Anlagenkennung aus. Um die Anlage vollständig zu entsorgen, geben Sie weder im Feld **Soll** noch im Feld **Haben** einen Wert ein.

[![Anlagenerfassung](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Durch die Anlagen-Ausschusstransaktion werden die Feldwerte für das Anlagenbuch wie folgt geändert:

- Im Abschnitt **Saldo** wird das Feld **Status** auf **Verschrottet** aktualisiert.
- Im Abschnitt **Abgang** wird das Feld **Abgangsdatum** auf das Datum festgelegt, an dem die Anlage verschrottet wurde.

[![Details zur Anlagenerfassung](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

Die folgende Abbildung zeigt das Anlagensaldo.

[![Anlagensaldo](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

Die folgende Abbildung zeigt den Beleg, der gebucht wird.

[![Nettobuchwert](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]