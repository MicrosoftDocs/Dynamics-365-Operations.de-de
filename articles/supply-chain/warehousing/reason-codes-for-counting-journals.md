---
title: Ursachencodes für Bestandszählungen anzeigen
description: In diesem Thema wird beschrieben, wie Ursachencodes für Inventuraufgaben eingerichtet werden.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: d72b171bfe149b25f5055d5bebef85b49e952295
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228488"
---
# <a name="reason-codes-for-inventory-counting"></a>Ursachencodes für Bestandszählungen anzeigen

[!include [banner](../includes/banner.md)]

Ursachencodes lassen Sie die Ergebnisse einer Inventur und sämtliche Abweichungen analysieren, die während dieses Vorgangs auftreten. Sie können den Grund für das Treffen der Anzahl, wie eine angebrochenes Palette oder einen vordefinierten Regulierung angeben, die auf Grundlage der Bestandsbeispiele liegt.

## <a name="recommendation"></a>Empfehlung

Bevor Sie das System so einrichten, wird empfohlen, dass Sie eine Strategie für die Arbeit mit Ursachencodes definieren. Beispielsweise versuchen Sie, die folgenden Fragen zu beantworten:

- Müssen für Lagerorte Ursachencodes erforderlich sein?
- Müssen Ursachencodes für mehrere Artikel obligatorisch oder optional sein?
- Wie viele Ursachencodes brauchen Sie?
- Wie sollen Benutzer von Strichcodescannern Ursachencodes verwenden? Müssen die Ursachencodes vorgewählt, erforderlich oder nicht bearbeitbar sein?
- Brauchen Lagerarbeiter anderes Ursachencodeverhalten auf mobile Scannern? Wenn die Antwort ja ist, können Sie keine weiteren Menüoptionen erstellen und diese unterschiedlichen Person zuweisen.

## <a name="where-reason-codes-apply"></a>Wo Ursachencodes gelten

Sie können mehrere Ursachencoderichtlinien erstellen, und jede Ursachencoderichtlinie kann zwei zählende Ursachencoderichtlinien haben. Die Inventurursachenrichtlinien können verschiedene Lagerortebene oder Artikelebenen verwenden.

## <a name="set-up-reason-code-policies"></a>Richten Sie Ursachencodes ein.

1. Wählen Sie **Lagerverwaltung** \> **Einstellungen** \> **Lager** \> **Richtlinien Inventurursachencodes** aus, und erstellen Sie eine neue Ursachencoderichtlinie.
2. Im Feld **Inventurursachencodetyp** wählen Sie entweder **Obligatorisch** oder **Fakultativ**, um anzugeben, ob die Auswahl eines Ursachencodes eine optionale oder erforderliche Aktivität in einer der folgenden Inventurerfassungen sollen:

    - Inventur (mobilen Gerät)
    - Lagerplatzinventur (mobile Gerät)
    - Schwelleninventur (mobile Gerät)
    - Regulierung in (mobiles Gerät)
    - Regulierung aus (mobiles Gerät)
    - Inventurerfassung (Rich Client)

Sie können Ursachencodes für einzelne Lagerorte und für Produkte einrichten. Die Ursachencodeeinstellung für Produkte Einstellung kann für Lagerorte missachten.

## <a name="mandatory-reason-codes"></a>Obligatorische Ursachencodes

Wenn der Parameter **Obligatorisch** in der Konfiguration von Ursachencodes für Lagerorte oder Artikel festgelegt ist, kann die Inventurerfassung nicht abgeschlossen werden, bis ein Ursachencode angegeben wird.

### <a name="set-up-reason-codes-for-warehouses"></a>Ursachencodes für Lagerorte einrichten

1. Klicken Sie auf **Lagerverwaltung** \> **Einstellungen** \> **Lageraufschlüsselung** \> **Lagerorte**
2. Auf der Registerkarte **Lagerort** im Feld **Inventurursachencoderichtlinie**, wählen Sie eine der folgenden Optionen aus:

    - **Leer** – Parameter, der der für den Artikel eingerichtet wurde, wird verwendet, um zu bestimmen, ob das Produkt für Inventurerfassungen erforderlich sind.
    - **Obligatorisch** – Ein Ursachencode ist immer auf für Inventurerfassungen für den Lagerort erforderlich.
    - **Obligatorisch** – Ein Ursachencode ist immer für Inventurerfassungen für den Lagerort erforderlich.

### <a name="set-up-reason-codes-for-products"></a>Ursachencodes für Lagerorte einrichten

1. Wechseln Sie **Produktinformationsverwaltung** \> **Produkte** \> **Freigegebene Produkte**.
2. Auf der Registerkarte **Lagerort** im Feld **Inventurursachencoderichtlinie** wählen Sie eine der folgenden Optionen aus:

    - **Leer** – Parameter, der für den Artikel eingerichtet wurde, wird verwendet, um zu bestimmen, ob das Produkt für Inventurerfassungen erforderlich ist.
    - **Obligatorisch** – Ein Ursachencode ist immer auch für Inventurerfassungen für das Produkt erforderlich. Diese Einstellung hat Priorität gegenüber Ursachencodeeinstellungen auf Lagerortebene.
    - **Obligatorisch** – Ein Ursachencode ist immer für Inventurerfassungen für das Produkt erforderlich. Diese Einstellung hat Priorität gegenüber Ursachencodeeinstellungen auf Lagerortebene.

### <a name="use-reason-codes-in-counting-journals"></a>Verwenden von Ursachencodes in den Inventurerfassungen

In einer Inventurerfassung können Sie Ursachencodes für viele der folgenden Typen hinzufügen:

- Inventurzählung
- Stellen-Anzahl
- Schwellenzählung
- Regulierung eingehend
- Regulierung ausgehend

Ursachencodes werden für Inventurerfassungen ine Erfassungspositionen im Typ **Inventurerfassung** hinzugefügt.

1. Wechseln Sie zu **Lagerverwaltung** \> **Erfassungseinträge** \> **Artikelinventur** \> **Inventur**.
2. In den Positionsdetails in der Inventurerfassung im Feld **Inventurursachencode** wählen Sie eine Option aus.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>Die Inventurerfassung annzeigen, da diese nach Ursachencodes erfasst ist.

- Wählen Sie **Lagerverwaltung** \> **Abfragen und Berichte** \> **Inventurerfassung**, aus, und klicken Sie dann im Feld **Inventurursachencode** aus, geben die Inventurerfassung angezeigt, die über einen Ursachencode erfasst wurde.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Verwenden Sie einen Ursachencode für eine Mengenanpassung

1. Wählen Sie auf der Seite **Verfügbarer Lagerbestand** **Menge anpassen** aus. Sie können die Seite **Verfügbarer Lagerbestand** auf mehrere Arten öffnen Wechseln Sie zu **Lagerverwaltung** \> **Abfragen und Berichte** \> **Verfügbarer Lagerbestand**.
2. Wählen Sie **Menge anpassen**, und dann, im Feld **Inventurursachencode** wählen Sie einen Ursachencode aus.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Konfigurieren Sie Ursachencodes für Menüoptionen für das mobile Gerät

Sie können Ursachencodes für alle Anzahlarten für eine Menüoption des mobilen Geräts konfigurieren. Die Variante der Menüoption des mobilen Geräts enthält die folgenden Informationen:

- Ob der Ursachencode des mobilen Geräts während des Zählens angezeigt wird.
- Der Standardursachencode ein, der für eines Menüelements des mobilen Geräts angezeigt wird.
- Ob der Benutzer den Ursachencode arbeiten kann.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Einstellungsursachencodes auf einem mobilen Gerät

1. Wählen Sie **Lagerortverwaltung** \> **Setup** \> **Mobiles Gerät** \> **Menüoptionen für mobiles Gerät** aus.
2. Auf der Registerkarte **Inventuren** wählen Sie **Zykluszählung** aus.
3. Wählen Sie im Feld **Standardinventurursachencode** Sie legen den Standardursachencode ein, der beim Melden Inventurauftrag erfasst werden soll, jedoch wird, indem die Menüoption des mobilen Geräts verwendet.
4. Wählen Sie im Feld **Hier werden Inventurursachencode an** **Position**, um die Ursachencodes anzeigen, nachdem eine Abweichung erfasst ist. Aktivieren Sie **Ausblenden** wenn der Ursachencode nicht angezeigt wird.
5. Hier können Sie die Option **Bearbeiten Sie Inventurursachencode** auf entweder **Ja** oder **Nein** festlegen. Wenn Sie Option auf **Ja** setzen, kann die Arbeitskraft den Ursachencode bearbeiten, wenn er im mobilen Gerät während des Zählens dargestellt wird.

> [!NOTE]
> Die Schaltfläche **Zykluszählung** kann auf einer beliebigen Menüoption des mobilen Geräts, die in die Inventur aktiviert werden ausgeführt werden kann. Beispiele umfassen die Menüoptionen für Stellenanzahlen, Benutzer-verwiesene Arbeit und System-verwiesene Arbeit.

## <a name="cycle-count-approvals"></a>Inventur-Zykluszählungen

Bevor eine Anzahl genehmigt wurde, kann der Benutzer den Ursachencodes ändern, der der Anzahl zugeordnet ist. Wenn die Anzahl genehmigt wird, wird der eingegebene Ursachencode für die Inventurerfassungspositionen.

### <a name="modify-cycle-count-approvals"></a>Inventur-Zykluszählungen bearbeiten

1. Wählen Sie **Lagerortverwaltung** \> **Zykluszählung** \> **Schwebende Prüfung der Gangzählungs-Arbeit** aus.
2. Wählen Sie **Zykluszählung**, und dann, im Feld **Inventurursachencode** wählen Sie einen Ursachencode aus.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>Ändern Sie die Menüoption des mobilen Geräts für ein- und ausgehende Regulierung

1. Wählen Sie **Lagerortverwaltung** \> **Einstellungen** \> **Mobiles Gerät** \> **Menüoptionen des mobilen Geräts**, und wählen Sie dann **Regulierung in und** aus.
2. Legen Sie die **Vorhandene Arbeit verwenden**-Option mit **Nein** fest.
3. Wählen Sie im Feld **Bearbeiten Erstellungsprozess** **Regulierung in** aus.

Die folgenden Felder werden der Menüoption des mobilen Geräts hinzugefügt, wenn **Regulierung in** oder **Regulierung aus** für den Arbeitserstellungsprozesses aktiviert ist:

- Standardursachencode für Zählungen
- Ursachencode für Zählungen anzeigen
- Ursachencode für Zählungen bearbeiten


[!INCLUDE[footer-include](../../includes/footer-banner.md)]