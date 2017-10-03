--- 
title: " Machine-Learning-unterstützte Produktempfehlungen konfigurieren"
description: "Dieses Verfahren aktualisiert die Daten im Entitätsspeicher, der durch das Machine-Learning-System verwendet wird, das Produktempfehlungen unterstützt, und aktiviert dann Produktempfehlungen auf POS-Clients."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c51c5f82efb50db1e238f4046506920975f33218
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

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


