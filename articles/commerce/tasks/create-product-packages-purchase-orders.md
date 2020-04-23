---
title: " Produktpakete für Bestellungen erstellen"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines Produktpakets und seine Verwendung in einer Bestellung.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b0084c6b4acbf14e3afec552575d5be26114237
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141361"
---
# <a name="create-product-packages-for-purchase-orders"></a> Produktpakete für Bestellungen erstellen

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines Produktpakets und seine Verwendung in einer Bestellung. Die Bestellung wird verwendet, um einen Auftrag für einen vordefinierten Satz Produkte zu erstellen. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.


## <a name="create-a-product-package"></a>Erstellen eines Produktpakets
1. Navigieren Sie zu Retail und Commerce > Lagerverwaltung > Wiederbeschaffung > Produktpakete.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Paketnummer" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie auf Hinzufügen.
8. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0160" ein.
9. Klicken Sie im Feld "Größe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
10. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
11. Geben Sie im Feld "Menge" eine Zahl ein.
12. Klicken Sie auf Hinzufügen.
13. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0160" ein.
14. Klicken Sie im Feld "Variantennummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
15. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
16. Geben Sie im Feld "Menge" eine Zahl ein.
17. Klicken Sie auf Hinzufügen.
18. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0175" ein.
19. Geben Sie im Feld "Menge" eine Zahl ein.
20. Klicken Sie auf "Speichern".
21. Schließen Sie die Seite.

## <a name="add-package-to-purchase-order"></a>Hinzufügen eines Pakets zur Bestellung
1. Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".
2. Klicken Sie auf "Neu".
3. Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Wählen Sie in der Liste den gleichen Kreditor aus, für den das Produktpaket zuvor erstellt wurde, wenn ein Kreditor ausgewählt wurde.
5. Schalten Sie die Erweiterung des Abschnitts "Allgemein" ein/aus.
6. Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
10. Klicken Sie auf "OK".
11. Schalten Sie die Erweiterung des Abschnitts "Positionsdetails" ein/aus.
12. Klicken Sie auf die Produktpaketregisterkarte.
13. Klicken Sie auf die Bestellposition.
14. Klicken Sie auf "Positionen aus Paket erstellen".
15. Wählen Sie in der Liste das Produktpaket aus, das im vorherigen Schritt erstellt wurde.
16. Geben Sie im Feld "Menge" eine Zahl ein.
17. Klicken Sie auf "Erstellen".
18. Klicken Sie auf "Speichern".
