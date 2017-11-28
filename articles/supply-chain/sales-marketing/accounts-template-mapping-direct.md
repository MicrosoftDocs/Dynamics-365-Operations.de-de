---
title: Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren
description: "Dieses Thema beschreibt die Vorlagen und die grundlegenden Aufgaben, die verwendet werden, um Konten aus Microsoft Dynamics 365 for Sales für Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 16bbca2d9eb8c3d9c33752404ebecbe4415517a2
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration) vertraut sein.

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Konten direkt aus Microsoft Dynamics 365 for Sales nach Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition zu synchronisieren.

## <a name="data-flow-in-prospect-to-cash"></a>Datenfluss in Interessent nach Bargeld

Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Finance and Operations und Sales hinweg zu synchronisieren.  Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales. Die folgende Abbildung zeigt, wie Daten zwischen Finance and Operations und Sales synchronisiert werden.

[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [PowerApps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration). Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.

Die folgende Vorlage und grundlegenden Aufgabe werden für die Synchronisierung von Konten aus Sales für Kunden in Finance and Operations verwendet:

- **Name der Vorlage in der Datenintegration:** Konten (Sales zu Finance and Operations) - direkt
- **Name der Aufgabe im Projekt:** Konten – Kunden

Keine Synchronisierungsaufgaben sind erforderlich, damit Konto-Kunde-Synchronisierung auftreten kann.

## <a name="entity-set"></a>Entitätssatz

| Vertrieb    | Finance and Operations |
|----------|------------------------|
| Konten | Debitoren V2           |

## <a name="entity-flow"></a>Entitätsfluss

Konten werden in Sales verwaltet und in Finance and Operations als Kunden synchronisiert. Die Eigenschaft **Is Externally Maintained** dieser Kunden wird auf **Ja** gesetzt, um die Kunden nachzuverfolgen, die aus Sales stammen. Während der Rechnungsstellung werden diese Informationen verwendet, um Rechnungen zu filtern, die für Sales synchronisiert wurden.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

Das Feld **Kontonummer** steht auf der Seite **Konto** zur Verfügung. Es wurde zu einem natürlichen und eindeutigen Schlüssel für die Unterstützung der Integration gemacht. Die natürliche Schlüsselfunktion der Customer Relationship Management (CRM)-Lösung wirkt sich möglicherweise auf Kunden aus, die das Feld **Kontonummer** bereits verwenden, aber keine eindeutigen **Kontonummer**-Werte pro Konto verwenden. Derzeit unterstützt die Integrationslösung diesen Fall nicht.

Wenn ein neues Konto angelegt wird und noch kein **Kontonummer**-Wert vorhanden ist, wird es automatisch unter Verwendung einer fortlaufenden Nummerierung erstellt. Der Wert besteht aus **ACC**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen. Beispiel: **ACC-01000-BVRCPS**

Wenn die Integrationslösung für Sales angewendet wird, füllt ein Upgrade-Skript das Feld **Kontonummer** für in Sales vorhandene Konten aus. Wenn es keine **Kontonummer**-Werte gibt, wird die zuvor beschriebene laufende Nummerierung verwendet.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

- Die **CustomerGroupId**-Zuordnung muss in Finance and Operations aktualisiert werden, um einen gültigen Wert zu enthalten. Sie können einen Standardwert spezifizieren, oder den Wert unter Verwendung einer Wertezuordnung festlegen.

    Der Standardvorlagenwert ist **10**.

- Durch Hinzufügen der folgenden Zuordnungen können Sie die Anzahl der erforderlichen manuellen Updates in Finance and Operations reduzieren. Sie können einen Standardwert oder eine Wertzuordnung beispielsweise aus **Land/Region** oder **Stadt** verwenden.

    - **SiteId** – Ein Standort ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen zu erstellen. Es kann ein Standardstandort vom Produkt oder vom Kunden aus dem Auftragskopf verwendet werden.

        Der Standardvorlagenwert ist **1**.

    - **WarehouseId** – Ein Lager ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen verarbeiten zu können. Es kann ein Standardlager vom Produkt oder vom Kunden aus dem Auftragskopf in Finance and Operations verwendet werden.

        Der Standardvorlagenwert ist **13**.

    - **LanguageId** – Eine Sprache ist erforderlich, um in Finance and Operations Angebote und Vertriebsaufträge zu erstellen. Standardmäßig wird die Sprache aus dem Auftragskopf des Kunden verwendet.

        Der Standardvorlagewert lautet **en-us**.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

> [!NOTE]
> Die Felder **Zahlungsbedingungen**, **Frachtbedingungen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten. Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration. 

> [!NOTE]
> Die Zuordnung zeigt, welche Feldinformationen von Sales zu Finance and Operations synchronisiert werden.

![Vorlagenzuordnung in Datenintegration](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Verwandte Themen


[Interessent zu Bargeld](prospect-to-cash.md)

[Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren](accounts-template-mapping-direct.md)

[Kontakte direkt von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren](contacts-template-mapping-direct.md)

[Auftragskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren](sales-order-template-mapping-direct.md)

[Verkaufsrechnungskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren](sales-invoice-template-mapping-direct.md)


