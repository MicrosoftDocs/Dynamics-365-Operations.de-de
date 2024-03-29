---
title: " Produktpakete für Bestellungen erstellen"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines Produktpakets und seine Verwendung in einer Bestellung.
author: josaw1
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb10164be8d7a0828169cf3865f884afaa2e8408472edebe4cb0c7d4db059d8c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723236"
---
# <a name="create-product-packages-for-purchase-orders"></a> Produktpakete für Bestellungen erstellen

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines Produktpakets und seine Verwendung in einer Bestellung. Die Bestellung wird verwendet, um einen Auftrag für einen vordefinierten Satz Produkte zu erstellen. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.


## <a name="create-a-product-package"></a>Erstellen eines Produktpakets
1. Navigieren Sie zu Einzelhandel und Handel > Lagerverwaltung > Wiederbeschaffung > Produktpakete.
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]