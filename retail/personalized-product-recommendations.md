---
title: Personalized product recommendations overview
description: "In Dynamics 365 für Arbeitsgänge, können Produktempfehlungen im Feld Verkaufsstelle (POS)- Gerät angezeigt werden. Die Empfehlungen sind Artikel, die der Debitor möglicherweise unter auf der Grundlage ihrer Einkaufshistorie, Artikel an seinem Wunschzettel und Artikel interessiert ist, dass weitere online in Debitoren und der physische Filiale &quot;Eingekauft&quot;. Für Einzelhändler mit großen Katalogen, von Empfehlungen den Debitor mit Produkterfassung. Indem die Produkte an Schau stellen, die Zinsen eines Debitors und die Kaufgewohnheiten Zielgruppe werden, können Produktempfehlungen Einzelhändlern mit Obenverkauf und Kreuzverkauf helfen und können einbehaltenen erhöhen. In Dynamics 365 für Arbeitsgänge, Produktempfehlungen werden durch kognitive Dienst- und Microsoft Azure-Lernfähigkeiteiner Maschine betrieben."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Personalized product recommendations overview

In Dynamics 365 für Arbeitsgänge, können Produktempfehlungen im Feld Verkaufsstelle (POS)- Gerät angezeigt werden. Die Empfehlungen sind Artikel, die der Debitor möglicherweise unter auf der Grundlage ihrer Einkaufshistorie, Artikel an seinem Wunschzettel und Artikel interessiert ist, dass weitere online in Debitoren und der physische Filiale "Eingekauft". Für Einzelhändler mit großen Katalogen, von Empfehlungen den Debitor mit Produkterfassung. Indem die Produkte an Schau stellen, die Zinsen eines Debitors und die Kaufgewohnheiten Zielgruppe werden, können Produktempfehlungen Einzelhändlern mit Obenverkauf und Kreuzverkauf helfen und können einbehaltenen erhöhen. In Dynamics 365 für Arbeitsgänge, Produktempfehlungen werden durch kognitive Dienst- und Microsoft Azure-Lernfähigkeiteiner Maschine betrieben.

<a name="scenarios"></a>Szenarien
---------

Produktempfehlungen werden für die folgenden POS-Szenarien aktiviert. Sie sind Mitglied der Cloud POS oder modernes POS (MPOS) verfügbar.

1.  ** Produktdetails ** auf der Seite die folgenden Schritte aus:

-   Wenn eine Filiale einen geplanten Besuchen zuordnen ** Produktdetails ** Seite, wenn die vorherige Buchungen über verschiedene Kanälen, das vorgeschlagen Empfehlungsmodul zusätzliche Artikel berücksichtigt, die wahrscheinlich Konfigurationsfehler, zusammen eingekauft werden.
-   Falls die Filiale hinzufügt einem Debitor der Buchung zuordnen und endet erst dann eine ** Produktdetails ** Seite, das Empfehlungsmodul bereitstellt personalisierte Empfehlungen mithilfe der Buchungshistorie des Debitors.

![proddetails ([]. /media/proddetails.png)]". /media/proddetails.png)

1.  ** ** Buchung auf der Seite die folgenden Schritte aus:

-   Das Empfehlungsmodul schlägt Artikel auf Basis der gesamten Liste von Artikeln im Korb vor.
-   Falls die Filiale hinzufügt einem Debitor der Buchung zuordnen, wird das Empfehlungsmodul persönliche Empfehlungen mithilfe der Buchungshistorie des Debitors und die Liste der Artikel im Korb bereit.

** Hinweis ** Empfehlungen anzeigen ** Buchung ** Seite, der Einzelhändler muss das Bildschirmlayout in Dynamics 365 für Arbeitsgänge aktualisieren. Das Steuerelement ** Empfehlungen ** der Buchung muss ** ** Seite an abgelegt werden. ![transactionscreenmultipleproductslargemessengersbag-5 ([]. /media/transactionscreenmultipleproductslargemessengersbag-5.jpg)]". /media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

1.  Auf der ** Debitorendetails ** Seite:
    -   Das Empfehlungsmodul schlägt Artikel auf Grundlage die Benutzerkennung und Artikel im Wunschzettel des Debitors vor.

![customerdetailsrecommendations ([]. /media/customerdetailsrecommendations.png)]". /media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Konfigurieren Dynamics 365, um Arbeitsgänge POS-Empfehlungen aktivieren
Um Produktempfehlungen einzurichten, müssen Sie folgende Schritte ausführen.

1.  Überprüfen Sie, ob Sie das richtige ausgewählt haben ** ** juristische Person.
2.  Navigieren Sie Entitätsshop ** **, wählen Sie ** Einzelhandelsverkauf ** aus, und klicken Sie dann ** ** Aktualisierung. ** ** Diese Angaben werden verwendet die Demodaten (oder Ihre Daten) aus der betrieblichen Datenbank werden und es auf Entitätsshop.
3.  Optional: Wenn Empfehlungen zum Buchungsbildschirm anzuzeigen, navigieren Sie ** Bildschirmlayout ** auswählen, vom Bildschirmlayout, starten, Bildschirmlayoutdesigner ** ** ** ** und dann fallenlassen ** Empfehlungssteuerelement ** wo erforderlich.
4.  Wechseln Sie ** Einzelhandelsparameter **, wählen Sie aus Maschine-Lernen ** **, wählen Sie die Option Ja ** ** unter aus ** aktivieren Sie POS-Empfehlungen **.
5.  Weitere Empfehlungen finden POS, Konfigurationseinzelvorgang globaler des Durchlaufs ** **1110. Um Änderungen widerzuspiegeln der dem POS- designer, aktivieren Kanalkonfigurationseinzelvorgang ** **1070.

## <a name="how-does-it-work"></a>[]()[]() Funktionsweise?
Wenn Sie die Entitätsshop ** ** Entität aktualisieren, werden folgenden Aktionen statt.

-   Daten im Format, das von den kognitiven Services erforderlich ist, werden vom Dynamics 365 für betriebliche Datenbank der Arbeitsgänge zum Entitätsshop extrahiert und gesendet.
-   Die Daten werden von Azure Datenen-Fabrik (ADF) verwendet, um die Daten mithilfe der Bienenstockskripte als Teil ADF-Aktivitäten zu reinigen. Gereinigte Daten werden im BLOB- gespeichert.
-   Daten vom BLOB- werden von den kognitiven API Dienstleistungen verwendet, um ein Empfehlungsmodell zu schulen.

Wenn Sie aktivieren ** aktivieren Sie Empfehlungen ** und die Konfigurationseinzelvorgänge aktivieren, werden folgenden Aktionen statt.

-   Entwerfen Sie Anmeldeinformationen und - kennung werden vom API abgeholt und gespeichert im Dynamics 365 für betriebliche Datenbank, der Arbeitsgänge im web.config für AOS und auch im Retail Server.
-   Entwerfen Sie Anmeldeinformationen und - kennung bereitgestellt werden für CRT vorgenommen, dass Anforderungen der empfehlungen Produkt aus der Cloud POS und MPOS im rechnerabhängigen Betriebs- eingelöst werden können.


<a name="see-also"></a>Siehe auch
--------

[Hinzufügen eines Empfehlungssteuerelement der Buchungsseite auf einem POS-Gerät] hinzufügen" add-recommendations-control-pos-screen.md )


