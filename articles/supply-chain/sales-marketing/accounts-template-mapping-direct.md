---
title: Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgaben, die verwendet werden, um die Konten aus Dynamics 365 Sales mit Supply Chain Management zu synchronisieren.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 270d83552a3e35042c32cb85888439d40068ff0c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355948"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Integration von Daten in Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator) vertraut sein.

Dieses Thema beschreibt die Vorlagen und die zugrunde liegende Aufgaben, die verwendet werden, um Konten direkt aus Dynamics 365 Sales mit Dynamics 365 Supply Chain Management zu synchronisieren.

## <a name="data-flow-in-prospect-to-cash"></a>Datenfluss in Interessent nach Bargeld

Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Supply Chain Management und Sales hinweg zu synchronisieren.  Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Supply Chain Management und Sales. Die folgende Abbildung zeigt, wie Daten zwischen Supply Chain Management und Sales synchronisiert werden.

[![Datenfluss in Interessent nach Bargeld.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [Power Apps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration). Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.

Die folgende Vorlage und grundlegende Aufgabe werden für die Synchronisierung von Konten aus Sales in Supply Chain Management verwendet:

- **Name der Vorlage in der Datenintegration:** Konten (Sales zu Finance and Operations) - direkt
- **Name der Aufgabe im Projekt:** Konten – Kunden

Keine Synchronisierungsaufgaben sind erforderlich, damit Konto-Kunde-Synchronisierung auftreten kann.

## <a name="entity-set"></a>Entitätssatz

| Verk.    | Lieferkettenverwaltung |
|----------|------------------------|
| Konten | Debitoren V2           |

## <a name="entity-flow"></a>Entitätsfluss

Konten werden in Sales verwaltet und mit Supply Chain Management als Kunden synchronisiert. Die Eigenschaft **Is Externally Maintained** dieser Kunden wird auf **Ja** gesetzt, um die Kunden nachzuverfolgen, die aus Sales stammen. Während der Rechnungsstellung werden diese Informationen verwendet, um Rechnungen zu filtern, die für Sales synchronisiert wurden.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

Die Spalte **Kontonummer** steht auf der Seite **Konto** zur Verfügung. Es wurde zu einem natürlichen und eindeutigen Schlüssel für die Unterstützung der Integration gemacht. Die natürliche Schlüsselfunktion der Customer Relationship Management (CRM)-Lösung wirkt sich möglicherweise auf Kunden aus, die die Spalte **Kontonummer** bereits verwenden, aber keine eindeutigen **Kontonummer**-Werte pro Konto verwenden. Derzeit unterstützt die Integrationslösung diesen Fall nicht.

Wenn ein neues Konto angelegt wird und noch kein **Kontonummer**-Wert vorhanden ist, wird es automatisch unter Verwendung einer fortlaufenden Nummerierung erstellt. Der Wert besteht aus **ACC**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen. Beispiel: **ACC-01000-BVRCPS**

Wenn die Integrationslösung für Sales angewendet wird, füllt ein Upgrade-Skript die Spalte **Kontonummer** für in Sales vorhandene Konten aus. Wenn es keine **Kontonummer**-Werte gibt, wird die zuvor beschriebene laufende Nummerierung verwendet.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

- Die **CustomerGroupId**-Zuordnung muss in Supply Chain Management aktualisiert werden, um einen gültigen Wert zu enthalten. Sie können einen Standardwert spezifizieren, oder den Wert unter Verwendung einer Wertezuordnung festlegen.

    Der Standardvorlagenwert ist **10**.

- Durch Hinzufügen der folgenden Zuordnungen können Sie die Anzahl der erforderlichen manuellen Updates in Supply Chain Management reduzieren. Sie können einen Standardwert oder eine Wertzuordnung beispielsweise aus **Land/Region** oder **Stadt** verwenden.

    - **SiteId** – Ein Standort ist erforderlich, um in Supply Chain Management Angebots- und Vertriebsauftragspositionen zu erstellen. Es kann ein Standardstandort vom Produkt oder vom Kunden aus dem Auftragskopf verwendet werden.

        Der Standardvorlagenwert ist **1**.

    - **WarehouseId** – Ein Lager ist erforderlich, um in Supply Chain Management Angebots- und Vertriebsauftragspositionen verarbeiten zu können. Es kann ein Standardlager vom Produkt oder vom Kunden aus dem Auftragskopf in Supply Chain Management verwendet werden.

        Der Standardvorlagenwert ist **13**.

    - **LanguageId** – Eine Sprache ist erforderlich, um in Supply Chain Management Angebote und Aufträge zu erstellen. Standardmäßig wird die Sprache aus dem Auftragskopf des Kunden verwendet.

        Der Standardvorlagewert lautet **en-us**.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

> [!NOTE]
> Die Spalten **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten. Um diese Spalten zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die für die Daten in den Organisationen, zwischen denen die Tabelle synchronisiert wird, spezifisch ist.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration. 

> [!NOTE]
> Die Zuordnung zeigt, welche Spalteninformationen von Sales zu Supply Chain Management synchronisiert werden.

![Vorlagenzuordnung in Datenintegration.](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Verwandte Themen


[Prospect-to-Cash](prospect-to-cash.md)

[Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren](accounts-template-mapping-direct.md)

[Kontakte direkt von Sales mit Kontakten oder Debitoren in Supply Chain Management synchronisieren](contacts-template-mapping-direct.md)

[Synchronisieren von Aufträgen direkt zwischen Sales und Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Rechnungskopfzeilen und ‑positionen direkt von Supply Chain Management zu Sales synchronisieren](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]