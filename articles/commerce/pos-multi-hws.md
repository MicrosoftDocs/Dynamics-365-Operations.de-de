---
title: Spezielle Zahlungsterminals und Eingabeaufforderungen für einen Drucker und eine Kassenschublade
description: Dieses Thema enthält Informationen zur Möglichkeit eines dedizierten Zahlungsterminals und fordert den Benutzer auf, eine Kassenschublade und einen Belegdrucker auszuwählen.
author: rubendel
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0611e90e47eabf0cb96208690acda22651d669ae812d2af2547a294c32ed0a1d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764536"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Spezielle Zahlungsterminals und Eingabeaufforderungen für einen Drucker und eine Kassenschublade

[!include [banner](includes/banner.md)]

Dieses Thema enthält Informationen zur Möglichkeit eines dedizierten Zahlungsterminals und fordert den Benutzer auf, eine Kassenschublade und einen Belegdrucker auszuwählen.

## <a name="overview"></a>Übersicht

Moderne Einzelhändler suchen nach Möglichkeiten, die Kaufabwicklung im Geschäft zu optimieren. Die jüngsten Trends zur papierlosen Kaufabwicklung durch elektronische Zahlungen tragen nicht nur dazu bei, das Einkaufserlebnis reibungsloser zu gestalten, sondern verringern auch die Notwendigkeit, jedem Filialmitarbeiter eine vollständige Auswahl an Peripheriegeräten zur Verfügung zu stellen.

Microsoft Dynamics 365 Commerce unterstützt diese Trends, indem ein Szenario aktiviert wird, in dem einem POS-Gerät ständig ein dediziertes Zahlungsterminal zugewiesen ist, jedoch kein eigener Belegdrucker oder keine eigene Kassenschublade vorhanden ist. Wenn Mitarbeiter eine Quittung ausdrucken oder eine Barzahlung vornehmen müssen, werden sie aufgefordert, eine Hardwarestation auszuwählen, auf der diese Geräte konfiguriert sind.

## <a name="key-terms"></a>Schlüsselbegriffe

| Zeitdauer | Beschreibung |
|---|---|
| Registrieren | Die Entität, mit der eine Instanz eines POS-Registers konfiguriert wird. |
| Gerät | Eine Darstellung der physischen Instanz eines POS-Registers und der ihm zugewiesenen modernen-Anwendung. |
| Deditzierte Hardwarestation | Die Geschäftslogik der Hardwarestation, die in den Modern POS für Windows und Modern POS für Android Anwendungen integriert ist. |
| Schubladenkick (d/k) Port | Eine herkömmliche Methode zum Anschließen einer Kassenschublade an einen Belegdrucker. |
| Netzwerkperipheriegeräte | Integrierte Unterstützung für netzwerkfähige Zahlungsterminals, Belegdrucker und Kassenschubladen. |

## <a name="supported-pos-clients-and-devices"></a>Unterstützte POS-Clients und -Geräte

Die in diesem Thema beschriebenen Funktionen werden vom Modern POS für Windows und vom Modern POS für Android POS-Clients unterstützt.

Diese Funktion unterstützt netzwerkfähige Zahlungsterminals und Belegdrucker. Sie können die Kassenschublade unterstützen, indem Sie die Kassenschublade über den d/k-Anschluss an den netzwerkfähigen Belegdrucker anschließen.

Die sofort einsatzbereite Unterstützung für diese Funktionalität wird von [Dynamics 365 Payment Connector für Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3) bereitgestellt. Andere Zahlungsconnectors werden jedoch möglicherweise über das Commerce Software Development Kit (SDK) für Zahlungen unterstützt. Zu den unterstützten Belegdruckern gehören netzwerkfähige Belegdrucker von Star Micronics und Epson.

Verwenden Sie zum Einrichten von Star Micronics-Belegdruckern das Star Micronics-Druckerdienstprogramm, um das Gerät so zu konfigurieren, dass es über das Netzwerk verwendet werden kann. Dieses Dienstprogramm gibt auch die IP-Adresse des Geräts an.

Verwenden Sie zum Einrichten von Epson-Belegdruckern das Dienstprogramm Epson ePOS-Print, um das Gerät für die Verwendung von Netzwerkprotokollen einzurichten.

Weitere Informationen zum Einrichten von Netzwerkperipheriegeräten finden Sie unter [Übersicht über die Unterstützung von Netzwerkperipheriegeräten](./dev-itpro/network-peripherals.md).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Dedizierte Zahlungsterminals und Eingabeaufforderungen für einen Drucker und eine Kassenschublade einrichten

### <a name="set-up-hardware-profiles"></a>Einrichten von Hardwareprofilen

Sie müssen zwei Arten von Hardwareprofilen haben. Der erste ist dem Register zugeordnet. Die zweite wird einer Hardwarestation auf Filialebene zugewiesen und zum logischen Gruppieren von Netzwerkbelegdruckern und Kassenschubladen verwendet.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Richten Sie ein Hardwareprofil für das Register ein

Führen Sie die folgenden Schritte aus, um das dem Register zugewiesene Hardwareprofil einzurichten.

1. In Dynamics 365 Commerce suchen Sie nach **Hardwareprofil**.
2. Wählen Sie **Neu** aus.
3. Weisen Sie eine Hardwareprofilnummer zu und geben Sie eine Beschreibung ein. Dieses Hardwareprofil wird dem Register selbst zugewiesen. Daher wird eine Beschreibung wie **Mit Fallback gewidmet** wird genügen.
4. Richten Sie die Inforegister für verschiedene Gerätetypen die folgenden Gerätetypen ein.

    | Gerät | Typ | Gerätename | Zusätzliche Details |
    |---|---|---|---|
    | Drucker | Netzwerk | *Beliebige* | Der Gerätename berücksichtigt Groß-/Kleinschreibung. Das **Belegprofil-ID** sollte gleich sein wie das **Belegprofil-ID**, das dem Netzwerkdrucker zugeordnet ist, der in dem Hardwareprofil eingerichtet ist, das der Hardwarestation auf Kanalebene zugewiesen ist. |
    | Geldlade | Netzwerk | *Beliebige* | Der Gerätename berücksichtigt Groß-/Kleinschreibung. Legen Sie die Option **Geteilte Schicht verwenden** auf **Ja** fest. |
    | Elektronische Überweisung - Dienst | Adyen | Nicht zutreffend | Informationen darüber, wie der Adyen-Zahlungskonnektor für Onlineshops konfiguriert wird, finden Sie unter [Dynamics 365 Zahlungskonnektor für Ayden](./dev-itpro/adyen-connector.md?tabs=8-1-3). Andere Zahlungsconnectors werden jedoch möglicherweise über das [Commerce Software Development Kit (SDK) für Zahlungen](./dev-itpro/end-to-end-payment-extension.md) unterstützt. |
    | PIN-Feld | Netzwerk | **MicrosoftAdyenDeviceV001** | Keiner. |

5. In Dynamics 365 Commerce nach **Register** suchen.
6. Wählen Sie ein Register aus, indem Sie die Registernummer auswählen, und wählen Sie dann **Bearbeiten**.
7. Weisen Sie das soeben erstellte Hardwareprofil dem Register zu, das ein dediziertes Zahlungsterminal verwenden soll. Das Gerät, das diesem Register zugeordnet ist, muss entweder die Anwendung Modern POS für Windows oder Modern POS für Android Anwendung verwenden.
8. Wählen Sie **Speichern** aus.
9. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Register**, und wählen Sie **IP-Adressen konfigurieren** aus.
10. Auf dem Inforegister **PIN-Pad** geben Sie die IP-Adresse des Zahlungsterminals ein. Informationen zum Abrufen der IP-Adresse des Zahlungsterminals mithilfe des Adyen-Connectors finden Sie unter [Dynamics 365 Payment Connector für Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3).
11. Wählen Sie **Speichern** aus.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Richten Sie ein Hardwareprofil für den Belegdrucker und die Kassenschublade ein

Führen Sie die folgenden Schritte aus, um das Hardwareprofil einzurichten, mit dem der Netzwerkbelegdrucker und die Kassenschublade gruppiert werden.

1. In Dynamics 365 Commerce suchen Sie nach **Hardwareprofil**.
2. Wählen Sie **Neu** aus.
3. Weisen Sie eine Hardwareprofilnummer zu und geben Sie eine Beschreibung ein. Dieses Hardwareprofil wird verwendet, um den Belegdrucker und die Kassenschublade zu gruppieren. Daher wird eine Beschreibung wie **Netzwerkdrucker und Kassenschublade** genügen.
4. Richten Sie die Inforegister für verschiedene Gerätetypen die folgenden Gerätetypen ein.

    | Gerät | Typ | Beschreibung | Zusätzliche Details |
    |---|---|---|---|
    | Drucker | Netzwerk | **Epson** oder **Star** | Der Gerätename berücksichtigt Groß-/Kleinschreibung. Die **Belegprofil-ID** sollte gleich sein wie die **Belegprofil-ID**, die dem Netzwerkdrucker zugeordnet ist, der in dem Hardwareprofil eingerichtet ist, das der Hardwarestation auf Kanalebene zugewiesen ist. |
    | Geldlade | Fallback | **Epson** oder **Star** | Der Gerätename berücksichtigt Groß-/Kleinschreibung. Legen Sie die Option **Geteilte Schicht verwenden** auf **Ja** fest. |

5. Wählen Sie **Speichern** aus.

### <a name="set-up-hardware-stations"></a>Eine Hardwarestation einrichten

Sie müssen zwei Hardwarestationen haben. Dier erste wird dem Register zugeordnet. Die zweite wird nach Bedarf ausgewählt, wenn eine Quittung gedruckt oder eine Kassenschublade geöffnet werden muss.

#### <a name="register-a-hardware-station"></a>Eine Hardwarestation erfassen

1. In Dynamics 365 Commerce suchen Sie nach **Alle Geschäfte**.
2. Wählen Sie ein Geschäft aus, indem Sie dessen Werte auf **ID des Einzelhandelskanals** festlegen und **Bearbeiten** auswählen.
3. Wählen Sie im Inforegister **Hardware-Stationen** die Option **Hinzufügen** aus.
4. Legen Sie das Feld **Hardware-Stationstyp** auf **Dediziert** fest.
5. Geben Sie eine Beschreibung ein, aber legen Sie keine anderen Werte für diese Hardwarestation fest. Diese Hardwarestation wird jederzeit für das Register verwendet. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Richten Sie eine Hardwarestation für den Belegdrucker und die Kassenschublade ein

1. In Dynamics 365 Commerce suchen Sie nach **Alle Geschäfte**.
2. Wählen Sie ein Geschäft aus, indem Sie dessen Werte auf **ID des Einzelhandelskanals** festlegen und **Bearbeiten** auswählen.
3. Wählen Sie im Inforegister **Hardware-Stationen** die Option **Hinzufügen** aus.
4. Legen Sie das Feld **Hardware-Stationstyp** auf **Dediziert** fest.
5. Geben Sie eine Beschreibung ein. Dieses Hardwarestation wird verwendet, um den Belegdrucker und die Kassenschublade zu gruppieren.
6. In dem **Hardwareprofil** wählen Sie im Feld das Hardwareprofil aus, das Sie zuvor für den Belegdrucker und die Kassenschublade erstellt haben.
7. Wählen Sie **Speichern** aus.
8. Während die Hardwarestation für den Belegdrucker und die Kassenschublade noch ausgewählt ist, wählen Sie **Konfigurieren Sie IP-Adressen**.
9. Erhalten Sie die IP-Adresse für den Drucker und geben Sie sie als IP-Adresse sowohl für den Belegdrucker als auch für die Kassenschublade ein.
10. Wählen Sie **Speichern**
11. Suchen nach **Verteilungsplänen**.
12. Wählen Sie den Verteilungszsifplan **1090** und wählen Sie dann **Jetzt ausführen**.
13. Wählen Sie den Verteilungszsifplan **1070** und wählen Sie dann **Jetzt ausführen**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Richten Sie das System so ein, dass Sie bei Bedarf zur Auswahl des Belegdruckers und der Kassenschublade aufgefordert werden

1. Schließen Sie in einem unterstützten POS-Client die aktuelle Schicht, wenn eine Schicht geöffnet ist.
2. Melden Sie sich an und wählen Sie dann **Schubladenbetrieb ohne Schublade**.
3. Verwenden Sie den Betrieb **Verwalten von Hardwarestationen** zum Einschalten einer Hardwarestation.
4. Wählen Sie die Hardwarestation aus, die Sie für das Register erstellt haben, um es zu aktivieren.
5. Melden Sie sich am POS ab und wieder an und öffnen Sie eine Schicht.

Das dem Hardwareprofil zugewiesene Zahlungsterminal ist jetzt immer aktiv und Sie werden gefragt, ob ein Belegdrucker oder eine Kassenschublade erforderlich ist.

Viele Händler, die diese Funktion angefordert haben, sind daran interessiert, Abfall zu reduzieren, indem sie E-Mail-Belege bereitstellen und elektronische Zahlungen fördern. Abhängig von der Konfiguration des POS werden Filialmitarbeiter nur dann aufgefordert, einen Belegdrucker oder eine Kassenschublade auszuwählen, wenn ein Kunde eine physische Quittung wünscht oder mit Bargeld bezahlen möchte.

Filialmitarbeiter werden aufgefordert, eine Hardwarestation nur einmal pro Transaktion auszuwählen, es sei denn, eine Quittung muss gedruckt werden und Bargeld wird zur Zahlung verwendet, aber das ursprünglich ausgewählte Hardwareprofil enthält nicht beide Geräte. In diesem Fall wird der Filialmitarbeiter erneut aufgefordert, eine Hardwarestation auszuwählen, mit der die Transaktion abgeschlossen werden kann.

## <a name="related-articles"></a>Zugehörige Artikel

- [POS Hybrid-App unter Android und iOS einrichten](./dev-itpro/hybridapp.md)
- [Zahlungskonnektor von Dynamics 365 für Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3)
- [Übersicht über die Unterstützung von Netzwerkperipheriegeräten](./dev-itpro/network-peripherals.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
