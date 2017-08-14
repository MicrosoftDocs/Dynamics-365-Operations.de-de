---
title: Synchronisieren von Produkten aus Finance und Operations mit Produkten in Sales
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte aus Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren."
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
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Synchronisieren von Produkten aus Finance und Operations mit Produkten in Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Damit Sie die Prospect to Cash-Lösung verwenden können, müssen Sie mit [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) vertraut sein. 

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte aus Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren.

## <a name="template-and-task"></a>Vorlage und Aufgabe

Die folgenden Vorlagen und zugrunde liegenden Aufgaben, die verwendet werden, um Produkte aus Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations), mit Microsoft Dynamics 365 for Sales (Sales) zu synchronisieren.

-   Name der Vorlage: Produkte (Finance and Operations nach Sales)

-   Name de Aufgabe im Projekt: Produkte

Synchronisierungsaufgaben, die vor der Produktsynchronisierung erforderlich sind: keine

## <a name="entity-set"></a>Entitätssatz

| **Finance and Operations** | **CDS** | **Verkäufe**  |
|----------------------------|---------|------------|
| Freigegebene Produkte für Verkauf | Produkt | Produkte   |

## <a name="entity-flow"></a>Entitätsfluss

Produkte werden in Finance and Operations verwaltet und mit Sales synchronisiert. Die Datenentität **Verkäufliche freigegebene Produkte** in Finance and Operations exportiert nur Produkte, die verkäuflich sind. Das bedeutet, dass Produkte die erforderlichen Informationen enthalten, die in einem Auftrag verwendet werden müssen. Die gleichen Regeln gelten, wenn ein Produkt mit der Funktion **Überprüfen** auf der Seite **Freigegebenes Produkt** überprüft wird.

Die **Produktnummer** wird als Schlüssel verwendet. Das heißt, dass Produktvarianten mit CDS und Sales mit einzelnen **Produkt-IDs** pro **Produktvariante** synchronisiert werden.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

In Sales wird ein neues Feld bei den Produkten **Wird extern verwaltet** hinzugefügt, um anzugeben, dass ein bestimmtes Produkt extern verwaltet wird. Der Wert wird beim Import nach Sales standardmäßig auf **Ja** festgelegt.

-   **Wird extern verwaltet = Ja**: Produkt hat in Finance and Operations seinen Ursprung und kann in Sales nicht bearbeitet werden.

-   **Wird extern verwaltet = nein**: Produkt wird direkt in Sales eingegeben.

-   **Wird extern verwaltet = leer**: Produkt ist in Sales vorhanden, bevor die Lösung „Interessent zu Bargeld” aktiviert wird.

Die Informationen **Wird extern verwaltet** werden verwendet, um sicherzustellen, dass nur **Angebote** und **Aufträge** mit **Extern verwalteten Produkten** mit Finance and Operations synchronisiert werden.

**Extern verwaltete Produkte** werden automatisch der ersten gültigen **Preisliste** mit derselben Währung hinzugefügt. Beachten Sie, dass die Liste alphabetisch nach **Name** sortiert wird. Der Produktverkaufspreis von Finance and Operations wird als Preis in der **Preisliste** verwendet. Das bedeutet, dass es erforderlich ist, eine **Preisliste** in Sales für jede **Produktverkaufswährung** in Finance and Operations zu haben. Die Währung für die freigegebenen verkäuflichen Produkte ist auf die Buchhaltungswährung in der juristischen Person festgelegt, von der das Produkt exportiert wird.

> [!NOTE]
> Produktsynchronisierung ist ohne eine **Preisliste** mit der übereinstimmenden Währung nicht erfolgreich.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

-   Bevor Sie die allererste Synchronisierung ausführen, müssen Sie die **Tabelle eindeutig identifizierbarer Produkte** für vorhandene Produkte in Finance and Operations auffüllen. Vorhandene Produkte werden nicht synchronisiert, bis der Einzelvorgang abgeschlossen ist.

    -   In Finance and Operations verwenden Sie Suche, um nach **Tabelle eindeutig identifizierbarer Produkte auffüllen** zu suchen.

    -   Klicken Sie auf **Tabelle eindeutig identifizierbarer Produkte auffüllen**, um den Einzelvorgang auszuführen. Dieser Einzelvorgang muss nur einmal ausgeführt werden.

-   Stellen Sie sicher, dass die erforderliche **ValueMap** für den Verkauf von **Maßeinheit** (ME) in Finance and Operations vorhanden ist in der **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.

-   Stellen Sie sicher, dass **Dezimalstellen unterstützt** für ME Ihren Anfordernungen in **CDS -\> Destination** entspricht. Wenn Sie andere Werte pro ME benötigen, kann dies mit **ValueMap** von Einheit erfolgen, beispielsweise [Each : 0] & [Pound : 2].

    -   Vorlagenwert ist standardmäßig auf 0 festgelegt.

-   Aktualisieren Sie die **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.

    -   Vorlagenwert ist standardmäßig auf ORG001 festgelegt.

-   Aktualisieren Sie **ValueMap** für **Einheitengruppe** (**defaultuomscheduleid.name**) in **CDS -\> Destination**, um der **Einheitengruppe** in Sales zu entsprechen.

    -   Vorlagenwert ist standardmäßig auf **Standardeinheit** festgelegt.

-   Stellen Sie sicher, dass alle Maßseinheiten für Produktverkäufe von Finance and Operations in Sales mit dem Wert **CDS-Entnahmelisten** vorhanden sind.

-   Vergewissern Sie sich, dass **Preislisten** in Sales für jede Produktverkaufswährung in Finance and Operations vorhanden sind.

-   Produkte können in Sales mit dem Status **Entwurf** oder **Aktiv** erstellt werden. Dies wird in **Systemeinstellungen** unter **Vertrieb** in Sales gesteuert.

    -   Produkte, die mit Entwurfsstatus erstellt werden, müssen aktiviert werden, bevor Sie zu **Angebot** oder **Auftrag** hinzugefügt werden.

## <a name="template-mapping-in-data-integrator"></a>Vorlagenzuordnung im Datenintegrator

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.

![Vorlagenzuordnung im Datenintegrator](./media/products-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung für Produkte im Datenintegrator](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Verwandte Themen

[Synchronisierung von Konten aus Sales für Kunden in Finance and Operations](accounts-template-mapping.md)

[Synchronisierung von Kontakten aus Sales für Kontakte oder Kunden in Finance and Operations](contacts-template-mapping.md)

[Synchronisierung von Vertriebsangebotsköpfen und -positionen aus Sales für Finance and Operations](sales-quotation-template-mapping.md)


