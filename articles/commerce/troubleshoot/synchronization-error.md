---
title: Fehler bei der Auftragssynchronisierung im Zusammenhang mit dem Standardzahlungsservice
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, mit deren Hilfe ein Fehler behoben werden kann, der bei der Synchronisierung eines Onlineauftrags auftreten kann.
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021126"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Fehler bei der Auftragssynchronisierung im Zusammenhang mit dem Standardzahlungsservice

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Fehlerbehebung, mit deren Hilfe ein Fehler behoben werden kann, der bei der Synchronisierung eines Onlineauftrags auftreten kann.

## <a name="description"></a>Beschreibung

Wenn Sie einen Onlineauftrag synchronisieren, wird die folgende Fehlermeldung angezeigt: „Für die Verarbeitung von Kreditkartentransaktionen muss ein Standardzahlungsservice vorhanden sein.“

![„Fehlender Standardzahlungsservice“-Fehler](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Lösung

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Standardzahlungsservice in der Commerce-Zentralverwaltung bestätigen oder festlegen

Befolgen Sie diese Schritte, um den Standardzahlungsservice in der Commerce-Zentralverwaltung zu bestätigen oder festzulegen.

1. Rufen Sie **Debitorenkonten \> Zahlungseinstellungen \> Zahlungsdienste** auf.
1. Vergewissern Sie sich, dass für einen Zahlungsdienst die Option **Standardmäßige Verarbeitungsstelle für neue Kreditkarten** auf **Ja** gesetzt ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichten, Genehmigen und Erfassen von Kreditkarten](../../finance/accounts-receivable/credit-card-authorizations.md)