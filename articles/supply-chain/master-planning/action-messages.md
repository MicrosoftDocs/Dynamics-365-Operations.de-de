---
title: Aktivitätsmeldungen
description: Eine Aktivitätsmeldung ist ein vom System generierter Vorschlag zum Ändern eines vorhandenen geplanten oder festen Bestellvorschlags.
author: ChristianRytt
manager: tfehr
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46e170b18a3c32d443c1de55516d19408b7947d3
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886846"
---
# <a name="action-messages"></a>Aktivitätsmeldungen

[!include [banner](../includes/banner.md)]

Eine Aktivitätsmeldung ist ein vom System generierter Vorschlag zum Ändern eines vorhandenen geplanten oder festen Bestellvorschlags.

## <a name="introduction"></a>Einführung

Aktivitätsmeldungen werden vom Produktprogrammplanungslauf bei der Kalkulation in Reaktion auf geänderte Anforderungen generiert. Beispielsweise hat sich möglicherweise das Versanddatum oder die Menge im einem Auftrag für den Sie bereits eine Bestellung erstellt haben um den Bedarf zu decken geändert. In diesem Fall werden ein oder mehrere Aktivitätsmeldungen von der Produktprogrammplanberechnung generiert, um die Bestellung zu aktualisieren. Ob die vorgeschlagenen Änderungen vorgenommen werden, entscheiden Sie.

Sie können konfigurieren, wie Aktivitätsmeldungen für eine Dispositionssteuerungsgruppe kalkuliert werden, die einem Artikel zugeordnet wird.

## <a name="select-action-messages"></a>Auswählen von Aktivitätsmeldungen

Im Formular **Dispositionssteuerungsgruppen** können Sie die Aktivitätsmeldungen, die das System generieren soll, und die Dispositionssteuerungsgruppen oder die Artikel auswählen, für die die Nachrichten gelten. Sie können die folgenden Aktivitätsmeldungen auswählen.

| Meldung             | Beschreibung                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Termin vorziehen**         | Wenn Sie diese Meldung auswählen, generiert das System wenn erforderlich Aktivitätsmeldungen, um Bestellungen auf ein früheres Datum zu verschieben. Im **Vorverlegungsgrenze**-Feld können Sie die maximale Anzahl der Tage zwischen Zugang und Abgang ohne Voraktivität angeben. |
| **Termin verschieben**        | Wenn Sie diese Meldung auswählen, generiert das System wenn erforderlich Aktivitätsmeldungen, um Bestellungen auf ein späteres Datum zu verschieben. Im **Vorverlegungsgrenze**-Feld können Sie die maximale Anzahl der Tage zwischen Zugang und Abgang ohne Verschiebungsaktion angeben.       |
| **Menge reduzieren**        | Wenn Sie diese Meldung auswählen, sollten Produktionsaufträge, Bestellungen und anderen Zugangsbuchungen verringert werden, um Bestandsüberschüsse zu vermeiden.                                                                                                   |
| **Menge erhöhen**        | Wenn Sie diese Meldung auswählen, sollten Produktionsaufträge, Bestellungen und anderen Zugangsbuchungen erhöht werden, um Bestandknappheiten zu vermeiden.                                                                                                    |
| **Abgeleitete Aktivitäten** | Wenn Sie diese Meldung auswählen, werden Aktivitätsmeldungen für abgeleitete Anforderungen erstellt (beispielsweise für Komponentenbestellungen für die Produktion).                                                                                                   |





