---
title: "Hinzufügen eines Empfehlungssteuerelement der Buchungsseite auf einem POS-Gerät"
description: "In diesem Thema wird beschrieben, wie Sie einem Empfehlungssteuerelement dem Buchungsbildschirm auf einem Verkaufsstelle (POS)-Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 for Retail Arbeitsgänge hinzufügen."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4cdfcbdcafdbbbab21c398ebc8002a45742e33e6
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Hinzufügen eines Empfehlungssteuerelement der Buchungsseite auf einem POS-Gerät

[!include[banner](includes/banner.md)]


In diesem Thema wird beschrieben, wie Sie einem Empfehlungssteuerelement dem Buchungsbildschirm auf einem Verkaufsstelle (POS)-Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 for Retail Arbeitsgänge hinzufügen.

Sie können Produktempfehlungen zu Ihrem POS-Gerät anzeigen, wenn Sie Microsoft Dynamics 365 for Retail verwenden. *Empfehlungen* sind Artikel, die Ihre Kunden möglicherweise interessieren und zwar auf Basis der ihrer Einkaufshistorie, Artikel auf einem Wunschzettel und Artikel, die andere Kunden online und in der physische Filiale gekauft haben. Um Produktempfehlungen anzuzeigen, müssen Sie dem Buchungsbildschirm eine Steuerung mithilfe des Bildschirmlayoutdesigners hinzufügen.

## <a name="open-layout-designer"></a>Layoutdesigner öffnen
1.  Wechseln Sie zu **Einzelhandel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS** &gt; **Bildschirmlayouts**.
2.  Suchen Sie mithilfe der Filteroptionen den Bildschirm, dem Sie eine Steuerung hinzufügen möchten. Filtern Sie beispielsweise im Feld **Bildschirmlayout-ID** einen Wert von "F2CP16: 9M".
3.  Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie beispielsweise "Name: F2CP16: 9M Bildschirmlayout Kennung: F2CP16: 9M".
4.  Klicken Sie auf **Layout-Designer**
5.  Folgen Sie den Aufforderungen, um den Layout-Designer zu starten. Wenn Sie aufgefordert werden, die Anmeldeinformationen einzugeben, geben Sie die gleichen Anmeldeinformationen ein, die verwendet wurden, als die Seite **Bildschirmlayouts** ausgelöst wurde.
6.  Wenn Sie sich anmelden, erscheint eine Seite, ähnlich jener unten. Das Layout ist verschieden, abhängig von den Anpassungen, die für Ihre Filiale vorgenommen wurden.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Wählen eine Anzeigeoption aus
-----------------------

Es stehen zwei Optionen für die Konfiguration zur Verfügung. Wählen Sie die Option, die am besten für Ihren Shop passt und folgen Sie den Anweisungen, um die Steueurung eizrichten. Es gibt zwei Optionen:
-   Empfehlungen sind immer angezeigt.
-   A Registerkarte **Empfehlungen** wird im Gitter auf der rechten Seite des Bildschirms angezeigt.

#### <a name="to-make-recommendations-always-visible"></a>Um Empfehlungen immer anzuzeigen

1.  Reduzieren Sie die Höhe des Buchungspositionsdetailbereichs, so dass er die gleiche Höhe hat wie der Debitorenbereich links.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Klicken Sie im Menü auf der linken Seite, und ziehen Sie das Empfehlungssteuerelement zwischen den Buchungspositionsdetailbereich und den Schaltflächenraster im mittleren unteren Transaktlions-Bildschirmrands. Ändern Sie die Steuerung, so dass die Größe in diesen Bereich passt.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Klicken Sie auf **X**, um zu speichern und den Layout-Designer zu beenden.
4.  In Dynamics 365 for Retail gehen Sie zu **Einzelhandel** &gt; **Einzelhandel IT** &gt; **Verteilungszeitpläne** .
5.  Wählen Sie in der **1090 Anmelden**
6.  Klicken Sie auf **Jetzt ausführen**

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Um eine Registerkarte "Empfehlungen" dem Schaltflächengitter auf der rechten Seite des Bildschirms hinzuzufügen

1.  Machen Sie einen Rechtsklick im Leerraum unter der letzten Registerkarte im Schaltflächenraster auf der rechten Seite.
2.  Klicken Sie auf **Anpassen**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Klicken Sie auf **Neue Registerkarte**
4.  Suchen Sie die neue Registerkarte, die Sie hinzugefügt haben. Sie müssen möglicherweise einen Bildlauf nach unten machen.
5.  Wählen Sie im Dropdown-Menü unter **Inhalte** **Empfohlene Produkte**. [![pic-6](./media/pic-6.png)](./media/pic-6.png)
6.  Wählen Sie im Feld **Beschriftung** einen Namen für die Registerkarte "Empfehlungen". Zum Beispiel Tpy "Empfohlene Produkte".
7.  Wählen Sie im Feld **Fild** das Bild, das auf der Registerkarte angezeigt werden soll.
8.  Klicken Sie auf **OK**. Die Registerkarte wird im neuen Schaltflächenraster angezeigt.
9.  Klicken Sie auf **X**, um zu speichern und den Layout-Designer zu beenden.
10. In Dynamics 365 for Retail gehen Sie zu **Einzelhandel** &gt; **Einzelhandel IT** &gt; **Verteilungszeitpläne** .
11. Wählen Sie in der **1090 Anmelden**
12. Klicken Sie auf **Jetzt ausführen**


<a name="see-also"></a>Siehe auch
--------

[Personalisierte Produktempfehlungen, Übersicht](personalized-product-recommendations.md)




