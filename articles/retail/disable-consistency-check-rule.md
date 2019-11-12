---
title: Regeln in der Konsistenzprüfung von Einzelhandelsbuchungen deaktivieren
description: Dieses Thema beschreibt die Funktionalität zum Deaktivieren der Regeln für die Konsistenzprüfung von Einzelhandelsbuchungen in Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586296"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Regeln in der Konsistenzprüfung von Einzelhandelsbuchungen deaktivieren 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Einzelhändler können individuelle Geschäftsszenarien und -prozesse nutzen. Daher sind nicht alle Regeln, die standardmäßig in der Konsistenzprüfung von Einzelhandelsbuchungen enthalten sind, für alle Einzelhändler anwendbar. Um Abweichungen auszugleichen, bietet Microsoft Dynamics 365 Retail Funktionen, mit denen Sie die nicht anwendbaren Regeln deaktivieren können.

Um die Liste der Regeln anzuzeigen, die in der Konsistenzprüfung von Einzelhandelsbuchungen in Ihrer Umgebung verfügbar sind, und um den Status jeder Regel anzuzeigen, wechseln Sie zu **Retail \> Zentralverwaltungseinrichtung \> Parameter \> Einzelhandelsparameter** und wählen Sie die Registerkarte **Buchungsprüfung** aus.

Standardmäßig wird der Status jeder Regel auf **Aktiviert** gesetzt. Daher werden alle Regeln verwendet, um Einzelhandelstransaktionen zu prüfen, bevor sie in die Einzelhandelsaufstellungen übernommen werden. Um eine Regel zu deaktivieren, ändern Sie ihren Status auf **Deaktiviert**. Deaktivierte Regeln werden nicht berücksichtigt, wenn Einzelhandelstransaktionen während des Aufstellungsberechnungsprozesses geprüft werden.

Um den gesamten Prüfungsprozess zu umgehen, unabhängig von den aktivierten Regeln, wechseln Sie zu **Retail \> Zentralverwaltungseinrichtung \> Parameter \> Einzelhandelsparameter**. Legen Sie dann auf der Registerkarte **Transaktionsprüfung** die Option **Konsistenzprüfung für Einzelhandelsbuchungen deaktivieren** auf **Ja** fest. Nachdem diese Option auf **Nein** festgelegt wurde, kann sie über die Benutzeroberfläche nicht mehr auf **Ja** zurückgestellt werden.
