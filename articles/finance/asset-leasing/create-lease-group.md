---
title: Eine Leasinggruppe erstellen
description: In diesem Thema wird erläutert, wie Sie Leasinggruppen einrichten. Leasinggruppen sind erforderlich, um neue Mietverträge zu erstellen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 49a905e9f27f01898628e88c7af781aed1f25ec7
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714116"
---
# <a name="create-a-lease-group"></a>Eine Leasinggruppe erstellen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Leasinggruppen einrichten. Leasinggruppen sind erforderlich, um neue Mietverträge zu erstellen. Leasingbücher sind jeder Leasinggruppe zugeordnet. Leasingbücher bestimmen die Standardbücher, die für jeden Mietvertrag erstellt werden müssen. Sie können einer Leasinggruppe auf der Seite **Leasingbuchungsparameter** bestimmte Konten zuweisen.

## <a name="create-a-lease-book-and-add-a-lease-group"></a>Erstellen Sie ein Leasingbuch und fügen Sie eine Leasinggruppe hinzu

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasinggruppen**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Leasinggruppe hinzuzufügen. Dem Raster wird eine Zeile hinzugefügt.
3. Geben Sie in der neuen Zeile im **Leasinggruppe** Feld einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.

Die Informationen, die Sie gerade eingegeben haben, werden dem **Leasinggruppe**-Feld auf der Seite **Mietvertrag hinzufügen** hinzugefügt.

## <a name="associate-a-book-with-a-lease-group"></a>Ein Buch mit einer Leasinggruppe verknüpfen

Nachdem Sie Leasinggruppen erstellt haben, können Sie jeder Gruppe Bücher zuweisen. Wenn Sie einen Mietvertrag erstellen und es einer Leasinggruppe zuweisen, erstellt das System eine Reihe von Zeitplänen für jedes Buch, das dieser Leasinggruppe zugeordnet ist.

> [!NOTE]
> Bücher müssen eingerichtet werden, bevor sie einer Leasinggruppe zugeordnet werden können.

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasinggruppe**.
2. Wählen Sie eine Leasinggruppe aus und wählen Sie dann **Bücher**.
3. Wählen Sie **Neu** und dann im Feld **Buchart** das Buch aus, das der Leasinggruppe zugewiesen werden soll. Sie können einer Leasinggruppe mehrere Bücher zuweisen, wenn ein Mietvertrag auf unterschiedliche Weise bilanziert werden muss.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
