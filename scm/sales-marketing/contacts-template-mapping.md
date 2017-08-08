---
title: "Synchronisierung von Kontakten aus Sales für Kontakte oder Kunden in Finance and Operations"
description: "Dieses Thema beschreibt die Vorlagen und die grundlegenden Aufgaben, die verwendet werden, um Kontakt (Kontakte) und Kontakt (Kunden) aus Microsoft Dynamics 365 for Sales für Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, zu synchronisieren."
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
ms.openlocfilehash: 7a856a9460d092925a34a0733f37f89354c2ddf1
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Synchronisierung von Kontakten aus Sales für Kontakte oder Kunden in Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) vertraut sein. 

Dieses Thema beschreibt die Vorlagen und die grundlegenden Aufgaben, die verwendet werden, um Kontakt-Entitäten (Kontakte) und Kontakt (Kunden) aus Microsoft Dynamics 365 for Sales (Sales) für Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition (Finance and Operations), zu synchronisieren.

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Die folgenden Vorlagen und grundlegenden Aufgaben werden für die Synchronisierung von Kontakt (Kontakte) aus Sales für Kontakt (Kunden) in Finance and Operations verwendet:

- **Namen der Vorlagen:**

    - Kontakte in Kontakt (Sales in Fin und Ops)
    - Kontakte in Kunde (Sales in Fin und Ops)

- **Namen der Aufgaben im Projekt:**

    - Kontakte
    - ContactToCustomer

Vor der Kontaktsynchronisierung muss die folgende Synchronisierungsaufgabe ausgeführt werden: Konten (Sales in Fin and Ops)

## <a name="entity-sets"></a>Entitätssätze

| Vertrieb    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Kontakte | Kontakt | CDS-Kontakte           |
| Kontakte | Konto | Debitoren V2           |

## <a name="entity-flow"></a>Entitätsfluss

Kontakte werden in Sales verwaltet und in Common Data Services (CDS) Finance and Operations synchronisiert.

Ein Kontakt in Sales kann zu einem Kontakt in CDS und Finance and Operations werden. Alternativ kann er zu einem Kontakt in CDS und einem Kunden in Finance and Operations werden. Um festzustellen, ob ein Kontakt aus Sales für die Synchronisierung in CDS und Finance and Operations ausgewählt werden soll (z. B. Kontakte in Sales &gt; Kontakt in CDS &gt; Kontakte in Finance and Operations), überprüft das System die folgenden Eigenschaften von Kontakt in Sales:

- **Synchronisierung auf Konto in CDS und Kunde in Finance and Operations:** Kontakte, wenn **Ist aktiver Kunde** auf **Ja** gesetzt ist
- **Synchronisierung auf Kontakt in CDS und Kontakt in Finance and Operations:** Kontakte, wenn **Ist aktiver Kunde** auf **Nein** gesetzt ist und **Unternehmen** (Übergeordnetes Konto/übergeordneter Kontakt) auf ein Konto (nicht auf einen Kontakt) verweist

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales 

Dem Kontakt wurde ein neues **Ist aktiver Kunde**-Feld hinzugefügt. Das Feld wird genutzt, um Kontakte mit Vertriebsaktivität von Kontakten ohne Vertriebsaktivität zu unterscheiden. **Ist aktiver Kunde** wird nur für Kontakte auf **Ja** gesetzt, für die es Angebote, Bestellungen oder Rechnungen gibt. Nur diese Kontakte werden in Finance and Operations als Kunden synchronisiert.

Dem Kontakt wurde ein neues **IsCompanyAnAccount**-Feld hinzugefügt. Dieses Feld wird verwendet, um anzuzeigen, ob ein Kontakt mit einem Unternehmen (übergeordnetes Konto/übergeordneter Kontakt) des **Konto**-Typs verknüpft ist. Diese Information wird verwendet, um Kontakte zu identifizieren, mit für Finance and Operations als Kontakte synchronisiert werden sollen.

Dem Kontakt wurde ein neues **Kontaktnummer**-Feld hinzugefügt, um sicherzustellen, dass ein natürlicher und eindeutiger Schlüssel für die Integration bereitsteht. Wenn ein neuer Kontakt angelegt wird, wird automatisch ein **Kontaktnummer**-Wert unter Verwendung einer fortlaufenden Nummerierung erstellt. Der Wert besteht aus **CON**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen. Beispiel: **CON-01000-BVRCPS**

Wenn Sales die Integrationslösung für Sales hinzugefügt wird, füllt ein Upgrade-Skript das Feld **Kontaktnummer** für vorhandene Kontakte unter Verwendung der oben genannten fortlaufenden Nummerierung aus. Außerdem setzt das Upgrade-Skript das Feld **Ist aktiver Kunde** für alle Kontakte mit Vertriebsaktivität auf **Ja**.

## <a name="in-finance-and-operations"></a>In Finance and Operations 

Kontakte werden mit der Eigenschaft **IsContactPersonExternallyMaintained** gekennzeichnet. Diese Eigenschaft zeigt an, das ein Kontakt extern verwaltet wird. In diesem Fall werden extern verwaltete Kontakte in Sales verwaltet.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

### <a name="contact-to-contact"></a>Kontakt zu Kontakt

- Aktualisieren Sie die **CDS-Organisations-ID** in der **Quell &gt; CDS**-Zuordnung.

    - Der Standardvorlagewert für **Organization_OrganizationId [Organisations-ID]** lautet **ORG001**.
    - Der Standardvorlagewert für **PrimaryAccount_Organization_OrganizationId [Organisations-ID]** lautet **ORG001**.

- In Finance and Operations ist ein **Address/Länder/Region-Code** erforderlich. Um Synchronisierungsfehler zu vermeiden, können Sie in der **CDS &gt; Operations**-Zuordnung einen Standardwert vorgeben. Der Standardwert wird verwendet, wenn das Feld in Sales leer geblieben ist. Der Standardvorlagewert für **PrimaryAddressCountryRegionISOCode** lautet **USA**.
- Stellen Sie sicher, dass in Finance and Operations ein Wert für die folgenden Felder vorhanden ist. In Finance and Operations ist die Information nicht erforderlich, Sie können die Zuordnung aus der **CDS &gt; Ziel**-Zuordnung entfernen.

    - **Feldname in Finance and Operations:** Entscheidung
    - **Zuordnung:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Kontakt zu Kunde

- Aktualisieren Sie die **CDS-Organisations-ID** in der **Quell &gt; CDS**-Zuordnung. Der Standardvorlagewert für **Organization_OrganizationId [Organisations-ID]** lautet **ORG001**.
- In Finance and Operations ist ein **Address/Länder/Region-Code** erforderlich. Um Synchronisierungsfehler zu vermeiden, können Sie in der **CDS &gt; Ziel**-Zuordnung einen Standardwert vorgeben. Der Standardwert wird verwendet, wenn das Feld in Sales leer geblieben ist. Der Standardvorlagewert für **PrimaryAddressCountryRegionISOCode** lautet **USA**.
- **CustomerGroup** ist in Finance and Operations erforderlich. Um Synchronisierungsfehler zu vermeiden, können Sie in der **CDS &gt; Ziel**-Zuordnung einen Standardwert vorgeben. Der Standardwert wird verwendet, wenn das Feld in Sales leer geblieben ist. Der Standardvorlagewert für **CustomerGroupId** lautet **10**.
- Durch Hinzufügen der folgenden Zuordnungen von **CDS &gt; Ziel** können Sie die Anzahl der manuellen Updates in Finance and Operations reduzieren. Sie können einen Standardwert oder eine Wertzuordnung beispielsweise aus **Land/Region** oder **Stadt** verwenden.

    - **SiteId** – Für Produkte in Finance and Operations kann auch eine Standardstandort definiert werden. Ein Standort ist erforderlich, um in Finance and Operations Angebote und Vertriebsaufträge zu erstellen. Für **SiteId** ist kein Vorlagenwert definiert.
    - **WarehouseId** – Für Produkte in Finance and Operations kann auch ein Standardlager definiert werden. Ein Lager ist erforderlich, um in Finance and Operations Angebote und Vertriebsaufträge zu erstellen. Für **WarehouseId** ist kein Vorlagenwert definiert.
    - **LanguageId** – Eine Sprache ist erforderlich, um in Finance and Operations Angebote und Vertriebsaufträge zu erstellen. Der Standardvorlagewert für **LanguageId** lautet **en-us**.

## <a name="template-mapping-in-data-integrator"></a>Vorlagenzuordnung im Datenintegrator

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.

### <a name="contact-to-contact"></a>Kontakt zu Kontakt

![Vorlagenzuordnung im Datenintegrator](./media/contacts-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung für Kontakte im Datenintegrator](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Kontakt zu Kunde

![Vorlagenzuordnung im Datenintegrator](./media/contacts-template-mapping-data-integrator-3.png)

![Vorlagenzuordnung für Kontakte im Datenintegrator](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Verwandte Themen

[Synchronisierung von Produkten aus Finance and Operations für Produkte in Sales](products-template-mapping.md)

[Synchronisierung von Konten aus Sales für Kunden in Finance and Operations](accounts-template-mapping.md)

[Synchronisierung von Vertriebsangebotsköpfen und -positionen aus Sales für Finance and Operations](sales-quotation-template-mapping.md)

