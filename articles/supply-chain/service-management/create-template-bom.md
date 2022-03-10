---
title: Erstellen einer Vorlagenstückliste
description: Eine Vorlagenstückliste kann auf viele Arten erstellt werden.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c10bf5e758a1752e1c50c602db85e0c53ee3e662
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571496"
---
# <a name="create-a-template-bom"></a>Erstellen einer Vorlagenstückliste   

[!include [banner](../includes/banner.md)]


Eine Vorlagenstückliste kann auf folgende Arten erstellt werden. Bei allen Verfahren gilt: Die Felder **Von Datum** und **Bis datum** sind optional und nur zu Informationszwecken vorhanden.

## <a name="create-a-template-bom-manually"></a>Manuelles Erstellen einer Vorlagenstückliste

1.  Gehen Sie zu **Serviceverwaltung** \> **Einrichten** \> **Serviceobjekte** \> **Vorlage Stücklisten**.

2.  Wählen Sie **Neu**, um das Formular **Vorlagenstückliste erstellen** zu öffnen.

3.  Wählen Sie unter **Stücklistenpositionen aus Referenz kopieren** die Option **Manuell** aus.

4.  Geben Sie im Feld **Artikelnummer** einen Artikel des Typs **Stückliste** ein.

5.  Geben Sie im Feld **Name** einen Namen für die Vorlage.

6.  Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.

7.  Wählen Sie **OK**.

Eine neue leere Vorlagenstückliste wird erstellt.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Erstellen einer Vorlagenstückliste auf Basis einer anderen Vorlagenstückliste

1.  Wählen Sie **Dienstverwaltung** \> **Einrichten** \> **Dienstobjekte** \> **Vorlagenstücklisten**.

2.  Wählen Sie **Neu**, um das Formular **Vorlagenstückliste erstellen** zu öffnen.

3.  Wählen Sie unter **Stücklistenpositionen aus Referenz kopieren** die Option **Vorlagenstückliste** aus.

4.  Wählen Sie im Feld **Referenznummer** eine vorhandene Vorlagenstückliste aus, die in die neue Vorlagenstückliste kopiert werden soll.

5.  Geben Sie im Feld **Name** einen Namen für die Vorlage.

6.  Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.

7.  Wählen Sie **OK**.

Eine neue Vorlagenstückliste wird erstellt. Diese enthält die gleichen Positionen wie die ursprüngliche Vorlagenstückliste.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Erstellen einer Vorlagenstückliste auf Basis einer Artikelstückliste

1.  Wählen Sie **Dienstverwaltung** \> **Einrichten** \> **Dienstobjekte** \> **Vorlagenstücklisten**.

2.  Wählen Sie **Neu**, um das Formular **Vorlagenstückliste erstellen** zu öffnen.

3.  Wählen Sie unter die **Stücklistenpositionen aus Referenz kopieren** **Stückliste** aus.

4.  Wählen Sie im Feld **Referenznummer** eine Stücklistenversion wählen Sie aus. Ein Artikel vom Typ "Stückliste" wird in das Feld **Artikelnummer** kopiert.

5.  Geben Sie im Feld **Name** einen Namen für die Vorlage.

6.  Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.

7.  Wählen Sie **OK**.

Eine neue Vorlagenstückliste erstellt. Diese enthält die gleichen Positionen, die auch in der unter **Stücklisten** aufgeführten Stückliste enthalten sind.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Erstellen einer Vorlagenstückliste auf Basis einer Produktionsstückliste

1.  Wählen Sie **Dienstverwaltung** \> **Einrichten** \> **Dienstobjekte** \> **Vorlagenstücklisten**.

2.  Wählen Sie **Neu**, um das Formular **Vorlagenstückliste erstellen** zu öffnen.

3.  Wählen Sie unter die **Stücklistenpositionen aus Referenz kopieren** **Produktion** aus.

4.  Wählen Sie im Feld **Referenznummer** eine Produktions-Stücklistenversion aus.

5.  Geben Sie im Feld **Name** einen Namen für die Vorlage.

6.  Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** ein Datumsintervall an, in dem die Vorlagenstückliste aktiv sein soll.

7.  Wählen Sie **OK**.

Eine neue Vorlagenstückliste erstellt. Diese enthält die gleichen Positionen, die auch in der unter **Stückliste** aufgeführten Stückliste enthalten sind.

## <a name="see-also"></a>Siehe auch

[Vorlagenstücklisten](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]