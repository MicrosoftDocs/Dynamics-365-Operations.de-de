---
title: Auftrag für ein konfigurierbares Produkt erstellen
description: Dieses Verfahren zeigt, wie die Konfigurationsvorlage für das Produkt auf einem Auftrag angewendet wird.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e42f121d1efa66f85a3dd811606962b907ed177d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570584"
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