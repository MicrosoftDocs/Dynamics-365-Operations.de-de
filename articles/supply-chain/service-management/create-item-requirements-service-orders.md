---
title: Erstellen von Artikelbedarf für Serviceaufträge
description: In diesem Artikel wird beschrieben, wie Sie Artikelbedarf für Serviceaufträge erstellen.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2c90ff76121b436d0fec532268cd3383de0eab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888411"
---
# <a name="create-item-requirements-for-service-orders"></a>Erstellen von Artikelbedarf für Serviceaufträge

[!include [banner](../includes/banner.md)]

Sie können einen Serviceauftrag erstellen, um Dienstleistungen nachzuverfolgen und zu verwalten, die Sie Ihren Debitoren anbieten. Wenn Sie bestimmte Artikel für einen Serviceauftrag reservieren müssen, können Sie Lagerartikelanforderungen für ihn erstellen. Eine Artikelanforderung kann sofort aus dem Bestand verbraucht werden, oder einen Produktionsauftrag für den Artikel initiieren.

Durch die Verwendung eines Artikelbedarfs anstelle einer Artikelbuchung kann die Lieferung direkt vor der tatsächlichen Verwendung der Artikel geplant werden. Sie können eine Bestellung erstellen, den Artikel in der Handelsvereinbarung berücksichtigen und den Artikelbedarf in die Produktionsplanung einbeziehen.

Artikelbedarf für Serviceaufträge wird im Rahmen eines Projekts verarbeitet. Zum Erstellen von Artikelbedarf für einen Serviceauftrag muss der Serviceauftrag einem Projekt zugewiesen werden. Nachdem Sie einen Artikelbedarfs für einen Serviceauftrag erstellen, können Sie den Artikelbedarf in dem Formular **Projekte** für das ausgewählte Projekt anzeigen.

## <a name="create-an-item-requirement-for-a-service-order"></a>Erstellen eines Artikelbedarfs für einem Serviceauftrag

1. Gehen Sie zu **Serviceverwaltung** \> **Allgemein** \> **Serviceaufträge** \> **Serviceaufträge**.
1. Wählen Sie den Serviceauftrag aus, für den ein Artikelbedarf erstellt werden soll.
1. Klicken Sie im **Aktivitätsbereich** auf der Registerkarte **Versand** auf **Artikelbedarf**.
1. Geben Sie im Formular **Artikelanforderungen** die Informationen für den erforderlichen Artikel ein. Weitere Informationen zu bestimmten Feldern finden Sie unter [Formular "Artikelbedarf"](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Erstellen eines Artikelbedarfs für eine Servicevereinbarung

1. Gehen Sie zu **Serviceverwaltung** \> **Allgemein** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.
1. Öffnen Sie die Servicevereinbarung, für die ein Artikelbedarf erstellt werden soll.
1. Wählen Sie im Inforegister **Positionen** die Option **Hinzufügen** aus, um eine neue Position zu erstellen.
1. Wählen Sie im Feld **Transaktionstyp** **Artikel** aus.
1. Wählen Sie im Feld **Artikeleinstellungen** **Artikelbedarf** aus.
1. Wählen Sie im Feld **Artikelnummer** den Artikel aus, der für die Servicevereinbarung erforderlich ist.
1. Wählen Sie auf dem Inforegister **Positionsdetails** auf der Registerkarte **Produktdimensionen**, im Feld **Standort**, wählen Sie hier den Standort für den Artikel aus.
1. Um einen Serviceauftrag aus der Vereinbarungsposition zu erstellen, wählen Sie im Inforegister **Positionen** die Option **Erstellen von Serviceaufträgen** aus, und geben dann die relevanten Informationen im Formular **Erstellen von Serviceaufträgen** ein.

## <a name="see-also"></a>Siehe auch

[Automatische Erstellung von Serviceaufträgen](create-service-orders-automatically.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
