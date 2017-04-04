---
title: nicht dokumentiert
description: "Eine Aktivitätsmeldung ist ein vom System generierter Vorschlag zum Ändern eines vorhandenen geplanten oder festen Bestellvorschlags."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 21 - 54
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f2ac69ddf485139b057dafa20e5f1a961fc32067
ms.lasthandoff: 03/29/2017


---

# <a name="undocumented"></a>nicht dokumentiert

Eine Aktivitätsmeldung ist ein vom System generierter Vorschlag zum Ändern eines vorhandenen geplanten oder festen Bestellvorschlags.

### <a name="introduction"></a>Einführung

Aktivitätsmeldungen werden vom Produktprogrammplanungslauf bei der Kalkulation in Reaktion auf geänderte Anforderungen generiert. Beispielsweise hat sich möglicherweise das Versanddatum oder die Menge im einem Auftrag für den Sie bereits eine Bestellung erstellt haben um den Bedarf zu decken geändert. In diesem Fall werden ein oder mehrere Aktivitätsmeldungen von der Produktprogrammplanberechnung generiert, um die Bestellung zu aktualisieren. Ob die vorgeschlagenen Änderungen vorgenommen werden, entscheiden Sie.

Sie können konfigurieren, wie Aktivitätsmeldungen für eine Dispositionssteuerungsgruppe kalkuliert werden, die einem Artikel zugeordnet wird.

 <a name="selecting-action-messages"></a>Auswählen von Aktivitätsmeldungen
==========================

Im Formular **Dispositionssteuerungsgruppen** können Sie die Aktivitätsmeldungen, die das System generieren soll, und die Dispositionssteuerungsgruppen oder die Artikel auswählen, für die die Nachrichten gelten. Sie können die folgenden Aktivitätsmeldungen auswählen.

| Meldung             | Beschreibung                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Termin vorziehen**         | Wenn Sie diese Meldung auswählen, generiert das System wenn erforderlich Aktivitätsmeldungen, um Bestellungen auf ein früheres Datum zu verschieben. Im **Vorverlegungsgrenze**-Feld können Sie die maximale Anzahl der Tage zwischen Zugang und Abgang ohne Voraktivität angeben. |
| **Termin verschieben**        | Wenn Sie diese Meldung auswählen, generiert das System wenn erforderlich Aktivitätsmeldungen, um Bestellungen auf ein späteres Datum zu verschieben. Im **Vorverlegungsgrenze**-Feld können Sie die maximale Anzahl der Tage zwischen Zugang und Abgang ohne Verschiebungsaktion angeben.       |
| **Menge reduzieren**        | Wenn Sie diese Meldung auswählen, sollten Produktionsaufträge, Bestellungen und anderen Zugangsbuchungen verringert werden, um Bestandsüberschüsse zu vermeiden.                                                                                                   |
| **Menge erhöhen**        | Wenn Sie diese Meldung auswählen, sollten Produktionsaufträge, Bestellungen und anderen Zugangsbuchungen erhöht werden, um Bestandknappheiten zu vermeiden.                                                                                                    |
| **Abgeleitete Aktivitäten** | Wenn Sie diese Meldung auswählen, werden Aktivitätsmeldungen für abgeleitete Anforderungen erstellt (beispielsweise für Komponentenbestellungen für die Produktion).                                                                                                   |




