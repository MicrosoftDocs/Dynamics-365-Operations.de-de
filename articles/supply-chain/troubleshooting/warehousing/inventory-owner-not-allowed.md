---
title: Bestandsbesitzer ist bei der Verarbeitung von Bewegungen nicht zulässig
description: Möglicherweise erhalten Sie die Fehlermeldung „Der Bestandsbesitzer %1 ist nicht zulässig“. Die Prozesse der Lagerortverwaltung unterstützen nur Bestände, die im Besitz der juristischen Person sind.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476420"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Bestandsbesitzer ist bei der Verarbeitung von Bewegungen in der Lagerort-App nicht zulässig.

## <a name="symptoms"></a>Symptome

Bei der Verarbeitung von Bewegungen in der mobilen Warehouse Management-App erhalten Sie möglicherweise die folgende Fehlermeldung:

> Der Bestandsbesitzer %1 ist in diesem Prozess nicht zulässig.

## <a name="cause"></a>Ursache

Der Grund hierfür ist, dass die Verfolgungsdimension **Besitzer** für die fehlt, wenn die mobile Warehouse Management-App verwendet wird, um Bewegungen durchzuführen. Eine reguläre Bestandsumlagerungserfassung aus dem Supply Chain Management Client scheint wie vorgesehen zu funktionieren und kann nur gebucht werden, wenn die Dimension **Besitzer** ausgefüllt ist.

## <a name="resolution"></a>Lösung

Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt. Derzeit unterstützen die Prozesse der Lagerortverwaltung nur Bestände, die im Besitz der juristischen Entität sind.
