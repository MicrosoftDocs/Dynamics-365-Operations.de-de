---
title: Clusterprofil kann nicht gefunden werden
description: Wenn Sie mit eingehenden Lagerortvorgängen arbeiten, erhalten Sie möglicherweise die Fehlermeldung, dass das Clusterprofil nicht gefunden werden kann. Stellen Sie sicher, dass Clusterprofile richtig eingerichtet sind.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bbf9c5bc70c8f3ba1fa26db425249e65e82c0518
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476488"
---
# <a name="cluster-profile-cant-be-found"></a>Clusterprofil kann nicht gefunden werden

## <a name="symptoms"></a>Symptome

Bei der Arbeit mit eingehenden Lagerortvorgängen erhalten Sie möglicherweise die folgende Fehlermeldung:

> „Qualitätsprüfungsauftrag %1 wurde generiert. Clusterprofil kann nicht gefunden werden. Bitte überprüfen Sie Ihre Konfiguration.“

Diese Fehlermeldung bezieht sich auf einen Eingangsvorgang, bei dem das Qualitätsmanagement (QMS) eingeschaltet ist. Abhängig von den Konfigurationen in Ihrer Umgebung können zusätzliche Details über die Transaktion, die die Fehlermeldung erzeugt, helfen, das Problem zu beheben.

## <a name="resolution"></a>Lösung

Überprüfen Sie zunächst die Clusterkommissionierung und stellen Sie sicher, dass Ihre Clusterprofile richtig eingerichtet sind. Sie können kein Menüelement für die Cluster-Kommissionierung auf einem mobilen Gerät verwenden, wenn keine Cluster-Profile festgelegt sind. Abhängig von Ihrer Umgebung müssen Sie möglicherweise auch andere zugehörige Konfigurationen überprüfen.
