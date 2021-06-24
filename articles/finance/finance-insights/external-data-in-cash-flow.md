---
title: Externe Daten in Cashflow-Planungen verwenden (Vorschau)
description: In diesem Thema werden die Einrichtungsschritte beschrieben, die Sie ausführen müssen, damit externe Daten eingegeben oder in Cashflow-Planungen importiert werden können.
author: rcarlson
ms.date: 06/03/2021
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
ms.openlocfilehash: 66bdb8bd638859bb4fc5565e3f12a8f671addcff
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186689"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Externe Daten in Cashflow-Planungen verwenden (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Externe Daten können eingegeben oder in Cashflow-Planungen importiert werden. In diesem Thema werden die Einrichtungsschritte beschrieben, die für die Verwendung externer Daten spezifisch sind und die es ermöglichen, die externen Daten in eine Cashflow-Planung aufzunehmen.

## <a name="external-data-setup"></a>Externe Daten einrichten

Verwenden Sie die **Externe Quelle**-Registerkarte auf der **Einrichtung der Cashflow-Planung**-Seite (**Bargeld- und Bankverwaltung \> Cashflow-Planung**), um Einstellungen einzugeben, die die Verwendung externer Daten in Cashflow-Planungen unterstützen.

Weitere Informationen zum Einrichten finden Sie unter [Cashflow-Planung](../cash-bank-management/cash-flow-forecasting.md).

Um externe Daten für Cashflow-Planungen einzugeben, können Sie die Erfahrung zum Öffnen in Excel zum Eingeben und Ändern externer Daten verwenden. Wählen Sie die Schaltfläche **Externe Daten** und dann entweder **Externe Daten hinzufügen** oder **Vorhandene externe Daten bearbeiten** aus. Wenn die Microsoft Excel-Datei geöffnet ist, können Sie Informationen in die folgenden Felder eingeben:

- **Eintragskennung**
- **Beschreibung** (optional)
- **Name der externen Quelle** – Wählen Sie einen der Werte in der Liste aus, die Sie beim Einrichten von Finance Insights definiert haben.
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
