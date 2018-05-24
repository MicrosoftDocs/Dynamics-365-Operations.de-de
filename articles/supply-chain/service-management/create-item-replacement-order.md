---
title: Erstellen eines Artikelersetzungsauftrags
description: "Aufträge für die Ersetzung von Artikeln werden normalerweise nach der Rückgabe und Prüfung eines Produkts erstellt."
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1f0cd629658972f98e2233dfa287940c4444b82a
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="create-an-item-replacement-order"></a>Erstellen eines Artikelersetzungsauftrags 

[!include [banner](../includes/banner.md)]


Aufträge für die Ersetzung von Artikeln werden normalerweise nach der Rückgabe und Prüfung eines Produkts erstellt. Wenn jedoch ein Artikel ersetzt werden muss, bevor er zurückgegeben wurde, oder wenn der Originalartikel nicht zurückgegeben wird, können Sie einen Auftrag für die Ersetzung des Artikels sofort nach dem Erstellen einer Rücklieferung erstellen.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Erstellen eines Ersetzungsauftrags, nachdem Sie einen Artikel erhalten haben, der zurückgegeben wurde

1.  Klicken auf **Vertrieb und Marketing** \> **Gemeinsam** \> **Rücklieferungen** \> **Alle Rücklieferungen**.

2.  Erstellen Sie eine neue Rücklieferung, oder wählen Sie einen Zurückgegebenen Auftrag aus der Liste aus, um das Formular **Rücklieferung - RMA-Nummer: %1, %2** zu öffnen.

3.  Klicken Sie **Rücklieferungsposition** und wählen Sie anschließend **Wiederbeschaffungsartikel** aus.

4.  Wählen Sie den Artikel aus, durch den der zurückgelieferten Artikel ersetzt werden soll. Geben Sie die Artikelspezifikationen ein, und klicken Sie anschließend auf **Übernehmen**.

5.  Klicken Sie auf **Lieferschein**, um den Lieferschein für die Rücklieferung zu generieren. Ein Auftrag wird für den Ersetzungsartikel generiert, den Sie ausgewählt haben.
    
    Nachdem der Auftrag für den Ersetzungsartikel erstellt wurde, werden Kaufverträge automatisch durchsucht, und wenn es einen entsprechenden Kaufvertrag gibt, wird dieser für den Auftrag übernommen.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Erstellen Sie einen Ersetzungsauftrag, bevor Sie einen Artikel erhalten, der zurückgegeben wird

1.  Klicken auf **Vertrieb und Marketing** \> **Gemeinsam** \> **Rücklieferungen** \> **Alle Rücklieferungen**.

2.  Erstellen Sie eine neue Rücklieferung, oder wählen Sie einen Zurückgegebenen Auftrag aus der Liste aus, um das Formular **Rücklieferung - RMA-Nummer: %1, %2** zu öffnen.

3.  Klicken Sie auf **Auftrag suchen**, wenn Sie den Auftrag für den zurückgelieferten Artikel ermitteln möchten. Schließen Sie das Formular **Auftrag suchen** ab und klicken Sie auf **OK**, um das Formular zu schließen und zum Formular **Retoure -: Rücksendungsnummer "%1", " %2 "** zurückzukehren. Die Auftragsposition für den zurückgelieferten Artikel wird zur Rücklieferung kopiert.

4.  Klicken Sie auf **Ersatzauftrag**, um das Formular **Auftrag erstellen** zu öffnen.

5.  Aktivieren Sie das Kontrollkästchen **Rücklieferungspositionen kopieren**, um Details aus der im Formular **Rücklieferung - RMA-Nummer: %1, %2** ausgewählten Rücklieferung in diesen Auftrag zu übertragen.

6.  Geben Sie ggf. Details ein oder ändern Sie diese.
    
    Wenn Sie den Auftrag in Schritt 3 identifiziert haben und wenn die Auftragsposition für den zurückgelieferten Artikel mit einem Kaufvertrag verknüpft ist, wird die Kennung des entsprechenden Kaufvertrags für den Artikelersetzungsauftrags automatisch im Feld **Kaufvertragskennung** angezeigt.

7.  Klicken Sie auf **OK**, um das Formular **Auftrag erstellen** zu schließen und das Formular **Auftrag** zu öffnen, in dem der Vorgang fortgesetzt werden kann, um Informationen für den neuen Auftrag einzugeben. Alle zutreffenden Rücklieferungspositionen werden in den neuen Auftrag kopiert. 
    
    Wenn die Kennung des Kaufvertrags automatisch im Feld **Kaufvertragskennung** angezeigt wird, dann ist der Kaufvertrag mit dem Auftragskopf für den Artikelersetzungsauftrags verknüpft worden. Wenn es eine entsprechende Zusage im Kaufvertrag gibt, die noch nicht erfüllt wurde und der Auftrag erstellt wird, bevor der Kaufvertrag abläuft, wird eine Verknüpfung zwischen der Kaufvertragsposition und der Auftragsposition eingerichtet. Daher werden Informationen aus dem Kaufvertrag, wie Artikelpreis, in die neue Auftragsposition kopiert. 
  



