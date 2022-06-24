---
title: Serienetiketten neu drucken und Zyklusbeschriftungen stornieren
description: In diesem Artikel wird erläutert, wie vorhandene Serienetiketten storniert und neu gedruckt werden.
author: perlynne
ms.date: 07/09/2020
ms.topic: article
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: f9f057d9985fb8431ec7c9ced23f2cd3c476570d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871832"
---
# <a name="reprint-and-void-wave-labels"></a>Serienetiketten neu drucken und Zyklusbeschriftungen stornieren

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie Etiketten verwalten, die durch die Wellenverarbeitung generiert werden. (Eine ausführliche Beschreibung und Konfigurationsanweisungen finden Sie unter [Konfigurieren des Serienetikettendrucks](../warehousing/configure-wave-label-printing.md).)

Sie können Serienetiketten jederzeit erneut drucken. Beispielsweise müssen Sie möglicherweise ein einzelnes Etikett drucken, wenn ein vorhandenes Etikett verloren gegangen oder beschädigt ist. Alternativ muss ein Lagerarbeiter oder Vorgesetzter möglicherweise eine ganze Rolle Etiketten erneut drucken, wenn sich die Anzahl und/oder Zusammensetzung einer ganzen Reihe von Serienetiketten geändert hat (z. B. aufgrund von Lagermangel oder anderen Gründen). Selbst wenn sich nur die Anzahl der Kartons geändert hat, muss häufig die gesamte Rolle nachgedruckt werden, um die Gesamtzahl im Abschnitt „Karton X von Y“ jedes Etiketts genau zu halten.

Die Funktion zum Nachdrucken von Serienetiketten unterstützt die folgenden Funktionen:

- Drucken Sie erneut Etikette sowohl von Lagerort-App als auch vom Rich-Client.
- Etiketten stornieren und gleichtzeitig neu drucken. (Die Möglichkeit, Etiketten zu stornieren, ist beispielsweise in Szenarien von Entnahme mit unzureichender Menge eingebettet.)
- Serienetikettenverlauf löschen.

In diesem Artikel wird eine Sammlung von Szenarien vorgestellt, die anhand von Beispielen zeigen, wie mit der Funktion zum Nachdrucken von Serienetiketten gearbeitet wird.

> [!IMPORTANT]
> Um die in diesem Artikel vorgestellten Szenarien durchzuarbeiten, müssen Sie zuerst die relevanten Druckfunktionen für Serienetiketten aktivieren und konfigurieren, wie in [Konfigurieren des Serienetikettendrucks](../warehousing/configure-wave-label-printing.md) beschrieben. Für einige der Szenarien in diesem Artikel müssen Sie zunächst die Szenarien in diesem Artikel durcharbeiten, um die erforderlichen Beispieldaten zu generieren.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>Szenario 1: Etiketten aus dem Webclient erneut drucken

Sie können Serienetiketten von den folgenden Seiten anzeigen und erneut drucken. Wählen Sie im Aktivitätsbereich jeder Seite, auf der Registerkarte **Lieferungen** in der Gruppe **Zugehörige Informationen** die Option **Serienetiketten**.

- Alle Lieferungen \> Lieferdetails
- Alle Ladungen \> Ladungsdetails
- Alle Wellen
- Serienetiketten
- Wellenbeschriftungsverlauf

Führen Sie die folgenden Schritte aus, um ein Serienetikett vom Web-Client erneut zu drucken.

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Wählen Sie die Welle aus, aus der Etiketten neu gedruckt werden sollen.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Welle** in der Gruppe **Drucken** auf **Serienetiketten**.
1. Befolgen Sie einen oder beide der folgenden Schritte:

    - Um das Etikett erneut zu drucken, wählen Sie einen Drucker im Feld **Druckername** aus. (Lassen Sie dieses Feld leer, wenn Sie nur die Serienetikettendetails aktualisieren möchten, ohne die Beschriftung erneut zu drucken.)
    - Um das Etikett zu aktualisieren, wählen Sie das Kontrollkästchen **Serienetikettendetails aktualisieren**. (Lassen Sie dieses Kontrollkästchen deaktiviert, wenn Sie nur das vorherige Etikett erneut drucken möchten.)

    > [!NOTE]
    > Jedes Mal, wenn ein Serienetikett gedruckt oder neu gedruckt wird, werden seine Daten durch das entsprechende Serienetikett-Layout konvertiert und alle Platzhalter durch tatsächliche Werte ersetzt. Die resultierende Zeichenfolge wird als Datensatz im Serienetikettenverlauf gespeichert. Wenn das Kontrollkästchen **Serienetikettendetails aktualisieren** deaktiviert ist, werden die gespeicherten ZPL-Daten (Zebra Programming Language) verwendet, wenn ein Etikett erneut gedruckt wird. Wenn das Kontrollkästchen **Serienetikettendetails aktualisieren** aktiviert ist, wird eine neue Zeichenfolge generiert. Die vorhandenen Serienetiketten werden ebenfalls neu berechnet, und alle überschüssigen Etiketten (z. B. wenn die zugehörigen Arbeitspositionen gelöscht oder geändert wurden) werden als **Storniert** markiert und werden nicht nachgedruckt.

1. Wählen Sie **OK**, um Ihre Auswahl zu bestätigen.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>Szenario 2: Etiketten aus der Lagerort-App erneut drucken

Dieses Szenario gilt normalerweise, wenn eine Etikettenrolle verloren gegangen oder beschädigt ist. Es enthält ein Beispiel, das zeigt, wie Menüelemente für Mobilgeräte eingerichtet werden, mit denen Mitarbeiter einzelne und mehrere Etiketten erneut drucken können. Anschließend wird gezeigt, wie Sie diese neuen Menüelemente verwenden, während Sie an einem mobilen Gerät arbeiten.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>Die erforderlichen Menüpunkte und das Menü für das mobile Gerät einrichten

Bevor Mitarbeiter Etiketten von einem mobilen Gerät aus erneut drucken können, müssen Sie Menüelemente einrichten, um diese Funktionalität bereitzustellen, und diese Elemente dann zum Menü der Lagerort-App hinzufügen.

#### <a name="create-new-mobile-device-menu-items"></a>Erstellen neuer Menüelemente für ein mobiles Gerät

Führen Sie die folgenden Schritte aus, um eine neue Sammlung von Menüelementen zum erneuten Drucken von Etiketten aus der Lagerort-App zu erstellen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Erstellen Sie ein Menüelement und legen Sie die folgenden Werte dafür fest:

    - **Name des Menüelements:** *Einzelnes Serienetikett neu drucken*
    - **Titel:** *Einzelnes Serienetikett neu drucken*
    - **Modus:** *Indirekt*
    - **Aktivitätscode:** *Einzelnes Serienetikett neu drucken*

1. Erstellen Sie ein zweitess Menüelement und legen Sie die folgenden Werte dafür fest:

    - **Name des Menüelements:** *Etiketten erneut drucken (Artikel)*
    - **Titel:** *Serienetiketten neu drucken (Artikel)*
    - **Modus:** *Indirekt*
    - **Aktivitätscode:** *Mehrere Serienetiketten neu drucken*
    - **Filter zur Gruppierung von Arbeitslisten anzeigen:** *Ja*
    - **Systemgruppierungsfeld:** *ShipmentID*
    - **Systemgruppierungsetikett:** *Lieferungs-ID*
    - **Druckmodus:** *Produkt*

1. Wählen Sie im Aktivitätsbereich **Feldliste** aus, um eine Seite zu öffnen, auf der Sie die Felder auswählen können, die angezeigt werden, damit die Mitarbeiter die richtige Etikettenrolle identifizieren können.
1. Sie können bis zu sieben Felder anzeigen. Verwenden Sie die Dropdownlisten, um das Feld auszuwählen, das an jeder verfügbaren Position angezeigt wird. Lassen Sie alle Felder, die Sie nicht benötigen, leer. 

    Hier ist ein Beispiel:

    - **Anzeigefeld:** *LabelItemId*
    - **Anzeigefeld 2:** *LabelItemName*
    - **Anzeigefeld 3:** *InventQty*
    - **Anzeigefeld 4:** *LabelUnitId*

1. Schließen Sie die Seite.
1. Erstellen Sie ein drittes Menüelement und legen Sie die folgenden Werte dafür fest:

    - **Name des Menüelements:** *Etiketten erneut drucken (Enumeration)*
    - **Titel:** *Serienetiketten neu drucken (Enumeration)*
    - **Modus:** *Indirekt**
    - **Aktivitätscode:** *Mehrere Serienetiketten neu drucken*
    - **Filter zur Gruppierung von Arbeitslisten anzeigen:** *Ja*
    - **Systemgruppierungsfeld:** *ShipmentID*
    - **Systemgruppierungsetikett:** *Lieferungs-ID*
    - **Druckmodus:** *Enumeration*

1. Wählen Sie im Aktivitätsbereich **Feldliste** aus, und verwenden Sie dann die Dropdownlisten, um die Felder auszuwählen, die angezeigt werden, damit die Mitarbeiter die richtige Etikettenrolle identifizieren können (z. B. *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId*, und *NumberOfLabels*).
1. Schließen Sie die Seite.
1. Erstellen Sie ein viertes Menüelement und legen Sie die folgenden Werte dafür fest:

    - **Name des Menüelements:** *Etiketten erneut drucken (nach letztem)*
    - **Titel:** *Serienetiketten neu drucken (nach letztem)*
    - **Modus:** *Indirekt*
    - **Aktivitätscode:** *Mehrere Serienetiketten neu drucken*
    - **Filter zur Gruppierung von Arbeitslisten anzeigen:** *Ja*
    - **Systemgruppierungsfeld:** *ShipmentID*
    - **Systemgruppierungsetikett:** *Lieferungs-ID*
    - **Druckmodus:** *Letzte gute Serienetiketten-ID*

1. Wählen Sie im Aktivitätsbereich **Feldliste** aus, und verwenden Sie dann die Dropdownlisten, um die Felder auszuwählen, die angezeigt werden, damit die Mitarbeiter die richtige Etikettenrolle identifizieren können (z. B. *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId*, und *NumberOfLabels*).
1. Schließen Sie die Seite.

#### <a name="set-up-the-mobile-device-menu"></a>Menü für mobiles Gerät einrichten

Befolgen Sie diese Schritte, um Ihre neuen Menüelemente zum Menü der Lagerort-App hinzuzufügen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menü für mobiles Gerät**.
1. Wählen Sie ein vorhandenes Menü **Ausgehend** aus.
1. Suchen Sie in der Liste links die soeben erstellten Nachdruck-Menüelemente und fügen Sie sie dann mit der Rechtspfeiltaste zur Liste rechts hinzu.
1. Schließen Sie die Seite.

### <a name="use-cases"></a>Anwendungsfälle

Die hier bereitgestellten Anwendungsfälle enthalten Beispiele, die zeigen, wie die verschiedenen Menüelemente für Mobilgeräte verwendet werden, die Sie eingerichtet haben, damit Mitarbeiter Serienetiketten erneut drucken können.

Bevor Sie diese Anwendungsfälle bearbeiten, müssen die folgenden Voraussetzungen erfüllt sein:

- Demodaten müssen installiert sein und Sie müssen die juristische Person **USMF** auswählen.
- Das Drucken von Serienetiketten muss konfiguriert und einige Etiketten müssen generiert werden, wie in [Konfigurieren des Serienetikettendrucks](../warehousing/configure-wave-label-printing.md) beschrieben.

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Anwendungsfall 2.1: Ein einzelnes Serienetikett ist zerkratzt und muss erneut gedruckt werden.

1. Melden Sie sich bei der Warehouse-App als ein Benutzer mit Zugriff auf Lagerort *62* an. (Sie können sich bei den Standard-Demo-Daten mit *62* als Benutzer-ID und *1* als Passwort anmelden.)
1. Gehen Sie zu **Ausgehend \> Einzelnes Serienetikett neu drucken**.
1. Geben Sie die Serienetiketten-ID ein oder scannen Sie sie.
1. Wählen Sie den Drucker aus, auf dem erneut gedruckt werden soll.
1. Wählen Sie **OK**, um die Aktivität zu bestätigen.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Anwendungsfall 2.2: Mehrere Etiketten für Kartons desselben Artikels wurden beschädigt und müssen erneut gedruckt werden. Jedes Etikett hat einen Produktbarcode, aber keine Aufzählung oder SSCC-Nummer.

1. Melden Sie sich bei der Warehouse-App als ein Benutzer mit Zugriff auf Lagerort *62* an. (Sie können sich bei den Standard-Demo-Daten mit *62* als Benutzer-ID und *1* als Passwort anmelden.)
1. Gehen Sie zu **Ausgehend \> Etiketten erneut drucken (Artikel)**.
1. Geben Sie die Lieferungs-ID ein oder scannen Sie sie.
1. Wählen Sie die Kachel mit der richtigen Etikettenrolle zum erneuten Drucken aus.
1. Scannen Sie den Produktbarcode von einem vorhandenen Etikett, um zu bestätigen, dass die richtige Zeile ausgewählt wurde.
1. Geben Sie die Anzahl der Etiketten ein, die erneut gedruckt werden sollen.
1. Wählen Sie den Drucker aus, auf dem erneut gedruckt werden soll.
1. Wählen Sie **OK**, um die Aktivität zu bestätigen.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Anwendungsfall 2.3: Mehrere Etiketten für Kartons wurden aufgrund eines Druckerstaus nicht gedruckt. Da die Etiketten eine Aufzählung aufweisen, können Sie den Kartonbereich definieren, der erneut gedruckt werden soll.

1. Melden Sie sich bei der Warehouse-App als ein Benutzer mit Zugriff auf Lagerort *62* an. (Sie können sich bei den Standard-Demo-Daten mit *62* als Benutzer-ID und *1* als Passwort anmelden.)
1. Gehen Sie zu **Ausgehend \> Etiketten erneut drucken (Enumeration)**.
1. Geben Sie die Lieferungs-ID ein oder scannen Sie sie.
1. Wählen Sie die Kachel mit der richtigen Etikettenrolle zum erneuten Drucken aus.
1. Geben Sie den ersten Karton ein, für den ein Etikett nachgedruckt werden soll.
1. Geben Sie den letzten Karton ein, für den ein Etikett nachgedruckt werden soll. Alternativ können Sie dieses Feld leer lassen, um Etiketten für alle Kartons nach dem angegebenen ersten Karton erneut zu drucken.
1. Wählen Sie den Drucker aus, auf dem erneut gedruckt werden soll.
1. Wählen Sie **OK**, um die Aktivität zu bestätigen.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Anwendungsfall 2.4: Mehrere Etiketten für Kartons wurden aufgrund eines Druckerstaus nicht gedruckt. Das letzte gute Etikett hat eine Serienetiketten-ID, die als Barcode gedruckt wird.

1. Melden Sie sich bei der Warehouse-App als ein Benutzer mit Zugriff auf Lagerort *62* an. (Sie können sich bei den Standard-Demo-Daten mit *62* als Benutzer-ID und *1* als Passwort anmelden.)
1. Gehen Sie zu **Ausgehend \> Etiketten erneut drucken (nach letztem)**.
1. Geben Sie die Lieferungs-ID ein oder scannen Sie sie.
1. Wählen Sie die Kachel mit der richtigen Etikettenrolle zum erneuten Drucken aus.
1. Geben Sie die Serienetiketten-ID des letzten guten Serienetiketts ein oder scannen Sie sie. Die App identifiziert das nächste Etikett in der Sequenz als den ersten Karton, für den ein Etikett nachgedruckt wird.
1. Geben Sie den letzten Karton ein, für den ein Etikett nachgedruckt werden soll. Alternativ können Sie dieses Feld leer lassen, um Etiketten für alle Kartons nach dem angegebenen ersten Karton erneut zu drucken.
1. Wählen Sie den Drucker aus, auf dem erneut gedruckt werden soll.
1. Wählen Sie **OK**, um die Aktivität zu bestätigen.

## <a name="scenario-3-short-pick-and-reprint"></a>Szenario 3: Kurze Entnahme und Nachdruck

Bevor Sie dieses Szenario bearbeiten, müssen die folgenden Voraussetzungen erfüllt sein:

- Demodaten müssen installiert sein und Sie müssen die juristische Person **USMF** auswählen.
- Das Drucken von Serienetiketten muss konfiguriert und einige Etiketten müssen generiert werden, wie in [Konfigurieren des Serienetikettendrucks](../warehousing/configure-wave-label-printing.md) beschrieben.

### <a name="set-up-work-exceptions"></a>Arbeitsausnahmen einrichten

Arbeitsausnahmen steuern das Verhalten der kurzen Entnahmen. Gehen Sie zum Einrichten einer Arbeitsausnahme folgendermaßen vor:

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsausnahmen**.
1. Erstellen Sie einen Datensatz mit den folgenden Einstellungen:

    - **Arbeitsausnahmecode:** *Kurze Entnahme und Druck*
    - **Ausnahmetyp:** *Kurze Entnahme*
    - **Nachdruck von Serienetiketten vorschlagen:** *Ja*

### <a name="void-and-reprint-after-a-short-pick"></a>Nach einer kurzen Entnahme stornieren und erneut drucken

1. Melden Sie sich bei der Warehouse-App als ein Benutzer mit Zugriff auf Lagerort *62* an. (Sie können sich bei den Standard-Demo-Daten mit *62* als Benutzer-ID und *1* als Passwort anmelden.)
1. Öffnen Sie einen Arbeitsablauf für die Kundenauftragsarbeit, die beim ursprünglichen Drucken von Serienetiketten erstellt wurde.
1. Wählen Sie **Kurze Entnahme**.
1. Wählen Sie den Arbeitsausnahmecode aus, den Sie für dieses Szenario erstellt haben.
1. Wenn Sie die richtige Ausnahme ausgewählt haben, sollte das Kontrollkästchen **Stornieren und erneut drucken** verfügbar sein. Aktivieren Sie dieses Kontrollkästchen und bestätigen Sie. Nach Bestätigung wird die Etikettenrollensequenz durch das Feld **Etiketten-Build-ID** basierend auf der geänderten Arbeitszeilenmenge neu berechnet. Es wird dann auf dem angegebenen Drucker nachgedruckt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Zyklusbeschriftungsdruck](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]