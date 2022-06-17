---
title: Regeln deaktivieren, die im Prüfungsprozess für die Erfassungsbuchung verwendet werden
description: In diesem Artikel werden die Funktionen zum Deaktivieren der Regeln zur Transaktionsprüfung in Microsoft Dynamics 365 Commerce beschrieben.
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
ms.openlocfilehash: 7d566aa3b829dad281528925a341382f9637fdba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884875"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Regeln deaktivieren, die im Prüfungsprozess für die Erfassungsbuchung verwendet werden

[!include [banner](../includes/banner.md)]

Einzelhändler können individuelle Geschäftsszenarien und -prozesse nutzen. Daher gelten nicht alle im Prüfungsprozess für die Erfassungsbuchung von Commerce-Transaktionen enthaltenen Regeln für alle Einzelhändler. Zur Anpassung von Unterschieden stellt Microsoft Dynamics 365 Commerce Funktionen zum Deaktivieren nicht anwendbarer Regeln bereit.

Um die Liste der Regeln anzuzeigen, die im Prüfungsprozess für die Erfassungsbuchung in Ihrer Umgebung verfügbar sind und um den Status der einzelnen Regeln anzuzeigen, gehen Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter**, und wählen Sie die Registerkarte **Transaktionsüberprüfung** aus. Alle aktivierten Regeln werden verwendet, um Transaktionen während des Prozesses **Geschäftsbuchungen überprüfen** zu prüfen, die bestanden werden müssen, damit Transaktionen gesammelt und in einer Transaktionsaufstellung gebucht werden.

Standardmäßig wird der Status jeder Regel auf **Aktiviert** gesetzt. Daher werden alle Regeln verwendet, um Einzelhandelstransaktionen zu prüfen, bevor sie in die Transaktionsaufstellungen übernommen werden können. Um eine Regel zu deaktivieren, ändern Sie ihren Status auf **Deaktiviert**. Deaktivierte Regeln werden nicht berücksichtigt, wenn Transaktionen während des Prozesses **Geschäftsbuchungen überprüfen** geprüft werden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
