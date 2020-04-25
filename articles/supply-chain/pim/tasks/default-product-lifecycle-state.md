---
title: Erstellen eines standardmäßigen Produktlebenszyklus-Status
description: Diese Prozedur zeigt, wie ein standardmäßiger Produktlebenszyklus-Status erstellt wird und wie der standardmäßige Status den freigegebenen Produkten zugeordnet wird.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd346f338a14476960ab47db2e3013402f4c43af
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213169"
---
# <a name="create-a-default-product-lifecycle-state"></a>Erstellen eines standardmäßigen Produktlebenszyklus-Status

[!include [banner](../../includes/banner.md)]

Diese Prozedur zeigt, wie ein standardmäßiger Produktlebenszyklus-Status erstellt wird und wie der standardmäßige Status den freigegebenen Produkten zugeordnet wird.


## <a name="create-a-default-lifecycle-state"></a>Erstellen eines standardmäßigen Lebenszyklusstatus
1. Wechseln Sie zu Produktinformationsverwaltung > Einstellungen > Produktlebenszyklus-Status.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld „Status” einen Wert ein.
4. Wählen Sie „Ja” im Feld „Standard, wenn für juristische Person freigegeben” aus.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Wählen Sie „Nein” im Feld „Ist aktiv für Planung” aus.

> [!NOTE]
> Wenn ein neues freigegebenes Produkt nicht in den Produktprogrammplan einbezogen werden soll, wählen Sie „Nein” aus. Wenn es in den Produktprogrammplan einbezogen werden soll, belassen Sie das Steuerelement beim Standardwert „Ja”.  

## <a name="create-a-new-released-product"></a>Neues freigegebenes Produkt erstellen
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".
3. Klicken Sie auf "Neu".
4. Geben Sie im Feld "Produktnummer" einen Wert ein.
5. Geben Sie im Feld "Produktname" einen Wert ein.
6. Geben Sie im Feld „Suchname” einen Wert ein.
7. Geben Sie im Feld "Artikelmodellgruppe" einen Wert ein oder wählen Sie einen Wert aus.
8. Geben Sie im Feld "Artikelgruppe" einen Wert ein oder wählen Sie einen Wert aus.
9. Geben Sie im Feld "Lagerdimensionsgruppe" einen Wert ein oder wählen Sie einen Wert aus.
10. Geben Sie im Feld "Rückverfolgungsangabengruppe" einen Wert ein oder wählen Sie einen Wert aus.
11. Klicken Sie auf "OK".

> [!NOTE]
> Der standardmäßige Produktlebenszyklus-Status ist eine globale Definition.  

## <a name="change-the-product-to-an-active-state"></a>Produkt zu aktivem Status ändern
1. Geben Sie im Feld „Produktlebenszyklus-Status” einen Wert ein, oder wählen Sie einen Wert aus.

> [!NOTE]
> Angenommen, Sie haben einen aktiven Status eingerichtet, dann können Sie jetzt den aktiven Status auswählen, um zuzulassen, dass das Produkt im Produktprogrammplan und der Stücklistenberechnung verwendet wird. Offensichtlich ist dies nur sinnvoll, wenn alle Produktdetails, die für eine konsistente Planung erforderlich sind, angegeben sind.  

