---
title: Serviceauftrags-Artikelbedarf
description: In diesem Thema wird der Serviceauftrags-Artikelbedarf beschrieben.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a6cd7e89e28b8fc00a8c09f51703995cd79ade5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674224"
---
# <a name="service-order-item-requirements"></a>Serviceauftrags-Artikelbedarf

[!include [banner](../includes/banner.md)]

Sie können einen Serviceauftrag erstellen, um Dienstleistungen nachzuverfolgen und zu verwalten, die Sie Ihren Debitoren anbieten. Wenn Sie bestimmte Artikel für einen Serviceauftrag reservieren müssen, können Sie Lagerartikelanforderungen für ihn erstellen. Eine Artikelanforderung kann sofort aus dem Bestand verbraucht werden, oder einen Produktionsauftrag für den Artikel initiieren.

Durch die Verwendung eines Artikelbedarfs anstelle einer Artikelbuchung kann die Lieferung direkt vor der tatsächlichen Verwendung der Artikel geplant werden. Sie können eine Bestellung erstellen, den Artikel in der Handelsvereinbarung berücksichtigen und den Artikelbedarf in die Produktionsplanung einbeziehen.

Artikelbedarf für Serviceaufträge wird im Rahmen eines Projekts verarbeitet. Zum Erstellen von Artikelbedarf für einen Serviceauftrag muss der Serviceauftrag einem Projekt zugeordnet werden.

Nach dem Erstellen eines Artikelbedarfs für einen Serviceauftrag kann dieser unter **Projekt** entweder im entsprechenden Serviceauftrag oder im Formular **Auftrag** angezeigt werden.

## <a name="view-an-item-requirement-from-a-service-order"></a>Anzeigen eines Artikelbedarfs in einem Serviceauftrag

1. Gehen Sie zu **Serviceverwaltung** \> **Allgemein** \> **Serviceaufträge** \> **Serviceaufträge**.
1. Wählen Sie **Versand** und dann **Artikelbedarf** aus, um das Formular **Artikelbedarf** zu öffnen.
1. Wählen Sie die Registerkarte **Projekt** aus, und aktivieren Sie das Kontrollkästchen **Serviceauftrag**, um die Serviceaufträge für den Artikelbedarf anzuzeigen.

## <a name="delete-service-orders-with-item-requirements"></a>Löschen von Serviceaufträgen mit Artikelbedarf

Wurde für einen Serviceauftrag ein Artikelbedarf erstellt, kann der Serviceauftrag nicht gelöscht werden. Löschen Sie zunächst den Artikelbedarf, um den Serviceauftrag löschen zu können.

1. Gehen Sie zu **Serviceverwaltung** \> **Allgemein** \> **Serviceaufträge** \> **Serviceaufträge**.
1. Wählen Sie **Versand** und dann **Artikelbedarf** aus, um das Formular **Artikelbedarf** zu öffnen. Dieses Formular enthält eine Liste mit dem für den Serviceauftrag erstellten Artikelbedarf.
1. Wählen Sie die zu löschende Artikelanforderung und dann **Löschen** aus.

- oder -

1. Gehen Sie zu **Projektverwaltung und Abrechnung** \> **Allgemein** \> **Projekte** \> **Alle Projekte**.
1. Öffnen Sie das Projekt mit dem Serviceauftrag, in dem die Artikelanforderung erstellt wurde.
1. Wählen Sie im Formular **Projekte** im rechten Bereich die Option **Artikelbedarf** aus. Das Formular **Artikelbedarf** wird mit einer Liste des dem ausgewählten Projekt zugeordneten Artikelbedarfs geöffnet.
1. Wählen Sie die zu löschende Artikelanforderung und dann **Löschen** aus.

## <a name="see-also"></a>Siehe auch

[Formular "Artikelbedarf"](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]