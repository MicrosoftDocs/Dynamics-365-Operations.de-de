---
title: Erstellen von Artikelbedarf für Serviceaufträge
description: Wenn Sie bestimmte Artikel für einen Serviceauftrag reservieren müssen, können Sie Lagerartikelanforderungen für ihn erstellen.
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
ms.openlocfilehash: a5a730ae945af15c7bd4020c734bac971d8186e2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553414"
---
# <a name="create-item-requirements-for-service-orders"></a>Erstellen von Artikelbedarf für Serviceaufträge 

[!include [banner](../includes/banner.md)]


Sie können einen Serviceauftrag erstellen, um Dienstleistungen nachzuverfolgen und zu verwalten, die Sie Ihren Debitoren anbieten. Wenn Sie bestimmte Artikel für einen Serviceauftrag reservieren müssen, können Sie Lagerartikelanforderungen für ihn erstellen. Eine Artikelanforderung kann sofort aus dem Bestand verbraucht werden, oder einen Produktionsauftrag für den Artikel initiieren.

Durch die Verwendung eines Artikelbedarfs anstelle einer Artikelbuchung kann die Lieferung direkt vor der tatsächlichen Verwendung der Artikel geplant werden. Sie können eine Bestellung erstellen, den Artikel in der Handelsvereinbarung berücksichtigen und den Artikelbedarf in die Produktionsplanung einbeziehen.

Artikelbedarf für Serviceaufträge wird im Rahmen eines Projekts verarbeitet. Zum Erstellen von Artikelbedarf für einen Serviceauftrag muss der Serviceauftrag einem Projekt zugewiesen werden. Nachdem Sie einen Artikelbedarfs für einen Serviceauftrag erstellen, können Sie den Artikelbedarf in dem Formular **Projekte** für das ausgewählte Projekt anzeigen.

## <a name="create-an-item-requirement-for-a-service-order"></a>Erstellen eines Artikelbedarfs für einem Serviceauftrag

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.

2.  Wählen Sie den Serviceauftrag aus, für den ein Artikelbedarf erstellt werden soll.

3.  Klicken Sie im **Aktivitätsbereich** auf der Registerkarte **Ausführung** auf **Artikelanforderung**.

4.  Geben Sie im Formular **Artikelanforderungen** die Informationen für den erforderlichen Artikel ein. Weitere Informationen zu bestimmten Feldern finden Sie unter [Formular "Artikelbedarf"](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Erstellen eines Artikelbedarfs für eine Servicevereinbarung

1.  Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.

2.  Öffnen Sie die Servicevereinbarung, für die ein Artikelbedarf erstellt werden soll.

3.  Klicken Sie im Inforegister **Positionen** auf **Hinzufügen**, um eine neue Position zu erstellen.

4.  Wählen Sie im Feld **Transaktionstyp** **Artikel** aus.

5.  Wählen Sie im Feld **Artikeleinstellungen** **Artikelbedarf** aus.

6.  Wählen Sie im Feld **Artikelnummer** den Artikel aus, der für die Servicevereinbarung erforderlich ist.

7.  Wählen Sie auf dem Inforegister **Positionsdetails** auf der Registerkarte **Produktdimensionen**, im Feld **Standort**, wählen Sie hier den Standort für den Artikel aus.

8.  Um einen Serviceauftrag aus der Vereinbarungsposition zu erstellen, klicken Sie im Inforegister **Positionen** auf **Erstellen von Serviceaufträgen**, und geben dann die relevanten Informationen im Formular **Erstellen von Serviceaufträgen** ein. 


## <a name="see-also"></a>Siehe auch

[Automatische Erstellung von Serviceaufträgen](create-service-orders-automatically.md).

  


