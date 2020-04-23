---
title: Auftrag für ein konfigurierbares Produkt erstellen
description: Dieses Verfahren zeigt, wie die Konfigurationsvorlage für das Produkt auf einem Auftrag angewendet wird.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e69fd2aa04a65d64db4d34f1839a01fb0f8e018
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213192"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Auftrag für ein konfigurierbares Produkt erstellen

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie die Konfigurationsvorlage für das Produkt auf einem Auftrag angewendet wird. Dieses Beispiel verwendet das Lausprechermodell D0006 im Demodatenunternehmen USMF. Diese Aufgaben werden normalerweise von einem Auftragsbearbeiter ausgeführt.


## <a name="create-a-sales-order"></a>Auftrag erstellen
1. Klicken Sie auf "Auftragsverarbeitung und -abfrage".
2. Klicken Sie auf "Neu".
3. Klicken Sie auf "Auftrag".
4. Wählen Sie im Feld Debitorenkonto US-001 aus. 
5. Klicken Sie auf "OK".
6. Wählen Sie im Feld "Artikelnummer" die Zeichenfolge "D0006" aus.
    * Für diese Aufgabe müssen Sie ein konfigurierbares Produkt auswählen.  
7. Klicken Sie auf "Produkt und Beschaffung".
8. Klicken Sie auf Klicken Sie auf die Zeile Konfigurieren..
    * Beachten Sie, dass der Preis geändert wurde, gemäß der ausgewählten Konfiguration, und dass das Feld "Inkl. Kabel" jetzt Wahr ist.  
    * Beachten Sie den Standardpreis und die Einstellungen, die für das Kabel ausgewählt sind.  
9. Klicken Sie auf Vorlage laden..
    * Dieses Beispiel verdeutlicht, wie Sie eine Vorlage verwenden können, um eine vordefinierte Konfiguration auszuwählen. Wenn Sie dieses Verfahren als Aufgabenleitfaden verwenden, und anderen die Attributwerte angezeigt werden sollen, die verfügbar sind, müssen Sie auf die Schaltfläche „Sperrung aufheben“ klicken.  
10. Klicken Sie auf "OK".
11. Klicken Sie auf "OK".
12. Erweitern Sie den Abschnitt "Positionsdetails".
13. Klicken Sie auf die Registerkarte "Produkt".
    * Die Konfiguration des Artikels wird jetzt unter Produktdimensionen aufgeführt.  
14. Schließen Sie die Seite.

## <a name="select-the-product-configuration"></a>Wählen der Produktkonfiguration

