---
title: Intercompany-Handel einrichten
description: In diesem Thema wird erläutert, wie Sie Intercompany-Handel einrichten.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5080267568f4d0626d2c727efb533295e7d8e397
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669390"
---
# <a name="set-up-intercompany-trade"></a>Intercompany-Handel einrichten

[!include [banner](../../includes/banner.md)]

Zur Verwendung der Intercompany-Funktionen in Microsoft Dynamics 365 Supply Chain Management ist zunächst die entsprechende Einrichtung der Debitoren und Kreditoren erforderlich. Sie müssen Kreditoren, Debitoren, Beschaffung sowie Vertrieb und Marketing einrichten.

## <a name="before-you-set-up-intercompany-trade"></a>Vor dem Einrichten der Intercompany-Funktionen

Bevor Sie den Intercompany-Handel einrichten, müssen Sie entscheiden, welche Debitoren als Intercompany-Debitoren und welche Kreditoren als Intercompany-Kreditoren fungieren. Für jede juristische Person in Microsoft Dynamics 365 Supply Chain Management müssen Sie entscheiden, welche Intercompany-Handelsrichtlinie für einen bestimmten Intercompany-Debitor oder Kreditor gelten soll.

Insbesondere wird empfohlen, dass Sie und Ihre Organisation sich mit den Intercompany-Parametern vertraut machen.

- besprechen Sie die Auswirkungen der Einstellungen mit Managern, die für den Intercompany-Handel in jeder juristischen Person zuständig sind.
- Richten Sie die entsprechenden Werte für jede juristische Person ein.

## <a name="set-up-trading-relations"></a>Handelsbeziehungen einrichten

Gehen Sie wie folgt vor, um den Intercompany-Handel für Debitoren und Kreditoren einzurichten.

1. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.
1. Dient zum Auswählen eines Debitorenkontos.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Allgemein**, und wählen Sie **Intercompany** aus.
1. Geben Sie Intercompany-Einstellungsparameter für das Debitorenkonto an. Diese Parameter betreffen die juristische Person, die den entsprechenden Kreditor und das Kreditorenkonto enthält. Die Parameter enthalten auch die Bestellungsrichtlinien, die Auftragsrichtlinien, die Wertzuordnung und Richtlinien für Rahmenbestellungen und Kaufverträge. Darüber hinaus geben Sie an, ob Stammdatenwerte vom Debitorenkonto oder vom Kreditorenkonto in der anderen juristischen Person verwendet werden.
1. Wiederholen Sie die Schritte 1 bis 4 für die übrigen Intercompany-Debitoren in der juristischen Person.
1. Gehen Sie zu **Kreditorenkonten \> Kreditoren \> Alle Kreditoren**.
1. Wählen Sie ein Kreditorenkonto aus.
1. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Allgemein**, und wählen Sie **Intercompany** aus.
1. Geben Sie Intercompany-Einstellungsparameter für das Kreditorenkonto an. Diese Parameter betreffen die juristische Person, die den entsprechenden Debitor und das Debitorenkonto enthält. Die Parameter enthalten auch die Auftragsrichtlinien, die Bestellungsrichtlinien, die Wertzuordnung und Richtlinien für Rahmenbestellungen und Kaufverträge. Darüber hinaus geben Sie an, ob Stammdatenwerte vom Kreditorenkonto oder vom Debitorenkonto in der anderen juristischen Person verwendet werden.
1. Wiederholen Sie die Schritte 6 bis 9 für die übrigen Intercompany-Kreditoren in der juristischen Person.

## <a name="set-up-products"></a>Produkte einrichten

Gehen Sie wie folgt vor, um den Intercompany-Handel für Debitoren und Kreditoren einzurichten.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Alle Produkte und Produktmaster**.
1. Definieren Sie die Produkte, die für die juristischen Personen freigegeben werden, in denen der Intercompany-Handel abgewickelt werden soll.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
