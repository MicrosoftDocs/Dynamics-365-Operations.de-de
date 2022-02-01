---
title: Zahlungsbetragstypen hinzufügen
description: In diesem Thema wird erläutert, wie Sie Zahlungsbetragstypen im Anlageleasing einrichten.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 037afa458277a3a07bcb937c6ec4d961d0dd5ca9
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968322"
---
# <a name="add-payment-amount-types"></a>Zahlungsbetragstypen hinzufügen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Zahlungsbetragstypen im Anlageleasing einrichten. Auf diese Weise können Sie den Leasingzahlungsbetrag einzeln aufführen, statt den Pauschalbetrag in den Zahlungsplanzeilen hinzuzufügen.

Gehen Sie folgendermaßen vor, um Zahlungsbetragstypen hinzuzufügen.

1. Wechseln Sie zu **Anlagenleasing \> Einstellungen \> Zahlungsbetragstypen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie der neue Zahlungstyp und eine Beschreibung ein.

> [!NOTE]
> Für die Indexneubewertung nach IFRS 16 müssen Sie ein Zahlungsbetragstyp erstellen und als **Wird für die Neubewertung des IRFS 16-Index verwendet** markieren. Dieser Zahlungsbetragstyp wird verwendet, wenn der Indexneubewertungsprozess gegen das IFRS 16-Buch ausgeführt wird, und berücksichtigt die Änderungen, die aufgrund des Indexneubewertungsprozesses aufgetreten sind.
>
> Wenn die **Zahlungsaufschlüsselung**-Option im Mietvertrag auf **Ja** festgelegt ist, wenn die Indexneubewertung für IFRS 16 ausgeführt wird, aber kein Zahlungstyp für IFRS 16 vorhanden ist, wird der Prozess nicht abgeschlossen.

Nur ein Datensatz kann als **Wird für die Neubewertung des IFRS 16-Index verwendet** gekennzeichnet werden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
