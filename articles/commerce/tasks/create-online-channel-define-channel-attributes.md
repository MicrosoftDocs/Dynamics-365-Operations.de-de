---
title: Erstellen Sie Onlinekanal und definieren Sie Kanalattribute
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines neuen Online Kanals und dessen Hinzufügen zur Organisationshierarchie.
author: jashanno
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98d218a2d4f3b31084adfbc013dd0999f459dc1572e29a6470edc7cb899809c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713365"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Erstellen Sie Onlinekanal und definieren Sie Kanalattribute

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines neuen Online Kanals und dessen Hinzufügen zur Organisationshierarchie. Sie müssen die Organisationshierarchie erstellen, bevor Sie einen neuen Online Kanal erstellen können. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.


## <a name="create-a-new-online-channel"></a>Neuen Onlinechannel erstellen
1. Navigieren Sie zu Einzelhandel und Handel > Kanäle > Onlineshops.
2. Klicken Sie auf Neu.
3. Geben Sie im Feld "Name" einen Wert ein.
4. Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.
5. Wählen Sie im Feld "Zeitzone des Shops" eine Option aus.
6. Geben Sie im Feld "Standarddebitor" einen Wert ein oder wählen Sie einen Wert aus.
7. Geben Sie im Feld "Debitorenadressbuch" einen Wert ein oder wählen Sie einen Wert aus.
8. Geben Sie im Feld "Zahlungsbedingungen" einen Wert ein, oder wählen Sie einen Wert aus.
9. Geben Sie im Feld "Zahlungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.
10. Geben Sie im Feld "E-Mail-Benachrichtigungsprofil" einen Wert ein, oder wählen Sie einen Wert aus.
11. Erweitern Sie den Finanzdimensionsabschnitt.
12. Geben Sie im Feld "BusinessUnit" einen Wert ein oder wählen Sie einen Wert aus.
    * Legen Sie auf ähnliche Weise den Wert für alle anderen Standarddimensionen fest.  
13. Klicken Sie auf "Speichern".

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Online Kanal zur Organisationshierarchie hinzufügen
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Organisationsverwaltung" > "Organisationen" > "Organisationshierarchien".
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie auf "Ansicht".
5. Klicken Sie auf "Bearbeiten".
    * Sie können einen beliebigen Hierarchieknoten auswählen, unter dem Sie den neuen Kanal einfügen möchten.  
6. Klicken Sie auf Einfügen.
7. Klicken Sie auf den Commerce-Kanal.
8. Klicken Sie auf "OK".
9. Klicken Sie auf "Veröffentlichen", um das Ablagedialogfeld zu öffnen.
10. Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.
11. Klicken Sie auf "Veröffentlichen".

## <a name="configure-orders-for-near-real-time-notification"></a>Konfigurieren von Aufträgen für die Benachrichtigung beinahe in Echtzeit
1. Gehen Sie zu Einzelhandel und Handel > Zentralverwaltungseinrichtung > Parameter > Commerce-Parameter.
2. Legen Sie „Echtzeitdienst für eCommerce-Auftragserstellung verwenden“ auf „Ja“ fest.
3. Führen Sie den Verteilungszeitplan 1070 aus, um Änderungen an der Kanaldatenbank zu synchronisieren. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]