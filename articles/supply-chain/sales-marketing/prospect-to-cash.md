---
title: Interessent zu Bargeld
description: Dieses Thema enthält einen Überblick der Prospect to Cash-Lösung zwischen Microsoft Dynamics 365 for Finance and Operationsund Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b46ece384a28f8e78989253fcf467fbf3feaf1b7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "309494"
---
# <a name="prospect-to-cash"></a>Interessent zu Bargeld

[!include [banner](../includes/banner.md)]

Die Prospect to Cash-Lösung bietet direkte Synchronisierung zwischen Dynamics 365 for Finance and Operationsund Dynamics 365 for Sales. Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales. Während die Daten zwischen Finance and Operations und Sales fließen, können Sie Vertriebs- und Marketingaktivitäten zwischen Finance and Operations und Sales ausführen und die Auftagserfüllung mit Bestandsverwaltung in Finance and Operations handhaben. 

Für weitere Informationen über die Integration Prospect to Cash sehen Sie sich das kurze YouTube-Video an: [Integration von Prospect to Cash](https://www.youtube.com/watch?v=AVV9x5x-XCg).

In der aktuellen Version enthält die Interessent in Bargeldlösung die folgenden Typen der direkten Synchronisierung:

- [Konten in Sales verwalten und direkt cvon Sales zu Finance and Operations synchronisieren](accounts-template-mapping-direct.md)
- [Produkte in Finance and Operations verwalten und direkt mit Sales synchronisieren](products-template-mapping-direct.md)
- [Kontakte in Sales verwalten und direkt mit Kontakten oder Debitoren in Finance and Operations synchronisieren](contacts-template-mapping-direct.md)
- [Synchronisieren von Verkaufsangeboten direkt von Sales mit Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Synchronisieren von Aufträgen direkt zwischen Sales und Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [Synchronisieren von Verkaufsrechnungen direkt von Finance and Operations mit Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a>Systemanforderungen für Finance and Operations
„Interessent zu Bargeld”-Integration wird in den folgenden Versionen unterstützt:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (Dezember 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (Dezember 2017) - Anwendungserstellung 7.3.11971.56116 mit Plattform-Update 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017) - mit Plattformupdate 8 (Anwendungserstellung 7.2.11792.56024 mit Plattformbuild 7.0.4565.16212).
- Die folgenden Hotfixes sind erforderlich:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** Dieser Hotfix aktiviert die Auftragspositionssynchronisierung von Sales zu Finance and Operations über die Datenintegrationsfunktion. Er enthält auch einige anderen Erweiterungen.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** Dieser Hotfix aktiviert die Auftragspositionssynchronisierung von Finance and Operations zu Sales über die Datenintegrationsfunktion.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** Dieser Hotfix aktiviert die Auftragspositionssynchronisierung von Finance and Operations zu Sales über die Datenintegrationsfunktion.

    > [!NOTE]
    > Sie müssen nur KB4045570 installieren, da diese Installation die Änderungen aus anderen Hotfixes enthält. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations Version 1611 (November 2016)

- Dynamics 365 for Finance and Operations-Version 1611 (November 2016) mit Plattformaktualisierung 8 oder höher

- Die folgenden Hotfixes sind erforderlich:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – Aktiviert Auftragssynchronisierung mit Datenenintegrator von Finance and Operations zu Sales. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – Aktiviert Auftragskopf- und Positionssynchronisierung mit Datenenintegrator von Finance and Operations zu Sales.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – Unterstützung für die Integration von „Interessent zu Bargeld” durch Datenentitäten ist erforderlich.
    
    > [!NOTE]
    > Nachdem Sie die Hotfixes installiert haben, müssen Sie die folgende Stapelverarbeitung vom Formular **SalesPopulateProspectToCash** auslösen. Dieses Formular wird ausgeblendet, da Sie es nur einmal benötigen. Um auf das Formular zuzugreifen, fügen Sie Folgendes der Browseradresse hinzu, wenn Sie sich bei der Umgebung angemeldet haben: *&mi=action:SalesPopulateProspectToCash*, beispielsweise `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Wenn das Formular geöffnet wird, klicken Sie auf OK. Dadurch wird ein neues Feld **LineCreationSequnceNumber** in den Tabellen **SalesLine**, **SalesQuotationLine** und **CustInvoiceTrans** mit eindeutigen Werte ergänzt, und die Produktliste wird aktualisiert. Dies ist erforderlich, damit die „Interessent zu Bargeld”-Integration funktioniert.


## <a name="system-requirements-for-sales"></a>Systemanforderungen für Sales

Um die Interessent zu Bargeld-Lösung zu nutzen, müssen Sie Folgendes installieren:

- Dynamics 365 for Sales-Version 1612 (8.2.1.207) (DB) 8.2.1.207 online oder eine höhere Version
- Prospect to Cash-Lösung für Dynamics 365 for Sales, Version 1.15.0.0 oder einer höheren Version. Die Lösung ist aus AppSource zum Download verfügbar. [Laden Sie Dynamics 365, Prospect to Cash herunter](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
