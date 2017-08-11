---
title: "Synchronisierung von Konten aus Sales für Kunden in Finance and Operations"
description: "Das Thema beschreibt die Vorlagen und die grundlegenden Aufgaben, die verwendet werden, um Konten aus Microsoft Dynamics 365 for Sales für Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: b497f078d9786a5c7630e924da6bb04cad37f5e9
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Synchronisierung von Konten aus Sales für Kunden in Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) vertraut sein. 

Das Thema beschreibt die Vorlagen und die grundlegenden Aufgaben, die verwendet werden, um Konten aus Microsoft Dynamics 365 for Sales (Sales) für Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition (Finance and Operations), zu synchronisieren.

## <a name="template-and-task"></a>Vorlage und Aufgabe

Die folgenden Vorlagen und grundlegenden Aufgaben werden für die Synchronisierung von Konten aus Sales für Kunden in Finance and Operations verwendet:

- **Name der Vorlage:** Konten (Sales in Fin and Ops)
- **Name der Aufgabe im Projekt:** Konten – Konto – Kunden

Synchronisierungsaufgaben vor der Synchronisierung von Konto/Kunde: Keine

## <a name="entity-set"></a>Entitätssatz

| Vertrieb    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Konten | Konto | Debitoren              |

## <a name="entity-flow"></a>Entitätsfluss

Konten werden in Sales verwaltet und in Finance and Operations als Kunden synchronisiert. Die Eigenschaft **Is Externally Maintained** dieser Kunden wird auf **Ja** gesetzt, um die Kunden nachzuverfolgen, die aus Sales stammen. Während der Rechnungsstellung werden diese Informationen verwendet, um Rechnungen zu filtern, die für Sales synchronisiert wurden.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

Das Feld **Kontonummer** steht auf der Seite **Konto** zur Verfügung. Es wurde zu einem natürlichen und eindeutigen Schlüssel für die Unterstützung der Integration gemacht. Die natürliche Schlüsselfunktion der Customer Relationship Management (CRM)-Lösung wirkt sich möglicherweise auf Kunden aus, die das Feld **Kontonummer** bereits verwenden, aber keine eindeutigen **Kontonummer**-Werte pro Konto verwenden. Derzeit unterstützt die Integrationslösung diesen Fall nicht.

Wenn ein neues Konto angelegt wird und noch kein **Kontonummer**-Wert vorhanden ist, wird es automatisch unter Verwendung einer fortlaufenden Nummerierung erstellt. Der Wert besteht aus **ACC**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen. Beispiel: **ACC-01000-BVRCPS**

Wenn die Integrationslösung für Sales angewendet wird, füllt ein Upgrade-Skript das Feld **Kontonummer** für in Sales vorhandene Konten aus. Wenn es keine **Kontonummer**-Werte gibt, wird die zuvor beschriebene laufende Nummerierung verwendet.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

- **CustomerGroupId** muss in Finance and Operations aktualisiert werden, um einen gültigen Wert zu enthalten. Sie können einen Standardwert spezifizieren, oder den Wert unter Verwendung einer Wertezuordnung festlegen. Der Standardvorlagenwert ist **10**.
- In Finance and Operations ist ein **Address/Länder/Region-Code** erforderlich. Um Synchronisierungsfehler zu vermeiden, können Sie einen Standardwert vorgeben. Der Standardwert wird verwendet, wenn das Feld in Sales leer geblieben ist.

    - Der Standardvorlagewert für **AddressCountryRegionISOCode** lautet **USA**.
    - Der Standardvorlagewert für **DeliveryAddressCountryRegionISOCode** lautet **USA**.

- Durch Hinzufügen der folgenden Zuordnungen von **CDS &gt; Ziel** können Sie die Anzahl der erforderlichen manuellen Updates in Finance and Operations reduzieren. Sie können einen Standardwert oder eine Wertzuordnung beispielsweise aus **Land/Region** oder **Stadt** verwenden.

    - **SiteId** – Ein Standort ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen zu erstellen. Es kann ein Standardstandort vom Produkt oder vom Kunden aus dem Auftragskopf verwendet werden. Der Standardvorlagewert für **SiteId** lautet **1**.
    - **WarehouseId** – Ein Lager ist erforderlich, um in Finance and Operations Angebots- und Vertriebsauftragspositionen verarbeiten zu können. Es kann ein Standardlager vom Produkt oder vom Kunden aus dem Auftragskopf in Finance and Operations verwendet werden. Der Standardvorlagewert für **WarehouseId** lautet **13**.
    - **LanguageId** – Eine Sprache ist erforderlich, um in Finance and Operations Angebote und Vertriebsaufträge zu erstellen. Standardmäßig wird die Sprache aus dem Auftragskopf des Kunden verwendet. Der Standardvorlagewert für **LanguageId** lautet **en-us**.

- Aktualisieren Sie die CDS Organisations-ID (**Organization_OrganizationId**) in der **Quell &gt; CDS**-Zuordnung. Der Standardvorlagenwert ist **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Vorlagenzuordnung im Datenintegrator

> [!NOTE]
> Die Felder **Zahlungsbedingungen**, **Frachtbedingungen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten. Um diese Felder zuzuordnen, müssen Sie eine Wertzuordnung einrichten. Wertzuordnungen sind spezifisch für die Daten in den Organisationen, zwischen denen die Entität synchronisiert wird.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.

![Vorlagenzuordnung im Datenintegrator](./media/accounts-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung für Konten im Datenintegrator](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Verwandte Themen

[Synchronisierung von Produkten aus Finance and Operations für Produkte in Sales](products-template-mapping.md)

[Synchronisierung von Kontakten aus Sales für Kontakte oder Kunden in Finance and Operations](contacts-template-mapping.md)

[Synchronisierung von Vertriebsangebotsköpfen und -positionen aus Sales für Finance and Operations](sales-quotation-template-mapping.md)



