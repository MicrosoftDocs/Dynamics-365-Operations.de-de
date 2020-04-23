---
title: Verwenden von Phasenursachencodes
description: Ursachencodes dienen zum Angeben der Ursache für die Stornierung einer Vereinbarung zum Servicelevel (Service Level Agreement, SLA) oder für die Überschreitung des durch eine Vereinbarung zum Servicelevel angegebenen Zeitlimits.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54dae6edb6681e1ba29709ebeeea2e5094262257
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206472"
---
# <a name="use-stage-reason-codes"></a>Verwenden von Phasenursachencodes 

[!include [banner](../includes/banner.md)]


Ursachencodes dienen zum Angeben der Ursache für die Stornierung einer Vereinbarung zum Servicelevel (Service Level Agreement, SLA) oder für die Überschreitung des durch eine Vereinbarung zum Servicelevel angegebenen Zeitlimits.

Sie können auch angeben, dass ein Ursachencode erforderlich ist, wenn eine Vereinbarung zum Servicelevel storniert wird oder wenn das Zeitlimit die Zeit überschreitet, die in der Vereinbarung zum Servicelevel für den Serviceauftrag angegeben ist.

Wenn Sie angegeben haben, dass ein Ursachencode erforderlich ist, müssen Sie einen Ursachencode in folgenden Situationen eingeben:

  - Wenn ein Serviceauftrag in eine Phase eintritt, in der keine SLA-Zeitaufzeichnung für den Serviceauftrag mehr stattfindet.

  - Der Serviceauftrag wird abgezeichnet.

  - Wenn die Zeitaufzeichnung manuell beendet wird.

## <a name="set-up-reason-codes"></a>Ursachencodes einrichten

1.  Klicken auf **Serviceverwaltung** \> **Einrichtung** \> **Serviceaufträge** \> **Phasenursachencodes**.

2.  Klicken Sie im Formular **Phasenursachencodes** auf **Neu**, um einen neuen Phasenursachencode zu erstellen.

3.  Geben Sie im Feld **Phasenursachencodes** einen eindeutigen Phasenursachencode ein.

4.  Geben Sie im Feld **Beschreibung** eine Beschreibung für den Phasenursachencode ein.

5.  Schließen Sie das Formular, um Ihre Änderungen zu speichern.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Erzwingen von Ursachencodes beim Stornieren einer Vereinbarung zum Servicelevel

1.  Klicken Sie auf **Serviceverwaltung** \> **Einrichtung** \> **Serviceverwaltungsparameter**.

2.  In der **Serviceverwaltungsparameter** Formular klicken Sie auf den Link **Allgemein**, und aktivieren Sie dann das Kontrollkästchen **Ursachencode bei Storno**.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Verlangen Sie Ursachencodes bei Überschreitung des in der Vereinbarung zum Servicelevel angegebenen Zeitlimits

1.  Klicken Sie auf **Serviceverwaltung** \> **Einrichtung** \> **Serviceverwaltungsparameter**.

2.  In der **Serviceverwaltungsparameter** Formular klicken Sie auf den Link **Allgemein**, und aktivieren Sie dann das Kontrollkästchen **Ursachencode bei Zeitüberschreitung**.

## <a name="see-also"></a>Siehe auch

[Starten und Beenden der Zeitaufzeichnung für einen Serviceauftrag](start-and-stop-time-recording-on-a-service-order.md)

  


