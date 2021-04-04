---
title: Auf der Kreditkarten-Eingabeseite wird beim Auschecken ein Fehler angezeigt
description: Dieses Thema enthält Anleitungen zur Problembehandlung, die hilfreich sein können, wenn der Abschnitt zur Zahlungsmethode nicht geladen wird und eine Fehlermeldung angezeigt wird.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585334"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Auf der Kreditkarten-Eingabeseite wird beim Auschecken ein Fehler angezeigt

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Problembehandlung, die hilfreich sein können, wenn der Abschnitt **Zahlungsmethode** nicht geladen wird und eine Fehlermeldung angezeigt wird.

## <a name="description"></a>Beschreibung

Wenn Sie die Checkout-Seite eines Onlineshops öffnen, wird der Abschnitt **Zahlungsmethode** nicht geladen und die folgende Fehlermeldung wird angezeigt: „Es ist ein Fehler aufgetreten. Bitte versuchen Sie es später erneut.“

![Zahlungsmodulfehler](media/payment-module-error.jpg)

## <a name="resolution"></a>Lösung

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Warten, bis der Commerce Scale Unit-Cache abgelaufen ist

Die Einstellungen für den Zahlungsdienst auf der Checkout-Seite des Onlineshops werden in der Commerce Scale Unit zwischengespeichert und können bis zu 15 Minuten brauchen, bis sie auf der E-Commerce-Website angezeigt werden. Diese Zahlungsdiensteinstellungen umfassen Änderungen an der Händlerkonto-ID, dem Cloud-API-Schlüssel und verschiedenen Konfigurationseinstellungen, die sich auf die Zahlungsmethode beziehen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einen Onlinechannel einrichten](../channel-setup-online.md)
