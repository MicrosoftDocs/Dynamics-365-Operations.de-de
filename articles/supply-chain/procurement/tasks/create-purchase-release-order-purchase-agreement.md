---
title: Einen Freigabeauftrag für den Einkauf aus einem Kaufvertrag anwenden
description: Im folgenden Verfahren, wie ein Kaufvertrag verwendet, wenn Sie eine Bestellung erstellen.
author: kamaybac
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1913181e85929951ce240ac31a0ac3f1351f6ae51f6ed2790bae577b2100b308
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731246"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Einen Freigabeauftrag für den Einkauf aus einem Kaufvertrag anwenden

[!include [banner](../../includes/banner.md)]

Im folgenden Verfahren, wie ein Kaufvertrag verwendet, wenn Sie eine Bestellung erstellen. Der Kaufvertrag muss angewendet werden, wenn Sie die Bestellung anlegen, da es allgemeine Begriffe gibt, die in den Bestellkopf kopiert werden sollen. In der Regel steht diese Aufgabe von einem Einkaufsvertreter ausgeführt. Als Komponente für dieses Manuell, müssen Sie einen gültigen Kaufvertrag mit einer Produktmengenzusage für einen Kreditor und Artikel verwenden. Die gleichen Verfahren kann verwendet werden, wenn Sie einen Kaufvertrag mit anderen Typen von Zusagen haben.

## <a name="create-a-purchase-order"></a>Eine Bestellung erstellen

1. Gehen Sie zu **Produktion und Beschaffung \> Arbeitsbereiche \> Bestellvorbereitung**.
1. Wählen Sie im Aktivitätsbereich **Neue Bestellung** aus.
1. Der **Bestellung erstellen** Dialog öffnet sich. Wählen Sie ein **Kreditorenkonto** aus. Überprüfen Sie die anderen Adressfelder und passen Sie sie nach Bedarf an.
1. Erweitern Sie das Inforegister **Allgemein**.
1. Im **Kaufvertrag** suchen und wählen Sie die gültige Vereinbarung aus, die Sie verwenden möchten. Alle verfügbaren Vereinbarungen für den Kreditor werden hier aufgeführt.  
1. Wählen Sie **Ja** aus.
1. Wählen Sie **OK** aus.

## <a name="add-a-line"></a>Position hinzufügen

1. Geben Sie im Feld **Artikelnummer** einen Wert ein. Sind bestimmte Lager- oder Lagerplatzdimensionen auf der Zusage besteht, müssen Sie die denselben Werten in der Bestellposition eingeben, um die Vereinbarung auszunutzen.
1. Klicken Sie im Feld **Standort** auf die Dropdown-Schaltfläche, um die Suche zu öffnen. Der Standort bereits wird mit dem Standardwert aus dem Auftrag oder Kreditor ausgefüllt werden. Ist dies der Fall, fahren Sie diesen Schritt.  
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
1. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
1. Geben Sie im Feld **Menge** eine Zahl ein. Überprüfen Sie, ob der Preis aus der Zusage kopiert wird.  

## <a name="look-up-the-commitment"></a>Hiermit wird die Zusage

1. Wählen Sie **Zeile aktualisieren**.
1. Wählen Sie **Zuordnen** aus. Hier können Sie Details für den Kaufvertrag abrufen. So können Sie den Preis finden und ob der Preis und Rabatt korrigiert werden, damit es, das heißt dass, wenn Sie Preis oder Rabatt auf die Bestellung zu einem anderen Wert als auf der Zusage ändern, das System den Link entfernt, sodass die Bestellposition nicht die Zusage erfüllt. Sie können außerdem feststellen, ob das Maximum erzwungene Option ist aktiviert ist, das heißt, dass die Menge in der Zusage nicht überschritten werden kann, indem Sie alle Einkäufe summiert, die die Zusage erfüllen.  
1. Schließen Sie die Seite.

## <a name="look-up-the-purchase-agreement"></a>Rahmenbestellung einrichten

1. Wählen Sie im **Aktivitätsbereich** **Allgemein** aus.
1. Wählen Sie **Kaufvereinbarung**.
1. Schließen Sie die Seite.
1. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]