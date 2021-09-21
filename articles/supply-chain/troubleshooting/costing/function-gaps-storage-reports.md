---
title: Funktionelle Lücken zwischen den Berichten über Bestandswert/Alterung und ihren Speicherversionen
description: Funktionelle Lücken zwischen den Berichten über Bestandswert/Alterung und ihren Speicherversionen
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a72e2d32e755e137cebbc0bf7afb0bed08fb93f2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476468"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Funktionelle Lücken zwischen den Berichten über Bestandswert/Alterung und ihren Speicherversionen

Die Funktionen [Speicherung von Bestandsalterungsberichten](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage.md) und [Speicherung von Bestandswerten](/dynamics365/supply-chain/cost-management/inventory-value-report-storage.md) ermöglichen es dem Supply Chain Management, große Mengen von Bestandstransaktionen anzuzeigen. In jedem Fall werden die Berichtsergebnisse zum Durchsuchen und Exportieren gespeichert, anders als bei den nicht-speicherbaren Versionen dieser Berichte. Einige Funktionen, die in den Nicht-Speicher-Versionen dieser Berichte vorhanden sind, gibt es jedoch in den Speicher-Versionen nicht. Die folgenden Unterabschnitte fassen die Unterschiede zusammen und bieten Umgehungsmöglichkeiten.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Speicherberichte enthalten keine Zwischensummen, auch wenn sie im Berichtslayout aktiviert sind

Zwischensummen können beim Exportieren des Ergebnisses zu Problemen führen, insbesondere wenn Benutzer die Sequenz der Datensätze ändern.

Um die Zwischensummen zu prüfen, können Sie das Ergebnis in Microsoft Excel exportieren. Wenn Sie die Zwischensummen innerhalb des Supply Chain Managements prüfen wollen, verwenden Sie alternativ die [Funktionsverwaltung](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um die Funktionen *Neue Rastersteuerung* und *Gruppierung in Rastern* zu aktivieren, die eine viel flexiblere Möglichkeit bieten, die Zwischensumme für jede Gruppe nach Spalten zu sehen. Weitere Informationen finden Sie unter [Rasterfunktionen](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities.md).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Bestandswert-Speicherbericht unterstützt keine Ledger-Kontoinformationen

Sie können den Test-Saldo ausführen, um den Saldo der Bestandskonten zu erhalten und diesen mit dem **Bestandswert-Speicherung**-Bericht zu vergleichen.
