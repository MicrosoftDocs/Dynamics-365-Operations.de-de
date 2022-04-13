---
title: Aktivitätsmeldungen
description: Eine Aktivitätsmeldung ist ein vom System generierter Vorschlag zum Ändern eines vorhandenen geplanten oder festen Bestellvorschlags.
author: t-benebo
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2acba2ba12f933c085de15eadbf4d433944c2cf3
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469449"
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







[!INCLUDE[footer-include](../../includes/footer-banner.md)]