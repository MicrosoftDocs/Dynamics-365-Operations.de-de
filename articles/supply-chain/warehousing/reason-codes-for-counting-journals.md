---
title: Ursachencodes für Bestandszählungen anzeigen
description: In diesem Artikel wird beschrieben, wie Ursachencodes für Inventuraufgaben eingerichtet werden.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 7d182f1d979543eeec700924d2bd180ee06be8ce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857111"
---
# <a name="reason-codes-for-inventory-counting"></a>Ursachencodes für Bestandszählungen anzeigen

[!include [banner](../includes/banner.md)]

Ursachencodes lassen Sie die Ergebnisse einer Inventur und sämtliche Abweichungen analysieren, die während dieses Vorgangs auftreten. Sie können den Grund für das Treffen der Anzahl, wie eine angebrochenes Palette oder einen vordefinierten Regulierung angeben, die auf Grundlage der Bestandsbeispiele liegt. Gleichzeitig können Sie die Regulierungsfunktion verwenden, um den Wert der Anpassungen am verfügbaren Lagerbestand basierend auf dem Grund für jede Bestandsregulierung auf das entsprechende Gegenkonto zu buchen.

## <a name="recommendation"></a>Empfehlung

Bevor Sie das System so einrichten, wird empfohlen, dass Sie eine Strategie für die Arbeit mit Ursachencodes definieren. Beispielsweise versuchen Sie, die folgenden Fragen zu beantworten:

- Müssen für Lagerorte Ursachencodes erforderlich sein?
- Müssen Ursachencodes für mehrere Artikel obligatorisch oder optional sein?
- Wie viele Ursachencodes brauchen Sie?
- Müssen Sie eine begrenzte Liste von Ursachencodes für Regulierungen vorab auswählen?
- Wie sollten Benutzer von Barcode-Scannern Ursachencodes verwenden? Müssen die Ursachencodes vorgewählt, erforderlich oder nicht bearbeitbar sein?
- Brauchen Lagerarbeiter anderes Ursachencodeverhalten auf mobile Scannern? Wenn die Antwort ja ist, können Sie keine weiteren Menüoptionen erstellen und diese unterschiedlichen Person zuweisen.
- Sollten die Ursachencodes die Buchung auf finanziellen Gegenkonten steuern?

## <a name="turn-on-reason-code-features-in-your-system"></a>Ursachencodefunktionen in Ihrem System aktivieren

Wenn in Ihrem System nicht alle in diesem Artikel beschriebenen Funktionen angezeigt werden, müssen Sie wahrscheinlich die Funktion *Regulierungen des verfügbaren Lagerbestands mit konfigurierbaren Ursachencodes buchen, die mit Ausgleichskonten verbunden sind* aktivieren. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Regulierungen des verfügbaren Lagerbestands mit konfigurierbaren Ursachencodes buchen, die mit Ausgleichskonten verbunden sind*

## <a name="set-up-reason-codes"></a>Ursachencodes einrichten

### <a name="set-up-reason-code-policies"></a>Richten Sie Ursachencodes ein.

Sie können mehrere Ursachencoderichtlinien erstellen, um zu steuern, wann und wie Ursachencodes für Zählungen angewendet werden. Jede Ursachencoderichtlinie kann einen von zwei Ursachencodetypen für Zählungen haben (*Optional* oder *Obligatorisch*). Die Richtlinien zu Ursachencodes für Zählungen können verschiedene Lagerortebenen oder Artikelebenen verwenden.

Führen Sie die folgenden Schritte aus, um eine Ursachencoderichtlinie zu erstellen.

1. Gehen Sie zu **Lagerverwaltung** \> **Einstellungen** \> **Bestand** \> **Richtlinien zu Ursachencodes für Zählungen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Richtlinie zum Raster hinzuzufügen.
1. Legen Sie das Feld **Name** für die neue Richtlinie fest.
1. Im Feld **Ursachencodetyp für Zählungen** wählen Sie entweder *Obligatorisch* oder *Optional*, um anzugeben, ob die Auswahl eines Ursachencodes eine optionale oder erforderliche Aktivität in den folgenden Prozessen zur Lagerregulierung sein soll:

    - Inventur (mobilen Gerät)
    - Lagerplatzinventur (mobile Gerät)
    - Schwelleninventur (mobile Gerät)
    - Regulierung in (mobiles Gerät)
    - Regulierung aus (mobiles Gerät)
    - Inventurerfassung (Rich Client)
    - Mengenregulierungen/Online-Inventur (Rich-Client)

Sie können Ursachencoderichtlinien sowohl für einzelne Lagerorte als auch für Produkte einrichten. Die Einrichtung des Ursachencodes für ein Produkt kann die Einrichtung für den Lagerort des Produkts außer Kraft setzen.

> [!NOTE]
> Bei Lagerorten und Artikeln, wo das Feld **Richtlinie zu Ursachencodes für Zählungen** auf *Obligatorisch* gesetzt ist, kann die Inventurerfassung nicht abgeschlossen und geschlossen werden, bis ein Ursachencode angegeben wird. Weitere Informationen finden Sie im nächsten Abschnitt.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Lagerorten Richtlinien zu Ursachencodes für Zählungen zuweisen

Führen Sie die folgenden Schritte aus, um einem Lagerort eine Richtlinie zu Ursachencodes für Zählungen zuzuweisen.

1. Gehen Sie zu **Lagerverwaltung** \> **Einstellungen** \> **Lageraufschlüsselung** \> **Lagerorte**.
1. Wählen Sie im Listenbereich einen Lagerort aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** in der Gruppe **Setup** **Richtlinie zu Ursachencodes für Zählungen** aus. Führen Sie dann im Dropdown-Dialogfeld **Richtlinie zu Ursachencodes für Zählungen zuweisen** einen der folgenden Schritte aus:

    - Um die Richtlinieneinrichtung für jeden Artikel zu verwenden, um zu bestimmen, ob Inventurerfassungen dafür obligatorisch sind, geben Sie keinen Wert ein (oder löschen Sie den vorhandenen Wert).
    - Um einen Ursachencode für Inventurerfassungen für den Lagerort anzufordern, wählen Sie eine Ursachenrichtlinie aus, bei der das Feld **Ursachencodetyp für Zählungen** auf *Obligatorisch* gesetzt ist.
    - Wenn ein Ursachencode für Inventurerfassungen für den Lagerort optional ist, wählen Sie eine Ursachenrichtlinie aus, bei der das Feld **Ursachencodetyp für Zählungen** auf *Optional* gesetzt ist.

### <a name="assign-counting-reason-code-policies-to-products"></a>Produkten Richtlinien zu Ursachencodes für Zählungen zuweisen

Führen Sie die folgenden Schritte aus, um einem Produkt eine Richtlinie zu Ursachencodes für Zählungen zuzuweisen.

1. Wechseln Sie zu **Produktinformationsverwaltung** \> **Produkte** \> **Freigegebene Produkte**.
1. Wählen Sie im Raster ein Produkt aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Setup** **Richtlinie zu Ursachencodes für Zählungen** aus. Führen Sie dann im Dropdown-Dialogfeld **Richtlinie zu Ursachencodes für Zählungen zuweisen** einen der folgenden Schritte aus:

    - Um die Richtlinieneinrichtung für den Lagerort zu verwenden, um zu bestimmen, ob Inventurerfassungen für das Produkt obligatorisch sind, geben Sie keinen Wert ein (oder löschen Sie den vorhandenen Wert).
    - Um einen Ursachencode für Inventurerfassungen für das Produkt anzufordern, wählen Sie eine Ursachenrichtlinie aus, bei der das Feld **Ursachencodetyp für Zählungen** auf *Obligatorisch* gesetzt ist. Diese Einstellung hat Priorität gegenüber Ursachencodeeinstellungen auf Lagerortebene.
    - Wenn ein Ursachencode für Inventurerfassungen für das Produkt optional ist, wählen Sie eine Ursachenrichtlinie aus, bei der das Feld **Ursachencodetyp für Zählungen** auf *Optional* gesetzt ist. Diese Einstellung hat Priorität gegenüber Ursachencodeeinstellungen auf Lagerortebene.

### <a name="set-up-counting-reason-codes"></a>Ursachencodes für Zählungen einrichten

Gehen Sie zum Einrichten Ihrer Urschencodes für Zählungen folgendermaßen vor.

1. Gehen Sie zu **Lagerverwaltung** \> **Einstellungen** \> **Bestand** \> **Ursachencodes für Zählungen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.
1. Legen Sie die Felder **Ursachencode für Zählungen** und **Beschreibung** für die neue Zeile fest.
1. Um ein Gegenkonto zuzuweisen, geben Sie einen Wert in das Feld **Gegenkonto** ein oder wählen Sie ihn aus.

    > [!NOTE]
    > Wenn ein Gegenkonto einem Ursachencode für Zählungen zugeordnet ist, wird der Wert beim Buchen einer Inventurerfassung mit diesem Ursachencode für Zählungen gegen das zugeordnete Gegenkonto gebucht und nicht gegen das Standardkonto des Lagerbuchungsprofils.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Ursachencodegruppen für Zählungen einrichten

*Ursachencodegruppen für Zählungen* können als Teil der Menüelemente *Regulierung eingehend* und *Regulierung ausgehend* mobilen Warehouse Management-App, um die Liste der Ursachencodes für Zählungen einzuschränken. (Weitere Informationen zu Ursachencodegruppen für Zählungen finden Sie im Abschnitt [Die Menüelemente des mobilen Geräts für ein- und ausgehende Regulierung einrichten](#setup-adjustment-in-out) weiter unten in diesem Artikel.)

1. Gehen Sie zu **Lagerverwaltung** \> **Einstellungen** \> **Bestand** \> **Ursachencodegruppen für Zählungen**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine Gruppe hinzuzufügen.
1. Legen Sie die Felder **Ursachencodegruppe** und **Gruppenbeschreibung** für die neue Gruppe fest.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Öffnen Sie im Abschnitt **Details** und wählen Sie **Neu** in der Symbolleiste, um dem Raster eine Zeile hinzuzufügen. Legen Sie dann das Feld **Ursachencode für Zählungen** für die neue Zeile fest. 
1. Wiederholen Sie den vorherigen Schritt, um nach Bedarf weitere Codes zuzuweisen. Wenn Sie einen Code aus der Gruppe entfernen müssen, wählen Sie ihn aus und wählen Sie dann **Löschen** auf der Symbolleiste.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Ursachencodes für Menüelemente für das mobile Gerät einrichten

Sie können Ursachencodes für die folgenden Arten von verfügbaren Regulierungen konfigurieren:

- Inventurzählung
- Stellen-Anzahl
- Schwellenzählung
- Regulierung eingehend
- Regulierung ausgehend

In den meisten Fällen können Sie für jedes relevante Menüelement des mobilen Geräts die folgenden Informationen festlegen:

- Ob der Ursachencode des mobilen Geräts während des Zählens angezeigt wird.
- Der Standardursachencode ein, der für eines Menüelements des mobilen Geräts angezeigt wird.
- Ob der Benutzer den Ursachencode arbeiten kann.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Menüelemente für einen Inventurprozess für das mobile Gerät einrichten

Um eine Menüelement für mobile Geräte für einen Inventurprozess einzurichten, führen Sie diese Schritte aus.

1. Gehen Sie zu **Lagerortverwaltung** \> **Setup** \> **Mobiles Gerät** \> **Menüelemente für mobiles Gerät**.
1. Wählen Sie das entsprechende Menüelement im Listenbereich aus oder erstellen Sie eine neues Menüelement.
1. Wählen Sie im Aktionsbereich **Zykluszählung**.
1. Wählen Sie im Feld **Standardursachencode für Zählungen** den Standardursachencode aus, der erfasst werden soll, wenn das Menüelement des mobilen Geräts für die Inventur verwendet wird.
1. Wählen Sie im Feld **Ursachencode für Zählungen anzeigen** einen der folgenden Werte aus:

    - *Position*: Zeigen Sie den Ursachencode an, nachdem jede Abweichung erfasst wurde.
    - *Ausblenden*: Den Ursachencode nicht anzeigen.

1. Setzen Sie die Option **Ursachencode für Zählungen bearbeiten** auf *Ja*, damit die Arbeitskraft den Ursachencode bearbeiten kann, wenn er im mobilen Gerät während des Zählens dargestellt wird. Setzen Sie sie auf *Nein*, um zu verhindern, dass die Arbeitskraft den Code bearbeitet.

> [!NOTE]
> Die Schaltfläche **Zykluszählung** kann auf einer beliebigen Menüoption des mobilen Geräts, die in die Inventur aktiviert werden ausgeführt werden kann. Beispiele umfassen die Menüoptionen für Stellenanzahlen, benutzergesteuerte Arbeit und systemgesteuerte Arbeit.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>Die Menüelemente des mobilen Geräts für ein- und ausgehende Regulierung einrichten

Um ein Menüelement für mobile Geräte für eine ein- oder ausgehende Regulierung einzurichten, führen Sie diese Schritte aus.

1. Gehen Sie zu **Lagerortverwaltung** \> **Setup** \> **Mobiles Gerät** \> **Menüelemente für mobiles Gerät**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um ein Menüelement zu erstellen.
1. Legen Sie die Felder **Name des mobilen Elements** und **Titel** für das neue Menüelement fest.
1. Legen Sie das Feld **Modus** auf *Arbeit* fest.
1. Legen Sie die **Vorhandene Arbeit verwenden**-Option mit *Nein* fest.
1. Wählen Sie im Feld **Arbeitserstellungsprozess** *Regulierung eingehen* oder *Regulierung ausgehend* aus.
1. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest. (Alle diese Felder werden hinzugefügt, wenn Sie *Regulierung eingehend* oder *Regulierung ausgehend* im Feld **Arbeitserstellungsprozess** auswählen.)

    - **Prozessleitfaden verwenden**: Wenn Sie einen *Regulierung ausgehend*-Prozess erstellen, stellen Sie diese Option unbedingt auf *Ja*. Wenn Sie einen *Regulierung ausgehend*-Prozess erstellen, steht diese Option immer auf *Ja*.
    - **Standardursachencode für Zählungen**: Legen Sie den Standardursachencode fest, der erfasst werden soll, wenn das Menüelement des mobilen Geräts für die Inventur verwendet wird.
    - **Ursachencode für Zählungen anzeigen**: Wählen Sie einen der folgenden Werte aus:

        - *Position*: Zeigen Sie den Ursachencode an, nachdem jede Abweichung erfasst wurde.
        - *Ausblenden*: Den Ursachencode nicht anzeigen.

    - **Ursachencode für Zählungen bearbeiten**: Setzen Sie die Option auf *Ja*, damit die Arbeitskraft den Ursachencode bearbeiten kann, wenn er im mobilen Gerät während des Zählens dargestellt wird. Setzen Sie sie auf *Nein*, um zu verhindern, dass die Arbeitskraft den Code bearbeitet.
    - **Ursachencodegruppe für Zählungen**: Wählen Sie eine Ursachencodegruppe aus, wenn Sie die Liste der Optionen einschränken möchten, die den Arbeitskräften angezeigt wird. Informationen zum Einrichten von Ursachencodegruppen finden Sie im Abschnitt [Ursachencodegruppen für Zählungen einrichten](#reason-groups) weiter oben in diesem Artikel. 

> [!NOTE]
> Wenn Sie eine Ursachencodegruppen für Zählungen den Menüelementen *Regulierung eingehend* und *Regulierung ausgehend* zuweisen, bei denen die Option **Prozessleitfaden verwenden** auf *Ja* steht, können Sie im Rahmen der Verarbeitung in der mobilen Warehouse Management-App eine eingeschränkte Liste der Ursachencodes für Zählungen abrufen.
>
> Die Option **Prozessleitfaden verwenden** kann auch dazu beitragen, dass nicht versehentlich große Anpassungsmengen auftreten. (Zum Beispiel könnte eine Arbeitskraft versehentlich einen Strichcode einer Artikelnummer anstelle eines Mengenwertes scannen.) Um diese Funktion einzurichten, stellen Sie die Option **Prozessleitfaden verwenden** für jedes relevante Menüelement auf *Ja*. Gehen Sie dann zu **Lagerortverwaltung \> Setup \> Arbeitskraft** und legen Sie das Feld **Regulierungsmengenbeschränkung** für jeden relevanten Lagerarbeiter fest, um die maximale Regulierungsmenge anzugeben, die die Arbeitskraft erfassen kann.

## <a name="processing-that-uses-counting-reason-codes"></a>Verarbeitungen, die Ursachencodes für Zählungen verwenden

Wenn Arbeitskräfte die mobile Warehouse Management-App verwenden, werden die Ursachencodes aufgezeichnet. Sofern kein Inventurgenehmigungsprozess definiert wurde, werden die erfassten Ursachencodes sofort als Teil der folgenden Inventurerfassungsbuchung verwendet.

### <a name="cycle-count-approvals"></a>Inventur-Zykluszählungen

Bevor eine Anzahl genehmigt wurde, kann die Arbeitskraft den Ursachencodes ändern, der der Anzahl zugeordnet ist. Wenn die Anzahl genehmigt wird, wird der eingegebene Ursachencode für die Inventurerfassungspositionen.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Ursachencodes für Zyklusanzahlgenehmigungen ändern

Gehen Sie wie folgt vor, um eine Zyklusanzahlgenehmigung zu ändern.

1. Gehen Sie zu **Lagerortverwaltung** \> **Zykluszählung** \> **Ausstehende Prüfung der Zykluszählarbeit** aus.
1. Wählen Sie im Raster eine Zyklusanzahl aus.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Arbeit** die Option **Zykluszählung**. Wählen Sie dann im Feld **Ursachencode** einen neuen Ursachencode aus.

Ursachencodes werden für Inventurerfassungen ine Erfassungspositionen im Typ *Inventurerfassung* hinzugefügt.

1. Gehen Sie zu **Lagerverwaltung** \> **Erfassungseinträge** \> **Artikelinventur** \> **Inventur**.
2. Wählen Sie in den Positionsdetails der Inventurerfassung im Feld **Ursachencode für Zählungen** den Ursachencode aus, der Ihrer aktuellen Situation entspricht.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>Die in der Inventurhistorie erfassten Ursachencodes anzeigen

Gehen Sie folgendermaßen vor, um die Ursachencodes anzuzeigen, die in der Inventurhistorie erfasst wurden.

1. Wechseln Sie zu **Lagerverwaltung** \> **Anfragen und Berichte** \> **Inventurhistorie**.
1. Wählen Sie im Listenbereich einen Elementanzahldatensatz aus.
1. Sehen Sie sich im Feld **Ursachencode für Zählungen** die Inventurhistorie an, die über einen Ursachencode aufgezeichnet wurde.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Ursachencodes für die Mengenregulierung oder Online-Inventur

Gehen Sie wie folgt vor, um einen Ursachencode für eine Mengenregulierung oder Online-Inventur zu verwenden.

1. Wechseln Sie zu **Lagerverwaltung \> Anfragen und Berichte \> Bestandsliste**.
1. Wählen Sie im Aktivitätsbereich **Mengenregulierung** aus.
1. Wählen Sie **Mengeregulierung** und dann im Feld **Ursachencode für Zählungen** einen Ursachencode aus.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
