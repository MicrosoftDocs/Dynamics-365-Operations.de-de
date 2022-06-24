---
title: Auf der Kreditkarten-Eingabeseite wird beim Auschecken ein Fehler angezeigt
description: Dieser Artikel enthält Anleitungen zur Problembehandlung, die hilfreich sein können, wenn der Abschnitt zur Zahlungsmethode nicht geladen wird und eine Fehlermeldung angezeigt wird.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 6d1f7ba2d1a63430431af94ed4bed3222c85f14d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910442"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Auf der Kreditkarten-Eingabeseite wird beim Auschecken ein Fehler angezeigt

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Anleitungen zur Problembehandlung, die hilfreich sein können, wenn der Abschnitt **Zahlungsmethode** nicht geladen wird und eine Fehlermeldung angezeigt wird.

## <a name="description"></a>Beschreibung

Wenn Sie die Checkout-Seite eines Onlineshops öffnen, wird der Abschnitt **Zahlungsmethode** nicht geladen und die folgende Fehlermeldung wird angezeigt: „Es ist ein Fehler aufgetreten. Bitte versuchen Sie es später erneut.“

![Zahlungsmodulfehler.](media/payment-module-error.jpg)

## <a name="resolution"></a>Lösung

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Warten, bis der Commerce Scale Unit-Cache abgelaufen ist

Die Einstellungen für den Zahlungsdienst auf der Checkout-Seite des Onlineshops werden in der Commerce Scale Unit zwischengespeichert und können bis zu 15 Minuten brauchen, bis sie auf der E-Commerce-Website angezeigt werden. Diese Zahlungsdiensteinstellungen umfassen Änderungen an der Händlerkonto-ID, dem Cloud-API-Schlüssel und verschiedenen Konfigurationseinstellungen, die sich auf die Zahlungsmethode beziehen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einen Onlinechannel einrichten](../channel-setup-online.md)
