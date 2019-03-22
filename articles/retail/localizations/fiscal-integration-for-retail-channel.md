---
title: Übersicht über die Steuerintegration für Retail Channels
description: Dieses Thema bietet einen Überblick der Steuerintegrationsfunktionen, die in Microsoft Dynamics 365 for Retail verfügbar sind.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: c6fcc93cfed35d73ae749856f33857ba84dbfd82
ms.sourcegitcommit: 70aeb93612ccd45ee88c605a1a4b87c469e3ff57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/01/2019
ms.locfileid: "773276"
---
# <a name="overview-of-fiscal-integration-for-retail-channels"></a>Übersicht über die Steuerintegration für Retail Channels

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Einführung

Dieses Thema bietet einen Überblick der Steuerintegrationsfunktionen, die in Microsoft Dynamics 365 for Retail verfügbar sind. Die Steuerintegration enthält die Integration in unterschiedliche steuerbezogene Geräte und Dienste, die Benutzern die Steuerregistrierung von Einzelhandelsverkäufen entsprechend lokalen Steuergesetzen zur Verhinderung von Steuerhinterziehung im Einzelhandel ermöglicht. Nachfolgend einige typische Szenarien, die erfasst werden können, indem die Steuerintegration verwendet wird:

- Erfassen eines Einzelhandelsverkaufs auf einem steuerbezogenen Gerät, das mit einem Retail point of sale (POS) verbunden ist, z. B. einem Belegdrucker, und Drucken eines Steuerbelegs für den Kunden.
- Senden Sie Informationen, die Verkäufen und Rücksendungen zugeordnet sind, die in Retail POS abgeschlossen werden, sicher an einen externen Webdienst, der von der Steuerbehörde betrieben wird.
- Gewährleisten Sie die Unveränderbarkeit von Verkaufsbuchungsdaten durch digitale Signaturen.

Die Steuerintegrationsfunktionen in Retail sind ein Framework, das eine allgemeine Lösung für die weitere Entwicklung und Anpassung der Integration zwischen Retail POS und steuerbezogenen Geräten und Diensten bereitstellt. Die Funktionalität umfasst auch Steuerintegrationsbeispiele, die grundlegende Einzelhandelsszenarien für bestimmte Länder/Regionen unterstützen und mit bestimmten steuerbezogenen Geräten oder Diensten verwendet werden können. Ein Steuerintegrationsbeispiel besteht aus mehreren Erweiterungen von Retail-Komponenten und ist im Retail Software Development Kit (SDK) enthalten. Weitere Informationen zu Steuerintegrationsbeispielen, die im Retail SDK verfügbar sind, finden Sie unter [Steuerintegrationsbeispiele im Retail SDK](#fiscal-integration-samples-in-the-retail-sdk). Informationen zur Installation und Verwendung des Retail SDK finden Sie unter [Retail SDK-Übersicht](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Um andere Szenarien zu unterstützen, die nicht von einem Steuerintegrationsbeispiel unterstützt werden, um Retail POS in andere steuerbezogene Geräte oder Dienste zu integrieren, oder um Anforderungen anderer Länder/Regionen zu erfüllen, müssen Sie entweder ein vorhandenes Steuerintegrationsbeispiel erweitern oder ein neues Beispiel mithilfe eines vorhandenen Beispiels erstellen.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>Steuerregistrierungsprozess und Steuerintegrationsbeispiele für steuerbezogene Geräte

Ein Steuerregistrierungsprozess in Retail POS kann aus einem oder mehreren Schritten bestehen. Jeder Schritt integriert die Steuerregistrierung bestimmter Einzelhandelstransaktionen oder -ereignisse in ein steuerbezogenes Gerät oder einen steuerbezogenen Dienst. Die folgenden Lösungskomponenten nehmen an der Steuerregistrierung in einem steuerbezogenen Gerät teil, das mit einer Hardwarestation verbunden ist:

- **Commerce Runtime (CRT)-Erweiterung** – Diese Komponente serialisiert Einzelhandelstransaktions-/-ereignisdaten in einem Format, das auch für die Interaktion mit dem steuerbezogenen Gerät verwendet wird, analysiert Antworten vom steuerbezogenen Gerät und speichert die Antworten in der Kanaldatenbank. Die Erweiterung definiert auch die spezifischen Transaktionen und Ereignisse, die erfasst werden müssen. Diese Komponente wird häufig als *Steuerdokumentanbieter* bezeichnet.
- **Hardwarestationserweiterung** – Diese Komponente Initialisiert die Kommunikation mit dem steuerbezogenen Gerät, sendet Anforderungen und leitet Befehle an das steuerbezogene Gerät auf Basis der Einzelhandelstransaktions-/-ereignisdaten, die aus dem Steuerdokument extrahiert werden, und empfängt Antworten vom steuerbezogenen Gerät. Diese Komponente wird häufig als *Steuerkonnektor* bezeichnet.

Ein Steuerintegrationsbeispiel für ein steuerbezogenes Gerät enthält jeweils die CRT- und Hardwarestationserweiterungen für einen Steuerdokumentanbieter und Steuerkonnektor. Es enthält auch die folgenden Komponentenkonfigurationen:

- **Steuerdokumentanbieter-Konfiguration** – Diese Konfiguration definiert eine Ausgabemethode und ein Format für Steuerdokumente. Es enthält auch eine Datenzuordnung für Steuern und Zahlungsmethoden, um Daten aus Retail POS mit den Werten, die in der Firmware des steuerbezogenen Geräts vordefiniert werden, kompatibel zu machen.
- **Steuerkonnektorkonfiguration** – Diese Konfiguration definiert die physische Kommunikation mit dem betreffenden steuerbezogenen Gerät.

Ein Steuerregistrierungsprozess für ein bestimmtes POS-Register wird von einer entsprechenden Einstellung im POS-Funktionsprofil definiert. Weitere Informationen zum Konfigurieren eines Steuerregistrierungsprozesses, Hochladen von Steuerdokumentanbieter- und Steuerkonnektorkonfigurationen und Ändern ihrer Parameter finden Sie unter [Einrichten eines Steuerregistrierungsprozesses](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Das folgende Beispiel zeigt einen typischen Steuerregistrierungs-Ausführungsfluss für ein steuerbezogenes Gerät. Der Fluss startet mit einem Ereignis im POS (beispielsweise dem Abschluss einer Verkaufsbuchung) und implementiert die folgende Schrittfolge:

1. Der POS fordert ein Steuerdokument von CRT an.
2. CRT bestimmt, ob das aktuelle Ereignis eine Steuerregistrierung erfordert.
3. Auf Grundlage der Steuerregistrierungsprozess-Einstellungen identifiziert CRT einen Steuerkonnektor und entsprechenden Steuerdokumentanbieter, der für die Steuerregistrierung verwendet werden soll.
4. CRT führt den Steuerdokumentanbieter aus, der ein Steuerdokument generiert (beispielsweise ein XML-Dokument), das die Einzelhandelstransaktion oder das Einzelhandelsereignis darstellt.
5. Der POS sendet das Steuerdokument, das CRT vorbereitet, an eine Hardwarestation.
6. Die Hardwarestation führt den Steuerkonnektor aus, der das Steuerdokument verarbeitet und es an das steuerbezogene Gerät oder den steuerbezogenen Dienst kommuniziert.
7. Der POS analysiert die Antwort vom steuerbezogenen Gerät oder Dienst, um zu bestimmen, ob die Steuerregistrierung erfolgreich war.
8. CRT speichert die Antwort in der Kanaldatenbank.

![Lösungsschema](media/emea-fiscal-integration-solution.png "Lösungsschema")

## <a name="error-handling"></a>Fehlerbehandlung

Das Steuerintegrationsframework bietet folgende Optionen, um Fehler bei der Steuerregistrierung zu behandeln:

- **Wiederholen** – Operatoren können diese Option verwenden, wenn der Fehler schnell behoben werden kann, und die Steuerregistrierung erneut ausgeführt werden kann. Beispielsweise kann diese Option verwendet werden, falls das steuerbezogene Gerät nicht verbunden ist, im Belegdrucker kein Papier mehr vorhanden ist oder Papierstau im Belegdrucker herrscht.
- **Abbrechen** – Mit dieser Option können Operatoren die Steuerregistrierung der aktuellen Transaktion oder des aktuellen Ereignisses verschieben, auch bei einem Fehler. Nachdem die Registrierung verschoben ist, kann der Operator am POS weiterarbeiten und jeden beliebigen Arbeitsgang abschließen, für den die Steuerregistrierung nicht erforderlich ist. Wenn ein Ereignis, das die Steuerregistrierung erfordert, am POS auftritt (beispielsweise wird eine neue Transaktion geöffnet), wird das Fehlerbehandlungsdialogfeld automatisch angezeigt, um den Operator zu benachrichtigen, dass die vorherige Transaktion nicht ordnungsgemäß erfasst wurde und um die Fehlerbehandlungsoptionen bereitzustellen.
- **Überspringen** – Operatoren können diese Option verwenden, wenn die Steuerregistrierung unter bestimmten Bedingungen ausgelassen werden kann und regelmäßige Vorgänge am POS fortgesetzt werden können. Beispielsweise kann diese Option verwendet werden, wenn eine Verkaufsbuchung, bei der ein Fehler bei der Steuerregistrierung aufgetreten ist, in einer Papiererfassung erfasst werden kann.
- **Als registriert markieren** – Operatoren können diese Option verwenden, wenn die Transaktion tatsächlich auf dem steuerbezogenen Gerät registriert wurde (z. B. wurde ein Steuerbeleg ausgedruckt), jedoch ein Fehler aufgetreten ist, als die Steuerantwort in der Kanaldatenbank gespeichert wurde.

> [!NOTE]
> Die Optionen **Überspringen** und **Als registriert markieren** müssen im Steuerregistrierungsprozess aktiviert werden, bevor sie verwendet werden. Darüber hinaus müssen Operatoren entsprechende Berechtigungen gewährt werden.

Mit den Optionen **Überspringen** und **Als registriert markieren** können Infocodes bestimmte Informationen zum Fehler erfassen, z. B. den Grund für den Fehler oder eine Begründung für das Überspringen der Steuerregistrierung oder das Markieren der Transaktion als registriert. Weitere Informationen zum Einrichten von Fehlerbehandlungsparametern finden Sie unter [Festlegen von Fehlerbehandlungseinstellungen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Speichern der Steuerantwort in der Steuertransaktion

Wenn die Steuerregistrierung einer Transaktion oder eines Ereignisses erfolgreich war, wird eine Steuertransaktion in der Kanaldatenbank erstellt und mit der ursprünglichen Transaktion oder dem ursprünglichen Ereignis verknüpft. Wenn die Option **Überspringen** oder **Als registriert markieren** für eine fehlgeschlagene Steuerregistrierung ausgewählt ist, werden diese Informationen in einer Steuertransaktion entsprechend gespeichert. Eine Steuertransaktion enthält die Steuerantwort vom steuerbezogenen Gerät oder Dienst. Wenn der Steuerregistrierungsprozess aus mehreren Schritten besteht, wird eine Steuertransaktion für die einzelnen Schritte des Prozesses erstellt, der zu einer erfolgreichen oder fehlgeschlagenen Registrierung geführt hat.

Steuertransaktionen werden vom *P-Einzelvorgang* in die Retail Zentralverwaltung übertragen, zusammen mit den Einzelhandelstransaktionen. Im Inforegister **Steuertransaktionen** auf der Seite **Einzelhandelsgeschäftsbuchungen** können Sie die Steuertransaktionen anzeigen, die mit den Einzelhandelstransaktionen verknüpft sind.


Eine Steuertransaktion speichert die folgenden Details:

- Steuerregistrierungsprozess-Details (Prozess, Konnektorgruppe, Konnektor usw.). Sie speichert außerdem die Seriennummer des steuerbezogenen Geräts im Feld **Registernummer**, wenn diese Informationen in der Steuerantwort enthalten sind.
- Der Status der Steuerregistrierung: **Abgeschlossen** für die erfolgreiche Registrierung, **Übersprungen**, wenn der Operator die Option **Überspringen** für eine fehlerhafte Registrierung ausgewählt hat, oder **Als registriert markiert**, wenn der Operator die Option **Als registriert markieren** ausgewählt hat.
- Infocodetransaktionen im Zusammenhang mit einer ausgewählten Steuertransaktion. Um die Infocodetransaktionen anzuzeigen, wählen Sie im Inforegister **Steuertransaktionen** eine Steuertransaktionen aus, die den Status **Übersprungen** oder **Als registriert markiert** aufweist, und wählen Sie dann **Infocodetransaktionen** aus.

## <a name="fiscal-texts-for-discounts"></a>Steuertexte für Rabatte

Einige Länder/Regionen haben spezielle Anforderungen zu zusätzlichen Texten, die auf Steuerbelege gedruckt werden müssen, wenn verschiedene Arten von Rabatten angewendet werden. Mit den Steuerintegrationsfunktionen können Sie einen bestimmten Text für einen Rabatt einrichten, der nach einer Rabattposition auf einen Steuerbeleg gedruckt wird. Bei manuellen Rabatten können Sie einen Steuertext für den Infocode konfigurieren, der als **Produktrabatt**-Infocode im POS-Funktionsprofil angegeben ist. Weitere Informationen zum Einrichten von Steuertexten für Rabatte finden Sie unter [Einrichten von Steuertexten für Rabatte](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Drucken von Steuer X- und Steuer Z-Berichten

Die Steuerintegrationsfunktionen unterstützen die Generierung von Tagesendeauszügen, die für das integrierte steuerbezogene Gerät oder den integrierten steuerbezogenen Dienst spezifisch sind:

- Neue Schaltflächen, die die entsprechenden Vorgänge ausführen, sollten zum POS-Bildschirmlayout hinzugefügt werden. Weitere Informationen finden Sie unter [Einrichten von Steuer X/Z-Berichten vom POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- Im Steuerintegrationsbeispiel sollten diese Vorgänge mit den gewünschten Vorgängen des steuerbezogenen Geräts abgeglichen werden.

## <a name="fiscal-integration-samples-in-the-retail-sdk"></a>Steuerintegrationsbeispiele im Retail SDK

Die folgenden Steuerintegrationsbeispiele sind derzeit im Retail SDK verfügbar, das mit Retail veröffentlicht wird:

- [Beispiel für Belegdruckerintegration für Italien](emea-ita-fpi-sample.md)
- [Beispiel für Belegdruckerintegration für Polen](emea-pol-fpi-sample.md)

Die folgenden Steuerintegrationsfunktionen sind ebenfalls im Retail SDK verfügbar, nutzen derzeit jedoch nicht das Steuerintegrationsframework. Die Migration dieser Funktionen in das Steuerintegrationsframework ist für spätere Aktualisierungen geplant.

- [Digitale Signatur für Frankreich](emea-fra-cash-registers.md)
- [Digitale Signatur für Norwegen](emea-nor-cash-registers.md)
- [Beispiel zur Integration der Kontrolleinheit für Schweden](./retail-sdk-control-unit-sample.md)

