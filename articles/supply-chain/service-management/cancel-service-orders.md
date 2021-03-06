---
title: Serviceaufträge stornieren
description: Sie können einen Serviceauftrag oder eine Serviceauftragsposition direkt im Serviceauftrag stornieren oder zum Stornieren mehrerer Serviceaufträge einen periodischen Einzelvorgang ausführen.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 779f535ac617d3f3940cc1b226fa53dc72e3411a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831601"
---
# <a name="cancel-service-orders"></a>Serviceaufträge stornieren   

[!include [banner](../includes/banner.md)]


Sie können einen Serviceauftrag oder eine Serviceauftragsposition direkt im Serviceauftrag stornieren oder zum Stornieren mehrerer Serviceaufträge einen periodischen Einzelvorgang ausführen.


> [!NOTE]
> <P>Serviceaufträge können nicht storniert werden, wenn die Phase des Serviceauftrags keine Stornierung zulässt, Artikelbedarf vorliegt oder der Serviceauftrag bereits gebucht wurde.</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>Stornieren eines Serviceauftrags im Formular "Serviceaufträge"

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**. Wählen Sie den gewünschten Serviceauftrag aus, und klicken Sie im Aktivitätsbereich auf **Auftrag stornieren**.

## <a name="cancel-a-service-order-line"></a>Stornieren einer Serviceauftragsposition

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**. Doppelklicken Sie auf den Serviceauftrag, der die zu stornierende Position enthält.

2.  Wählen Sie die Serviceauftragsposition aus, die Sie stornieren möchten, und klicken Sie auf **Auftragsposition stornieren**, um den Status der Position in **Storniert** zu ändern.


> [!TIP]
> <P>Um die Stornierung einer Serviceauftragsposition zu widerrufen und den Status wieder in <STRONG>Erstellt</STRONG> zu ändern, klicken Sie auf <STRONG>Stornierung widerrufen</STRONG>.</P>


## <a name="cancel-multiple-service-orders"></a>Stornieren mehrerer Serviceaufträge

1.  Klicken Sie auf **Serviceverwaltung** \> **Periodisch** \> **Serviceaufträge** \> **Serviceaufträge stornieren**.

2.  Klicken Sie auf die Schaltfläche **Auswählen**.

3.  Wählen Sie im Formular **Abfrage** in der Spalte **Kriterien** die zu löschenden Serviceaufträge aus.

4.  Klicken Sie auf **OK**, um das **Abfrageformular** zu schließen.

5.  Aktivieren Sie zum Generieren eines Infologs mit den stornierten Serviceaufträgen das Kontrollkästchen **Infolog anzeigen**.

6.  Aktivieren Sie das Kontrollkästchen **Stornierung widerrufen**, wenn Sie den Status **Storniert** eines Serviceauftrags widerrufen möchten.

7.  Klicken Sie auf **OK**.

Die ausgewählten Serviceaufträge werden entweder storniert, oder der Status **Storniert** wird auf **In Bearbeitung ...** zurückgesetzt.


> [!NOTE]
> <P>Wenn Sie das Kontrollkästchen <STRONG>Stornierung widerrufen</STRONG> aktivieren, werden Serviceaufträge mit dem Status <STRONG>Storniert</STRONG> widerrufen und Serviceaufträge mit dem Status <STRONG>In Bearbeitung ...</STRONG> nicht storniert.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]