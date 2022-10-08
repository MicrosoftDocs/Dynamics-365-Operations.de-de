---
title: Übersicht über die Fiskalintegration für Commerce-Kanäle
description: Dieser Artikel bietet einen Überblick der Steuerintegrationsfunktionen, die in Dynamics 365 Commerce verfügbar sind.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1812405db3c1e58eaf7cd1df3896f786e7bf026f
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631235"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>Übersicht über die Fiskalintegration für Commerce-Kanäle

[!include [banner](../includes/banner.md)]

Dieser Artikel bietet einen Überblick der Steuerintegrationsfunktionen, die in Dynamics 365 Commerce verfügbar sind. 

Die Steuerintegration enthält die Integration in unterschiedliche steuerbezogene Geräte und Dienste, die Benutzern die Steuerregistrierung von Verkäufen entsprechend lokaler Steuergesetze zur Verhinderung von Steuerhinterziehung im Einzelhandel ermöglicht. Nachfolgend einige typische Szenarien, die erfasst werden können, indem die Steuerintegration verwendet wird:

- Erfassen Sie einen Verkauf auf einem steuerbezogenen Gerät, das mit einem Retail Point of Sale (POS) verbunden ist, z. B. einem Belegdrucker, und drucken Sie einen Steuerbeleg für den Kunden.
- Senden Sie Informationen, die Verkäufen und Rücksendungen zugeordnet sind, die in Retail POS abgeschlossen werden, sicher an einen externen Webdienst, der von der Steuerbehörde betrieben wird.
- Sie helfen dabei, die Unveränderbarkeit der Daten von Verkaufstransaktionen durch digitale Signaturen sicherzustellen.

Die Steuerintegrationsfunktionen sind ein Framework, das eine allgemeine Lösung für die weitere Entwicklung und Anpassung der Integration zwischen Retail POS und steuerbezogenen Geräten und Diensten bereitstellt. Die Funktionalität umfasst auch Beispiele für die fiskalische Integration, die grundlegende Szenarien für bestimmte Länder oder Regionen unterstützen und die mit bestimmten fiskalischen Geräten oder Diensten arbeiten. Ein Steuerintegrationsbeispiel besteht aus mehreren Erweiterungen von Commerce-Komponenten und ist im Software Development Kit (SDK) enthalten. Weitere Informationen zu den Beispielen für die steuerliche Integration finden Sie unter [Beispiele für die steuerliche Integration im Commerce SDK](#fiscal-integration-samples-in-the-commerce-sdk). Informationen zur Installation und Verwendung des Commerce SDK finden Sie unter [Retail Software Development Kit (SDK) Architektur](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Um andere Szenarien zu unterstützen, die nicht von einem Steuerintegrationsbeispiel unterstützt werden, um Retail POS in andere steuerbezogene Geräte oder Dienste zu integrieren, oder um Anforderungen anderer Länder/Regionen zu erfüllen, müssen Sie entweder ein vorhandenes Steuerintegrationsbeispiel erweitern oder ein neues Beispiel mithilfe eines vorhandenen Beispiels erstellen.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Beispiele für den Prozess der Fiskalregistrierung und der Fiskalintegration für Fiskalgeräte und -dienste

Ein Steuerregistrierungsprozess in Retail POS kann aus einem oder mehreren Schritten bestehen. Jeder Schritt umfasst die Steuerregistrierung bestimmter Transaktionen oder -ereignisse in einem steuerbezogenes Gerät oder einem steuerbezogenen Dienst. Die folgenden Lösungskomponenten nehmen an der Fiskalregistrierung in einem Fiskalgerät oder -dienst teil:

- **Anbieter von fiskalischen Belegen** - Diese Komponente serialisiert Transaktions-/Ereignisdaten in dem Format, das auch für die Interaktion mit dem fiskalischen Gerät oder Dienst verwendet wird, parst Antworten vom fiskalischen Gerät oder Dienst und speichert die Antworten in der Channel-Datenbank. Die Erweiterung definiert auch die spezifischen Transaktionen und Ereignisse, die erfasst werden müssen.
- **Fiskalischer Konnektor** - Diese Komponente initialisiert die Kommunikation mit dem fiskalischen Gerät oder Dienst, sendet Anfragen oder direkte Befehle an das fiskalische Gerät oder den Dienst, basierend auf den Daten zu Transaktionen/Ereignissen, die aus dem fiskalischen Beleg extrahiert werden, und empfängt Antworten vom fiskalischen Gerät oder Dienst.

Ein Beispiel für eine Fiskalintegration kann die Commerce Runtime (CRT), die Hardware-Station und POS-Erweiterungen für einen Anbieter von fiskalischen Belegen und einen fiskalischen Konnektor enthalten. Es enthält auch die folgenden Komponentenkonfigurationen:

- **Steuerdokumentanbieter-Konfiguration**: Diese Konfiguration definiert eine Ausgabemethode und ein Format für Steuerdokumente. Er enthält auch eine Datenzuordnung für Steuern und Zahlungsformen, um Daten aus Retail POS mit den Werten kompatibel zu machen, die in der Fiskalgerät- oder Service-Firmware vordefiniert sind.
- **Fiscal Konnektor Konfiguration** - Diese Konfiguration definiert die physische Kommunikation mit dem spezifischen Fiskalgerät oder -dienst.

Ein Steuerregistrierungsprozess für ein bestimmtes POS-Register wird von einer entsprechenden Einstellung im POS-Funktionsprofil definiert. Weitere Einzelheiten zum Konfigurieren eines fiskalischen Registrierungsprozesses, zum Hochladen von Konfigurationen für fiskalische Belege und fiskalische Konnektoren sowie zum Ändern von Konfigurationsparametern finden Sie unter [Einrichten eines fiskalischen Registrierungsprozesses](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

> [!NOTE]
> Wenn Sie Geräte für nicht fiskalische Vorgänge benötigen, wie z.B. die Suche im Produktkatalog, das Nachschlagefeld für Kunden oder die Erstellung von Transaktionsentwürfen, können Sie diese als Register mit fiskalischen Prozesseinschränkungen auswählen. Weitere Informationen finden Sie unter [Register mit steuerlichen Registrierungsbeschränkungen festlegen](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions).

Der folgende typische Fiskalregistrierungs Flow beginnt mit einem Ereignis in der Kasse (z.B. Abschluss einer Verkaufstransaktion) und implementiert eine vordefinierte Sequenz von Schritten, an denen andere Commerce Komponenten beteiligt sind (z.B. die CRT und Hardware Station).

1. Die Kasse fordert einen Fiskalbeleg vom Fiscal Integration Framework (FIF) an.
1. Die FIF bestimmt, ob das aktuelle Ereignis eine steuerliche Registrierung erfordert.
1. Basierend auf den Einstellungen für die Fiskalregistrierung identifiziert die FIF einen fiskalischen Konnektor und einen entsprechenden Anbieter von fiskalischen Belegen, die für die Fiskalregistrierung verwendet werden sollen.
1. Die FIF führt den Fiskalbeleg-Anbieter aus, der einen Fiskalbeleg (z.B. ein XML-Dokument) erzeugt, der die Transaktion oder das Ereignis darstellt.
1. Die FIF gibt den erzeugten fiskalischen Beleg an die Kasse zurück.
1. Das POS fordert das FIF auf, den fiskalischen Beleg an das Fiskalgerät oder den Fiskaldienst zu senden.
1. Die FIF führt den fiskalischen Konnektor aus, der den fiskalischen Beleg verarbeitet und ihn an das fiskalische Gerät oder den fiskalischen Dienst sendet.
1. Das FIF gibt die Fiskalantwort (d.h. die Antwort des Fiskalgeräts oder -dienstes) an die Kasse zurück.
1. Die Kasse analysiert die Fiskalantwort, um festzustellen, ob die Fiskalregistrierung erfolgreich war. Je nach Bedarf fordert die Kasse den FIF auf, aufgetretene Fehler zu bearbeiten. 
1. Die Kasse fordert die FIF auf, die Fiskalantwort zu verarbeiten und zu speichern.
1. Der Anbieter des Fiskalbelegs verarbeitet die Fiskalantwort. Als Teil dieser Verarbeitung parst der Anbieter des fiskalischen Belegs die Antwort und extrahiert daraus erweiterte Daten.
1. Der FIF speichert die Antwort und die erweiterten Daten in der Channel-Datenbank.
1. Bei Bedarf druckt die Kasse einen Bon über einen regulären Bondrucker, der an die Hardware-Station angeschlossen ist. Der Beleg kann die erforderlichen Daten aus der Fiskalantwort enthalten.
 
Die folgenden Beispiele zeigen die Flows zur Ausführung der steuerlichen Registrierung für typische steuerliche Geräte oder Dienstleistungen.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Die steuerliche Registrierung erfolgt über ein Gerät, das mit der Hardwarestation verbunden ist.

Diese Konfiguration wird verwendet, wenn ein physisches Fiskalgerät, wie z.B. ein Fiskaldrucker, mit der Hardwarestation verbunden ist. Es ist auch anwendbar, wenn die Kommunikation mit einem Fiskalgerät oder -dienst über eine Software erfolgt, die auf der Hardware-Station installiert ist. In diesem Fall befindet sich der Anbieter von fiskalischen Belegen auf der CRT und der fiskalische Konnektor befindet sich auf der Station Hardware.

![Fiskalische Registrierung über ein an die Hardware-Station angeschlossenes Gerät.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Die steuerliche Registrierung erfolgt über einen externen Dienst

Diese Konfiguration wird verwendet, wenn die fiskalische Registrierung über einen externen Dienst erfolgt, z.B. einen Webservice, der von der Steuerbehörde betrieben wird. In diesem Fall befinden sich sowohl der Anbieter des fiskalischen Belegs als auch der fiskalische Konnektor auf der CRT.

![Die steuerliche Registrierung erfolgt über einen externen Dienst.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Die steuerliche Registrierung erfolgt intern in der CRT.

Diese Konfiguration wird verwendet, wenn kein externes Fiskalgerät oder ein externer Dienst für die steuerliche Registrierung erforderlich ist. Es wird z.B. verwendet, wenn die steuerliche Registrierung durch digitales Signieren von Verkaufstransaktionen erfolgt. In diesem Fall befinden sich sowohl der Anbieter des fiskalischen Belegs als auch der fiskalische Konnektor auf der CRT.

![Die steuerliche Registrierung wird intern in der CRT durchgeführt.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Die steuerliche Registrierung erfolgt über ein Gerät oder einen Dienst im lokalen Netzwerk

Diese Konfiguration wird verwendet, wenn ein physisches Fiskalgerät oder ein Fiskalservice im lokalen Netzwerk des Stores vorhanden ist und eine HTTPS-Anwendungsprogrammierschnittstelle (API) bietet. In diesem Fall befindet sich der Anbieter der fiskalischen Belege auf der CRT, und der fiskalische Konnektor befindet sich auf dem POS.

![Die steuerliche Registrierung erfolgt über ein Gerät oder einen Dienst im lokalen Netzwerk.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Fehlerbehandlung

Das Steuerintegrationsframework bietet folgende Optionen, um Fehler bei der Steuerregistrierung zu behandeln:

- **Wiederholen**: Der Operator kann diese Option verwenden, wenn der Fehler schnell behoben werden kann, und die Steuerregistrierung erneut ausgeführt werden kann. Beispielsweise kann diese Option verwendet werden, falls das steuerbezogene Gerät nicht verbunden ist, im Belegdrucker kein Papier mehr vorhanden ist oder Papierstau im Belegdrucker herrscht.
- **Abbrechen**: Mit dieser Option kann der Operator die Steuerregistrierung der aktuellen Transaktion oder des aktuellen Ereignisses zurückstellen, auch bei einem Fehler. Nachdem die Registrierung zurückgestellt wurde, kann der Operator am POS weiterarbeiten und jeden beliebigen Arbeitsgang abschließen, für den die Steuerregistrierung nicht erforderlich ist. Wenn ein Ereignis, das die Steuerregistrierung erfordert, am POS auftritt (beispielsweise wird eine neue Transaktion geöffnet), wird das Fehlerbehandlungsdialogfeld automatisch angezeigt, um den Operator zu benachrichtigen, dass die vorherige Transaktion nicht ordnungsgemäß erfasst wurde und um die Fehlerbehandlungsoptionen bereitzustellen.
- **Überspringen**: Der Operator kann diese Option verwenden, wenn es nicht möglich ist, die Steuerregistrierung der aktuellen Transaktion oder des aktuellen Ereignisses abzuschließen, z. B. wenn der Belegdrucker außer Betrieb ist, **und** die Steuerregistrierung kann unter bestimmten Voraussetzungen entfallen. Beispielsweise kann diese Option verwendet werden, wenn eine Verkaufsbuchung, bei der ein Fehler bei der Steuerregistrierung aufgetreten ist, in einer Papiererfassung erfasst werden kann. Nach dem Überspringen der Steuerregistrierung kann der reguläre Betrieb am POS fortgesetzt werden. 
- **Als registriert markieren**: Der Operator kann diese Option verwenden, wenn die aktuelle Transaktion oder das aktuelle Ereignis auf dem Fiskalgerät registriert wurde, z. B. wenn ein Steuerbeleg ausgedruckt wurde, jedoch ein Fehler auftritt, wenn die Steuerantwort in der Kanaldatenbank gespeichert wird. Nachdem die aktuelle Transaktion oder das aktuelle Ereignis als registriert markiert wurde, kann der reguläre Betrieb am POS fortgesetzt werden.
- **Aufschieben**: Der Operator kann diese Option verwenden, wenn die Transaktion nicht registriert wurde, weil das Registrierungsgerät oder der Registrierungsdienst nicht verfügbar ist **und** einer der folgenden Fälle zutrifft:
    - Es gibt eine Sicherungsoption für die Steuerregistrierung und der Steuerregistrierungsprozess für die aktuelle Transaktion kann fortgesetzt werden. Zum Beispiel kann ein lokales [Fiskalgerät](./latam-bra-cf-e-sat.md#scenario-4-make-a-cash-and-carry-sale-of-goods-by-using-sat-as-contingency-mode) eine Sicherungsoption für einen Online-Steuerregistrierungsdienst sein, wenn der Dienst nicht verfügbar ist.
    - Die Steuerregistrierung kann später mit anderen Mitteln als dem Steuerintegrationsframework abgeschlossen werden. Zum Beispiel können aufgeschobene Transaktionen kann die Steuerregistrierung später in einem Stapel durch eine [separate Funktionalität](./latam-bra-nfce.md#scenario-3-make-a-cash-and-carry-sale-of-goods-in-offline-contingency-mode) durchgeführt werden.
    
    Nachdem die aktuelle Transaktion oder das aktuelle Ereignis verschoben wurde, kann der reguläre Betrieb am POS fortgesetzt werden.

> [!WARNING]
> Die Optionen **Überspringen**, **Als registriert markieren** und **Verschieben** sollten als Notfalloptionen betrachtet und nur in Ausnahmefällen verwendet werden. Besprechen Sie diese Optionen zur Fehlerbehandlung mit Ihrem Rechtsanwalt oder Steuerberater und setzen Sie Ihren gesunden Menschenverstand ein, bevor Sie sie aktivieren. Die Optionen müssen im Steuerregistrierungsprozess aktiviert werden, bevor sie verwendet werden. Um sicherzustellen, dass Operatoren sie nicht regelmäßig verwenden, müssen ihnen entsprechende Berechtigungen erteilt werden.

Eine [Steuertransaktion](#storing-fiscal-response-in-fiscal-transaction) wird erstellt, wenn die Optionen **Überspringen**, **Als registriert markieren** oder **Verschieben** ausgewählt sind, die Steuertransaktion aber keine Steuerantwort erhält. Auf diese Weise können Sie das Ereignis einer fehlgeschlagenen Steuerregistrierung erfassen. Mit diesen Optionen können darüber hinaus mithilfe von Infocodes bestimmte Informationen über einen Fehler erfasst werden, z. B. der Grund für den Fehler oder eine Begründung für das Überspringen der Steuerregistrierung oder das Markieren der Transaktion als registriert. Weitere Informationen zum Einrichten von Fehlerbehandlungsparametern finden Sie unter [Festlegen von Fehlerbehandlungseinstellungen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Optionale Steuerregistrierung

Steuerliche Erfassung ist möglicherweise erforderlich für einige Vorgänge aber für andere optional. Beispielsweise kann die Steuererfassung von regulärenr Verkäufen und Rücklieferungen zwingend sein, aber die steuerliche Erfassung, die sich auf Debitoreneinzahlungen bezieht ist optional. In diesem Fall sollte die fehlende steuerliche Erfassung eines Verkaufs andere Aufträge sperren, wenn aber die steuerliche Erfassung einer Debitoreneinzahlung nicht abgeschlosse ist, sollten andere Aufträge nicht gesperrt werden. Um die erforderlichen und optionalen Arbeitsgänge zu unterscheiden, sollten Sie sie durch verschiedene Dokumentanbieter abwickeln und separate Schritte für den steuerlichen Erfassungsprozesses für diese Anbieter einrichten. Der Parameter muss **Bei Fehler fortsetzen** für einen Schritt aktiviert werden, der der optionalen steuerlichen Erfassung zugeordnet ist. Weitere Informationen zum Einrichten von Fehlerbehandlungsparametern finden Sie unter [Festlegen von Fehlerbehandlungseinstellungen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Fiskalische Registrierung manuell wiederholen

Wenn die Steuerregistrierung einer Transaktion oder eines Ereignisses nach einem Fehler (beispielsweise wenn der Operator **Abbrechen** im Fehlerbehandlungsdialogfeld gewählt hat) zurückgestellt wurde, können Sie die Steuerregistrierung manuell überprüfen, indem Sie einen entsprechenden Arbeitsgang aufrufen. Weitere Details finden Sie unter [Manuelle Ausführung der zurückgestellten Steuerregistrierung aktivieren](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).

### <a name="fiscal-registration-health-check"></a>Steuerliche Erfassungsintegritätsprüfung

Die Integritätsprüfungsprozedur für die steuerliche Registrierungen überprüft die Verfügbarkeit des steuerlichen Geräts oder der Dienstleistung, wenn bestimmte Ereignisse auftreten. Wenn die steuerliche Erfassung gerade nicht abgeschlossen werden kann, wird der Mitarbeiter im Voraus benachrichtigt.

Der POS führt die Integritätsprüfung aus, wenn die folgenden Ereignisse auftreten:

- Eine neue Transaktion wird geöffnet.
- Eine ausgesetzte Transaktion wird zurückgerufen.
- Ein Verkaufs- oder eine Rücklieferungstransaktion ist abgeschlossen.

Wenn die Integritätsprüfung fehlschlägt, wird im POS das Integritätsprüfungsdialogfeld angezeigt. Dieses Dialogfeld enthält die folgenden Schaltflächen:

- **OK** – Mit dieser Schaltfläch kann der Mitarbeiter einen Integritätsprüfungsfehler ignorieren und den Arbeitsgang weiter verarbeiten. Mitarbeiter können diese Schaltfläche nur auswählen, wenn die Berechtigung **integritätsprüfungsfehler überspringen zulassen** aktiviert ist.
- **Abbrechen** – Wenn der Mitarbeiter diese Schaltfläche auswählt, bricht der POS die letzte Aktion ab (beispielsweise wird ein Artikel der neuen Transaktlion nicht hinzugefügt).

> [!NOTE]
> Die Gesundheitsprüfung wird nur ausgeführt, wenn der aktuelle Vorgang eine Fiskalregistrierung erfordert und wenn der Parameter **Fortsetzen bei Fehler** für den aktuellen Schritt des Fiskalregistrierungsprozesses deaktiviert ist. Weitere Informationen finden Sie unter [Fehlerbehandlungseinstellungen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Speichern der Steuerantwort in der Steuertransaktion

Wenn die Steuerregistrierung einer Transaktion oder eines Ereignisses erfolgreich war, wird eine Steuertransaktion in der Kanaldatenbank erstellt und mit der ursprünglichen Transaktion oder dem ursprünglichen Ereignis verknüpft. Wenn die Option **Überspringen**, **Als registriert markieren** oder **Verschieben** für eine fehlgeschlagene Steuerregistrierung ausgewählt ist, werden diese Informationen in einer Steuertransaktion entsprechend gespeichert. Eine Steuertransaktion enthält die Steuerantwort vom steuerbezogenen Gerät oder Dienst. Wenn der Steuerregistrierungsprozess aus mehreren Schritten besteht, wird eine Steuertransaktion für die einzelnen Schritte des Prozesses erstellt, der zu einer erfolgreichen oder fehlgeschlagenen Registrierung geführt hat.

Steuerbezogene Buchungen werden zusammen mit den Transaktionen über den *P-Job* an die Zentralverwaltung übertragen. Im Inforegister **Steuerbezogene Buchungen** auf der Seite für **Geschäftsbuchungen** können Sie die steuerbezogenen Buchungen anzeigen, die mit den Transaktionen verknüpft sind.

Eine Steuertransaktion speichert die folgenden Details:

- Steuerregistrierungsprozess-Details (Prozess, Konnektorgruppe, Konnektor usw.). Sie speichert außerdem die Seriennummer des steuerbezogenen Geräts im Feld **Registernummer**, wenn diese Informationen in der Steuerantwort enthalten sind.
- Der Status der steuerlichen Registrierung: **Erledigt** für eine erfolgreiche Registrierung, **Übersprungen**, wenn der Bediener die Option **Überspringen** für eine fehlgeschlagene Registrierung gewählt hat, **Als registriert markiert**, wenn der Bediener die Option **Als registriert markieren** gewählt hat, oder **Aufgeschoben**, wenn der Bediener die Option **Aufgeschoben** gewählt hat.
- Infocodetransaktionen im Zusammenhang mit einer ausgewählten Steuertransaktion. Um die Infocode-Transaktionen anzuzeigen, wählen Sie auf der Registerkarte **Fiskalische Transaktionen** eine fiskalische Transaktion mit dem Status **Übersprungen**, **Als registriert markiert** oder **Aufgeschoben** aus und wählen Sie dann **Infocode-Transaktionen**.

Indem Sie **Erweiterte Daten** wählen, können Sie auch einige Eigenschaften der fiskalischen Transaktion anzeigen. Die Liste der Eigenschaften, die angezeigt werden können, ist spezifisch für die Fiskalregistrierungsfunktion, die die fiskalische Transaktion erzeugt hat. Sie können z. B. die digitale Signatur, die fortlaufende Nummer, den Thumbprint des Zertifikats, die Identifizierung des Hash-Algorithmus und andere Eigenschaften der fiskalischen Transaktion für die digitale Signierfunktion für Frankreich anzeigen.

## <a name="fiscal-texts-for-discounts"></a>Steuertexte für Rabatte

Einige Länder/Regionen haben spezielle Anforderungen zu zusätzlichen Texten, die auf Steuerbelege gedruckt werden müssen, wenn verschiedene Arten von Rabatten angewendet werden. Mit den Steuerintegrationsfunktionen können Sie einen bestimmten Text für einen Rabatt einrichten, der nach einer Rabattposition auf einen Steuerbeleg gedruckt wird. Bei manuellen Rabatten können Sie einen Steuertext für den Infocode konfigurieren, der als **Produktrabatt**-Infocode im POS-Funktionsprofil angegeben ist. Weitere Informationen zum Einrichten von Steuertexten für Rabatte finden Sie unter [Einrichten von Steuertexten für Rabatte](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Drucken von Steuer X- und Steuer Z-Berichten

Die Steuerintegrationsfunktionen unterstützen die Generierung von Tagesendeauszügen, die für das integrierte steuerbezogene Gerät oder den integrierten steuerbezogenen Dienst spezifisch sind:

- Neue Schaltflächen, die die entsprechenden Vorgänge ausführen, sollten zum POS-Bildschirmlayout hinzugefügt werden. Weitere Informationen finden Sie unter [Einrichten von Steuer X/Z-Berichten vom POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Im Steuerintegrationsbeispiel sollten diese Vorgänge mit den gewünschten Vorgängen des steuerbezogenen Geräts abgeglichen werden.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Beispiele für die Fiskalintegration im Commerce SDK

Die folgenden Beispiele für die Fiskalintegration sind derzeit im Commerce SDK verfügbar:

- [Beispiel für die Integration eines Belegdruckers für Italien](./emea-ita-fpi-sample.md)
- [Beispiel für Belegdruckerintegration für Polen](./emea-pol-fpi-sample.md)
- [Integrationsbeispiel für Steuererfassungsdienst für Österreich](./emea-aut-fi-sample.md)
- [Integrationsbeispiel für Steuererfassungsdienst für Tschechische Republik](./emea-cze-fi-sample.md)
- [Beispiel zur Integration der Kontrolleinheit für Schweden](./emea-swe-fi-sample.md)
- [Integrationsbeispiel für Steuererfassungsdienst für Deutschland](./emea-deu-fi-sample.md)
- [Beispiel für Belegdruckerintegration für Russland](./rus-fpi-sample.md)

Die folgende Fiskalintegrationsfunktionalität wird auch durch die Verwendung des Fiskalintegrations-Frameworks implementiert, ist aber "out of the box" verfügbar und ist nicht im Commerce SDK enthalten:

- [Fiskalische Registrierung für Brasilien](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Digitale Signatur für Frankreich](./emea-fra-cash-registers.md)

Die folgende Fiskalintegrationsfunktionalität ist ebenfalls im Commerce SDK verfügbar, nutzt aber derzeit nicht das Fiskalintegrations-Framework. Die Migration dieser Funktionen in das Steuerintegrationsframework ist für spätere Aktualisierungen geplant.

- [Digitale Signatur für Norwegen](./emea-nor-cash-registers.md)

Die folgende, im Commerce SDK verfügbare Funktionalität zur Fiskalintegration nutzt nicht das Fiskalintegrations-Framework und wird in späteren Updates außer Betrieb genommen:

- [Beispiel zur Integration der Kontrolleinheit für Schweden (veraltet)](./retail-sdk-control-unit-sample.md)
- [Digitale Signatur für Frankreich (veraltet)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
