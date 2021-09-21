---
title: Menge nicht für Kommissionierarbeiten mit mehreren LPs gültig
description: Bei Entnahmearbeiten mit mehreren Ladungsträgern an einem Lagerplatz, ist die Menge für Einheit ea nicht gültig. Überprüfen Sie, ob die folgenden Felder korrekt sind.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476403"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Ungültige Menge bei Entnahmearbeiten mit mehreren LPs an einem Standort

## <a name="symptoms"></a>Symptome

Bei Entnahmearbeiten mit mehreren Ladungsträgern an einem Lagerplatz, ist die Menge für Einheit *ea* nicht gültig und Sie erhalten die folgende Fehlermeldung.

> Die Menge ist für Einheit 1% ungültig.

## <a name="resolution"></a>Lösung

Stellen Sie sicher, dass die Felder **Einheit Sequenz Gruppen-ID** und **Einheit Umrechnungen** auf dem freigegebenen Produkt oder der Produktvariante korrekt festgelegt sind.

Beachten Sie, dass die Fehlermeldung in Version 10.0.15 verbessert wurde, um die erwartete Menge anzuzeigen (siehe [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Die neue Fehlermeldung lautet:

> Die Menge ist ungültig. Erwartet wird %1 %2.
