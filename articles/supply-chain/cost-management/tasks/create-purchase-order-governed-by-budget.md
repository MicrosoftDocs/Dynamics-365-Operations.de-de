---
title: Eine durch das Budget gesteuerte Bestellung erstellen
description: Erstellen Sie mit diesem Verfahren eine Bestellung, die auf einem verfügbaren Budget basiert.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e2bfec4d7d38ef95d1f0ce3bd89938337ecf731
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572048"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Eine durch das Budget gesteuerte Bestellung erstellen

[!include [banner](../../includes/banner.md)]

Erstellen Sie mit diesem Verfahren eine Bestellung, die auf einem verfügbaren Budget basiert. Für diese Aufzeichnung wird das Demo-Datenunternehmen USMF verwendet.


## <a name="review-the-budget-control-configuration"></a>Budgetsteuerungskonfiguration überprüfen.
1. Klicken auf Budgetierung >Einrichtung > Budgetsteuerung > Budgetsteuerungskonfiguration.
2. Klicken Sie auf verfügbare Budgetmittel.
3. Klicken Sie auf die Dokument- und Erfassungsregisterkarte.
4. Klicken Sie auf die Registerkarte Budgetsteuerregel definieren.
5. Klicken Sie auf die Registerkarte Budgetgruppe definieren.
6. Schließen Sie die Seite.

## <a name="create-the-purchase-order-header"></a>Erstellen Sie den Bestellkopf
1. Wechseln Sie zu "Beschaffung" > "Bestellung" > "Alle Bestellungen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Kreditorenkonto" einen Wert ein, oder wählen Sie einen Wert aus.
4. Erweitern Sie den Abschnitt "Allgemein".
5. Wählen Sie im Feld Buchhaltungsdatum das Datum auf 2016-01-01 fest.
6. Klicken Sie auf "OK".

## <a name="add-a-purchase-order-line"></a>Fügen Sie eine Bestellposition hinzu
1. Geben Sie im Feld "Beschaffungskategorie" einen Wert ein oder wählen Sie einen Wert aus.
2. Legen Sie "Menge" auf "2" fest.
3. Geben Sie im Feld 'Einheit' einen Wert ein, oder wählen Sie einen Wert aus.
4. Legen Sie "Preis je Einheit" auf "10000" fest.
5. Klicken Sie auf "Finanzdaten".
6. Verteilungsbeträge anzeigen
7. Geben Sie im Feld "Sachkonto" den Wert 601300-001-023-- an.
8. Schließen Sie die Seite.

## <a name="perform-budget-checking"></a>Budgetprüfung ausführen
1. Klicken Sie auf "Finanzdaten".
2. Budgetprüfung ausführen anklicken.
3. Klicken Sie auf "Finanzdaten".
4. Klicken Sie auf Fehler oder Warnungen der Budgetprüfung anzeigen.
5. Klicken Sie auf "Schließen".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]