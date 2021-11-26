---
title: Vorhersagen für Kundenzahlungen aktivieren
description: In diesem Thema wird erläutert, wie Sie die Funktion „Debitorenzahlungsvorhersagen“ in Finance Insights aktivieren und konfigurieren.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 16ccd7f2e11f0b46aaa646de272e668d29ccc0c0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752927"
---
# <a name="enable-customer-payment-predictions"></a>Vorhersagen für Kundenzahlungen aktivieren

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Sie die Funktion „Debitorenzahlungsvorhersagen“ in Finance Insights aktivieren und konfigurieren. Sie aktivieren die Funktion im Arbeitsbereich **Funktionsverwaltung** und geben die Konfigurationseinstellungen auf der Seite **Konfiguration von Finance Insights** ein. Dieses Thema enthält auch Informationen, mit denen Sie die Funktion effektiv nutzen können.

> [!NOTE]
> Bevor Sie die folgenden Schritte ausführen, müssen Sie die erforderlichen Schritte im Thema [Konfigurieren für Finance Insights](configure-for-fin-insites.md) ausführen.

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
