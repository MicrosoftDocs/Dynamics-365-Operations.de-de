---
title: Artikelbedarf für Serviceauftrag
description: Wenn Sie bestimmte Artikel für einen Serviceauftrag reservieren müssen, können Sie Lagerartikelanforderungen für ihn erstellen.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bbd15ca83ab116286a3d681887f076896653c76
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810581"
---
# <a name="service-order-item-requirements"></a>Artikelbedarf für Serviceauftrag   

[!include [banner](../includes/banner.md)]


Sie können einen Serviceauftrag erstellen, um Dienstleistungen nachzuverfolgen und zu verwalten, die Sie Ihren Debitoren anbieten. Wenn Sie bestimmte Artikel für einen Serviceauftrag reservieren müssen, können Sie Lagerartikelanforderungen für ihn erstellen. Eine Artikelanforderung kann sofort aus dem Bestand verbraucht werden, oder einen Produktionsauftrag für den Artikel initiieren.

Durch die Verwendung eines Artikelbedarfs anstelle einer Artikelbuchung kann die Lieferung direkt vor der tatsächlichen Verwendung der Artikel geplant werden. Sie können eine Bestellung erstellen, den Artikel in der Handelsvereinbarung berücksichtigen und den Artikelbedarf in die Produktionsplanung einbeziehen.

Artikelbedarf für Serviceaufträge wird im Rahmen eines Projekts verarbeitet. Zum Erstellen von Artikelbedarf für einen Serviceauftrag muss der Serviceauftrag einem Projekt zugeordnet werden.

Nach dem Erstellen eines Artikelbedarfs für einen Serviceauftrag kann dieser unter **Projekt** entweder im entsprechenden Serviceauftrag oder im Formular **Auftrag** angezeigt werden.

## <a name="view-an-item-requirement-from-a-service-order"></a>Anzeigen eines Artikelbedarfs in einem Serviceauftrag

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.

2.  Klicken Sie **Versand** und **Artikelbedarf**, um das Formular **Artikelbedarf** zu öffnen.

3.  Klicken Sie auf die Registerkarte **Projekt**, und aktivieren Sie das Kontrollkästchen **Serviceauftrag**, um die Serviceaufträge für den Artikelbedarf anzuzeigen.

## <a name="delete-service-orders-with-item-requirements"></a>Löschen von Serviceaufträgen mit Artikelbedarf

Wurde für einen Serviceauftrag ein Artikelbedarf erstellt, kann der Serviceauftrag nicht gelöscht werden. Löschen Sie zunächst den Artikelbedarf, um den Serviceauftrag löschen zu können.

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.

2.  Klicken Sie **Versand** und **Artikelbedarf**, um das Formular **Artikelbedarf** zu öffnen. Dieses Formular enthält eine Liste mit dem für den Serviceauftrag erstellten Artikelbedarf.

3.  Wählen Sie die zu löschende Artikelanforderung aus, und klicken Sie dann **Löschen**.

-oder-

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** \> **Allgemein** \> **Projekte** \> **Alle Projekte**.

2.  Öffnen Sie das Projekt mit dem Serviceauftrag, in dem die Artikelanforderung erstellt wurde.

3.  In der **Projekte** Formular, im rechten Bereich **Artikelbedarf**. Das Formular **Artikelbedarf** wird mit einer Liste des dem ausgewählten Projekt zugeordneten Artikelbedarfs geöffnet.

4.  Wählen Sie die zu löschende Artikelanforderung aus, und klicken Sie dann **Löschen**.

## <a name="see-also"></a>Siehe auch

[Formular "Artikelbedarf"](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]