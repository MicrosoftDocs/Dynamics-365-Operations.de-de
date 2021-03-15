---
title: Teillieferung einer Transportladung
description: In diesem Thema wird erläutert, wie Sie eine Ladung teilweise liefern können und die Planung der Kapazität für die Ladung verschieben können.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 68a3d175e89e89d0909b140863b1aa61a184fce6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963284"
---
# <a name="partial-shipment-of-a-transport-load"></a>Teillieferung einer Transportladung

[!include[banner](../includes/banner.md)]

Durch Einrichten einer Teillieferung von Ladungen können Sie Ladungen handhaben, wo die Kapazität nicht bestimmt werden kann, bis alle Verkaufspositionen zu einer Ladung hinzugefügt wurden. Der Prozess kann dann abgeschlossen werden, wenn die genaue Palettenanzahl bekannt ist. Daher müssen Sie nicht entscheiden, welche Paletten welchem Transport zugewiesen werden, bis zum Augenblick, an dem der Transport physisch aus dem bereitgestellten Bestand geladen wird.

Diese Funktion bietet eine Alternative zur Durchführung einer steiferen Struktur, in der Sie bestimmen müssen, welche Paletten welchem Transport zugewiesen werden, bevor die Entnahmearbeit und Ladearbeit erstellt werden kann. Stattdessen können Benutzer Einzellasten für eine Teillieferungsbestätigung konfigurieren. Die Transportladeprozesse für diese Ladungen können dann erfolgen. Daher kann die Transportplanungsabteilung Ladungen planen, ohne die Kapazität einzelner Transporte berücksichtigen zu müssen.

Zum Zeitpunkt des Ladens können Arbeitskräfte eine neue Transportladung definieren, zu der eine Palette geladen werden kann. Alternativ können sie eine vorhandene Transportladung identifizieren. Diese Daten können über ein mobiles Gerät erfasst werden. Daher können mehrere Lagerarbeitskräfte Lagerbestand aus denselben Ladungen oder verschiedenen Ladungen auf denselben LKW laden. Die Ladungen können dann vollständig oder teilweise geliefert werden.

> [!NOTE] 
> Um Lagerbestand aus einer Ladung in eine bestimmte Transportladung zu laden und die Ladung teilweise zu liefern, muss Arbeit generiert werden, indem eine Ladungsklasse in einer Arbeitsvorlage verwendet wird. Gewöhnliche Entnahmearbeit des Typs **Entnahme** kann nicht in eine Transportladung, wie einen LKW, geladen werden.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Transportladungen für Teillieferung einrichten

Die Einrichtung für die Teillieferung von Ladungen besteht aus den folgenden zwei Prozeduren.

### <a name="set-the-loading-strategy"></a>Die Ladestrategie festlegen

Sie müssen die Teilladung aktivieren, indem Sie die Ladestrategie festlegen. Sie können die Ladenstrategie festlegen, nachdem Sie eine Ladung erstellt haben.

1. Wählen Sie **Lagerortverwaltung** \> **Ladungen** \> **Alle Ladungen** aus.
2. Wählen Sie eine Ladung aus, und klicken Sie dann auf **Kopfzeile**.
3. Wählen Sie im Feld **Ladungsstrategie** die Option **Teilladungslieferung zulässig** aus.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Erstellen Sie eine Menüoption für das Laden von Transportladungen

Sie müssen eine neue Menüoption erstellen, mit der Transportladungen geladen werden können. Mithilfe einer Transportladung können Sie Arbeitspositionen aus einer Ladung oder mehreren Ladungen gruppieren. Alles, was zur Transportladung hinzugefügt wird, kann dann mithilfe eines mobilen Scanners versendet werden.

1. Wählen Sie **Lagerortverwaltung** \> **Setup** \> **Mobiles Gerät** \> **Menüoptionen für mobiles Gerät** aus.
2. Wählen Sie **Neu** aus und anschließend im Feld **Modus** die Option **Arbeit**.
3. Legen Sie die **Vorhandene Arbeit verwenden**-Option mit **Ja** fest.
4. Wählen Sie auf der Registerkarte **Allgemein** im Feld **Angewiesen von** die Option **Transportverladung** aus.
5. Um die Lieferbestätigung auf einem mobilen Scanner zu aktivieren, wählen Sie im Feld **Zulässiger Lieferbestätigungstyp** die Option **Transportladung** aus.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Bestätigen der Lieferung einer Transportladung vom Client aus

Mit dieser Einstellung können Sie bestätigen, dass eine Transportladung, die eine vollständige Ladung oder eine teilweise geladene Ladung enthält, geliefert wird.

1. Wählen Sie **Lagerortverwaltung** \> **Ladungen** \> **Transportladungen** aus.
2. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Liefern und empfangen** in der Gruppe **Bestätigen** die Option **Transport** aus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]