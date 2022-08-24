---
title: Chargenfreigabe von teilweise reservierten Umlagerungsaufträgen
description: In diesem Artikel wird beschrieben, wie Sie die Optionen für teilweise reservierte Umlagerungsaufträge auf einem mobilen Gerät einrichten und anwenden.
author: perlynne
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 741377a43e2bfe702b213647cc6460a3d6ad93fb
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218681"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Chargenfreigabe von teilweise reservierten Umlagerungsaufträgen

[!include [banner](../includes/banner.md)]

Die Funktionen für Chargenfreigabe von teilweise reservierten Umlagerungsaufträgen können Sie Umlagerungsaufträge teilweise einem Lagerort freigeben, indem eines Stapelverarbeitungsauftrags können.
Da Sie die Möglichkeit haben, eine Teilmenge freizugeben, müssen Sie nicht für die gesamte Auftragsmenge warten, die am Lagerort verfügbar ist, bevor ein Auftrag freigegeben wird.

Die Freigabe von Bestellungen an ein Lager ist ein Prozess der Lagerverwaltung (WMS). Dieser Prozess beinhaltet Aktivitäten wie Entnahme, Verpackung und Versand, die ein Lagerarbeiter ausführen kann, indem er ein mobiles Gerät verwendet.

## <a name="where-it-applies"></a>Wofür es angewendet wird

Für diese Funktion werden Umlagerungsaufträge einem Lagerort freigegeben, indem Sie einen Stapelverarbeitungsauftrag verwenden. Diese Funktionalität ist hilfreich, wenn Sie nicht genügend Bestand am Lagerort haben, aber dennoch Artikel aus einem Lagerort an einen anderen übertragen möchten.

## <a name="how-it-is-set-up"></a>Wie er installiert wird

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Geben Sie Erfüllungskriterien für Umlagerungsaufträge und Aufträge an

Bevor ein Auftrag einem Lagerort in einer Charge teilweise freigegeben werden kann, müssen die Erfüllungskriterien erfüllt werden. Diese Erfüllungskriterien werden durch die Erfüllungsrichtlinie bestimmt.

Erfüllungspolitische Richtlinien für Umlagerungsaufträge und Aufträge werden auf Unternehmensebene angegeben. Je nach den Einstellungen der Erfüllungsrichtlinie wird die Freisetzung von Aufträgen in einer Charge angenommen oder abgelehnt. Die Aufträge werden dann entsprechend verarbeitet.

- Um Erfüllungsrichtlinien für Umlagerungsaufträge und Aufträge zu erstellen, gehen Sie zu **Lagerortverwaltung \> Einstellungen \> An Lagerort freigeben \> Erfüllungsrichtlinien** und erstellen Sie dann eine Erfüllungsrichtlinie, indem Sie einen Namen und eine Beschreibung eingeben.
- Um eine Erfüllungsrate anzugeben, legen Sie einen Werttyp und die Meldung fest, die angezeigt werden soll, wenn gegen die Erfüllungsrichtlinie verstoßen wird. Gehen Sie dazu zu **Lagerortverwaltung \> Einstellungen \> An Lagerort freigeben \> Erfüllungsrichtlinien** und legen Sie dann die Felder **Erfüllungsrate**, **Werttyp** und **Erfüllungsverstoßmeldung** fest.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Geben Sie Erfüllungskriterien für Umlagerungsaufträge und Aufträge an

- Um die Erfüllungsrichtlinien für Umlagerungsaufträge festzulegen, gehen sie zu **Lagerverwaltung \> Einstellungen \> Parameter für Lager- und Lagerortverwaltung** und wählen Sie dann auf der Registerkarte **Umlagerungsaufträge** im Abschnitt **Lagerortverwaltung** die Erfüllungsrichtlinie eines Umlagerungsauftrags aus.
- Um die Erfüllungsrichtlinie für Aufträge einzurichten, gehen Sie zu **Debitoren \> Einstellungen \> Debitorenparameter** und wählen Sie dann auf der Registerkarte **Lagerortverwaltung** eine Erfüllungsrichtlinie eines Auftrags aus.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-released-in-a-batch"></a>Freigabe in Stapelverarbeitung zulassen und die Menge definieren, die Freigabe in einem Stapel freigegeben werden soll

Ein Stapelverarbeitungsauftrag wird verwendet, um Aufträge in einer Stapelverarbeitung freizugeben. Die Parameter, die sich vom Auftrag unterscheiden, sollten in einer Stapelverarbeitung ausgeführt werden und auf Stapelverarbeitungsauftrag auch festgelegt werden.

Der Parameter **Menge** gibt an, ob die gesamte Menge oder die physisch reservierte Menge in der Charge verwendet werden sollen. Der Parameter **Teilweise Freisetzung von freigegebenen Aufträgen** bestimmt, ob Aufträge in der Charge übernommen oder abgelehnt werden sollen, wenn sie zuvor vollständig freigegeben wurden.

- Wenn Sie die Parameter **Menge** und **Teilweise Freisetzung von Aufträgen ermöglichen** für Umlagerungsaufträge festlegen, gehen Sie auf **Lagerortverwaltung \> An Lagerort freigeben \> Umlagerungsaufträge automatisch freigeben**.
- Wenn Sie die Parameter **Menge** und **Teilweise Freisetzung von Aufträgen ermöglichen** für Aufträge festlegen, gehen Sie auf **Lagerortverwaltung \> An Lagerort freigeben \> Aufträge automatisch freigeben**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
