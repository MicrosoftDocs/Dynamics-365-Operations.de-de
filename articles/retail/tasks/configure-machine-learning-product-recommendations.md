--- 
title: " Machine-Learning-unterstützte Produktempfehlungen konfigurieren"
description: "Dieses Verfahren aktualisiert die Daten im Entitätsspeicher, der durch das Machine-Learning-System verwendet wird, das Produktempfehlungen unterstützt, und aktiviert dann Produktempfehlungen auf POS-Clients."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e32c7cf1283487cb7a52f7d8e261b6b587b76364
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a> Machine-Learning-unterstützte Produktempfehlungen konfigurieren

[!include[task guide banner](../includes/task-guide-banner.md)]

Dieses Verfahren aktualisiert die Daten im Entitätsspeicher, der durch das Machine-Learning-System verwendet wird, das Produktempfehlungen unterstützt, und aktiviert dann Produktempfehlungen auf POS-Clients. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Gehen Sie zu Systemadministration > Einstellungen > Entitätsspeicher
2. Suchen Sie in der Liste den Datensatz "RetailSales", und wählen Sie ihn aus.
3. Klicken Sie auf Aktualisieren.
4. Klicken Sie auf "OK".
5. Schließen Sie die Seite.
6. Navigieren Sie zu "Einzelhandel und Handel" > "Hauptsitz einrichten" > "Parameter" > "Einzelhandelsparameter".
7. Klicken Sie auf die Registerkarte "Machine Learning".
8. Wählen Sie "Ja" im Feld "Produktempfehlungen aktivieren" aus.
    * Wenn die Meldung erhalten "Die Empfehlungsmodelle konnten nicht abgerufen werden.", liegt dies daran, dass Sie den Entitätsspeicher vor kurzem aktualisiert haben und das System die Einbeziehung der neuen Daten nicht abgeschlossen hat. Warten Sie 2-3 Stunden und versuchen Sie es erneut.  
9. Klicken Sie auf "Speichern".
10. Schließen Sie die Seite.


