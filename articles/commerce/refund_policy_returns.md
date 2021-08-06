---
title: Erstellen und Aktualisieren einer Rücklieferungs- und Rückerstattungsrichtlinie für einen Kanal
description: In diesem Thema wird erläutert, wie Sie eine Rücklieferungs- und Rückerstattungsrichtlinie für einen Kanal einrichten.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: ca5797cfc2d92c4cbc98d3f64d60e1fd260f0418
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558296"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Retouren- und Rückerstattungsrichtlinie für einen Kanal erstellen und aktualisieren

[!include [banner](includes/banner.md)]

Die Kanal-Rücklieferungsrichtlinie in Dynamics 365 Commerce ermöglicht Einzelhändlern, Durchsetzungsbestimmungen für Zahlungsmittel festzulegen, die für die Verarbeitung einer Rücklieferung an einem POS-Gerät (Point of Sale) zugelassen werden können.  

In diesem Thema werden die Schritte beschrieben, wie Sie eine Rücklieferungs- und Rückerstattungsrichtlinie für einen Kanal einrichten.

Der Geltungsbereich der Richtlinie beschränkt sich derzeit auf die Festlegung der Zahlungsmittel, die für einen Kanal zulässig sind. Die Liste „Zulässig“ basiert auf den Zahlungsmethoden, die für den Kauf verwendet wurden. Beispiel:

- Wenn ein Kauf mit einer Geschenkkarte getätigt wurde, besteht die Shoprichtlinie darin, Rückerstattungen nur für eine neue Geschenkkarte zu verarbeiten oder eine Gutschrift für den Shop zu erteilen. 
- Wenn ein Verkauf mit Bargeld erfolgte, sind die zulässigen Optionen für die Rückerstattung Bargeld, Geschenkkarte und Kundenkonto, jedoch keine Kreditkarte. 

## <a name="enable-return-policy"></a>Aktivieren der Rücklieferungsrichtlinie

Führen Sie die folgenden Schritte aus, um die Rückgaberichtlinienfunktionalität in der Commerce-Zentralverwaltung zu aktivieren.

1. Gehen Sie in Dynamics 365 Commerce zum Arbeitsbereich **Funktionsverwaltung**.
1. Suchen Sie in der Liste der Funktionsnamen nach der Funktion **Aktivieren der Kanal-Rücklieferungsrichtlinien**.
1. Wählen Sie **Jetzt aktivieren**.
1. Führen Sie auf der Seite **Verteilungsplan** den Vorgang **1110** (globale Konfiguration) zum Verteilen der Funktionsänderung aus.

## <a name="initialize-the-commerce-scheduler"></a>Commerce-Planer initialisieren

Nach dem Aktivieren der **Richtlinien zur Kanalrückgabe aktivieren** müssen Sie den Commerce-Planer initialisieren, um sicherzustellen, dass neue Änderungen der Funktionsdatenbank über Commerce Data Exchange (CDX)-Synchronisierung hinzugefügt werden. 

Um den Commerce-Planer in der Commerce-Zentralverwaltung zu initialisieren, folgen Sie diesen Schritten.

- Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Commerce-Planer initialisieren**. Suchen Sie alternativ nach „Commerce-Planer initialisieren“.
- Stellen Sie im Dialogfeld **Commerce-Planer initialisieren** sicher, dass die Option **Vorhandene Konfiguration löschen** auf **Nein** gesetzt ist, und wählen Sie dann **OK** aus.

## <a name="configure-return-policy"></a>Konfigurieren der Rücklieferungsrichtlinie

Folgen Sie diesen Schritten, um eine Rücklieferungsrichtlinie für einen Einzelhandelsshop oder einen Online-Einzelhandelskanal zu konfigurieren.

1. Gehen Sie zu **Einzelhandel und Handel** \> **Kanaleinrichtung** \> **Rücklieferungen** \> **Kanal-Rücklieferungsrichtlinie**.

1. Wählen Sie **Neu** aus, um eine neue Rücklieferungsrichtlinienvorlage zu erstellen. Um eine vorhandene Vorlage zu verwenden, wählen Sie die Vorlage im linken Bereich aus. Fügen Sie für neue Vorlagen einen Namen und eine Beschreibung hinzu, anhand derer Sie die Richtlinie identifizieren können, wenn sie auf den Kanal angewendet wird.

   ![Hinzufügen einer neuen Rückgaberichtlinie.](media/Return-policy-page1.png)
     
   
1. Definieren Sie im Abschnitt **Zulässige Rückerstattungszahlungsmethoden** die **zulässigen** Rücklieferungszahlungsmittel, die für jede Zahlungsmethode spezifisch sind.
   ![Festlegen zulässiger Zahlungsmethoden pro Zahlungstyp.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - Die Zahlungsmethoden leiten sich aus den für die Organisation festgelegten Zahlungsmethoden ab.
    > - Durch Hinzufügen eines zulässigen Rücklieferungszahlungsmitteltyps für jede aufgelistete Zahlungsmethode wird sichergestellt, dass Rücklieferungen an den zulässigen Rücklieferungszahlungsmitteltyp erfolgen können.
    
1. Ordnen Sie die Rücklieferungsrichtlinienvorlage den Filialen zu, in denen sie verwendet werden soll. Wählen Sie in der Registerkarte **Retail Channels** die Option **Hinzufügen** aus und ordnen Sie die verfügbaren Kanäle zu. 

    - Wählen Sie im Dialogfenster **Organisationsknoten auswählen** die Filialen, Regionen und Organisationen aus, denen die Vorlage zugeordnet werden soll.
    - Jeder Filiale kann nur eine Rücklieferungsrichtlinienvorlage zugeordnet werden.
    - Verwenden Sie die Pfeiltasten, um Filialen, Regionen oder Organisationen auszuwählen.
    - Das Gültigkeitsdatum der Richtlinie ist das Datum, an dem die Richtlinien auf die Kanäle angewendet und die Kanalvorgänge ausgeführt werden. 

    ![Auswählen des Organisationsknoten-Dialogfensters.](media/Return-policy-page3.png)

1. Führen Sie auf der Seite **Verteilungszeitplan** den Vorgang **1070** durch, um die Kanal-Rücklieferungsrichtlinie für den POS verfügbar zu machen.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Vorschau der Kanal-Rücklieferungsrichtlinie im POS

Folgen Sie den Schritten in einem der folgenden Beispiele, um die zulässigen Rücklieferungszahlungsmitteltypen im POS anzuzeigen.

1. Melden Sie sich als Kassierer oder Manager am POS an.
1. Wählen Sie unter **Schicht und Kasse** die Option **Erfassung anzeigen** aus.
1. Wählen Sie die Transaktion aus, die Teil der Rücklieferung ist. 
1. Wählen Sie die Artikel, die erstattet werden sollen, und die Zahlungsmethode aus.  
    - Befindet sich das ausgewählte Zahlungsmittel in der Liste der zulässigen Rücklieferungszahlungsmitteltypen, kann der Kassierer die Transaktion abschließen.
    - Wenn das ausgewählte Zahlungsmittel nicht zulässig ist, wird eine Fehlermeldung angezeigt.
    - Wählen Sie **Fälliger Betrag** aus, um eine Liste aller zulässigen Rücklieferungszahlungsmitteltypen anzuzeigen.

– oder –

1. Melden Sie sich als Kassierer oder Manager am POS an.
1. Wählen Sie **Rücklieferungstransaktion** aus und geben Sie die Quittungs-ID mit einem Barcode-Scan oder durch manuelle Eingabe ein. 
1. Wählen Sie die Transaktion aus, die Teil der Rücklieferung ist. 
1. Wählen Sie die Artikel, die erstattet werden sollen, und die Zahlungsmethode aus.  
    - Befindet sich das ausgewählte Zahlungsmittel in der Liste der zulässigen Rücklieferungszahlungsmitteltypen, kann der Kassierer die Transaktion abschließen.
    - Wenn das ausgewählte Zahlungsmittel nicht zulässig ist, wird eine Fehlermeldung angezeigt.
    - Wählen Sie **Fälliger Betrag** aus, um eine Liste aller zulässigen Rücklieferungszahlungsmitteltypen anzuzeigen.

![Nicht zulässiger Rückerstattungstyp.](media/Return-policy-page6.png)



![Zulässige Rückerstattungstypen.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
