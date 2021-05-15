---
title: Auftrag für ein konfigurierbares Produkt erstellen
description: Dieses Verfahren zeigt, wie die Konfigurationsvorlage für das Produkt auf einem Auftrag angewendet wird.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921288"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Auftrag für ein konfigurierbares Produkt erstellen

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie die Konfigurationsvorlage für das Produkt auf einem Auftrag angewendet wird. Dieses Beispiel verwendet das Lausprechermodell D0006 im Demodatenunternehmen USMF. Diese Aufgaben werden normalerweise von einem Auftragsbearbeiter ausgeführt.

## <a name="create-a-sales-order"></a>Auftrag erstellen

1. Gehen Sie zu **Vertrieb und Marketing \> Arbeitsbereiche \> Verkaufsauftragsverarbeitung und Abfrage**.
1. Wählen Sie **Neu** aus.
1. **Auftrag** auswählen.
1. Wählen Sie im Feld **Kundenkonto** die Option *US-001* aus. 
1. Wählen Sie **OK**.
1. Wählen Sie im Feld *Artikelnummer* die Option **D0006** aus.
    * Für diese Aufgabe müssen Sie ein konfigurierbares Produkt auswählen.  
1. Wählen Sie **Produkt und Lieferung**.
1. Wählen Sie **Zeile konfigurieren**.
    * Beachten Sie, dass sich der Preis basierend auf der gewählten Konfiguration geändert hat und dass das Feld **Website bearbeiten** jetzt auf *Wahr* festgelegt ist.  
    * Beachten Sie den Standardpreis und die Einstellungen, die für das Kabel ausgewählt sind.  
1. Wählen Sie **Vorlage laden**.
    * Dieses Beispiel verdeutlicht, wie Sie eine Vorlage verwenden können, um eine vordefinierte Konfiguration auszuwählen. Wenn Sie diese Vorgehensweise als Anleitung verwenden und die anderen verfügbaren Attributwerte sehen wollen, müssen Sie die Schaltfläche **Entsperren** wählen.  
1. Wählen Sie **OK**.
1. Wählen Sie **OK**.
1. Erweitern Sie den Abschnitt **Positionsdetails**.
1. Wählen Sie die Registerkarte **Produkt**.
    * Die Konfiguration des Artikels wird jetzt unter Produktdimensionen aufgeführt.  
1. Schließen Sie die Seite.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]