---
title: Erstellen eines standardmäßigen Produktlebenszyklus-Status
description: Diese Prozedur zeigt, wie ein standardmäßiger Produktlebenszyklus-Status erstellt wird und wie der standardmäßige Status den freigegebenen Produkten zugeordnet wird.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a628ed2b609f48c22076f409889c212e4d9463ac
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578199"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]