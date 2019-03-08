---
title: Serviceaufträge stornieren
description: Sie können einen Serviceauftrag oder eine Serviceauftragsposition direkt im Serviceauftrag stornieren oder zum Stornieren mehrerer Serviceaufträge einen periodischen Einzelvorgang ausführen.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1495fa139ea2c3cb7f2450b402126822f5549f60
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "327043"
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


  


