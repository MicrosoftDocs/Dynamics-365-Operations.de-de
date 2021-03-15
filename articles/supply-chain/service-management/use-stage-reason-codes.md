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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4acba8f723ceb3d629671833db59c97a900c9f01
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965704"
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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]