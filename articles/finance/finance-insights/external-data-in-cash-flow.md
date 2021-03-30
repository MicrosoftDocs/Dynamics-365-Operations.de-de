---
title: Externe Daten in Cashflow-Planungen verwenden (Vorschau)
description: In diesem Thema werden die Einrichtungsschritte beschrieben, die Sie ausführen müssen, damit externe Daten eingegeben oder in Cashflow-Planungen importiert werden können.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 03318eaae0b3329dc758c48202f8f47ca2c4ab08
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245567"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Externe Daten in Cashflow-Planungen verwenden (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Externe Daten können eingegeben oder in Cashflow-Planungen importiert werden. In diesem Thema werden die Einrichtungsschritte beschrieben, die für die Verwendung externer Daten spezifisch sind und die es ermöglichen, die externen Daten in eine Cashflow-Planung aufzunehmen.

## <a name="external-data-setup"></a>Externe Daten einrichten

Verwenden Sie die **Externe Quelle**-Registerkarte auf der **Einrichtung der Cashflow-Planung**-Seite (**Bargeld- und Bankverwaltung \> Cashflow-Planung**), um Einstellungen einzugeben, die die Verwendung externer Daten in Cashflow-Planungen unterstützen.

Weitere Informationen zum Einrichten finden Sie unter [Cashflow-Planung](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).

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

#### <a name="privacy-notice"></a>Datenschutzhinweis
Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]