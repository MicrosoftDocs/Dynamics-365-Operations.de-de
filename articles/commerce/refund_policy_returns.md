---
title: Erstellen und Aktualisieren einer Rücklieferungs- und Rückerstattungsrichtlinie für einen Kanal
description: In diesem Thema wird erläutert, wie Sie eine Rücklieferungs- und Rückerstattungsrichtlinie für einen Kanal einrichten.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: c2a9325f09ffe43c3436b7e0ca2ab511e1f57f83
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412665"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Erstellen und Aktualisieren einer Rücklieferungs- und Rückerstattungsrichtlinie für einen Kanal

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Übersicht

Die Kanal-Rücklieferungsrichtlinie in Dynamics 365 Commerce ermöglicht Einzelhändlern, Durchsetzungsbestimmungen für Zahlungsmittel festzulegen, die für die Verarbeitung einer Rücklieferung an einem POS-Gerät (Point of Sale) zugelassen werden können.  

In diesem Thema werden die Schritte beschrieben, wie Sie eine Rücklieferungs- und Rückerstattungsrichtlinie für einen Kanal einrichten.

Der Geltungsbereich der Richtlinie beschränkt sich derzeit auf die Festlegung der Zahlungsmittel, die für einen Kanal zulässig sind. Die Liste „Zulässig“ basiert auf den Zahlungsmethoden, die für den Kauf verwendet wurden. Beispiel:

- Wenn ein Kauf mit einer Geschenkkarte getätigt wurde, besteht die Shoprichtlinie darin, Rückerstattungen nur für eine neue Geschenkkarte zu verarbeiten oder eine Gutschrift für den Shop zu erteilen. 
- Wenn ein Verkauf mit Bargeld erfolgte, sind die zulässigen Optionen für die Rückerstattung Bargeld, Geschenkkarte und Kundenkonto, jedoch keine Kreditkarte. 


## <a name="enable-return-policy"></a>Aktivieren der Rücklieferungsrichtlinie

Gehen Sie wie folgt vor, um die Funktion der Kanal-Rücklieferungsrichtlinie zu aktivieren:

1. Gehen Sie in Dynamics 365 Commerce zum Arbeitsbereich **Funktionsverwaltung**.
2. Suchen Sie in der Liste der Funktionsnamen nach der Funktion **Aktivieren der Kanal-Rücklieferungsrichtlinien**.
3. Wählen Sie **Jetzt aktivieren**. 

## <a name="configure-return-policy"></a>Konfigurieren der Rücklieferungsrichtlinie

Folgen Sie diesen Schritten, um eine Rücklieferungsrichtlinie für einen Einzelhandelsshop oder einen Online-Einzelhandelskanal zu konfigurieren.

1. Gehen Sie zu **Retail und Commerce** \> **Kanaleinrichtung** \> **Rücklieferungen** \> **Kanal-Rücklieferungsrichtlinie**.

2. Wählen Sie **Neu** aus, um eine neue Rücklieferungsrichtlinienvorlage zu erstellen. Um eine vorhandene Vorlage zu verwenden, wählen Sie die Vorlage im linken Bereich aus. Fügen Sie für neue Vorlagen einen Namen und eine Beschreibung hinzu, anhand derer Sie die Richtlinie identifizieren können, wenn sie auf den Kanal angewendet wird.

   ![Hinzufügen einer neuen Rücklieferungsrichtlinie](media/Return-policy-page1.png "Hinzufügen einer neuen Rücklieferungsrichtlinie")
     
   
3. Definieren Sie im Abschnitt **Zulässige Rückerstattungszahlungsmethoden** die **zulässigen** Rücklieferungszahlungsmittel, die für jede Zahlungsmethode spezifisch sind.
   ![Hinzufügen von Zahlungsmethoden](media/Return-policy-page2.PNG "Festlegen zulässiger Zahlungsmethoden pro Zahlungstyp")
   
    > [!IMPORTANT]
    > - Die Zahlungsmethoden leiten sich aus den für die Organisation festgelegten Zahlungsmethoden ab.
    > - Durch Hinzufügen eines zulässigen Rücklieferungszahlungsmitteltyps für jede aufgelistete Zahlungsmethode wird sichergestellt, dass Rücklieferungen an den zulässigen Rücklieferungszahlungsmitteltyp erfolgen können.
    
4. Ordnen Sie die Rücklieferungsrichtlinienvorlage den Filialen zu, in denen sie verwendet werden soll. Wählen Sie in der Registerkarte **Retail Channels** die Option **Hinzufügen** aus und ordnen Sie die verfügbaren Kanäle zu. 

    - Wählen Sie im Dialogfenster **Organisationsknoten auswählen** die Filialen, Regionen und Organisationen aus, denen die Vorlage zugeordnet werden soll.
    - Jeder Filiale kann nur eine Rücklieferungsrichtlinienvorlage zugeordnet werden.
    - Verwenden Sie die Pfeiltasten, um Filialen, Regionen oder Organisationen auszuwählen.
    - Das Gültigkeitsdatum der Richtlinie ist das Datum, an dem die Richtlinien auf die Kanäle angewendet und die Kanalvorgänge ausgeführt werden. 

    ![Auswählen des Organisationsknoten-Dialogfensters](media/Return-policy-page3.PNG "Auswählen des Organisationsknoten-Dialogfensters")

5. Führen Sie auf der Seite **Verteilungszeitplan** den Vorgang **1070** durch, um die Kanal-Rücklieferungsrichtlinie für den POS verfügbar zu machen.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Vorschau der Kanal-Rücklieferungsrichtlinie im POS

Folgen Sie den Schritten in einem der folgenden Beispiele, um die zulässigen Rücklieferungszahlungsmitteltypen im POS anzuzeigen.

1. Melden Sie sich als Kassierer oder Manager am POS an.
2. Wählen Sie unter **Schicht und Kasse** die Option **Erfassung anzeigen** aus.
3. Wählen Sie die Transaktion aus, die Teil der Rücklieferung ist. 
4. Wählen Sie die Artikel, die erstattet werden sollen, und die Zahlungsmethode aus.  
- Befindet sich das ausgewählte Zahlungsmittel in der Liste der zulässigen Rücklieferungszahlungsmitteltypen, kann der Kassierer die Transaktion abschließen.
- Wenn das ausgewählte Zahlungsmittel nicht zulässig ist, wird eine Fehlermeldung angezeigt.
- Wählen Sie **Fälliger Betrag** aus, um eine Liste aller zulässigen Rücklieferungszahlungsmitteltypen anzuzeigen.

– oder –

1. Melden Sie sich als Kassierer oder Manager am POS an.
2. Wählen Sie **Rücklieferungstransaktion** aus und geben Sie die Quittungs-ID mit einem Barcode-Scan oder durch manuelle Eingabe ein. 
3. Wählen Sie die Transaktion aus, die Teil der Rücklieferung ist. 
4. Wählen Sie die Artikel, die erstattet werden sollen, und die Zahlungsmethode aus.  
- Befindet sich das ausgewählte Zahlungsmittel in der Liste der zulässigen Rücklieferungszahlungsmitteltypen, kann der Kassierer die Transaktion abschließen.
- Wenn das ausgewählte Zahlungsmittel nicht zulässig ist, wird eine Fehlermeldung angezeigt.
- Wählen Sie **Fälliger Betrag** aus, um eine Liste aller zulässigen Rücklieferungszahlungsmitteltypen anzuzeigen.

![Nicht zulässige Rückerstattung](media/Return-policy-page6.png "Nicht zulässiger Rückerstattungstyp")



![Liste der Zahlungsmethoden](media/Return-policy-page5.PNG "Zulässige Rückerstattungstypen")
