---
title: Interessent zu Bargeld
description: "Das Thema bietet eine Übersicht der Lösung „Interessent zu Bargeld” zwischen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, und Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
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
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: de-de
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>Interessent zu Bargeld

[!include[banner](../includes/banner.md)]

Der Interessent für Bargeldlösungen bietet direkte Synchronisation zwischen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, und Microsoft Dynamics 365 for Sales. Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales. Während die Daten zwischen Finance and Operations und Sales fließen, können Sie Vertriebs- und Marketingaktivitäten zwischen Finance and Operations und Sales ausführen und die Auftagserfüllung mit Bestandsverwaltung in Finance and Operations handhaben.

In der aktuellen Version enthält die Interessent in Bargeldlösung die folgenden Typen der direkten Synchronisierung:

- [Konten in Sales verwalten und direkt cvon Sales zu Finance and Operations synchronisieren](accounts-template-mapping-direct.md)
- [Produkte in Finance and Operations verwalten und direkt mit Sales synchronisieren](products-template-mapping-direct.md)
- [Kontakte in Sales verwalten und direkt mit Kontakten oder Debitoren in Finance and Operations synchronisieren](contacts-template-mapping-direct.md)
- [Synchronisieren von Verkaufsangeboten direkt von Sales mit Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Synchronisieren von Verkaufsaufträgen direkt von Finance and Operations mit Sales](sales-order-template-mapping-direct.md)
- [Synchronisieren von Aufträgen direkt zwischen Sales und Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [Synchronisieren von Verkaufsrechnungen direkt von Finance and Operations mit Sales](sales-invoice-template-mapping-direct.md)

In der früheren Version enthält die Interessent in Bargeldlösung die folgenden Typen der nicht-direkten Synchronisierung:

- [Konten in Sales verwalten und mit Finance and Operations synchronisieren](accounts-template-mapping.md)
- [Kontakte in Sales verwalten und mit Finance and Operations synchronisieren](contacts-template-mapping.md)
- [Produkte in Finance and Operations verwalten und mit Sales synchronisieren](products-template-mapping.md)
- [Verkaufsangebote in Sales erstellen und mit Finance and Operations synchronisieren](sales-quotation-template-mapping.md)
- [Verkaufsaufträge in Finance and Operations erstellen und mit Sales synchronisieren](sales-order-template-mapping.md)
- [Verkaufsrechnungen in Finance and Operations erstellen und mit Sales synchronisieren](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Systemanforderungen für Finance and Operations

Um die Interessent zu Bargeld-Lösung zu nutzen, müssen Sie Folgendes installieren:

### <a name="july-2017"></a>2017. Juli 

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Juli 2017) mit Plattform-Update 8 (Anwendungsbuild 7.2.11792.56024 mit Plattformbuild 7.0.4565.16212)
- Die folgenden Hotfixes für Finance and Operations:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** Dieser Hotfix aktiviert die Auftragspositionssynchronisierung von Sales zu Finance and Operations über die Datenintegrationsfunktion. Er enthält auch einige anderen Erweiterungen.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** Dieser Hotfix aktiviert die Auftragspositionssynchronisierung von Finance and Operations zu Sales über die Datenintegrationsfunktion.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** Dieser Hotfix aktiviert die Auftragspositionssynchronisierung von Finance and Operations zu Sales über die Datenintegrationsfunktion.

    > [!NOTE]
    > Sie müssen nur KB4045570 installieren, da diese Installation Änderungen aus den anderen Microsodft Wissensdatenbanken (KB) enthält.

### <a name="november-2016-version-1611"></a>November 2016 (Version 1611)

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (November 2016) mit Plattform-Update 8 oder höher

- Die folgenden Hotfixes für Finance and Operations:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Aktiviert Auftragssynchronisierung mit Datenenintegrator von Microsoft Dynamics 365 for Finance and Operations zu Sales 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Aktiviert Auftragskopf.- und Zeilensynchronisation mit dem Datenenintegrator von Microsoft Dynamics 365 for Finance and Operations zu Sales
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support für Interessenten der Bargeldintegration über Datenentitäten ist obligatorisch
    
    > [!NOTE]
    > Nachdem Sie die Hotfixes eingerichtet haben, müssen Sie die folgende Stapelverarbeitung von SalesPopulateProspectToCash starten. Dieses Formular wird ausgeblendet, während Sie es nur einmal erfordern. Um darauf zuzugreifen, fügen Sie Folgendes der Browseradresse hinzu, wenn Sie sich bei der Umgebung angemeldet haben: &mi=action: SalesPopulateProspectToCash. https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash Im Formular, das geöffnet wird, klicken Sie auf OK.
    Dadurch wird ein neues Feld "LineCreationSequnceNumber" in Tabellen "SalesLine", "SalesQuotationLine" und "CustInvoiceTrans" mit eindeutigen Werte ergänzt und die Produkte aktualisiert. Dies ist erforderlich, damit die P2C-Integration auf 7,1 arbeitet


## <a name="system-requirements-for-sales"></a>Systemanforderungen für Sales

Um die Interessent zu Bargeld-Lösung zu nutzen, müssen Sie Folgendes installieren:

- Microsoft Dynamics 365 for Sales, Version 1612 (8.2.1.207) (DB 8.2.1.207) online
- Interessent zu Bargeld-Lösung für Microsoft Dynamics 365 for Sales, Version 1.15.0.0 (v15) 

   > [!NOTE]
   >
   > Vorlagen mit 1.0.0.0 Version und 1.0.0.1 werden auf Interessenten der Bargeldlösung für Microsoft Dynamics 365 for Sales, Version 1.14.1.0 unterstützt
   >
   > Vorlagen mit 2.0.0.0 Version und 2.1.0.0 werden auf Interessenten der Bargeldlösung für Microsoft Dynamics 365 for Sales, Version 1.15.0.0 unterstützt

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Installieren der Interessent zu Bargeld-Lösung für Sales

1. Laden Sie die [Interessent zu Bargeld-Lösungspaket-ZIP-Datei für Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) von CustomerSource herunter.
2. Überprüfen Sie, dass die ZIP-Datei entsperrt ist. Andernfalls wenn Sie versuchen, das Lösungspaket einzurichten, erhalten Sie die folgende Fehlermeldung: Es wurden keine Importpakete gefunden. Klicken Sie mit der rechten Maustaste auf **Eigenschaften**, und wählen Sie dann Entsperren aus. Wählen Sie dann **Entsperren** aus.
3. Entpacken Sie die Datei, und führen Sie **PackageDeployer.exe** aus.
4. Installieren Sie die Interessent zu Bargeld-Cash-Lösung auf Ihrer Sales-Instance:

    1. Wählen Sie den **Office 365**-Bereitstellungstyp aus.
    2. Wählen Sie die Option zum **Anzeigen von Erweiterungen** aus.
    3. Wählen Sie für eine schnelle Installation die Region aus. Wenn Sie **Ich weiß nicht** auswählen, sucht das System nach allen Regionen und die Installation dauert länger.
    4. Geben Sie Benutzername und Kennwort für einen Administratorbenutzer ein, der über Benutzerrechte zum Installieren verfügt.

