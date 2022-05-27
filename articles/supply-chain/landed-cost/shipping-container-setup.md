---
title: Versandcontainer
description: In diesem Thema wird beschrieben, wie Sie Transportcontainer für das Modul Gesamttransportkosten festlegen.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 96710cf2b5a2e39f9492aadb0ba6f3241f0666f4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690553"
---
# <a name="shipping-container-setup"></a>Einrichten von Transportcontainern

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Transportcontainer für das Modul **Gesamttransportkosten** festlegen.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Transportcontainer-Typen festlegen

Die Transportcontainer-Typen definieren die Arten von Transportcontainern, die für die Verwendung bei Schifffahrten und Fahrten zur Verfügung stehen.

Um mit den Transportcontainer-Typen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Container einrichten \> Transportcontainer-Typen**. Dort können Sie Datensätze für Ihre Containertypen anzeigen, hinzufügen und entfernen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Versandcontainertyp | Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Transportcontainer-Typ ein. |
| Beschreibung | Geben Sie eine Beschreibung für den Transportcontainer-Typ ein. |
| Volumen | Geben Sie das maximale Volumen ein, das in Transportcontainern dieses Typs erlaubt ist. |
| Gewicht | Geben Sie das maximale Gewicht ein, das in Transportcontainern dieses Typs zulässig ist. |
| Retourfähig | Geben Sie an, ob Transportcontainer dieses Typs an den Lieferanten zurückgegeben werden können, nachdem sie während einer Fahrt benutzt wurden. Wenn diese Option auf *Ja* festgelegt ist, können zusätzliche Kosten für die Rückgabe von Transportcontainern dieses Typs an den Hafen anfallen. |

## <a name="set-up-shipping-containers"></a>Festlegen von Transportcontainern

Sie verwenden Transportcontainer-Datensätze, um jeden Container zu identifizieren, den Sie auf Fahrten verwenden. Wenn Sie eine Fahrt erstellen, können Sie in der Liste aller Transportcontainer-Datensätze, die Sie hier definiert haben, einen bestimmten Container für diese Fahrt auswählen. Diese Funktion ist besonders nützlich, wenn Ihre Firma eigene Transportcontainer besitzt.

Sie müssen keine Transportcontainernummern für Transportcontainer eingeben, die nur einmalig verwendet werden sollen. Stattdessen können Sie die Transportcontainer-Nummer hinzufügen, wenn Sie eine Fahrt erstellen.

Transportcontainer-Datensätze werden nur in den Gesamttransportkosten verwendet. Sie sind nicht im Standardmodul **Transportverwaltung** (TMS) verfügbar.

Um mit Transportcontainern zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Container einrichten \> Transportcontainer**. Dort können Sie Datensätze Ihrer Transportcontainer anzeigen, hinzufügen und entfernen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Versandcontainer | Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Transportcontainer ein. |
| Versandcontainertyp | Wählen Sie den Typ des Transportcontainers. Weitere Informationen finden Sie im Abschnitt [Versandcontainer-Typen festlegen](#shipping-container-types) weiter oben in diesem Thema. |

> [!NOTE]
> - Das Einrichten des Transportcontainers ist optional. Normalerweise werden Sie sie nur verwenden, wenn Ihre Firma eigene Transportcontainer besitzt oder häufig dieselben Transportcontainer wiederverwendet.
> - Für Transportcontainer-Nummern werden keine Prüfziffern berechnet.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Einheitstypen festlegen

Einheitstypen legen zusätzliche Gruppierungen und Identifikationsmethoden für Transportcontainer fest. Die Art der Einheit wird typischerweise verwendet, um die Art des Behälters zu identifizieren, in dem Waren verpackt sind, wie z. B. Paletten oder Fässer. Sie können einen Einheitstyp auswählen, wenn Sie einen Container auf der Seite **Alle Transportcontainer** festlegen.

Einheitentypen werden nur in Gesamttransportkosten kalkuliert. Sie sind in TMS nicht verfügbar.

Um mit Einheitentypen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Container einrichten \> Einheitentypen**. Dort können Sie Datensätze für Ihre Einheitentypen anzeigen, hinzufügen und entfernen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Einheitstyp | Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Einheitentyp ein. |
| Beschreibung | Geben Sie eine Beschreibung für den Einheitentyp ein. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Kältetypen festlegen

Kühltypen legen zusätzliche Gruppierungen und Identifikationsmethoden für Transportcontainer (in der Regel Kühlcontainer) fest. Sie können einen Kühltyp auswählen, wenn Sie einen Transportcontainer auf der Seite **Alle Transportcontainer** festlegen.

Um mit Kühltypen zu arbeiten, gehen Sie auf die Seite **Gesamttransportkosten \> Container einrichten \> Kühltypen**. Dort können Sie Datensätze für Ihre Kühltypen anzeigen, hinzufügen und entfernen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Kühlungsart | Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Kühltyp ein. |
| Beschreibung | Geben Sie eine Beschreibung des Kühlschranktyps ein. |
