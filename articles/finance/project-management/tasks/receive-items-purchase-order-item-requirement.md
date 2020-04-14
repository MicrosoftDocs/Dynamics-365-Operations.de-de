---
title: Artikel zu Bestellung aus Artikelbedarf empfangen
description: In diesem Thema wird erläutert, wie Sie Artikel auf einer Bestellung von einem Artikelbedarf erhalten.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f288a47f952a30d98a4a5b96409dc53f880d41d
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139055"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Artikel zu Bestellung aus Artikelbedarf empfangen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Artikel auf einer Bestellung von einem Artikelbedarf erhalten.

Durch die Verwendung eines Artikelbedarfs anstelle einer Artikelbuchung kann die Lieferung direkt vor der tatsächlichen Verwendung der Artikel geplant werden. Sie können eine Bestellung erstellen, den Artikel in der Handelsvereinbarung berücksichtigen und den Artikelbedarf in die Produktionsplanung einbeziehen. 

Diese Aufgabe verwendet das USSI-Dataset.

1. Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und Rechnungswesen > Projekte > Alle Projekte**.
2. Wählen Sie in der Liste den Link in der gewünschten Zeile aus.
3. Wählen Sie im Aktivitätsbereich **Plan** aus.
4. Wählen Sie **Artikelanforderungen**.
5. Wählen Sie **Neu** aus.
6. Geben Sie in der neuen Zeile einen Wert im Feld **Artikelnummer** ein oder wählen Sie ihn aus.
7. Geben Sie im Feld **Menge** eine Zahl ein.
8. Wählen Sie **Speichern**.
9. Wählen Sie im Aktionsbereich **Management**.
10. Wählen Sie **Funktionen**.
11. Wählen Sie **Bestellung anlegen**.
12. Aktivieren Sie das Kontrollkästchen **Alle einbeziehen**.
13. Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus.
14. Wählen Sie **OK**.
15. Gehen Sie im Navigationsbereich zu **Module > Kreditorenbuchhaltung > Bestellungen > Alle Bestellungen**.
16. Wählen Sie in der Liste den Link in der gewünschten Zeile aus.
17. Wählen Sie im Aktivitätsbereich **Einkauf** aus.
18. Wählen Sie **Bestätigen** aus.
19. Wählen Sie im Aktivitätsbereich **Wareneingang** aus.
20. Wählen Sie **Produktzugang** aus.
21. Geben Sie im Feld **Produktzugang** einen Wert ein.
22. Wählen Sie **OK**.

