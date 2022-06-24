---
title: Vorhersagen für Kundenzahlungen aktivieren
description: In diesem Artikel wird erläutert, wie Sie die Funktion „Debitorenzahlungsvorhersagen“ in Finance Insights aktivieren und konfigurieren.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f04ee9db5efe3595dea30d641c5097d6b90c0d77
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898206"
---
# <a name="enable-customer-payment-predictions"></a>Vorhersagen für Kundenzahlungen aktivieren

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie die Funktion „Debitorenzahlungsvorhersagen“ in Finance Insights aktivieren und konfigurieren. Sie aktivieren die Funktion im Arbeitsbereich **Funktionsverwaltung** und geben die Konfigurationseinstellungen auf der Seite **Konfiguration von Finance Insights** ein. Dieser Artikel enthält auch Informationen, mit denen Sie die Funktion effektiv nutzen können.

> [!NOTE]
> Bevor Sie die folgenden Schritte ausführen, müssen Sie die erforderlichen Schritte im Artikel [Konfigurieren für Finance Insights](configure-for-fin-insites.md) ausführen.

1. Aktivieren Sie die Debitorenzahlungsvorhersage-Funktion:

    1. Öffnen Sie den Arbeitsbereich **Funktionsverwaltung**.
    2. Wählen Sie **Nach Updates suchen**.
    3. Sichen Sie auf der Registerkarte **Alle** nach **Zahlungsvorhersagen für Debitoren**. Wenn Sie diese Funktion nicht finden, suchen Sie nach **(Vorschau) Zahlungsvorhersagen für Debitoren**. 
    4. Aktivieren Sie die Funktion.

    Die Funktion „Zahlungsvorhersagen für Debitoren“ ist jetzt aktiviert und kann konfiguriert werden.

2. Konfigurieren Sie die Debitorenzahlungseinblicke-Funktion:

    1. Gehen Sie zu **Kredit und Inkasso \> Einrichtung \> Finance Insights \> Zahlungsvorhersagen für Debitoren**.
    2. Wählen Sie auf der **Konfiguration von Finance Insights**-Seite auf der **Zahlungsvorhersagen für Debitoren**-Registerkarte den Link **Die im Vorhersagemodell verwendeten Datenfelder anzeigen** an, um die **Datenfelder für das Vorhersagemodell**-Seite anzuzeigen. Dort können Sie die Standardliste der Felder anzeigen, die zum Erstellen des Vorhersagemodells für künstliche Intelligenz (KI) für Debitorenzahlungsvorhersagen verwendet werden.

        Um die Standardliste der Felder zum Erstellen des Vorhersagemodells zu verwenden, schließen Sie die **Datenfelder für das Vorhersagemodell**-Seite und legen Sie dann auf der **Konfiguration von Finance Insights**-Seite die **Funktion aktivieren** Option auf **Ja** fest.
        
   > [!NOTE]
   > Die Funktion **Vorhersagen für Kundenzahlungen** erfordert mehr als 100 Transaktionen in den letzten sechs bis neun Monaten. Bei den Transaktionen kann es sich um Freitextrechnungen, Verkaufsaufträge und Kundenzahlungen handeln. Diese Daten müssen über die Einstellungen **Pünktlich**, **Spät** und **Sehr spät** verteilt sein.    
     

    3. Geben Sie den „sehr späten“ Transaktionszeitraum an, um zu definieren, was der **Sehr spät**-Vorhersage-Bucket für Ihr Unternehmen bedeutet.

        Für jede offene Rechnung sagt das System die Zahlungswahrscheinlichkeit in drei Buckets voraus: **Pünktlich**, **Verspätet** und **Sehr spät**.

        - **Pünktlich** – Dieser Bucket enthält Zahlungen, deren Zahlung voraussichtlich am oder vor dem Fälligkeitsdatum der Transaktion erfolgt.
        - **Verspätet** – Dieser Bucket enthält Zahlungen, die voraussichtlich nach dem Fälligkeitsdatum der Transaktion, jedoch vor dem Beginn des „sehr späten“ Transaktionszeitraums gezahlt werden.
        - **Sehr spät** – Dieser Bucket enthält Zahlungen, die voraussichtlich nach dem Beginn des „sehr späten“ Transaktionszeitraums gezahlt werden.

        > [!NOTE]
        > Wenn Sie den Transaktionszeitraum „sehr spät“ ändern und **Schwellenwert für „Verspätet“ ändern** auswählen, nachdem das KI-Vorhersagemodell für Debitorenzahlungen erstellt wurde, wird das vorhandene Vorhersagemodell gelöscht und ein neues Modell erstellt. Das neue Vorhersagemodell verschiebt Transaktionen basierend auf den zur Definition eingegebenen Einstellungen in den „sehr späten“ Zeitraum.

    4. Nachdem Sie den Transaktionszeitraum „sehr spät“ definiert haben, wählen Sie **Vorhersagemodell erstellen** aus, um das Vorhersagemodell zu erstellen. Der **Vorhersagemodell**-Abschnitt auf der **Konfiguration von Finance Insights**-Seite zeigt den Status des Vorhersagemodells.

        > [!NOTE]
        > Sie können jederzeit während der Erstellung des Vorhersagemodells **Modellerstellung zurücksetzen** auswählen, um den Prozess neu zu starten.

    Die Funktion wurde konfiguriert und kann jetzt verwendet werden.

Nachdem die Funktion aktiviert und konfiguriert und das Vorhersagemodell erstellt wurde und funktioniert, zeigt der **Vorhersagemodell**-Abschnitt der **Parameter für Finance Insights**-Seite die Genauigkeit des Modells.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
