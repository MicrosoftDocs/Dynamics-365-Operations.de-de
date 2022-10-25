---
title: Umleitungen für Schritte in den Menüpunkten des Mobilgeräts konfigurieren
description: In diesem Artikel wird beschrieben, wie Umleitungen für Menüelemente konfiguriert werden, damit Mitarbeiter die aktuelle Aufgabe parken, eine andere Aufgabe ausführen und dann zur ursprünglichen Aufgabe zurückkehren können, ohne Informationen zu verlieren.
author: Mirzaab
ms.date: 09/01/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour, WHSMobileAppFlowStepDetourSelectFields, WHSMobileAppFlowStepSelectPromotedFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e387dd4e6499912f2d53dddc17ccc053f1ca699
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689309"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Umleitungen für Schritte in den Menüpunkten des Mobilgeräts konfigurieren

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

> [!IMPORTANT]
> Die Funktionen, die in diesem Artikel beschrieben werden, gelten nur für die neue Warehouse Management Mobile-App. Sie betreffen nicht die alte Lager-App, die jetzt außer Betrieb genommen ist.

In diesem Artikel wird beschrieben, wie Umleitungen für Menüelemente konfiguriert werden, damit Mitarbeiter die aktuelle Aufgabe "parken", eine andere Aufgabe ausführen und dann zur ursprünglichen Aufgabe zurückkehren können, ohne Informationen zu verlieren.

Ein Umweg ist ein separater Menüpunkt, der von einem Schritt in einer Hauptaufgabe aus geöffnet werden kann. Am Ende des Umwegs wird der Arbeiter an den Ort zurückgebracht, an dem er die Hauptaufgabe verlassen hat. Bei der Konfiguration legen Sie den Menüpunkt fest, der als Umleitung fungieren soll. Außerdem wählen Sie aus, welche Feldwerte aus der Hauptaufgabe automatisch auf die Umleitung weitergeleitet (kopiert) und dort eingetragen werden sollen. Daher müssen Sie verstehen, an welcher Stelle im Aufgabenfluss die Umleitung für die Mitarbeiter verfügbar sein soll. Außerdem müssen Sie sicherstellen, dass die Informationen, die auf die Umleitung kopiert werden müssen, für diesen Schritt des TaskFlows verfügbar sind.

## <a name="enable-detours-in-your-system"></a>Ermöglichen Sie Umleitungen in Ihrem System

Bevor Sie Umleitungen für Schritte in Menüpunkten mobiler Geräte konfigurieren können, müssen Sie das folgende Verfahren ausführen, um die erforderlichen Funktionen zu aktivieren und die erforderlichen Feldnamen in der Mobile-App Warehouse Management zu generieren.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.
1. Stellen Sie sicher, dass die *Schrittanweisungen für die Warehouse-App* Funktion für Ihr System aktiviert ist. Ab Supply Chain Management Version 10.0.29 ist diese Funktion standardmäßig aktiviert. Für weitere Informationen über die Funktion *Schrittanleitung für die Warehouse-App* siehe [Passen Sie Schritttitel und Anweisungen für die mobile Warehouse Management-App an](mobile-app-titles-instructions.md). Diese Funktion ist Voraussetzung für die Funktion *Umwege über die Warehouse Management-App*.
1. Aktivieren Sie die folgenden Features, die die in diesem Artikel beschriebene Funktionalität bereitstellen:
    - *Umleitung für Warehouse Management-App*<br>(Ab Supply Chain Management Version 10.0.29 ist diese Funktion standardmäßig aktiviert.)
    - *Umleitungen auf mehreren Ebenen für die mobile Warehouse Management-App*
    - *Umleitungsschritte für die mobile Warehouse Management-App automatisch übermitteln*
1. Wie die Funktion *Umleitung für Warehouse Management-App* und/oder *Umleitungen auf mehreren Ebenen für die mobile Warehouse Management-App* nicht bereits aktiviert ist, aktualisieren Sie die Feldnamen in der mobilen App für Warehouse Management, indem Sie zu **Lagerverwaltung \> Einstellungen \> Mobiles Gerät \> Feldnamen der Warehouse-App** und wählen **Standard-Setup erstellen**. Weitere Informationen finden Sie unter [Felder für die Warehouse Management Mobile App konfigurieren](configure-app-field-names-priorities-warehouse.md).
1. Wiederholen Sie den vorherigen Schritt für jede juristische Person (Firma), in der Sie die mobile App Warehouse Management verwenden.

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Konfigurieren Sie eine Umleitung von einer menüspezifischen Außerkraftsetzung

Gehen Sie wie folgt vor, um eine Umleitung von einer menüspezifischen Außerkraftsetzung einzurichten.

1. Erstellen Sie eine menüspezifische Überschreibung für das entsprechende Menü und den entsprechenden Schritt wie in [Schritttitel und Anweisungen für die mobile Warehouse Management-App anpassen](mobile-app-titles-instructions.md) beschrieben.
1. Suchen Sie die Kombination der Werte **Schritt-ID** und **Name des Elements**, die Sie bearbeiten wollen, und wählen Sie dann den Wert in der Spalte **Schritt-ID**.
1. Auf der angezeigten Seite, im Inforegister **Verfügbare Umleitungen (Menüpunkte)** können Sie den Menüpunkt angeben, der als Umleitung fungieren soll. Außerdem können Sie auswählen, welche Feldwerte aus der Hauptaufgabe automatisch in und aus der Umleitung kopiert werden sollten. Beispiele für die Verwendung dieser Einstellungen finden Sie in den Szenarien weiter unten in diesem Artikel.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a><a name="scenario-1"></a>Beispielszenario 1: Verkaufskommissionierung, bei der eine Standortanfrage als Umweg dient

Dieses Szenario zeigt, wie Sie eine Standortanfrage als Umweg in einem mitarbeitergesteuerten Verkaufskommissionierungs-Aufgabenablauf konfigurieren. Dieser Umweg ermöglicht es den Arbeitern, alle Nummernschilder an dem Ort, an dem sie kommissionieren, nachzuschlagen und das Nummernschild auszuwählen, das sie verwenden möchten, um die Kommissionierung abzuschließen. Dieser Umweg kann sinnvoll sein, wenn der Strichcode beschädigt und daher vom Scanner nicht lesbar ist. Alternativ kann es nützlich sein, wenn ein Mitarbeiter lernen muss, was tatsächlich im System vorhanden ist. Beachten Sie, dass dieses Szenario nur funktioniert, wenn Sie von kennzeichenkontrollierten Standorten auswählen.

### <a name="enable-sample-data"></a>Beispieldaten aktivieren

Um die festgelegten Beispieldatensätze und -werte zur Bearbeitung dieses Szenarios zu verwenden, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert sind. Sie müssen auch die **USMF** juristische Person auswählen, bevor Sie beginnen.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Erstellen Sie einen menüspezifischen Override und konfigurieren Sie die Umleitung für Szenario 1

In diesem Verfahren konfigurieren Sie eine Umleitung für den Menüpunkt **Verkaufskommissionierung** im Nummernschildschritt.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Mobiles Gerät \> Mobiles Gerät Schritte**.
1. Suchen und wählen Sie die benannte Schritt-ID *LicensePlateId*.
1. Wählen Sie im Aktionsbereich **Schrittkonfiguration hinzufügen**.
1. Verwenden Sie im Dropdown-Dialogfeld das Feld **Menüpunkt** zum Suchen und Auswählen von *Verkaufsauswahl*.
1. Wählen Sie **OK** aus.
1. Die Detailseite für die soeben erstellte Überschreibung wird angezeigt. Wählen Sie im Inforegister **Verfügbare Umleitungen (Menüpunkte)** die Option **Hinzufügen** auf der Symbolleiste.
1. Im Dialogfeld **Umleitung hinzufügen** wählen Sie **Standortanfrage** als Umweg, der in der Mobile-App Warehouse Management zur Verfügung gestellt wird.
1. Wählen Sie **OK** aus.
1. Wählen Sie im Inforegister **Verfügbare Umleitungen (Menüpunkte)** die soeben hinzugefügte Umleitung aus und wählen Sie dann **Wählen Sie die zu sendenden Felder aus** auf der Symbolleiste.
1. Geben Sie im Dialogfeld **Wählen Sie die zu sendenden Felder aus** die Informationen an, die zu und von der Umleitung gesendet werden sollen. In diesem Szenario ermöglichen Sie den Mitarbeitern, den Standort, aus dem sie auswählen sollen, als Eingabe für die Umleitung der Standortanfrage zu verwenden. Wählen Sie daher im Abschnitt **Aus Verkaufskommissionierung versenden** **Hinzufügen** auf der Symbolleiste, um dem Raster eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Werte fest:

    - **Kopie aus der Verkaufskommissionierung:** *Standort*
    - **Standortanfrage einfügen:** *Standort*
    - **Automatisch einreichen:** *Ausgewählt* (Die Seite wird mit dem eingefügten Wert *Ort* aktualisiert)

1. Da die Umleitung in diesem Szenario im Nummernschildschritt konfiguriert wird, ist es sinnvoll, wenn Mitarbeiter das Nummernschild aus der Abfrage zurück in den Hauptfluss bringen können. Wählen Sie daher im Abschnitt **Aus Standortabfrage zurückbringen** **Hinzufügen** auf der Symbolleiste, um dem Raster eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Werte fest:

    - **Kopie aus Standortanfrage:** *Nummernschild*
    - **In Verkaufskommissionierung einfügen:** *Nummernschild*
    - **Automatisch einreichen:** *Gelöscht* (Bei der Rückkehr von der Umleitung mit einem Wert *Nummernschild* erfolgt kein automatisches Update)

1. Wählen Sie **OK** aus.

Die Umleitung ist nun vollständig konfiguriert. Eine Schaltfläche zum Starten der Umleitung **Standortanfrage** erscheint jetzt auf der Nummernschildstufe für den Menüpunkt **Verkaufskommissionierung**.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Vervollständigen Sie eine Verkaufsauswahl auf einem mobilen Gerät und nutzen Sie den Umweg

In diesem Verfahren schließen Sie eine Verkaufskommissionierung mit der mobilen Warehouse Management-App ab. Sie verwenden den soeben konfigurierten Umweg, um das Nummernschild zu finden, mit dem Sie den Auswahlschritt abschließen.

1. Bei Microsoft Dynamics 365 Supply Chain Management erstellen Sie einen Kundenauftrag, der einen Entnahmeschritt erfordert, um von einem Lagerort zu kommissionieren, für den ein Nummernschild verfolgt wird. Dann geben Sie den Auftrag für den Lagerort frei. Notieren Sie sich die erstellte Arbeits-ID.
1. Öffnen Sie die Warehouse Management Mobile App und melden Sie sich bei Lagerort 24 an. (Melden Sie sich bei den Standard-Demo-Daten mit *24* als Benutzer-ID und *1* als Passwort an.)
1. Wählen Sie das Menü **Ausgehend** und wählen Sie dann den Menüpunkt **Verkaufsauswahl**.
1. Befolgen Sie die Anweisungen zur Dateneingabe auf dem Bildschirm, um die in Schritt 1 generierte Arbeits-ID einzugeben.
1. Auf dem Schritt, der den Text **Scannen Sie ein Nummernschild** enthält, öffnen Sie das Aktionsmenü. Sie sollten eine neue Schaltfläche mit der Bezeichnung **Standortanfrage** sehen. Ein Pfeil in der oberen linken Ecke zeigt an, dass die Schaltfläche eine Umleitung startet. Wählen Sie **Standortanfrage**.
1. Die Umleitung wird gestartet. Bestätigen Sie auf der nächsten Seite den Speicherort, der aus dem Hauptflow kopiert wurde.
1. Tippen Sie in der Liste der verfügbaren Nummernschilder am Standort auf das Nummernschild, das Sie zurück in den Hauptfluss kopieren möchten. Wählen Sie dann die **Zurück**-Taste.
1. Sie kehren zum Hauptfluss der Verkaufskommissionierung zurück, und das Nummernschild wurde von der Umleitung dorthin zurückkopiert. Bestätigen Sie den Wert, um mit dem nächsten Schritt fortzufahren.
1. Sie können nun den Rest des Standardablaufs abschließen, indem Sie die angeforderten Dateneingabeanweisungen eingeben.

Die Lagerarbeiten sind nun abgeschlossen. Der Arbeiter eröffnete erfolgreich einen Umweg, um eine Nebenaufgabe (Standortabfrage) durchzuführen, ohne seinen Platz in der Hauptaufgabe zu verlieren, und brachte die Informationen zurück, die zur Erledigung der Hauptaufgabe erforderlich waren.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>Beispielszenario 2: Artikelanfrage mit Bewegungs- und Verstellumwegen

Dieses Szenario zeigt, wie Sie Bewegungen und Anpassungen als mehrere Umwege im Taskflow Standortabfrage konfigurieren. Diese Funktion kann in Situationen nützlich sein, in denen ein Arbeiter an einem Standort ankommt, feststellt, dass der Lagerbestand am Standort sich von dem im System registrierten unterscheidet und daher Waren anpassen oder bewegen muss.

Die Standortanfrage können Sie je nach Bedarf durch eine Kennzeichenanfrage oder eine Artikelanfrage ersetzen.

### <a name="enable-sample-data"></a>Beispieldaten aktivieren

Um die festgelegten Beispieldatensätze und -werte zur Bearbeitung dieses Szenarios zu verwenden, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert sind. Sie müssen auch die **USMF** juristische Person auswählen, bevor Sie beginnen.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Erstellen Sie einen menüspezifischen Override und konfigurieren Sie die Umleitung für Szenario 2

In diesem Verfahren konfigurieren Sie eine Umleitung für den Menüpunkt **Verkaufskommissionierung** im Nummernschildschritt.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> Mobiles Gerät \> Mobiles Gerät Schritte**.
1. Suchen und wählen Sie die benannte Schritt-ID *LocationInquiryList*.

    > [!NOTE]
    > Um eine Artikelanfrage anstelle einer Standortanfrage zu verwenden, wählen Sie eine Zeile aus, in der die Schritt-ID *ItemInquiryList* benannt ist. Um eine Kennzeichenabfrage zu verwenden, wählen Sie eine Zeile aus, in der die Schritt-ID *LPInquiryList* benannt ist.

1. Wählen Sie im Aktionsbereich **Schrittkonfiguration hinzufügen**.
1. Verwenden Sie im Dropdown-Dialogfeld das Feld **Menüpunkt** zum Suchen und Auswählen von *Standortanfrage*.
1. Wählen Sie **OK** aus.
1. Die Detailseite für die soeben erstellte Überschreibung wird angezeigt. Wählen Sie im Inforegister **Verfügbare Umleitungen (Menüpunkte)** die Option **Hinzufügen** auf der Symbolleiste.
1. Im Dialogfeld **Umleitung hinzufügen** wählen Sie **Bewegung** als Umweg, der in der Mobile-App Warehouse Management zur Verfügung gestellt wird.
1. Wählen Sie **OK** aus.
1. Wählen Sie im Inforegister **Verfügbare Umleitungen (Menüpunkte)** die soeben hinzugefügte Umleitung aus und wählen Sie dann **Wählen Sie die zu sendenden Felder aus** auf der Symbolleiste.
1. Geben Sie im Dialog **Wählen Sie die zu sendenden Felder aus** die Informationen an, die zu und von der Umleitung gesendet werden sollen. In diesem Szenario erwarten Sie, dass Mitarbeiter nach kennzeichenkontrollierten Standorten suchen. Daher ist es hilfreich, das Nummernschild aus der Anfrage in die Umleitung **Bewegung** zu kopieren. Wählen Sie im Abschnitt **Aus Verkaufskommissionierung versenden** **Hinzufügen** auf der Symbolleiste, um dem Raster eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Werte fest:

    - **Aus Standortanfrage kopieren:** *Standort*
    - **In Bewegung einfügen:** *Loc / LP*
    - **Automatisch einreichen:** *Gelöscht* (es erfolgt kein automatisches Update)

    Auf diesem Umweg erwarten Sie nicht, dass Informationen zurückkopiert werden, da der Hauptfluss eine Anfrage war, bei der keine zusätzlichen Schritte erforderlich sind.

1. Wählen Sie **OK** aus.

Die Umleitung ist nun vollständig konfiguriert. Eine Schaltfläche zum Starten der Umleitung **Bewegung** erscheint jetzt auf der Nummernschildstufe für den Menüpunkt **Standortanfrage**.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Machen Sie eine Standortabfrage auf einem mobilen Gerät und nutzen Sie den Umweg

In diesem Verfahren führen Sie eine Standortanfrage mit der mobilen Warehouse Management-App durch. Den Umweg nutzen Sie dann, um eine Warenbewegung abzuschließen.

1. Öffnen Sie die Warehouse Management Mobile App und melden Sie sich bei Lagerort 24 an. (Melden Sie sich bei den Standard-Demo-Daten mit *24* als Benutzer-ID und *1* als Passwort an.)
1. Wählen Sie das Menü **Bestand** und wählen Sie dann den Menüpunkt **Standortanfrage**.
1. Geben Sie einen Ort ein, zu dem Sie eine Anfrage stellen möchten, z. B. *FL-001*.
1. Wenn die Liste angezeigt wird, tippen und halten Sie eine der Karten darin, um die verfügbaren Umleitungen anzuzeigen.
1. Wählen Sie **Bewegung**.
1. Beachten Sie, dass das Nummernschild von der ausgewählten Karte kopiert wurde. Bestätigen Sie den Wert.
1. Sie können nun dem Standard-Taskflow folgen, um die Bewegung abzuschließen. Öffnen Sie nach Abschluss der Arbeit das Aktionsmenü und wählen Sie **Abbrechen**.
1. Sie sind zur Seite **Standortanfrage** zurückgekehrt. Beachten Sie, dass die Werte nicht automatisch aktualisiert werden. Daher müssen Sie die Seite manuell aktualisieren, um die Änderungen von der Bewegungsumleitung zu sehen.

> [!NOTE]
> Mit der Funktion *Umleitungen auf mehreren Ebenen für die mobile Warehouse Management-App* können Sie mehrstufige Umleitungen (Umleitungen innerhalb von Umleitungen) definieren, die es den Mitarbeitern ermöglichen, von einer bestehenden Umleitung zwei zu einer zweiten und dann wieder zurück zu springen. Die Funktion unterstützt standardmäßig zwei Umleitungsebenen, und bei Bedarf können Sie Ihr System so anpassen, dass es drei oder mehr Umleitungsebenen unterstützt, indem Sie Codeerweiterungen in der Tabelle `WHSWorkUserSessionState` erstellen.
>
> Die Funktion *Automatische Übermittlung von Umleitungsschritten für die mobile Warehouse Management-App* kann es Arbeitern schneller und einfacher machen, Umleitungsflüsse in der mobilen Warehouse Management-App abzuschließen. Es ermöglicht, dass einige Ablaufschritte übersprungen werden, indem die App Umleitungsdaten im Backend ausfüllt und dann automatisch zum nächsten Schritt übergeht, indem die Seite automatisch gesendet wird, wie in gezeigt [*Beispielszenario 1: Verkaufskommissionierung, bei der eine Standortanfrage als Umweg dient*](#scenario-1).
