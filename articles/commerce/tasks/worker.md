---
title: " Eine Arbeitskraft konfigurieren"
description: Diese Prozedur zeigt, wie eine Arbeitskraft als Verkäufer konfiguriert wird, der im POS für Provisionen freigegeben ist.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 120705200f223e31c72290059e8634e7db6f9fdd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232616"
---
# <a name="configure-a-worker"></a> Eine Arbeitskraft konfigurieren

[!include [banner](../includes/banner.md)]

Diese Prozedur zeigt, wie eine Arbeitskraft als Verkäufer konfiguriert wird, der im POS für Provisionen freigegeben ist. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.


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
4. Klicken Sie auf die Registerkarte Commerce.
    * Eine Arbeitskraft kann einer Standardverkaufsgruppe zugewiesen werden. Die Standardverkaufsgruppe wird automatisch zu Verkaufspositionen in POS hinzugefügt, wenn die Option im Funktionsprofil für die Filiale aktiviert ist.  
5. Klicken Sie auf "Bearbeiten".
6. Geben Sie im Feld "Standardgruppe" einen Wert ein oder wählen Sie einen Wert aus.
7. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]