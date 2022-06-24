---
title: Erweiterten Bankabstimmungsimport mithilfe der elektronischen Berichterstellung einrichten
description: In diesem Artikel wird erläutert, wie Sie die elektronische Berichterstellung verwenden, um den erweiterten Bankabstimmungsimportprozess einzurichten.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 2ac8811a5c10490d90f782472d3c198474c7edc0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889119"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Erweiterten Bankabstimmungsimport mithilfe der elektronischen Berichterstellung einrichten

[!include [banner](../includes/banner.md)]

Mit der erweiterten Bankabstimmungsfunktion können Sie elektronische Bankauszüge importieren und diese in Microsoft Dynamics 365 Finance automatisch mit Bankbuchungen abstimmen. Dieser Artikel erläutert die Einrichtung der Importfunktion für Ihre Bankauszüge. Die Einrichtung des Bankabstimmungsimports variiert je nach Format des elektronischen Bankauszugs. Microsoft Dynamics 365 Finance unterstützt drei Bankauszugsformate: ISO20022 MT940 und BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Konfiguration der elektronischen Berichterstellung einrichten

1. Wechseln Sie zu **Arbeitsbereiche \> Elektronische Berichterstellung**.
2. Auf der Kachel für den Konfigurationsanbieter **Microsoft** wählen Sie **Repositorys** aus.
3. Wählen Sie **Global** und dann **Öffnen** aus.
4. Wenn eine Verbindung zum Repository hergestellt werden muss, wählen Sie den blauen Link im Dialogfeld aus.
5. Suchen Sie in der Konfigurationsliste nach **Kontoauszugsmodell \> Kontoauszugsmodell von BAI2**.
6. Wählen Sie das **BAI2**-Format aus.
7. Wählen Sie im Inforegister **Versionen** die neueste Version, und wählen Sie dann **Importieren** aus.

## <a name="set-up-the-bank-statement-format"></a>Bankauszugsformat einrichten

1. Gehen Sie zu **Barmittel und Bankverwaltung \> Einrichtung \> Einrichtung der erweiterten Bankabstimmung \> Bankauszugsformat**.
2. Wählen Sie **Neu** aus.
3. Legen Sie die Felder **Auszugsformat** und **Name** fest.
4. Aktivieren Sie das Kontrollkästchen **Allgemeines elektronisches Importformat**.
5. Legen Sie das Feld **Formatkonfiguration importieren** auf das Format **BAI2** fest.

## <a name="set-up-the-bank-account"></a>Bankkonto einrichten

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten**.
2. Öffnen Sie das Bankkonto.
3. Legen Sie auf dem Inforegister **Abstimmung** die Option **Erweiterte Bankabstimmung** auf **Ja** fest.
4. Legen Sie im Feld **Auszugsformat** das Format **BAI2** fest, das Sie zuvor erstellt haben.

## <a name="import-the-bank-statement"></a>Bankauszug importieren

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Bankauszug für Abstimmung \> Bankauszüge**.
2. Wählen Sie oben auf der Seite **Kontoauszüge** die Option **Auszug importieren** aus.
3. Legen Sie das Feld **Bankkonto** auf das Bankkonto im Auszug fest.
4. Legen Sie im Feld **Auszugsformat** das Format **BAI2** fest, das Sie zuvor erstellt haben.
5. Wählen Sie **Durchsuchen** und die Datei **BAI** aus.
6. Wählen Sie **Hochladen** aus.
7. Wählen Sie **OK** aus, um die ausgewählte Datei zu importieren.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Beispiele für Bankauszugsformate und technische Layouts
Die folgende Tabelle zeigt Beispiele der technischen Layoutdefinitionen für erweiterte Importdateien zur Bankabstimmung und drei entsprechende Beispieldateien für Bankauszüge: [Dateibeispiele importieren](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Technische Layoutdefinition                             | Beispieldatei für Bankauszüge          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

