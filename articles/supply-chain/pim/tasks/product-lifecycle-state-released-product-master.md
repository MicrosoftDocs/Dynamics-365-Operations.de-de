---
title: Ein Produktlebensyklusstatus einem freigegebenen Produktmaster zuweisen
description: Diese Prozedur zeigt, wie ein Produktlebenszyklus-Status einem freigegebenen Produktmaster und seinen Varianten zugewiesen wird.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9f8f519c54ffe4f1a2a44da51ac5d97c56182a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992219"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Ein Produktlebensyklusstatus einem freigegebenen Produktmaster zuweisen

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie ein Produktlebenszyklus-Status einem freigegebenen Produktmaster und seinen Varianten zugewiesen wird. Voraussetzung: Sie müssen zuerst den Aufgabenleitfaden wiedergeben „Einen neuen Produktlebenszyklus-Status erstellen”, um sicherzustellen, dass mindestens ein Produktlebenszyklus-Status erstellt wird, bevor Sie diesen Aufgabenleitfaden wiedergeben können.


## <a name="find-a-released-product-master"></a>Einen freigegebenen Produktmaster suchen
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.

> [!NOTE]
> Ein Produktmaster hat den Produktuntertyp-Produktmaster.  

## <a name="update-the-lifecycle-state"></a>Den Lebenszyklusstatus aktualisieren
1. Klicken Sie auf "Bearbeiten".
2. Geben Sie im Feld „Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.
3. Klicken Sie auf "Speichern".
4. Klicken Sie auf "Ja".

> [!NOTE]
> Wenn „Ja” ausgewählt ist, werden alle zugeordneten freigegebenen Produktvarianten, die denselben ursprünglichen Status wie der freigegebene Produktmaster haben, ebenfalls auf den neuen Produktlebenszyklus-Status aktualisiert. Wenn „Nein” ausgewählt ist, behalten alle Varianten ihren tatsächlichen Status. Varianten, die einen anderen Produktlebenszyklus-Status als der freigegebene Produktmaster haben, werden nicht aktualisiert.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Den Lebenszyklusstatus der Varianten überprüfen
1. Klicken Sie auf Varianten für freigegebenes Produkt.

> [!NOTE]
> Beachten Sie, dass alle Varianten den ausgewählten Lebenszyklusstatus vom freigegebenen Produktmaster geerbt haben.  

2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Geben Sie im Feld „Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.

