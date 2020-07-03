---
title: Erstellen und Anwenden von Bedingungen für einbehaltene Kreditorenbeträge
description: 'Dieses Thema enthält Informationen zum Einrichten und Verwalten von Bedingungen für einbehaltene Kreditorenbeträge:'
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410225"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Erstellen und Anwenden von Bedingungen für einbehaltene Kreditorenbeträge

[!include [banner](../includes/banner.md)] 

Das Einrichten von Aufbewahrungsbedingungen für Lieferantenzahlungen für ein Projekt ist hilfreich, wenn Ihre Organisation einen Teil der an einen Lieferanten geleisteten Zahlungen behalten möchte. Zum Beispiel, wenn Sie die Zahlung an einen Lieferanten halten möchten, bis die gelieferten Produkte Ihren Erwartungen entsprechen. Wenn Sie mit einem Kreditor verhandeln, können Sie Bedingungen für das Einbehalten der Kreditorenzahlungsbeträgen bestimmen.

## <a name="create-vendor-payment-retention-terms"></a>Bedingungen für einbehaltene Kreditorenzahlungen erstellen

Sie können den einzubehaltenden Prozentsatz einer Kreditorenzahlung eingeben wie auch den freizugebenden Prozentsatz der zuvor einbehaltenen Beträge. Beträge werden bei Kreditorenrechnungen automatisch einbehalten, bis der festgelegte Vollendungsgrad erreicht ist. Nachdem Sie die Bedingungen für den Einbehalt für einen Kreditor eingerichtet haben, können Sie diese auf jedes beliebige Projekt anwenden, an dem der Kreditor beteiligt ist.

Folgen Sie diesen Schritten, um die Bedingungen für den Einbehalt von Kreditorenzahlungen einzurichten und zu verwalten. 

1. Gehen Sie zu **Projektmanagement und Buchhaltung** > **Aufbewahrung** > **Aufbewahrungsbedingungen für Lieferantenzahlungen**.
2. Wählen Sie **Neu**, um eine neue Bedingung für einbehaltene Kreditorenbeträge hinzuzufügen. Der Wert **Regelkennung** für die neue Bedingung wird automatisch eingegeben. 
3. Geben Sie eine kurze Beschreibung in das Feld **Beschreibung** ein und wählen Sie auf dem Inforegister **Bedingungen** **Zeile hinzufügen** aus, um die Bedingungswerte für Folgendes einzugeben:

   - Geben Sie im Feld **Prozentsatz gelieferter Einheiten** einen Vollendungsgrad für die Bestimmung ein. Beträge werden bei Kreditorenrechnungen automatisch einbehalten, bis die Projektvollendungsstufe gleich dem Prozentsatz ist, den Sie eingeben haben. Beispiel: Bei der Eingabe von 50.00 werden Beträge einbehalten, bis das Projekt zu 50 Prozent abgeschlossen ist.
   - Geben Sie im Feld **: Einzubehaltender Prozentsatz** den einzubehaltenden Prozentsatz eines Kreditorenrechnungsbetrags ein. Wenn Sie beispielsweise 10,00 in dieses Feld eingeben, werden 10 Prozent des Betrags für Kreditorenrechnungen einbehalten, bis das Projekt den Vollendungsgrad erreicht, den Sie im Feld **Prozentsatz der gelieferten Einheiten** festgelegt haben.
   - **Feizugebender Prozentsatz**: Geben Sie im Feld **Zeile hinzufügen** den Prozentsatz zuvor einbehaltener Kreditorenrechnungsbeträge ein, die beim ausgewählten Vollendungsgrad des Projekts freizugeben sind.

> [!NOTE]
> Wenn Sie mehrere Meilensteine für verschiedene Vollendungsgrade des Projekts bestimmt haben, geben Sie für jede Einbehaltungsregel eine separate Position für Bedingungen für die einbehaltenen Kreditorenbeträge ein. Jede Position kann jeweils unterschiedliche Prozentsätze zur Einbehaltung oder zur Prozentsätze für die Freigabe für jeden Vollendungsgrad des Projekts bestimmen.

Nachdem Sie die Bedingungen für den Einbehalt für einen Kreditor eingerichtet haben, können Sie diese auf ein Projekt anwenden, an dem der Kreditor beteiligt ist.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Wenden Sie Lieferantenbindungsbedingungen auf ein Projekt an

1. Gehen Sie zu **Projektmanagement und Buchhaltung** > **Projekte** > **Alle Projekte** und öffnen Sie ein Projekt auf der Projektlistenseite.
2. Wählen Sie im Inforegister **Kreditorenvereinbarungen** die Option **Position hinzufügen** aus.
3. Wählen Sie im **Kontocodefeld** eine der folgenden Optionen aus: 

   - **Tabelle**: Die Bedingungen für einbehaltene Kreditorenbeträge gelten für einen einzelnen Kreditor.
   - **Gruppe**: Die Bedingungen für einbehaltene Kreditorenbeträge gelten für alle Kreditoren in einer Kreditorengruppe.
   - **Alle**: Die Bedingungen für einbehaltene Kreditorenbeträge gelten für alle Kreditoren.

4. Wählen Sie im **Kreditor/Kreditorengruppenfeld** den Kreditor oder die Kreditorengruppe aus, für die die Bedingungen für einbehaltene Kreditorenbeträge gelten. (Dieses Feld ist nur verfügbar, wenn im vorangegangenen Schritt nicht die Option **Alle** ausgewählt wurde.)
5. Wählen Sie im Feld **Bedingungen für einbehaltene Kreditorenbeträge** die Bedingungen für einbehaltene Kreditorenbeträge aus, die Sie im vorherigen Verfahren erstellt haben.
6. Wenn das Projekt auch Pay-When-Paid (PWP)-Begriffe für den Kreditor enthält, geben Sie in das Feld **Pay When Paid - Schwellenwertprozentsatz** den Schwellenwertprozentsatz für das Projekt ein.

Die Bedingungen für einbehaltene Kreditorenbeträge werden auch in Bestellungen angezeigt, die Sie für den Kreditor erstellt werden.
