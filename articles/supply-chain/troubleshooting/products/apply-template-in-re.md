---
title: Sie können keine Vorlage auf ein freigegebenes Produkt anwenden
description: Sie können keine Vorlage auf ein freigegebenes Produkt anwenden.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 566686b6a86e67c87f75f9f2e397592174d3d749034f18997ca8ce651c2594a2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760393"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>Sie können keine Vorlage anwenden, um ein freigegebenes Produkt zu erstellen

KB-Nummer: 4612097

## <a name="symptoms"></a>Symptome

Wenn Sie ein neues freigegebenes Produkt erstellen, indem Sie das Dialogfeld **Neu freigegebenes Produkt** verwenden, können Sie eine Vorlage auswählen. Die Vorlage sollte Standardeinstellungen für viele Felder des neuen freigegebenen Produkts enthalten. Einige oder alle Felder werden jedoch nicht festgelegt, nachdem Sie die Vorlage ausgewählt haben.

## <a name="cause"></a>Ursache

Viele Seiten in Microsoft Dynamics 365 Supply Chain Management lassen Sie eine Vorlage erstellen, mit der die Anfangseinstellungen für die auf diesen Seiten angezeigten Datensätze festgelegt werden. Sie können eine dieser Vorlagen erstellen, indem Sie **Datensatzinfo** auf der Registerseite **Optionen** des Aktionsbereichs auswählen. Freigegebene Produkte sind jedoch viel komplexer als die meisten anderen Arten von Datensätzen. Obwohl Sie auswählen **Datensatzinfo** auf der Seite **Freigegebene Produkte** zum Erstellen einer Vorlage auswählen können und obwohl Sie diese Vorlage beim Erstellen eines freigegebenen Produkts auswählen können, liefert die Vorlage nicht die erwarteten Feldwerte für das neue freigegebene Produkt. Daher können Sie für freigegebene Produkte keine „Datensatzinfo“-Vorlagen verwenden. Stattdessen müssen Sie dedizierte Produktvorlagen erstellen.

## <a name="resolution"></a>Lösung

Verwenden Sie zum Erstellen einer Produktvorlage das Menü **Vorlage** auf der Registerkarte **Produkt** des Aktionsbereichs, nicht die Schaltfläche **Datensatzinfo** auf der Registerkarte **Optionen**.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Produkt** **Neu** und dann **Vorlage** aus. Wählen Sie dann entweder, wie erforderlich, **Persönliche Vorlage erstellen** oder **Gemeinsame Vorlage erstellen**.
