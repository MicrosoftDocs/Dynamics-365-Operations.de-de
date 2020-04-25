---
title: Manuelles Erstellen von Serviceaufträgen
description: Serviceaufträge können mithilfe einer Servicevereinbarung oder mithilfe des Formulars **Serviceaufträge** manuell erstellt werden.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d80461694a28a0842155cbd8ca224c37bd85dde7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202697"
---
# <a name="create-service-orders-manually"></a>Manuelles Erstellen von Serviceaufträgen    

[!include [banner](../includes/banner.md)]


Serviceaufträge können mithilfe einer Servicevereinbarung oder mithilfe des Formulars **Serviceaufträge** manuell erstellt werden. Sie haben außerdem die Möglichkeit, einen Serviceauftrag auf der Grundlage eines Projekts zu erstellen.

> [!TIP]
> <P>Serviceaufträge können auch mithilfe automatischer Prozesse erstellt werden. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Manuelles Erstellen eines Serviceauftrags auf der Grundlage einer Servicevereinbarung

1.  Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.

2.  Wählen Sie eine Servicevereinbarung aus, oder erstellen Sie eine neue Servicevereinbarung.

3.  Klicken Sie auf die Registerkarte **Liefern** und in der Gruppe **Erstellen** auf **Geplante Serviceaufträge** um das **Serviceaufträge erstellen**-Formular zu öffnen.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Manuelles Erstellen eines Serviceauftrags im Formular "Serviceaufträge"

1.  Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.

2.  Drücken Sie STRG+N, um einen neuen Serviceauftrag zu erstellen.

3.  Erstellen Sie Serviceauftragspositionen für den Serviceauftrag.

> [!NOTE]
> <P>Wenn das Kontrollkästchen <STRONG>Ohne Servicevertrag zulassen</STRONG> im Formular <STRONG>Serviceverwaltungsparameter</STRONG> aktiviert ist, können Sie die Buchungen der Serviceauftragspositionen vornehmen, ohne den Serviceauftrag einer Servicevereinbarung zuzuordnen. Wenn das Kontrollkästchen deaktiviert ist, müssen Sie den manuell erstellten Serviceauftrag einem Projekt zuordnen, bevor Sie die Serviceauftragspositionen buchen.</P>

## <a name="create-a-service-order-from-a-project"></a>Erstellen eines Serviceauftrags auf der Grundlage eines Projekts

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** \> **Allgemein** \> **Projekte** \> **Alle Projekte**.

2.  Klicken Sie im Formular **Projekte** auf den **Aktivitätsbereich**, klicken Sie auf die Registerkarte **Verwalten** \> klicken Sie auf **Service** \> **Serviceaufträge**.

3.  Führen Sie das vorherige Verfahren zur manuellen Erstellung eines Serviceauftrags über das Formular "**Serviceaufträge**" durch. Im Feld **Projektkennung** wird die Projektreferenz angezeigt.

> [!NOTE]
> <P>Wenn das Kontrollkästchen <STRONG>Ohne Servicevertrag zulassen</STRONG> im Formular <STRONG>Serviceverwaltungsparameter</STRONG> aktiviert ist, können Sie die Buchungen der Serviceauftragspositionen vornehmen, ohne den Serviceauftrag einer Servicevereinbarung zuzuordnen. Wenn das Kontrollkästchen deaktiviert ist, müssen Sie den manuell erstellten Serviceauftrag einem Projekt zuordnen, bevor Sie die Serviceauftragspositionen buchen.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Erstellen eines Serviceauftrags über das Formular "Auftrag"

Serviceaufträge können im Formular **Aufträge** erstellen, indem Sie den Assistenten **Neuen auftragsbasierten Serviceauftrag erstellen**.

1.  Klicken auf Bereichsseitenknoten: **Vertrieb und Marketing** \> **Gemeinsam** \> **Aufträge** \> **Alle Aufträge**.

2.  Öffnen Sie den entsprechenden Auftrag.

3.  Klicken Sie auf der Registerkarte **Aufträge** auf **Serviceauftrag**, um den Assistenten **Neuen auftragsbasierten Serviceauftrag erstellen** zu starten.

4.  Klicken Sie auf **Weiter \>** und schließen Sie dann die folgenden Schritte auf der Seite **Vereinbarung für Serviceauftrag auswählen** ab:
    
      - Wählen Sie im Feld **Servicevertrag** die Servicevereinbarung aus, der der neue Serviceauftrag zugeordnet werden soll.
    
      - Optional: Ordnen Sie diesen Serviceauftrag im Feld **Projektkennung** einem bestimmten Projekt zu.

5.  Klicken Sie auf **Weiter \>** und schließen Sie dann die folgenden Schritte auf der Seite **Serviceauftrag erstellen** ab:
    
      - Geben Sie im Feld **Bevorzugte Servicezeit** ein Datum und eine Uhrzeit für den Beginn des Serviceeinsatzes ein.
    
      - Optional: Ändern Sie den Text im Feld **Beschreibung**. Dieses Feld enthält standardmäßig die Beschreibung der auf der vorherigen Seite ausgewählten Servicevereinbarung.
    
      - Wählen Sie im Feld **Verantwortlich** die Kennung des für die Vereinbarung zuständigen Mitarbeiters und ggf. die Kennung des vom Debitor bevorzugten Technikers für den Serviceeinsatz aus.
    
      - Wählen Sie im Feld **Kontaktkennung** die Person im Unternehmen des Debitors aus, die im Zusammenhang mit diesem Serviceauftrag kontaktiert werden soll.

6.  Klicken Sie auf **Weiter\>** und anschließend auf **Abschließen**.


## <a name="see-also"></a>Siehe auch

[Serviceaufträge](service-orders.md)

[Automatische Erstellung von Serviceaufträgen](create-service-orders-automatically.md)

[Klassenformular "Serviceaufträge erstellen"](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 

