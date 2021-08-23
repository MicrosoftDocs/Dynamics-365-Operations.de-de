---
title: Sysemdiagnose für POS-Peripheriegeräte und -Dienste
description: Dieses Thema bietet einen Überblick über den Systemdiagnose-Vorgang am Point of Sale (POS).
author: rubendel
ms.date: 03/06/2020
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
ms.openlocfilehash: 89f926af540ff7c7a57824419edb295ab3b78ee8b22684cb14a0ab6f3436bb01
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715381"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>Sysemdiagnose für POS-Peripheriegeräte und -Dienste

[!include [banner](includes/banner.md)]

Dieses Thema gibt einen Überblick über den Systemdiagnose-Vorgang am Point of Sale (POS).

## <a name="overview"></a>Übersicht

Einzelhandelsgeschäfte können komplexe Umgebungen sein, in denen viele Anwendungen und Geräte verwendet werden. Wenn der Betrieb wächst, kann es schwierig werden, sicherzustellen, dass der Betrieb immer reibungslos läuft, da beispielsweise Abhängigkeiten von Peripheriegeräten auftreten, die im Laufe eines Tages ausfallen oder versehentlich vom Stromnetz getrennt werden können. Die Fehlerbehebung bei Problemen im Zusammenhang mit Geräten und Diensten kann für größere Händler kostspielig und für kleinere Betriebe gleichermaßen frustrierend sein.

Microsoft Dynamics 365 Commerce Versionen 10.0.10 und höher enthalten eine Integritätsprüfung, mit der einige dieser Kosten und Frustrationen vermieden werden können. Diese Operation bietet eine Methode zum Testen von Geräten direkt vom POS außerhalb des normalen Betriebs. Daher kann es Einzelhändlern helfen, Probleme zu erkennen, bevor sie auftreten.

## <a name="key-terms"></a>Schlüsselbegriffe

| Zeitdauer | Beschreibung |
|---|---|
| Peripheriegerät | Jedes Gerät, mit dem die POS-Anwendung Transaktionen und andere Vorgänge im Geschäft erleichtert. Beispiele hierfür sind Kassenschubladen, Barcodescanner und Zahlungsterminals. |
| Service | In diesem Thema ist ein Dienst eine Zusatzanwendung, von der die POS-Anwendung abhängt, um Transaktionen und tägliche Vorgänge auszuführen. Beispiele hierfür sind Apps, die bei Steuer- oder Versandberechnungen helfen. |

## <a name="health-check-operation"></a>Systemdiagnoseprüfung

Die Systemdiagnoseprüfung ist die Prüfung 717 auf der Seite **POS-Betrieb** in der Handelszentrale. Es kann verwendet werden, während sich der POS im Nicht-Schubladen-Modus befindet. Eine Hardwarestation muss aber aktiv sein.

Standardmäßig testet die Integritätsprüfung nur Geräte, die im Hardwareprofil für die Hardwarestation konfiguriert sind, die derzeit für ein Register aktiv ist. Wenn ein Register im Laufe eines Tages mehrere Hardwarestationen verwendet, um Integritätsprüfungen für alle durchzuführen, muss es jeweils eine Verbindung zu einer Hardwarestation herstellen. Es gibt keine Integritätsprüfung auf Filialebene. Es ist jedoch möglich, dass diese Art der Überprüfung über die Commerce Server-Erweiterbarkeit durchgeführt werden kann.

### <a name="out-of-box-health-checks"></a>Out-of-Box-Integritätsprüfungen

| Typ | Verbindung | Detaildaten |
|---|---|---|
| Drucker | OPOS | Diese Prüfung testet die grundlegende Objektverknüpfung und -einbettung für POS-Funktionen (OPOS). Im Folgenden finden Sie einige Beispiele hierfür:<ul><li>Öffnen: **Öffnen** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Schließen: **DeviceEnabled = False** &gt; **ReleaseDevice** &gt; **Schließen**</li></ul> |
| Zeilenanzeige | OPOS | Diese Prüfung testet grundlegende OPOS-Funktionen. Im Folgenden finden Sie einige Beispiele hierfür:<ul><li>Öffnen: **Öffnen** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Schließen: **DeviceEnabled = False** &gt; **ReleaseDevice** &gt; **Schließen**</li></ul> |
| Duale Anzeige | Windows | Diese Überprüfung stellt sicher, dass das Betriebssystem eine zweite Windows-Anzeige erkennt. | 
| MSR | OPOS | Diese Prüfung testet grundlegende OPOS-Funktionen. Im Folgenden finden Sie einige Beispiele hierfür:<ul><li>Öffnen: **Öffnen** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Schließen: **DeviceEnabled = False** &gt; **ReleaseDevice** &gt; **Schließen**</li></ul> |
| Aussteller | OPOS | Diese Prüfung testet grundlegende OPOS-Funktionen. Im Folgenden finden Sie einige Beispiele hierfür:<ul><li>Öffnen: **Öffnen** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Schließen: **DeviceEnabled = False** &gt; **ReleaseDevice** &gt; **Schließen**</li></ul> | 
| Scanner | OPOS | Diese Prüfung testet grundlegende OPOS-Funktionen. Im Folgenden finden Sie einige Beispiele hierfür:<ul><li>Öffnen: **Öffnen** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Schließen: **DeviceEnabled = False** &gt; **ReleaseDevice** &gt; **Schließen**</li></ul> | 
| Skalieren | OPOS | Diese Prüfung testet grundlegende OPOS-Funktionen. Im Folgenden finden Sie einige Beispiele hierfür:<ul><li>Öffnen: **Öffnen** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Schließen: **DeviceEnabled = False** &gt; **ReleaseDevice** &gt; **Schließen**</li></ul> |
| PIN-Feld | OPOS | Diese Prüfung testet grundlegende OPOS-Funktionen. Im Folgenden finden Sie einige Beispiele hierfür:<ul><li>Öffnen: **Öffnen** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Schließen: **DeviceEnabled = False** &gt; **ReleaseDevice** &gt; **Schließen**</li></ul> |
| Zahlungsterminal | SDK zu Zahlungen | Diese Prüfung testet die grundlegenden Funktionen des Zahlungsterminals, die vom Zahlungs-SDK bereitgestellt werden. <ul><li>Sperren</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>Abschluss</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>Verwenden der Integritätsprüfung am POS

Wenn die Integritätsprüfung am POS gestartet wird, werden in einem Bereich rechts die konfigurierten Geräte aufgelistet und der Status jedes Geräts angezeigt. Um eine Integritätsprüfung für ein einzelnes Gerät durchzuführen, wählen Sie das Gerät aus und wählen Sie dann **Test ausgewählt**. Um eine Integritätsprüfung für alle Geräte durchzuführen, wählen Sie **Alle testen**. Die Funktion **Alle testen** testet alle Geräte einzeln und aktualisiert den Status jedes Geräts in der Säule **Status**.

Die Spalte **Letzte Überprüfung** zeig an, wann die Integritätsprüfung für jedes Gerät zuletzt durchgeführt wurde.

Wenn die Integritätsprüfung für ein Gerät bestanden wurde (d.h wenn keine Fehler aufgetreten sind), lautet der Status des Geräts **in Ordnung**. Wenn die Integritätsprüfung fehlschlägt, zeigt der Status an, dass ein Fehler aufgetreten ist. In diesem Fall enthält der rechte Bereich Details, die sich auf den Fehler beziehen, oder weist den Benutzer an, sich an den Systemadministrator zu wenden.

Einige Geräte, wie z. B. die OPOS-Tastensperre, verfügen nicht über sofort einsatzbereite Integritätsprüfungen. Wenn für ein verwendetes Gerät kein Integritätsprüfungstest erkannt wird, lautet der Status **Nicht unterstützt**.

### <a name="extending-health-checks"></a>Integritätsprüfung erweitern

Die sofort einsatzbereiten Integritätsprüfungen sind so konfiguriert, dass sie einige benutzerfreundliche Meldungen für typische Fehler enthalten. Es werden jedoch nicht alle Szenarien behandelt. Durch die Erweiterbarkeit können Händler benutzerfreundliche Nachrichten Fehlern zuordnen, die möglicherweise spezifisch für ihre Umgebung sind.

Benutzerdefinierte Integritätsprüfungen können auch erstellt werden, um Geräte zu testen, die nicht sofort unterstützt werden, oder um Dienste zu testen, von denen der POS abhängt.

## <a name="related-articles"></a>Zugehörige Artikel

[Modern POS (MPOS) – Auslöser und Drucken](dev-itpro/pos-trigger-printing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]