---
title: Ein Fehler aufgrund eines ungültigen Kennzeichens oder Standorts ist in der mobilen App aufgetreten
description: Wenn Sie eine Kennzeichen-ID oder einen Lagerplatz scannen, erhalten Sie möglicherweise eine Fehlermeldung, dass dies ungültig ist. Stellen Sie sicher, dass die Ladungsträger-ID nicht durch etwas anderes reserviert ist.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f9f10dbade0d13b8fc4b0fc92981d84e6e28e83e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476495"
---
# <a name="invalid-license-plate-or-location-error-when-scanning-in-the-mobile-app"></a>Ein Fehler aufgrund eines ungültigen Kennzeichens oder Standorts ist beim Scannen in der mobilen App aufgetreten.

## <a name="symptoms"></a>Symptome

Wenn Sie eine Kennzeichen-ID oder einen Lagerplatz scannen, erhalten Sie möglicherweise die folgende Fehlermeldung:

> Der Ladungsträger oder der Lagerplatz ist ungültig.

## <a name="resolution"></a>Lösung

Stellen Sie sicher, dass die Ladungsträger-ID nicht durch etwas anderes reserviert ist. Dieses Problem trat früher auf, wenn der Wert, den ein Benutzer in der Warehouse Management Mobile App gescannt hat, sowohl ein gültiger Lagerplatz als auch eine gültige Ladungsträger-ID war. Dieses Problem wurde jedoch in Version 10.0.11 behoben.
