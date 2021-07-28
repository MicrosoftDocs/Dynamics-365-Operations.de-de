---
title: Die Rückerstattung einer Rücklieferung wird abgelehnt
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Rückerstattung für eine Rücklieferung abgelehnt wird, da sich die für die Fakturierung verwendete Kreditkarte von der Karte unterscheidet, die während der ursprünglichen Zahlungsautorisierung verwendet wurde.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 89fe41d7ce57b584be34b156696b4044c4571afe
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347271"
---
# <a name="refund-on-a-return-order-is-declined"></a>Die Rückerstattung einer Rücklieferung wird abgelehnt

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Rückerstattung für eine Rücklieferung abgelehnt wird, da sich die für die Fakturierung verwendete Kreditkarte von der Karte unterscheidet, die während der ursprünglichen Zahlungsautorisierung verwendet wurde.

## <a name="description"></a>Beschreibung

Eine Rückerstattung wird abgelehnt, wenn die Kreditkarte, mit der eine Rücklieferung fakturiert wird, von der Karte abweicht, die während der ursprünglichen Zahlungsautorisierung verwendet wurde. Sie erhalten die folgende Fehlermeldung: „Einige Zahlungen haben nicht den richtigen Status für die Buchung. Bitte überprüfen Sie den Status aller Zahlungen vor der Fakturierung erneut.“

Die Details der Zahlungsautorisierung enthalten folgende Fehlermeldung: „Adyen-Gateway SendRequest() ist mit dem Status 'InternalServerError'.22144 fehlgeschlagen; leere Antwort von Adyen zurückgegeben.(22001);“

![Abgelehnte Rückerstattung einer Rücklieferung – Fehler.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Lösung

### <a name="enable-blind-returns-in-adyen"></a>Blindretouren in Adyen aktivieren

Befolgen Sie die Schritte in [Problembehandlung beim Zahlungskonnektor von Dynamics 365 für Adyen](adyen-support.md). Wenden Sie sich an das Adyen-Supportteam, und fordern Sie an, dass Blindretouren in Ihrem Adyen-Händlerkonto aktiviert werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Zahlungskonnektor von Dynamics 365 für Adyen](../dev-itpro/adyen-connector.md)

[Adyen-Zahlungskonnektor für Dynamics 365 einrichten](https://docs.adyen.com/plugins/microsoft-dynamics)
