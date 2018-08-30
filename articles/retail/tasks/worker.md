--- 
title: "Einzelhandelsarbeitskräfte konfigurieren"
description: "Dieses Verfahren zeigt, wie eine Einzelhandelsarbeitskraft als Verkäufer konfiguriert wird, der im POS für Provisionen freigegeben ist."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: f583c421c2f6dfd019d9586cb7d14f3298127d94
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="configure-retail-workers"></a>Einzelhandelsarbeitskräfte konfigurieren

[!include [task guide banner](../includes/task-guide-banner.md)]

Dieses Verfahren zeigt, wie eine Einzelhandelsarbeitskraft als Verkäufer konfiguriert wird, der im POS für Provisionen freigegeben ist. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Verkaufsprovisionsgruppe für die Arbeitskraft erstellen
1. Wechseln Sie zu Vertrieb und Marketing > Provisionen > Vertriebsgruppen.
    * Arbeitskräfte können mindestens einer Verkaufsgruppe zugewiesen werden. In POS können Sie eine Verkaufsgruppe auswählen, die den Arbeitskräften des Adressbuchs des Shops enthält.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Gruppe" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Klicken Sie auf "Speichern".
6. Klicken Sie im Aktivitätsbereich auf "Allgemein".
7. Klicken Sie auf "Verkäufer".
    * Eine Verkaufsgruppe kann mehr als einer Arbeitskraft enthalten. Provisionen können aufgeteilt werden zwischen Arbeitskräften basierend auf dem, was Sie in der Provisionsfreigabe definieren.  
8. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
9. Geben Sie im Feld 'Provisionsanteil' eine Zahl ein.
10. Klicken Sie auf "Speichern".
11. Schließen Sie die Seite.
12. Schließen Sie die Seite.

## <a name="assign-the-workers-default-sales-group"></a>Standardverkaufsgruppe der Arbeitskraft zuweisen
1. Navigieren Sie zu Einzelhandel und Handel > Mitarbeiter > Arbeitskräfte.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie auf die Registerkarte Einzelhandel.
    * Eine Arbeitskraft kann einer Standardverkaufsgruppe zugewiesen werden. Die Standardverkaufsgruppe wird automatisch zu Verkaufspositionen in POS hinzugefügt, wenn die Option im Funktionsprofil für die Filiale aktiviert ist.  
5. Klicken Sie auf "Bearbeiten".
6. Geben Sie im Feld "Standardgruppe" einen Wert ein oder wählen Sie einen Wert aus.
7. Klicken Sie auf "Speichern".


