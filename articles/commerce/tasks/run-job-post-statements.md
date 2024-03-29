---
title: Konfigurieren und Aktivieren eines Einzelvorgangs, um Auszüge zu buchen
description: Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen eines wiederkehrenden Batchauftrags zum Buchen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops.
author: josaw1
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfff9e4520659ac1a9d0f85dd0e091f9fa5e2528ff092b650296a47aef9ca7b5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765855"
---
# <a name="configure-and-run-job-to-post-statements"></a>Konfigurieren und Aktivieren eines Einzelvorgangs, um Auszüge zu buchen

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen eines wiederkehrenden Batchauftrags zum Buchen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Gehen Sie zu Alle Arbeitsbereiche >.. > Finanzdaten für Shop.
2. Klicken Sie auf „Aufstellungen in Charge buchen“.
    * Wählen Sie eine Organisationshierarchie und anschließend in der Organisationsknotenstruktur einen einzelnen Shop oder einen Knoten aus. Wählen Sie einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.  
    * Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.  
3. Klicken Sie auf die Registerkarte „Im Hintergrund ausführen“. ![Im Hintergrund ausführen.](../dev-itpro/media/runbackground.png "Im Hintergrund ausführen") 
4. Aktivieren oder deaktivieren Sie das Kontrollkästchen ''Stapelverarbeitung".
![Stapelverarbeitung.](../dev-itpro/media/batchprocessing.png "Stapelverarbeitung und Wiederholung") 
5. Klicken Sie auf "Wiederholung".
6. Geben Sie im Feld "Startdatum" ein Datum ein.
7. Geben Sie im Startzeit-Feld eine Zeit ein.
    * Wählen Sie aus, ob die Wiederholung beenden möchten nach einer bestimmten Anzahl von Ausführungen, an einem bestimmten Datum, oder nie. Wählen Sie dann die verschiedenen Optionen aus, um zu definieren, wie häufig der Einzelvorgang ausgeführt werden soll.  
8. Klicken Sie auf "OK".
9. Klicken Sie auf "OK".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]