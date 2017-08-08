---
title: "Aktivitätsmeldungen"
description: "Eine Aktivitätsmeldung ist ein vom System generierter Vorschlag zum Ändern eines vorhandenen geplanten oder festen Bestellvorschlags."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fbae19bd9699f17e7ce581415bf859cb87ebdb83
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="action-messages"></a>Aktivitätsmeldungen

[!include[banner](../includes/banner.md)]


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






