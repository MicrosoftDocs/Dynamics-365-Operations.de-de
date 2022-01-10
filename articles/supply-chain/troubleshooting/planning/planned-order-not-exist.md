---
title: Das System kann bei Vorgängen zu mehreren Aufträgen keinen geplanten Auftrag finden
description: Der Fehler „Geplanter Auftrag existiert nicht“ tritt auf, wenn Sie Vorgänge für mehrere geplante Aufträge durchführen und mindestens zwei Aufträge zur gleichen Element-ID gehören.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920803"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Das System kann bei Vorgängen zu mehreren Aufträgen keinen geplanten Auftrag finden

Fehlercode: SYS24774

## <a name="symptoms"></a>Symptome

Sie erhalten die folgende Fehlermeldung, wenn Sie versuchen, einen Vorgang für mehrere geplante Aufträge gleichzeitig durchzuführen, und mindestens zwei der Aufträge zur gleichen Artikel-ID gehören. Der Fehler kann zum Beispiel auftreten, wenn die Aufträge umgewandelt oder ihre Auftragsart geändert wird.

> Der Auftragsvorschlag '%1' ist nicht vorhanden.

## <a name="cause"></a>Ursache

Wenn das System einen Auftrag fixiert oder die Art des Auftrags ändert, muss es die bestehenden geplanter Aufträge für das Element erneut prüfen, um sicherzustellen, dass der geplante Vorrat mit dem Bedarf und dem vorhandenen Angebot übereinstimmt. Als Teil dieses Prozesses erstellt das System geplanter Aufträge für den Artikel neu. Der zweite geplanter Auftrag, den das System zu verarbeiten erwartet, existiert also nicht mehr.

## <a name="workaround"></a>Problemumgehung

Genehmigen Sie die Aufträge, bevor Sie sie verarbeiten. Auf diese Weise werden die Bestellungen nicht gelöscht, wenn das System die erste Bestellung für das Element verarbeitet.
