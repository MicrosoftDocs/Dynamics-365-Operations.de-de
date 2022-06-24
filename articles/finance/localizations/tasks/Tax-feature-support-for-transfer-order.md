---
title: Unterstützung der Steuerfunktion bei Umlagerungsaufträgen
description: In diesem Artikel wird die neue Steuerfunktionsunterstützung für Umlagerungsaufträge mithilfe des Steuerberechnungsdienstes erläutert.
author: Kai-Cloud
ms.date: 10/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 281ee90b7cae2d24d37d0684ad9975118560bb3e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869980"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Unterstützung der Steuerfunktion bei Umlagerungsaufträgen

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Informationen zur Steuerberechnung und Buchungsintegration in Umlagerungsaufträgen. Mit dieser Funktion können Sie die Steuerberechnung und Buchung in Umlagerungsaufträgen für Bestandsübertragungen einrichten. Nach den Bestimmungen der Europäischen Union (EU) zur Mehrwertsteuer (MwSt.) werden Bestandsübertragungen als innergemeinschaftliche Versorgung und innergemeinschaftliche Akquisitionen betrachtet.

Um diese Funktionalität zu konfigurieren und zu verwenden, müssen Sie drei Hauptschritte ausführen:

1. **RCS-Einrichtung:** Richten Sie im Regulatory Configuration Service die Steuerfunktion, Steuercodes und die Anwendbarkeit von Steuercodes für die Ermittlung des Steuercodes in Umlagerungsaufträgen ein.
2. **Dynamics 365 Finance-Einrichtung:** Aktivieren Sie in Finance die Funktion **Steuer im Umlagerungsauftrag**, richten Sie die Berechnungsdienstparameter für den Bestand ein und richten Sie die wichtigsten Steuerparameter ein.
3. **Bestandseinrichtung:** Richten Sie die Bestandskonfiguration für Umlagerungsauftragstransaktionen ein.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Einrichten von RCS für Steuer- und Umlagerungsauftragstransaktionen

Befolgen Sie diese Schritte, um die Steuer einzurichten, die in einem Umlagerungsauftrag enthalten ist. In dem hier gezeigten Beispiel erfolgt der Umlagerungsauftrag von den Niederlanden nach Belgien.

1. Wählen Sie auf der Seite **Steuerliche Merkmale** auf der Registerkarte **Versionen** den Entwurf der Funktionsversion aus und wählen Sie dann **Bearbeiten**.

2. Wählen Sie auf der Seite **Einrichtung der Steuerfunktionen** auf der **Steuercode**-Registerkarte **Hinzufügen** aus, um neue Steuercodes zu erstellen. In diesem Beispiel werden drei Steuercodes erstellt: **NL-befreit**, **BE-RC-21** und **BE-RC+21**.

    - Wenn ein Umlagerungsauftrag aus einem Lager in den Niederlanden versendet wird, wird der niederländische Steuercode für Mehrwertsteuerbefreiung (**NL-befreit**) angewandt.
      
        Erstellen Sie den Steuercode **NL-befreit**.
        1. Wählen Sie **Hinzufügen**, geben Sie **NL-befreit** in dem **Steuercode**-Feld ein.
        2. Wählen Sie **Nach Nettobetrag** in dem **Steuerkomponente**-Feld.
        3. Wählen Sie **Speichern** aus.
        4. Wählen Sie **Hinzufügen** in der **Satz**-Tabelle.
        5. Stellen Sie **Ist befreit** auf **Ja** im Abschnitt **Allgemein** ein.
        6. Geben Sie im Feld **Befreiungscode** **C** ein.

    - Wenn ein Umlagerungsauftrag in einem belgischen Lager eingeht, wird die Verlagerung der Steuerschuld mithilfe der Steuercodes **BE-RC-21** und **BE-RC+21** angewendet.
        
        Erstellen Sie den Steuercode **BE-RC-21**.      
        1. Wählen Sie **Hinzufügen**, geben Sie **BE-RC-21** in dem **Steuercode**-Feld ein.
        2. Wählen Sie **Nach Nettobetrag** in dem **Steuerkomponente**-Feld.
        3. Wählen Sie **Speichern** aus.
        4. Wählen Sie **Hinzufügen** in der **Satz**-Tabelle.
        5. Geben Sie **-21** im Feld **Steuersatz** ein.
        6. Stellen Sie **Ist Verlagerung der Steuerschuld** auf **Ja** im Abschnitt **Allgemein** ein.
        7. Wählen Sie **Speichern** aus.
        
        Erstellen Sie den Steuercode **BE-RC+21**.
        1. Wählen Sie **Hinzufügen**, geben Sie **BE-RC-21** in dem **Steuercode**-Feld ein.
        2. Wählen Sie **Nach Nettobetrag** in dem **Steuerkomponente**-Feld.
        3. Wählen Sie **Speichern** aus.
        4. Wählen Sie **Hinzufügen** in der **Satz**-Tabelle.
        5. Geben Sie **21** im Feld **Steuersatz** ein.
        6. Wählen Sie **Speichern** aus.

3. Definieren Sie die Steuergruppe.
    1. Wählen Sie **Spalten verwalten**, und wählen Sie dann das Zeilenfeld **Steuergruppe**.
    2. Wählen Sie **->** und dann **OK** aus.
    3. Wählen Sie zum Hinzufügen einer Steuergruppe **Hinzufügen**.
    4. Geben Sie in der Spalte **Steuergruppe** **AR-EU** ein und wählen Sie dann den Steuercode **NL-Befreit**.
    5. Wählen Sie zum Hinzufügen einer Steuergruppe **Hinzufügen**.
    6. Geben Sie in der Spalte **Steuergruppe** **RC-VAT** ein und wählen Sie dann die Steuercodes **BE-RC-21** und **BE-RC+21**.
4. Definieren Sie die Artikelsteuergruppe.
    1. Wählen Sie **Spalten verwalten**, und wählen Sie dann das Zeilenfeld **Artikelsteuergruppe**.
    2. Wählen Sie **->** und dann **OK** aus.
    3. Wählen Sie zum Hinzufügen einer Artikelsteuergruppe **Hinzufügen**.
    4. Geben Sie **VOLL** in der Spalte **Artikelsteuergruppe** ein. Wählen Sie die Steuercodes **BE-RC-21**, **BE-RC+21**, und **NL-Befreit** aus.
5. Definieren Sie die Anwendbarkeit der Steuergruppe.

    1. Wählen Sie **Spalten verwalten** und dann Spalten aus, die zum Erstellen der Anwendbarkeitstabelle verwendet werden sollen.

        > [!NOTE]
        > Stellen Sie sicher, dass Sie die Spalten **Geschäftsprozess** und **Steuerarten** zur Tabelle hinzufügen. Beide Spalten sind für die Steuerfunktionalität in Umlagerungsaufträgen von wesentlicher Bedeutung.

    2. Fügen Sie Anwendbarkeitsregeln hinzu. Lassen Sie das Feld **Steuergruppe** nicht leer.
        
        Fügen Sie eine neue Regel für die Lieferung von Umlagerungsaufträgen hinzu.
        1. Wählen Sie **Hinzufügen** in der **Anwendbarkeitsregeln**-Tabelle.
        2. Wählen Sie im **Geschäftsprozess**-Feld **Bestand** aus, um die Regel für einen Umlagerungsauftrag anwendbar zu machen.
        3. Geben Sie im **Lieferung von Land/Region**-Feld **NLD** ein.
        4. Geben Sie im **Lieferung an Land/Region**-Feld **BEL** ein.
        5. Wählen Sie im **Steuerart**-Feld **Ausgabe** aus, um die Regel für die Lieferung eines Umlagerungsauftrags anwendbar zu machen.
        6. Wählen Sie im Feld **Steuergruppe** **AR-EU**.
        
        Fügen Sie eine weitere Regel für den Empfang von Umlagerungsaufträgen hinzu.
        
        1. Wählen Sie **Hinzufügen** in der **Anwendbarkeitsregeln**-Tabelle.
        2. Wählen Sie im **Geschäftsprozess**-Feld **Bestand** aus, um die Regel für einen Umlagerungsauftrag anwendbar zu machen.
        3. Geben Sie im **Lieferung von Land/Region**-Feld **NLD** ein.
        4. Geben Sie im **Lieferung an Land/Region**-Feld **BEL** ein.
        5. Wählen Sie im **Steuerart**-Feld **Eingabe** aus, um die Regel für den Empfang eines Umlagerungsauftrags anwendbar zu machen.
        6. Wählen Sie im Feld **Steuergruppe** **RC-VAT**.

6. Definieren Sie die Anwendbarkeit der Artikelsteuergruppe.

    1. Wählen Sie **Spalten verwalten** und dann Spalten aus, die zum Erstellen der Anwendbarkeitstabelle verwendet werden sollen.
    2. Fügen Sie Anwendbarkeitsregeln hinzu. Lassen Sie das Feld **Artikelsteuergruppe** nicht leer.
        
        Fügen Sie eine neue Regel für die Lieferung un den Empfang von Umlagerungsaufträgen hinzu.
        1. Wählen Sie auf der Seite **Anwendbarkeitsregeln** die Option **Hinzufügen**.
        2. Wählen Sie im **Geschäftsprozess**-Feld **Bestand** aus, um die Regel für den Umlagerungsauftrag anwendbar zu machen.
        3. Wählen Sie im Feld **Artikelsteuergruppe** **VOLL**.
7. Vervollständigen und veröffentlichen Sie die neue Steuerfunktionsversion.


## <a name="set-up-finance-for-transfer-order-transactions"></a>Einrichten von Finance für Umlagerungsauftragstransaktionen

Führen Sie folgende Schritte aus, um Steuern für Umlagerungsaufträge zu aktivieren und einzurichten.

1. Navigieren Sie in Finanzen zu **Arbeitsbereiche** > **Funktionsverwaltung**.
2. Suchen und wählen Sie in der Liste die Funktion **Steuer im Umlagerungsauftrag** und dann **Jetzt aktivieren** aus, um sie einzuschalten.

    > [!IMPORTANT]
    > Die Funktion **Steuer im Umlagerungsauftrag** ist vollständig vom Berechnungsdienst abhängig. Daher kann es erst aktiviert werden, nachdem Sie den Berechnungsdienst installiert haben.

    ![Funktion „Steuer in Umlagerungsauftrag“.](../media/image7.png)

3. Aktivieren Sie den Steuerberechnungsdienst und wählen Sie den **Bestand**-Geschäftsprozess.

    > [!IMPORTANT]
    > Sie müssen diesen Schritt für jede juristische Person in Finance ausführen, für die der Steuerberechnungsdienst und die Funktionalität für Steuern in Umlagerungsaufträgen verfügbar sein sollen.

    1. Gehen Sie zu **Steuern** > **Einrichtung** > **Steuerkonfiguration** > **Steuerberechnungsparameter**.
    2. Wählen Sie im **Geschäftsprozess**-Feld **Bestand** aus.

4. Stellen Sie sicher, dass der Mechanismus zur Verlagerung der Steuerschuld eingerichtet ist. Gehen Sie zu **Hauptbuch** \> **Einrichtung** \> **Parameter** und überprüfen Sie dann auf der Registerkarte **Verlagerung der Steuerschuld**, ob die Option **Verlagerung der Steuerschuld aktivieren** auf **Ja** gesetzt ist.

    ![Aktivieren der Option zur Verlagerung der Steuerschuld.](../media/image9.png)

5. Stellen Sie sicher, dass die zugehörigen Steuercodes, Steuergruppen, Artikelsteuergruppen und Mehrwertsteuererfassungsnummern in Finance gemäß dem Steuerberechnugsdienstleitfaden eingerichtet wurden.
6. Richten Sie ein Zwischentransitkonto ein. Dieser Schritt ist nur erforderlich, wenn die Steuer, die auf einen Umlagerungsauftrag angewendet wird, nicht auf einen Mechanismus für Steuerbefreiung oder Verlagerung der Steuerschuld anwendbar ist.

    1. Navigieren Sie zu **Steuer** > **Einstellungen** > **Mehrwertsteuer** > **Sachkontenbuchungsgruppen**.
    2. Wählen Sie im Feld **Zwischentransit** ein Sachkonto aus.

       ![Auswählen eines Zwischentransitkontos.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Einrichten von Basisbestand für Umlagerungsauftragstransaktionen

Befolgen Sie diese Schritte, um den Grundbestand einzurichten und Umlagerungsauftragstransaktionen zu ermöglichen.

1. Erstellen Sie „Lieferung von“- und „Lieferung an“-Sites für Ihre Lager in verschiedenen Ländern oder Regionen und fügen Sie die primäre Adresse für jede Site hinzu.

    1. Gehen Sie zu **Lagerortverwaltung** > **Einrichtung** > **Lager** > **Standorte**.
    2. Wählen Sie **Neu**, um die Site zu erstellen, die Sie später einem Lager zuweisen werden.
    3. Wiederholen Sie Schritt 2 für alle anderen Sites, die Sie erstellen müssen.

    > [!NOTE]
    > Eine der von Ihnen erstellten Sites sollte **Transit** benannt werden. In späteren Schritten dieses Verfahrens ordnen Sie diese Site dem Transitlager zu, damit steuerliche Bestandsbelege in „Lieferung“- und „Empfang“-Transaktionen für Umlagerungsaufträge gebucht werden können. Die Adresse der Transit-Site spielt für die Steuerberechnung keine Rolle. Sie können es daher leer lassen.

    ![Einrichten von Sites.](../media/image11.png)

2. Erstellen Sie „Lieferung von“-, „Transit“- und „Lieferung an“-Lagerorte. Alle Adressinformationen, die in einem Lagerhaus verwaltet werden, überschreiben die Site-Adresse bei der Steuerberechnung.

    1. Navigieren Sie zu **Lagerortverwaltung** > **Einstellungen** > **Lagerort** > **Lagerorte**.
    2. Wählen Sie **Neu**, um einen Lagerort zu erstellen und einer entsprechenden Site zuzuweisen.
    3. Wiederholen Sie Schritt 2, um nach Bedarf ein Lager für jede Site zu erstellen.

       ![Einrichten von Lagerorten.](../media/image12.png)

    > [!NOTE]
    > Für ein „Lieferung von“-Lager muss ein Transitlager im Feld **Transitlager** für Umlagerungsauftragstransaktionen ausgewählt werden.
    >
    > ![Transitlager auswählen.](../media/image13.png)

3. Überprüfen Sie, ob die Bestandsbuchungskonfiguration für Umlagerungsauftragstransaktionen eingerichtet ist.

    1. Navigieren Sie zu **Bestandsverwaltung** > **Einstellungen** > **Buchung** > **Buchung**.
    2. Überprüfen Sie auf der Registerkarte **Bestand**, ob ein Sachkonto für beide Buchungen, **Lagerabgang** und **Lagerzugang**, eingerichtet ist.

        ![Einrichten der Lagerabgang- und Lagerzugang-Buchung.](../media/image14.png)

    3. Stellen Sie sicher, dass ein Sachkonto für die **Umlagerungszugang**-Buchung eingerichtet ist.

        ![Einrichten der Umlagerungszugang-Buchung.](../media/image15.png)

    4. Stellen Sie sicher, dass ein Sachkonto für die **Umlagerungsabgang**-Buchung eingerichtet ist.

        ![Einrichten der Umlagerungsabgang-Buchung.](../media/image16.png)
        
        
  [!INCLUDE[footer-include](../../../includes/footer-banner.md)]
