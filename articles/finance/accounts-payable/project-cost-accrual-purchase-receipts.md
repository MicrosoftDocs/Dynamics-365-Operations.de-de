---
title: Projektkostenabgrenzung beim Empfang von Bestellungen
description: In diesem Thema wird beschrieben, wie Projektkosten von Bestellbelegen in Microsoft Dynamics 365 Finance nachverfolgt werden können.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d27fba816ca289e6a84e8684f7f90686864fb0b6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972080"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>Projektkostenabgrenzung beim Empfang von Bestellungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Projektkosten von Bestellbelegen in Microsoft Dynamics 365 Finance nachverfolgt werden können. 

Rechnungen für ein Projekt werden häufig später als die Waren und Dienstleistungen geliefert, was erheblichen Auswirkungen auf Projektleistungskennzahlen (KPIs) haben kann. Es wichtig, in der Lage zu sein, diese Buchungen in Projektberichten und Finanzberichten zu verfolgen.

Das folgende Beiespielszenario illustriert dieses. 

Contoso Consulting hat ein neues Cloudbereitstellungsprojekt gestartet. Eine Bestellung wird erstellt, um einen Computer für das Projekt zu erwerben. Der Computer kostet 1500 USD und Installationsdienstleistungen kosten 150 USD. Der Kreditor hat den Computer geliefert und installiert, aber die Rechnung noch nicht Contoso Consulting erreicht. Der Projektmanager möchte eine Projektkostenabgrenzung von 1650 USD haben, bevor die Rechnung gesendet wird. Diese Kosten müssen in den Monatsendefinanzaufstellungen des Unternehmens auch angezeigt werden. 

Die antizipierten Kosten müssen auf der Finanzebene und Projektebene und für Berichtszwecke erfasst werden. Die wertmäßige Aktualisierung des Produktzugangs für den Artikel und die Beschaffungskategorien kann nachverfolgt werden. 

Für Artikel auf der **Kreditorenparameter** Seite wählen Sie die **Produktzugänge im Sachkonto** Option aus.
[![Kreditorenparameter Seite](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Für auf Beschaffungskategorien der **Kategorierichtlinienregel** Seite, wählen Sie **Einkauf** Richtlinien, und wählen Sie dann **Einkaufausgaben fallen auf Beleg an** für jede Beschaffungskategorie aus.
[![Kategorie Richtlinienregel Seite](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Die **Einkaufaufwendungen nicht fakturiert** und **Einkaufsabgrenzung** Konten in **Buchungseinstellungen** verwendet werden, wenn Belege, die dem Produktzugang zugeordnet sind, gebucht werden.

Das Verwenden dieses Szenarios gleichen lassen Sie prüfen, wie Sie das Buchen eines Produktzugangs Hauptbuch und Projektinformationen auswirkt. 

**Schritt 1:** Erstellen und Bestätigen Sie eine neue Bestellung für das Projekt, den Einkauf eines Computers für 1500 USD und der Installations-Services für 150 USD erfasst.
[![Neue Bestellung anlegen](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Wenn die Bestellung bestätigt wurde, werden Buchungen für die zugesagten Kosten für das Projekt erstellt. 
[![Transaktionen erstellt](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Die Buchungen für die zugesagten Kosten besitzen das **Buchungs-Ursprung** Feld auf **Bestellung** festgelegt. Eine Bestellung der Informationen erstellt, bestätigend, keine Buchungen für ein Projekt. 

**Schritt 2:** Waren und Dienstleistungen geliefert wird ab und ein Produktzugang erfasst wird. 

Beim Buchen eines Produktzugangs generiert und gebucht einen Beleg auf Sachkonto. Der Beleg für die Einkaufaufwendungen, das Konto und das Kreditkaufabgrenzungskonto nicht. 
[![Belegbuchungen](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Einen Produktzugang buchen verwendet die Buchungseinstellungen für Beschaffungskategorien und Produkte und nicht die Buchungseinstellungen für die Projektkategorien. Um Finanzauswirkungen von Einkaufabgrenzungen ordnungsgemäß widerzuspiegeln, muss diese Einstellung vorgenommen werden. 

Es ist möglich, Beschaffungskategorien auf die Projektkategorien auf der Seite **Beschaffungskategorie** zuordnen.
[![Beschaffungskategorie Seite](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Schritt 3:** Standardmäßige Entwurfskreditorenrechnung erstellen 

Das Buchen eines Produktzugangs wirkt sich nicht auf die Projektinformationen aus. Als Problemumgehung können Sie ein Entwurfskreditorenrechnungs-Recht erstellen, wenn Sie den Empfang von Bestellungen gebucht wurden. Wechseln Sie zu **Bestellung** Seite &gt; **Rechnungsregisterkarte** &gt; **Generieren** &gt; **Rechnung**. Dies erstellt ein ausstehendes Rechnungsdokument, das Projektinformationen aktualisiert. 

Das Erstellen einer Entwurfskreditorenrechnung generiert ausstehende Projektbuchungen. 
[![Ausstehende Projektbuchungen](./media/accruals8-1024x225.png)](./media/accruals8.png) 

In der **Zugesagte Kosten** Seite werden die in Schritt 1 erstellten Datensätze geschlossen und neue Datensätze werden erstellt, damit die Zusage von der ausstehenden Kreditorenrechnung wiedergegeben wird. Die **Buchungsgrundlage** Feld für die zugesagten Kosten wird auf **Kreditorenrechnung** festgelegt.
[![Verpflichtungskosten Seite](./media/accruals9-1024x200.png)](./media/accruals9.png)

Die Kreditorenrechnung wird zwar weiterhin im einem ausstehenden Status, wenn die tatsächliche Kreditorenrechnung Eingang.



