---
title: Intercompany-Preise und -Rabatte synchronisieren
description: In diesem Thema wird die Synchronisierung von Preisen und Rabatten für Intercompany-Aufträge und -Bestellungen erläutert.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a9467e8d06a44cfaab9e3c8ea3944675c3eb8fb5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548276"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Intercompany-Preise und -Rabatte synchronisieren

[!include [banner](../../includes/banner.md)]

Rabatte und Preise werden zwischen dem Intercompany-Auftrag und der Intercompany-Bestellung immer synchronisiert. Sie können auch die Preise und Rabatte mit dem Originalauftrag synchronisieren, sodass alle Aufträge die gleichen Preise und Rabatte aufweisen. Dies erfolgt auf der Seite **Intercompany**, die über die Registerkarte **Allgemein** auf der Seite mit der Liste **Alle Debitoren** entweder über **Verkauf und Marketing** oder über **Beschaffung** aufgerufen wird.

Das Feld **Preis und Rabatt** wird mit der Intercompany-Auftragsposition synchronisiert. Dies bedeutet, dass Sie mit der Auswahl der Felder **Preisbearbeitung zulassen** field and the **Rabattbearbeitung zulassen** eine Änderung zwischen Intercompany-Auftrag und Intercompany-Bestellung zulassen. Mit einer Änderung des Einheitenpreises, der Preiseinheit oder der Belastungen für einen Intercompany-Auftrag legen Sie den Preis in der Intercompany-Bestellposition fest.

Wenn die Felder **Preisbearbeitung zulassen** und **Rabattbearbeitung zulassen** im Intercompany-Auftrag bzw. in der Intercompany-Bestellung aktiviert sind, können Sie manuelle Änderungen am Preis oder am Rabatt vornehmen. Andernfalls ist dies nicht möglich.

Wenn die Felder **Preisbearbeitung zulassen** und **Rabattbearbeitung zulassen** im Intercompany-Auftrag nicht aktiviert sind, können Sie im Intercompany-Auftrag keine manuellen Änderungen am Preis (oder an den Gebühren) bzw. am Rabatt vornehmen.

Wenn die Felder **Preisbearbeitung zulassen** und **Rabattbearbeitung zulassen** in der Intercompany-Bestellung nicht aktiviert sind, können Sie in der Intercompany-Bestellung keine manuellen Änderungen am Preis (oder an den Gebühren) bzw. am Rabatt vornehmen.

Wenn die Felder **Preisbearbeitung zulassen** und **Rabattbearbeitung zulassen** sowohl in der Intercompany-Bestellung als auch im Intercompany-Auftrag aktiviert sind, können Sie manuelle Änderungen an der Bestellung und am Auftrag vornehmen. Dies kann jedoch zu einer Situation führen, in der von einer Person vorgenommene Aktualisierungen von Aktualisierungen überschrieben werden, die eine andere Person in einem anderen Unternehmen an der Bestellung bzw. am Auftrag vornimmt.

> [!NOTE]
> Ist das Feld **Preis und Rabatt** sowohl in der Intercompany-Bestellung als auch im Intercompany-Auftrag aktiviert, haben Sie keine Kontrolle über die Preisgestaltung.

Um derartige Konflikte zu vermeiden, empfiehlt es sich, Änderungen an Preisen und Rabatten nur im Intercompany-Auftrag oder in der Intercompany-Bestellung zuzulassen. Zu diesem Zweck werden die Felder **Preisbearbeitung zulassen** und **Rabattbearbeitung zulassen** entweder im Auftrag oder in der Bestellung aktiviert.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
