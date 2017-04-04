---
title: "Hinzufügen eines Empfehlungssteuerelement der Buchungsseite auf einem POS-Gerät hinzu"
description: "In diesem Thema wird beschrieben, wie Sie einem Empfehlungssteuerelement dem Buchungsbildschirm auf einem Verkaufsstelle (POS)- Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 für Arbeitsgänge hinzugefügt."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Hinzufügen eines Empfehlungssteuerelement der Buchungsseite auf einem POS-Gerät hinzu

In diesem Thema wird beschrieben, wie Sie einem Empfehlungssteuerelement dem Buchungsbildschirm auf einem Verkaufsstelle (POS)- Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 für Arbeitsgänge hinzugefügt.

Sie können Produktempfehlungen zu Ihrem POS-Gerät anzeigen, wenn von Microsoft Dynamics 365 für Arbeitsgänge verwenden. *Recommendations* sind Artikel, die von Ihrem Debitor möglicherweise unter auf der Grundlage ihrer Einkaufshistorie, Artikel an seinem Wunschzettel und Artikel interessiert ist, dass weitere online in Debitoren und der physische Filiale "Eingekauft". Um Produktempfehlungen anzuzeigen, müssen Sie eine Kontrolle der Buchungsbildschirm mithilfe des Bildschirmlayoutdesigners hinzufügen.

## <a name="open-layout-designer"></a>Öffnet Sie Bereich
1.  Wechseln ** Einzelhandel und Handel ** &gt; ** richtet der Kanal ** &gt; ** POS eingerichtet ** &gt; ** POS ** &gt; ** Bildschirmlayouts **.
2.  Mithilfe des Schnellfilters, um den Inhalt zu suchen, an die das Steuerelement hinzufügen möchten. Filtern Sie beispielsweise im Feld Kennung ** Bildschirmlayout ** Feld mit einem Wert von "F2CP16: 9M".
3.  Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie beispielsweise "Namen aus: F2CP16: 9M Bildschirmlayout Kennung: F2CP16: 9M".
4.  ** ** Bereich auf.
5.  Gehen Sie den Aufforderungen, um den Bereich zu starten. Wenn Sie auf Anmeldeinformationen aufgefordert werden, geben Sie die gleichen Anmeldeinformationen ein, die verwendet wurden, als der Bildschirmlayouts Bereich ** ** von der Seite ausgelöst wurde.
6.  Wenn Sie sich anmelden, erscheint eine Seite, die bis die ähnlich befindet sich unten. Das Layout ist abhängig von in Anpassungen unterscheiden, die für Ihren Filiale vorgenommen wurden.

![screenlayout-pic-1 ([]. /media/screenlayout-pic-1.png)]". /media/screenlayout-pic-1.png) Wählen eine Anzeigeoption aus
-----------------------

Zwei verfügbare Konfigurationsoptionen. Wählen Sie die Option, die am für den Shop bearbeitet, und folgen Sie den Anweisungen des verbleibenden, Kontrolle einzurichten zu beenden. Die zwei Optionen:
-   Empfehlungen sind immer angezeigt.
-   A ** Empfehlungen ** Registerkarte wird im Gitter auf der rechten Seite des Bildschirms.

#### <a name="to-make-recommendations-always-visible"></a>Weitere Empfehlungen stets sichtbar werden

1.  Reduzieren Sie die Höhe des Buchungspositionsdetailbereichs, dass er die gleichen wie der Höhe Debitorenbereich sein bleibt. [] (. /media/picture-2.png) [] (screenlayout-pic-2![. /media/screenlayout-pic-2.png)]". /media/screenlayout-pic-2.png)
2.  Klicken Sie im auf der linken Seite, das per Drag & Drop der Empfehlungssteuerelement zwischen dem und dem Buchungspositionsdetailbereich Schaltflächenraster im mittleren unteren Bildschirmrand Buchung. Ändern Sie die Steuerung Größe passt damit es in diesen Leerzeichen. [] (. /media/picture-3.png) [] (screenlayout-pic-3![. /media/screenlayout-pic-3.png)]". /media/screenlayout-pic-3.png)
3.  Klicken ** X um ** Bereich zu speichern und zu beenden.
4.  In Dynamics 365 für Arbeitsgänge, fahren ** Einzelhandel und Handel ** &gt; ** Einzelhandel IT ** &gt; ** Verteilungszeitpläne **.
5.  Wählen Sie in der Liste aus ** 1090 Register **.
6.  ** Auf Ausführung nun **.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>So geben Sie eine Empfehlungsregisterkarte Schaltflächenraster Feld auf der rechten Seite des Bildschirms hinzufügen

1.  Klicken Sie im Leerraum unter der letzten Registerkarte im Schaltflächenraster mit der rechten Maustaste auf der rechten Seite der Seite in ist.
2.  ** Auf Abgleichen mit **.![picture-5 ([]. /media/picture-5.png)]". /media/picture-5.png)
3.  ** Auf neue ** Registerkarte.
4.  Suchen Sie die neue, der Sie momentan Registerkarte hinzugefügt. Sie müssen einen Bildlauf nach unten durch.
5.  Im ** Inhalt ** wählen Sie aus Dropdown ** empfohlene ** Produkte. ![picture-6 ([]. /media/picture-6.png)]". /media/picture-6.png)
6.  Wählen Sie im ** Beschriftung ** Feld geben einen Namen für die Empfehlungsregisterkarte ein. Beispielsweise empfohlene Produkte "Typ".
7.  ** Bild ** Wählen Sie im Feld das Bild aus, die auf der Registerkarte angezeigt.
8.  Click **OK**. Die Registerkarte wird im neue Schaltflächenraster.
9.  Klicken ** X um ** Bereich zu speichern und zu beenden.
10. In Dynamics 365 für Arbeitsgänge, fahren ** Einzelhandel und Handel ** &gt; ** Einzelhandel IT ** &gt; ** Verteilungszeitpläne **.
11. Wählen Sie in der Liste aus ** 1090 Register **.
12. ** Auf Ausführung nun **.


<a name="see-also"></a>Siehe auch
--------

[Personalisierter Produktempfehlungsüberblick] (personalized-product-recommendations.md)


