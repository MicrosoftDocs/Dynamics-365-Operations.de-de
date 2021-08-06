---
title: Vorhersagen für Debitorenzahlungen aktivieren (Vorschau)
description: In diesem Thema wird erläutert, wie Sie die Funktion „Debitorenzahlungsvorhersagen“ in Finance Insights aktivieren und konfigurieren.
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.openlocfilehash: 03320aa925ae94ef39d54e64701846089ec66084
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638583"
---
# <a name="enable-customer-payment-predictions-preview"></a>Vorhersagen für Debitorenzahlungen aktivieren (Vorschau)

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Funktion „Debitorenzahlungsvorhersagen“ in Finance Insights aktivieren und konfigurieren. Sie aktivieren die Funktion im Arbeitsbereich **Funktionsverwaltung** und geben die Konfigurationseinstellungen auf der Seite **Parameter für Finance Insights** ein. Dieses Thema enthält auch Informationen, mit denen Sie die Funktion effektiv nutzen können.

> [!NOTE]
> Bevor Sie die folgenden Schritte ausführen, müssen Sie die erforderlichen Schritte im Thema [Konfigurieren für Finance Insights](configure-for-fin-insites.md) ausführen.

1. Verwenden Sie Informationen von der Umgebungsseite in Microsoft Dynamics Lifecycle Services (LCS), um eine Verbindung mit der primären Instanz von Azure-SQL für diese Umgebung herzustellen. Führen Sie den folgenden Transact-SQL-Befehl (T-SQL) aus, um Flights für die Sandboxumgebung zu aktivieren. (Möglicherweise müssen Sie den Zugriff für Ihre IP-Adresse in LCS aktivieren, bevor Sie eine Remoteverbindung mit Application Object Server \[AOS\] herstellen können.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > Überspringen Sie diesen Schritt, wenn Sie Version 10.0.20 oder höher verwenden oder wenn Sie eine Service Fabric-Bereitstellung verwenden. Das Finance Insights-Team sollte das Flight bereits für Sie aktiviert haben. Wenn die Funktion nicht im **Funktionsverwaltung**-Arbeitsbereich angezeigt wird, oder wenn Sie Probleme beim Aktivieren haben, wenden Sie sich an <fiap@microsoft.com>. 

2. Aktivieren Sie die Debitorenzahlungseinblicke-Funktion:

    1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.
    2. Suchen Sie die Funktion namens **Debitorenzahlungseinblicke (Vorschau)**.
    3. Wählen Sie **Jetzt aktivieren**.

    Die Debitorenzahlungsvorschau-Funktion ist jetzt aktiviert und kann konfiguriert werden.

3. Konfigurieren Sie die Debitorenzahlungseinblicke-Funktion:

    1. Gehen Sie zu **Kredit und Inkasso \> Einrichtung \> Finance Insights \> Parameter für Finance Insights**.

        [![Seite der Parameter für Finance Insights, bevor die Funktion konfiguriert wird.](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. Wählen Sie auf der **Parameter für Finance Insights**-Seite auf der **Debitorenzahlungseinblicke**-Registerkarte den Link **Die im Vorhersagemodell verwendeten Datenfelder anzeigen** an, um die **Datenfelder für das Vorhersagemodell**-Seite anzuzeigen. Dort können Sie die Standardliste der Felder anzeigen, die zum Erstellen des Vorhersagemodells für künstliche Intelligenz (KI) für Debitorenzahlungsvorhersagen verwendet werden.

        Um die Standardliste der Felder zum Erstellen des Vorhersagemodells zu verwenden, schließen Sie die **Datenfelder für das Vorhersagemodell**-Seite und legen Sie dann auf der **Parameter für Finance Insights**-Seite die **Funktion aktivieren** Option auf **Ja** fest.

    3. Geben Sie den „sehr späten“ Transaktionszeitraum an, um zu definieren, was der **Sehr spät**-Vorhersage-Bucket für Ihr Unternehmen bedeutet.

        Für jede offene Rechnung sagt das System die Zahlungswahrscheinlichkeit in drei Buckets voraus: **Pünktlich**, **Verspätet** und **Sehr spät**.

        - **Pünktlich** – Dieser Bucket enthält Zahlungen, deren Zahlung voraussichtlich am oder vor dem Fälligkeitsdatum der Transaktion erfolgt.
        - **Verspätet** – Dieser Bucket enthält Zahlungen, die voraussichtlich nach dem Fälligkeitsdatum der Transaktion, jedoch vor dem Beginn des „sehr späten“ Transaktionszeitraums gezahlt werden.
        - **Sehr spät** – Dieser Bucket enthält Zahlungen, die voraussichtlich nach dem Beginn des „sehr späten“ Transaktionszeitraums gezahlt werden.

        > [!NOTE]
        > Wenn Sie den Transaktionszeitraum „sehr spät“ ändern und **Schwellenwert für „Verspätet“ ändern** auswählen, nachdem das KI-Vorhersagemodell für Debitorenzahlungen erstellt wurde, wird das vorhandene Vorhersagemodell gelöscht und ein neues Modell erstellt. Das neue Vorhersagemodell verschiebt Transaktionen basierend auf den zur Definition eingegebenen Einstellungen in den „sehr späten“ Zeitraum.

    4. Nachdem Sie den Transaktionszeitraum „sehr spät“ definiert haben, wählen Sie **Vorhersagemodell erstellen** aus, um das Vorhersagemodell zu erstellen. Der **Vorhersagemodell**-Abschnitt auf der **Parameter für Finance Insights**-Seite zeigt den Status des Vorhersagemodells.

        > [!NOTE]
        > Sie können jederzeit während der Erstellung des Vorhersagemodells **Modellerstellung zurücksetzen** auswählen, um den Prozess neu zu starten.

    Die Funktion wurde konfiguriert und kann jetzt verwendet werden.

Nachdem die Funktion aktiviert und konfiguriert und das Vorhersagemodell erstellt wurde und funktioniert, zeigt der **Vorhersagemodell**-Abschnitt der **Parameter für Finance Insights**-Seite die Genauigkeit des Modells, wie in der folgenden Abbildung gezeigt an.

[![Genauigkeit des Vorhersagemodells auf der Seite Parameter für Financial Insights.](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Freigabedetails

Die öffentliche Finance Insights-Vorschau ist für Testbereitstellungen in den Vereinigten Staaten von Amerika, Europa und Großbritannien verfügbar. Microsoft fügt schrittweise Unterstützung für weitere Regionen hinzu.

Öffentliche Vorschaufunktionen können und sollten nur in Sandbox-Umgebungen der Stufe 2 aktiviert werden. Einrichtungs- und KI-Mopelle, die in einer Sandbox-Umgebung erstellt werden, können nicht in eine Produktionsumgebung migriert werden. Weitere Informationen finden Sie unter [Ergänzende Nutzungsbedingungen für Microsoft Dynamics 365 Vorschauen](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
