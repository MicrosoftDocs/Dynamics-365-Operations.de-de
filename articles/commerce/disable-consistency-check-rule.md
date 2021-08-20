---
title: Regeln in der Konsistenzprüfung von Einzelhandelsbuchungen deaktivieren
description: In diesem Thema werden die Funktionen zum Deaktivieren der Regeln in der Konsistenzprüfung von Buchungen in Microsoft Dynamics 365 Commerce beschrieben.
author: josaw1
ms.date: 10/15/2019
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
ms.openlocfilehash: 381bc8534d4b0a06a50c8c18b3f78aba9d43a1f497bfd271361216ed1dee9197
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746660"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Regeln in der Konsistenzprüfung von Einzelhandelsbuchungen deaktivieren 

[!include [banner](../includes/banner.md)]

Einzelhändler können individuelle Geschäftsszenarien und -prozesse nutzen. Daher gelten nicht alle standardmäßig in der Konsistenzprüfung von Commerce-Transaktionen enthaltenen Regeln für alle Einzelhändler. Zur Anpassung von Unterschieden stellt Microsoft Dynamics 365 Commerce Funktionen zum Deaktivieren nicht anwendbarer Regeln bereit.

Um die Liste der Regeln anzuzeigen, die in der Konsistenzprüfung von Einzelhandelsbuchungen in Ihrer Umgebung verfügbar sind, und um den Status jeder Regel anzuzeigen, wechseln Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter**, und wählen Sie die Registerkarte **Buchungsprüfung** aus.

Standardmäßig wird der Status jeder Regel auf **Aktiviert** gesetzt. Daher werden alle Regeln verwendet, um Einzelhandelstransaktionen zu prüfen, bevor sie in die Handelsaufstellungen übernommen werden. Um eine Regel zu deaktivieren, ändern Sie ihren Status auf **Deaktiviert**. Deaktivierte Regeln werden nicht berücksichtigt, wenn Transaktionen während des Aufstellungsberechnungsprozesses geprüft werden.

Um den gesamten Prüfungsprozess zu umgehen, unabhängig von den aktivierten Regeln, wechseln Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Handelsparameter**. Legen Sie dann auf der Registerkarte **Transaktionsprüfung** die Option **Konsistenzprüfung für Handelsbuchungen deaktivieren** auf **Ja** fest. Nachdem diese Option auf **Nein** festgelegt wurde, kann sie über die Benutzeroberfläche nicht mehr auf **Ja** zurückgestellt werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]