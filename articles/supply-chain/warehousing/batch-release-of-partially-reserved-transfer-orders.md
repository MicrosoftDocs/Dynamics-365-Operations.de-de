---
title: "Chargenfreigabe von teilweise reservierten Umlagerungsaufträgen"
description: "In diesem Thema wird beschrieben, wie Sie die Optionen für teilweise reservierte Umlagerungsaufträge auf einem mobilen Gerät einrichten und anwenden."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4569ba5d24f84166254cfce86d9fe2cc9b98ac09
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Chargenfreigabe von teilweise reservierten Umlagerungsaufträgen

[!include[banner](../includes/banner.md)]

Die Funktionen für Chargenfreigabe von teilweise reservierten Umlagerungsaufträgen können Sie Umlagerungsaufträge teilweise einem Lagerort freigeben, indem eines Stapelverarbeitungsauftrags können.
Da Sie die Möglichkeit haben, eine Teilmenge freizugeben, müssen Sie nicht für die gesamte Auftragsmenge warten, die am Lagerort verfügbar ist, bevor ein Auftrag freigegeben wird.

Die Version von Aufträgen an einen Lagerort ist ein erweiterter Lagerortverwaltungsprozess. Dieser Prozess beinhaltet Aktivitäten wie Entnahme, Verpackung und Versand, die ein Lagerarbeiter ausführen kann, indem er ein mobiles Gerät verwendet.

## <a name="where-it-applies"></a>Wofür es angewendet wird

Für diese Funktion werden Umlagerungsaufträge einem Lagerort freigegeben, indem Sie einen Stapelverarbeitungsauftrag verwenden. Diese Funktionalität ist hilfreich, wenn Sie nicht genügend Bestand am Lagerort haben, aber dennoch Artikel aus einem Lagerort an einen anderen übertragen möchten.

## <a name="how-it-is-set-up"></a>Wie er installiert wird

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Geben Sie Erfüllungskriterien für Umlagerungsaufträge und Aufträge an

Bevor ein Auftrag einem Lagerort in einer Charge teilweise freigegeben werden kann, müssen die Erfüllungskriterien erfüllt werden. Diese Erfüllungskriterien werden durch die Erfüllungsrichtlinie bestimmt.

Erfüllungspolitische Richtlinien für Umlagerungsaufträge und Aufträge werden auf Unternehmensebene angegeben. Je nach den Einstellungen der Erfüllungsrichtlinie wird die Freisetzung von Aufträgen in einer Charge angenommen oder abgelehnt. Die Aufträge werden dann entsprechend verarbeitet.

-   Weitere Erfüllungspolitische Richtlinien für Aufträge und Umlagerungsaufträge klicken Sie auf **Lagerortverwaltung** \> **Einstellungen** \> **Freigebung Lagerort** \> **Erfüllungsrichtlinie**, und erstellen Sie dann eine Erfüllungsrichtlinie, indem Sie einen Namen und eine Beschreibung eingeben.

-   Um einen Erfüllungssatz anzugeben, legen Sie einen Werttyp und die Meldung fest, die angezeigt werden soll, wenn gegen die Erfüllungsrichtlinie verstoßen wird. Klicken Sie auf **Lagerortverwaltung** \> **Einstellungen** \> **Freigegebener Lagerort** \>  **Erfüllungsrichtlinie** und dann**Erfüllungssatz**, **Werttyp** und **Erfüllungsverstoßnachricht**.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Geben Sie Erfüllungskriterien für Umlagerungsaufträge und Aufträge an

-   Um die Erfüllungsrichtlinien für Umlagerungsaufträge festzulegen, klicken Sie auf **Lagerverwaltung** \> **Einstellungen** \> **Parameter für Lager- und Lagerortverwaltung** \> **Umlagerungsaufträge** \> **Lagerortverwaltung**, und wählen Sie dann eine Umlagerungsauftragserfüllungsrichtlinie aus.

-   Um die Erfüllungsrichtlinie für Aufträge einzurichten, klicken Sie auf **Debitoren** \> **Einstellungen** \> **Debitorenparameter** \> **Lagerortverwaltung**, und wählen Sie dann eine Auftragserfüllungsrichtlinie aus.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a>Friegabe in Stapelverarbeitung zulassen und die Menge definieren, die Freigabe in einem Stapel freigegeben werden soll

Ein Stapelverarbeitungsauftrag wird verwendet, um Aufträge in einer Stapelverarbeitung freizugeben. Die Parameter, die sich vom Auftrag unterscheiden, sollten in einer Stapelverarbeitung ausgeführt werden und auf Stapelverarbeitungsauftrag auch festgelegt werden.

Der Parameter **Menge** gibt an, ob die gesamte Menge oder die physisch reservierte Menge in der Charge verwendet werden sollen. Der Parameter **Teilweise Freisetzung von freigegebenen Aufträgen** bestimmt, ob Aufträge in der Charge übernommen oder abgelehnt werden sollen, wenn sie zuvor vollständig freigegeben wurden.

-   Wenn Sie die **Menge** und **Teilweise Freisetzung von Aufträgen ermöglichen** für Umlagerungsaufträge festlegen, klicken Sie auf**Lagerortverwaltung** \> **Freigebung Lagerort** \> **Automatische Freigabe der Umlagerungsaufträge**.

-   Wenn Sie die **Menge** und **Teilweise Freisetzung von Aufträgen ermöglichen** für Umlagerungsaufträge festlegen, klicken Sie auf**Lagerortverwaltung** \> **Freigebung Lagerort** \> **Automatische Freigabe der Umlagerungsaufträge**.

