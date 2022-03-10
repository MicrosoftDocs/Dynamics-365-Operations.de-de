---
title: Regeln deaktivieren, die im Prüfungsprozess für die Erfassungsbuchung verwendet werden
description: In diesem Thema werden die Funktionen zum Deaktivieren der Regeln zur Transaktionsprüfung in Microsoft Dynamics 365 Commerce beschrieben.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: cdaea51b4c84e6a62f0eb9412315ae77b4c11503
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919524"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Regeln deaktivieren, die im Prüfungsprozess für die Erfassungsbuchung verwendet werden

[!include [banner](../includes/banner.md)]

Einzelhändler können individuelle Geschäftsszenarien und -prozesse nutzen. Daher gelten nicht alle im Prüfungsprozess für die Erfassungsbuchung von Commerce-Transaktionen enthaltenen Regeln für alle Einzelhändler. Zur Anpassung von Unterschieden stellt Microsoft Dynamics 365 Commerce Funktionen zum Deaktivieren nicht anwendbarer Regeln bereit.

Um die Liste der Regeln anzuzeigen, die im Prüfungsprozess für die Erfassungsbuchung in Ihrer Umgebung verfügbar sind und um den Status der einzelnen Regeln anzuzeigen, gehen Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter**, und wählen Sie die Registerkarte **Transaktionsüberprüfung** aus. Alle aktivierten Regeln werden verwendet, um Transaktionen während des Prozesses **Geschäftsbuchungen überprüfen** zu prüfen, die bestanden werden müssen, damit Transaktionen gesammelt und in einer Transaktionsaufstellung gebucht werden.

Standardmäßig wird der Status jeder Regel auf **Aktiviert** gesetzt. Daher werden alle Regeln verwendet, um Einzelhandelstransaktionen zu prüfen, bevor sie in die Transaktionsaufstellungen übernommen werden können. Um eine Regel zu deaktivieren, ändern Sie ihren Status auf **Deaktiviert**. Deaktivierte Regeln werden nicht berücksichtigt, wenn Transaktionen während des Prozesses **Geschäftsbuchungen überprüfen** geprüft werden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
