---
title: Arbeitsplan für ein Produktmodell verwalten
description: Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 704a6b72c9eb8dc49ba9410ccd3689ba5ccfdd1f03e538b95ad174f6c1ee9796
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746135"
---
# <a name="maintain-route-for-a-product-model"></a>Arbeitsplan für ein Produktmodell verwalten

[!include [banner](../../includes/banner.md)]

Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell. Bei diesem Verfahren wird das Spitzenlautsprechermodell im Vorführungsunternehmen USMF verwendet.

## <a name="add-a-route-operation"></a>Hinzufügen eines Arbeitsplanarbeitsgangs

1. Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie den Spitzenlautsprecher für diese Aufgabe aus.  
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Erweitern Sie den Abschnitt **Arbeitsplanvorgänge**.
1. Wählen Sie **Hinzufügen** aus.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Geben Sie im Feld **Beschreibung** einen Wert ein.
1. Wählen Sie **Speichern** aus.

## <a name="enter-route-operation-details"></a>Eingeben von Arbeitsplanarbeitsgangdetails

1. Wählen Sie **Details zum Arbeitsplanvorgang**.
1. Geben Sie im Feld **Vorgang** einen Wert ein oder wählen Sie ihn aus.
1. In dem **Vorgang. Nr.** eine Zahl ein.
    * Vorgangsnummer legen die Arbeitsplansequenz fest.  
    * Jede Eigenschaft eines Arbeitsplanvorgang kann einen statischen Wert enthalten oder einem Attribut zugeordnet werden. Die Zuordnung zu einem Attribut arbeitet mit dem Wert, die als Teil der Konfiguration festgelegt ist.  
1. Geben Sie im Feld **Arbeitsplan-Gruppe** einen Wert ein oder wählen Sie einen Wert aus.
    * Die Arbeitsgangsteuerungsgruppe bestimmt das grundlegende Verhalten der Nachkalkulation, des Verbrauch und der Einstellungen.  
1. Wählen Sie die Registerkarte **Einrichten**.
1. Wählen Sie die Registerkarte **Zeiten**.
1. Geben Sie im Feld **Anzahl verarbeiten** eine Zahl ein.
    * Bestimmen Sie, wie viele während eines Arbeitsgangs verarbeitet werden.  
1. Geben Sie im Feld **Stunden/Zeit** eine Zahl ein.
    * Geben Sie einen Zeitanteil ein.  
1. Aktivieren Sie das Kontrollkästchen **Setzen**.
1. Geben Sie im Feld **Laufzeit** eine Zahl ein.
    * Bestimmen Sie die Bearbeitungszeit zur Menge, die Sie angegeben haben.  
1. Wählen Sie die Registerkarte **Ressourcenanforderung**.
1. Wählen Sie **Hinzufügen** aus.
1. Markieren Sie in der Liste die ausgewählte Zeile.
1. Wählen Sie im Feld **Bedarfstyp** eine Option.
    * Entscheiden Sie, ob spezifische Ressourcen oder Funktionen vorhanden sein müssen.  
1. Geben Sie im Feld **Anforderung** einen Wert ein oder wählen Sie ihn aus.
1. Wählen Sie **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]