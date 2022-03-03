---
title: Externe Daten in Cashflow Planungen
description: In diesem Thema werden die Einrichtungsschritte beschrieben, die Sie durchführen müssen, damit externe Daten eingegeben oder in Cashflow-Planungen importiert werden können.
author: rcarlson
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23342114c25cd1b59d47aa7ce63f09de029fa690
ms.sourcegitcommit: 465c84eb5cdc211692e2ae09b45d1400f9a315ee
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8314707"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Externe Daten in Cashflow Planungen

[!include [banner](../includes/banner.md)]

Externe Daten können eingegeben oder in Cashflow-Planungen importiert werden. In diesem Thema werden die Einrichtungsschritte beschrieben, die für die Verwendung externer Daten spezifisch sind und die es ermöglichen, die externen Daten in eine Cashflow-Planung aufzunehmen.

## <a name="external-data-setup"></a>Externe Daten einrichten

Verwenden Sie die **Externe Quelle**-Registerkarte auf der Einrichtung der **Cashflow-Planung**-Seite (**Bargeld- und Bankverwaltung \> Cashflow-Planung \> Cashflow-Planungssetup**), um Einstellungen einzugeben, die die Verwendung externer Daten in Cashflow-Planungen unterstützen.

Externe Daten können eingegeben oder in Cashflow-Planungen importiert werden. Bevor externe Daten eingegeben oder importiert werden, müssen externe Quellen eingerichtet werden. Richten Sie auf der Registerkarte **Externe Quelle** externe Cashflow-Kategorien ein. Eine Kategorie kann entweder **ausgehend** oder **eingehend** sein. **Liquidität** sollte als Buchungsart gewählt werden. Wählen Sie im Raster **Einstellungen juristische Person** wählen Sie die juristischen Personen und die entsprechenden Hauptkonten aus, für die die externen Cashflow-Kategorien gelten.

Weitere Informationen dazu, wie Cashflow-Planungen eingerichtet wird, finden Sie unter [Cashflow-Planung](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Externe Daten eingeben

Um externe Daten für Cashflow-Planungen einzugeben und zu ändern, können Sie die Umgebung zum **Öffnen in Excel** verwenden. Wählen Sie die Schaltfläche **Externe Daten** auf der Seite des Arbeitsbereichs der **Cashflow-Planungseinstellung** und dann entweder **Externe Daten hinzufügen** oder **Vorhandene externe Daten bearbeiten** aus. Wenn die Microsoft Excel-Datei geöffnet ist, können Sie Informationen in die folgenden Felder eingeben:

- **Eintragskennung** (eindeutig)
- **Beschreibung** (optional)
- **Name der externen Quelle**: Wählen Sie einen der Werte in der Liste aus, die Sie beim Einrichten von Finance Insights definiert haben.
- **Juristische Person**
- **Datum**
- **Betrag in Buchungswährung**
- **Währungscode**
- **Standarddimension** (Optional)
- **Dokumentnummer** (Optional)
- **Kontonummer** (Optional)
- **Kontoname** (Optional)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Importieren externer Daten mithilfe des Datenverwaltungsframeworks

Sie können externe Daten für Cashflow-Planungen mithilfe des **Datenverwaltung**-Arbeitsbereichs und der Entität namens **Cashflow-Planung – externer Quelleneintrag** importieren.

Wenn Sie Einrichtungsdaten von einer Umgebung in eine andere verschieben müssen, steht außerdem der folgende Entitätsbereich für die erforderlichen Einrichtungstabellen zur Verfügung:

- Einrichtung der externen Quelle für Cashflow-Planung
- Einrichtung der juristischen Person für externe Quelle für Cashflow-Planung

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
