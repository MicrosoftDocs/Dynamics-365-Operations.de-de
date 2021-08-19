---
title: Arbeitsvorlage für Bestellungen einrichten
description: In diesem Thema wird beschrieben, wie Sie eine einfache Arbeitsvorlage einrichten, die beim Einlagern empfangener Artikel verwendet wird.
author: ShylaThompson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fb9038a680bd804f12ea7debe1eb631f6631da1da9667e4c335ed8673a179f1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718827"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Arbeitsvorlage für Bestellungen einrichten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine einfache Arbeitsvorlage einrichten, die beim Einlagern empfangener Artikel verwendet wird. Arbeitsvorlagen bestimmen die Sammlung von Anweisungen, die dem Lagerarbeiter auf einem mobilen Gerät dargestellt wird, wenn Artikel aus dem Wareneingangsbereich umgelagert werden. Sie können diese Prozedur mit dem Daten des Demodatenunternehmen USMF oder mit eigenen Daten verwenden. Bevor Sie dieses Handbuch starten, erstellen Sie eine Arbeitspool-ID. In diesem Beispiel wird eine Arbeitspool-ID mit der Bezeichnung "Eingehend" verwendet. Diese Prozedur ist für die Lagerverwaltung vorgesehen.

1. Gehen Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einrichtung > Arbeit > Arbeitsvorlagen**.
2. Wählen Sie im Feld **Arbeitsauftragsart** **Bestellungen**.

## <a name="create-a-work-template-header"></a>Kopfzeile der Arbeitsvorlage erstellen
1. Wählen Sie **Neu** aus.
2. Geben Sie im Feld **Laufende Nummer** eine Zahl ein. Dies ist die Sequenz, in der die Arbeitsvorlagen ausgewertet werden. Sie können die Reihenfolge bei Bedarf ändern.  
3. Geben Sie in das Feld **Arbeitsvorlage** einen Wert ein. Dies ist eindeutige Bezeichner für die Vorlage.  
4. Geben Sie im Feld **Arbeitsvorlagenbeschreibung** einen Wert ein.
    - Die Option **Gültig** wird erst aktiviert, wenn Sie alle Informationen, die von der Vorlage benötigt werden, ausgefüllt und dann **Speichern** ausgewählt haben.  
    - Ein Arbeitsauftrag vom Typ **Bestellauftrag** kann nicht automatisch bearbeitet werden, also lassen Sie die Option **Automatischer Prozess** auf **Nein** gesetzt.  
5. Geben Sie im Feld **Arbeitsplatz-ID** einen Wert ein. Mithilfe der Arbeitspool-IDs können Sie die Arbeit in Gruppen organisieren. Der Wert, der hier festgelegt ist, ist der Standardwert für jede Arbeit, die anhand dieser Vorlage erstellt wird.  
6. Geben Sie im Feld **Arbeitspriorität** `1` ein. Dadurch wird die Wichtigkeit der Arbeit angegeben. Der hier festgelegte Wert wird als Standard für jede Arbeit festgelegt, die anhand dieser Vorlage erstellt wird.  
7. Wählen Sie **Speichern**. Sie müssen den Kopf der Arbeitsvorlage speichern, bevor die Schaltfläche **Abfrage bearbeiten** verfügbar wird.  

## <a name="set-up-the-query-for-the-work-template"></a>Abfrage für Arbeitsvorlage erstellen
1. Wählen Sie **Abfrage bearbeiten**. Wir legen eine Einschränkung fest, damit die Vorlage nur innerhalb eines bestimmten Lagerorts verwendet werden kann.  
2. Wählen Sie **Hinzufügen** aus.
3. Geben Sie in das Feld **Feld** der neuen Zeile `warehouse` ein.
4. Geben Sie im Feld **Kriterien** einen Wert ein.
5. Wählen Sie **OK**.
6. Wählen Sie **Ja** aus.

## <a name="set-work-template-details"></a>Arbeitsvorlagendetails einrichten
1. Wählen Sie **Neu** aus.
2. Wählen Sie im Feld **Arbeitsart** **Auswahl**.
3. Geben Sie im Feld **Arbeitsklassen-ID** `purchase` ein. Die hier festgelegte Arbeitsklasse ist der Standard für alle Arbeitspositionen vom Typ "Entnahme", die anhand dieser Vorlage erstellt werden. Die Arbeitsklasse kann nicht von den Arbeitsauftragspositionen überschrieben werden. Arbeitsklassen werden verwendet, um den Typ der Arbeitsauftragspositionen zuzuweisen und/oder einzuschränken, die ein Lagerarbeiter auf einem mobilen Gerät verarbeiten kann.  
4. Wählen Sie **Neu** aus.
5. Wählen Sie im Feld **Arbeitsart** **Eingabe**.
6. Geben Sie im Feld **Arbeitsklassenkennung** einen Wert ein. Die Entnahme- und Einlagerungsanweisungen sind ein Satz. Jede Entnahme/Einlagerung muss dieselbe Arbeitsklasse aufweisen. Verwenden Sie die gleiche Arbeitsklasse, die Sie für die Entnahmeanweisung angegeben haben.  
7. Wählen Sie **Speichern**. Beachten Sie, dass das Kontrollkästchen **Valid** nun aktiviert ist.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]