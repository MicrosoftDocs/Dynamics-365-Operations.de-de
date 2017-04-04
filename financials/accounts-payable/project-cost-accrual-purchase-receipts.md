---
title: "Projektkostenabgrenzung auf den Empfängen von Bestellungen"
description: "In diesem Thema wird beschrieben, wie Projektkosten antizipierte von den Empfängen von Bestellungen in Microsoft Dynamics 365 für Arbeitsgänge nachverfolgt werden können."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Projektkostenabgrenzung auf den Empfängen von Bestellungen

In diesem Thema wird beschrieben, wie Projektkosten antizipierte von den Empfängen von Bestellungen in Microsoft Dynamics 365 für Arbeitsgänge nachverfolgt werden können. 

Rechnungen für ein Projekt werden häufig später an, an dem die Waren und Dienstleistungen geliefert werden, die u erheblichen Auswirkungen auf Projektleistungskennzahlen (KPIs) sind. Es wichtig, in der Lage sein soll, diese Buchungen in Projektberichten Experten im Finanz- und zu verfolgen.

Das folgende Beispielsszenario dieses veranschaulicht. 

Contoso-Beratung hat ein neues Cloudbereitstellungsprojekt gestartet. Eine Bestellung soll, einen Computer für das Projekt zu erwerben erstellt. Der Computer kostet $1500 und Installationsdienstleistungen Kosten). Der Kreditor hat den Computer geliefert und festgelegt, er die Rechnung noch nicht Contoso-Beratung erreicht. Der Projektmanager möchte Projektkostenabgrenzung von $1650 finden, bevor die Rechnung gesendet wird. Diese Kosten müssen in den Monatsendefinanzaufstellungen des Unternehmens auch angezeigt werden. 

Die antizipierten Kosten müssen auf der Finanzebene Projektebene und für Berichtszwecke erfasst werden. In Dynamics 365 für Arbeitsgänge, kann die wertmäßige Aktualisierung des Produktzugangs für den Artikel und die Beschaffungskategorien nachverfolgt werden. 

Für Artikel auf der Kreditorenparameter ** ** Seite, die Sie buchen die ** Sie Produktzugänge im Sachkonto ** Option aus.
![accruals1 ([]. /media/accruals1-1024x409.png)]". /media/accruals1.png) 

Für auf Beschaffungskategorien der ** Kategorierichtlinienregel ** Seite, wählen Sie ** Einkauf ** Richtlinien, und wählen Sie dann Einkaufausgaben ** fallen auf Beleg an ** Für jede Beschaffungskategorie aus.
![accruals2 ([]. /media/accruals2-1024x569.png)]". /media/accruals2.png) 

** Einkaufaufwendungen nicht fakturiert ** und ** ** Einkaufsabgrenzung Konten in ** Buchungseinstellungen ** verwendet werden, wenn Belege, die dem Produktzugang zugeordnet sind, gebucht werden.
![accruals3 ([]. /media/accruals3-1024x429.png)]". /media/accruals3.png) 

Das Verwenden dieses Szenarios gleichen lassen Sie prüfen, wie Sie das Buchen eines Produktzugangs Hauptbuch und Projektinformationen auswirkt. 

** Schritt 1: ** Erstellen und Bestätigen Sie eine neue Bestellung für das Projekt, den Einkauf eines Computers für $1500 und der Installations-Services für Euro erfasst.
![accruals4 ([]. /media/accruals4-1024x497.png)]". /media/accruals4.png) 

Wenn die Bestellung bestätigt wurde, werden Buchungen für die zugesagten Kosten für das Projekt erstellt. 
![accruals5 ([]. /media/accruals5-1024x219.png)]". /media/accruals5.png) 

> [!NOTE]
> Die Buchungen für die zugesagten Kosten besitzen das Buchungs-Ursprung ** ** Feld, das auf festgelegt ** ** Bestellung. Eine Bestellung der Informationen erstellt, bestätigend, keine Buchungen für ein Projekt. 

** Schritt 2: ** Waren und Dienstleistungen geliefert wird ab und ein Produktzugang erfasst wird. 

Beim Buchen eines Produktzugangs generiert und gebucht einen Beleg auf Sachkonto. Der Beleg für die Einkaufaufwendungen, das Konto und das Kreditkaufabgrenzungskonto nicht. 
![accruals6 ([]. /media/accruals6-1024x214.png)]". /media/accruals6.png)

> [!NOTE]
> Einen Produktzugang buchen, verwendet die Buchungseinstellungen für Beschaffungskategorien und Produkte und nicht die Buchungseinstellungen für die Projektkategorien. Um Finanzauswirkungen von Einkaufabgrenzungen ordnungsgemäß widerzuspiegeln, muss diese Einstellung vorgenommen werden. 

Es ist möglich, Beschaffungskategorien auf die Projektkategorien auf der Seite ** ** Beschaffungskategorie zuordnen.
![accruals7 ([]. /media/accruals7-1024x390.png)]". /media/accruals7.png)

** Schritt 3: ** Erstellen einer Trattekreditorenrechnung. 

In Dynamics 365 für Arbeitsgänge, wirkt das Buchen eines Produktzugangs nicht Projektinformationen aus. Als Problemumgehung können Sie ein Trattekreditorenrechnungsrecht erstellen, wenn Sie den Empfang von Bestellungen gebucht wurden. Zur ** Bestellung ** Seite &gt; ** Rechnungsregisterkarte ** ** &gt; generieren ** ** &gt; ** Rechnung. Dies basiert schwebendes ein Rechnungsdokument Projektinformationen, das aktualisiert. 

Das Erstellen einer Trattekreditorenrechnung generiert für Projektbuchungen. 
![accruals8 ([]. /media/accruals8-1024x225.png)]". /media/accruals8.png) 

In der ** zugesagte Kosten ** Seite werden die Datensätze angezeigt, die in Schritt 1 erstellten, geschlossen und neue Datensätze erstellt werden, damit wiedergegeben Zusage die Kosten, die von der ausstehenden Kreditorenrechnung stammt. ** Die Buchungsgrundlage ** Feld für die zugesagten Kosten wird auf festgelegt ** Kreditorenrechnung **.
![accruals9 ([]. /media/accruals9-1024x200.png)]". /media/accruals9.png)

Die Kreditorenrechnung wird zwar weiterhin im einem ausstehenden Status, wenn die tatsächliche Kreditorenrechnung Eingang.


