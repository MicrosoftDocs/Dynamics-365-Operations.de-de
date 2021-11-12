---
title: Auftragssuche für Gast-Checkouts aktivieren
description: In diesem Thema wird beschrieben, wie Sie die Bestellsuche für Gastbezahlvorgänge in Microsoft Dynamics 365 Commerce aktivieren.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 639ee670b83198423425d03dad308306c9eed25c
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674975"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Auftragssuche für Gast-Checkouts aktivieren

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die Bestellsuche für Gastbezahlvorgänge in Microsoft Dynamics 365 Commerce aktivieren.

Mit der Funktion zum Nachschlagen von Bestellungen für Gastbezahlvorgängen können Kunden, die als Gastbenutzer Einkäufe tätigen, ihre Bestellungen nachschlagen. Die Funktion zum Nachschlagen von Bestellungen ist nützlich, wenn Kunden Aktionen wie das Überprüfen des Erfüllungsstatus von Produkten einer Bestellung, die Überprüfung der Lieferadresse einer Bestellung, die Nachbestellung eines Produkts oder die Bestätigung des Geschäfts, in dem eine Bestellung abgeholt wird, durchführen möchten.

Kunden, die als registrierte Benutzer Bestellungen aufgeben, können ihre Bestelldetails sehen, wenn sie eingeloggt sind, aber Kunden, die den Gastbezahlvorgang zum Aufgeben von Bestellungen verwenden, können dies nicht. Wenn jedoch die Funktion zur Bestellsuche für Gastbezahlvorgänge aktiviert ist, wird ein Formular bereitgestellt, mit dem Kunden nach Bestellungen suchen können, die sie als Gäste aufgegeben haben. In diesem Formular geben Kunden die Bestellbestätigungs-ID und (optional) die E-Mail-Adresse ein, die sie an der Kasse angegeben haben.

Darüber hinaus kann in jede auftragsbezogene Transaktions-E-Mail ein Link oder eine Schaltfläche eingefügt werden, die den Kunden direkt zur Bestelldetailseite für seine Bestellung führt. Dieser Link oder diese Schaltfläche funktioniert für Bestellungen, die sowohl von registrierten Benutzern als auch von Gastbenutzern aufgegeben werden.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Aktivieren Sie die erforderlichen Funktionen in der Commerce-Zentrale

Um die Bestellsuche für Gastbezahlvorgänge zu aktivieren, müssen Sie die folgenden Funktionen unter **Arbeitsbereiche \> Funktionsverwaltung** in der Commerce-Zentrale aktivieren.

| Funktion | Kostenträger |
|---------|---------|
| Retail-Funktion zur Einbeziehung von Auftragsdetails in die anonyme Benutzersuche | Diese Funktion macht die Benutzeroberfläche in Commerce-Parametern verfügbar, mit der Sie die API für Bestellsuche für nicht authentifizierte Benutzer aktivieren und konfigurieren können, wie personenbezogene Daten angezeigt werden. |
| Generierung einer stärkeren Kanalreferenzkennung aktivieren | Diese Funktion generiert eine sicherere 12-stellige Kanalreferenz-ID (Bestellbestätigungs-ID), die beim Nachschlagen einer Bestellung in der Abfragezeichenfolge übergeben werden kann. |
| Konsistentes Format für die Kanalreferenz-ID in allen Kanälen generieren | Diese Funktion generiert eine sichere Kanalreferenz-ID für Bestellungen, die über eine E-Commerce-Site, die Einzelhandelsverkaufsstelle (POS) oder ein Callcenter aufgegeben werden. Bevor Sie diese Funktion aktivieren können, muss die **Generierung einer stärkeren Kanalreferenz-ID aktivieren**-Funktion aktiviert sein. |

Nach dem Einschalten der **Funktion für anonyme Benutzersuchauftragsdetails im Einzelhandel**-Funktion müssen Sie die API aktivieren, die die Suche nicht authentifizierte Aufträge in der Commerce-Zentrale unterstützt. Gehen Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Kundenbestellungen**. Stellen Sie auf der **Kundenbestellungen**-Seite, auf dem **Auftragssuche**-Inforegister die **Nicht authentifizierte Auftragssuche aktivieren**-Option auf **Ja** ein, wie in der folgenden Abbildung gezeigt.

## <a name="manage-the-display-of-personal-data"></a>Verwalten der Anzeige personenbezogener Daten

Das **Auftragssuche**-Inforegister auf der **Kundenbestellungen**-Seite in der Commerce-Zentrale enthält ein Feld **Personenbezogene Daten in Gastbestellungssuche einfügen**, mit dem Sie steuern können, ob Kunden personenbezogene Daten angezeigt werden. Zu diesen personenbezogenen Daten gehören die Lieferadresse des Kunden und die letzten vier Ziffern der Kreditkartennummer des Kunden. Standardmäßig werden Kunden keine personenbezogenen Daten angezeigt, wenn die Suche für nicht authentifizierte Bestellungen aktiviert ist. In der folgenden Tabelle werden die verfügbaren Optionen beschrieben.

| Option | Ergebnis |
|--------|--------|
| Nie | Der Standardwert. Bei der Auftragssuche werden keine personenbezogenen Daten angezeigt. Wenn registrierte Benutzer, die eingeloggt sind, eine Bestellung aufrufen, die sie erstellt haben, während sie eingeloggt waren, können sie ihre persönlichen Daten sehen. |
| Nur Gastaufträge | Personenbezogene Daten werden bei der Bestellsuche für Bestellungen angezeigt, die Kunden als Gäste erstellt haben. Wenn eine Bestellung von einem registrierten Benutzer erstellt wurde, muss sich dieser Benutzer anmelden, um seine persönlichen Daten zu sehen. |
| Alle Aufträge | Bei allen Auftragssuchen werden personenbezogenen Daten angezeigt. |

> [!NOTE]
> Diese Optionen legen fest, wann anonymen Gastnutzern personenbezogene Daten wie die Adresse des Kunden und die letzten vier Ziffern der Kreditkartennummer des Kunden angezeigt werden. Um die Privatsphäre registrierter Kunden zu schützen, empfehlen wir Ihnen, die **Nur Gastbestellungen**-Option. Die sicherste Option ist jedoch **Niemals**.

Nachdem Sie den Wert des Felds **Personenbezogene Daten in die Suche nach Gastbestellungen einfügen** geändert haben, müssen Sie den Job 1070 (**Kanalkonfiguration**) in der Commerce-Zentrale ausführen, indem Sie zu **Retail und Commerce \> Retail und Commerce IT \> Verteilungsplan** ausführen.

## <a name="configure-the-order-lookup-module"></a>Das Auftragssuchmodul konfigurieren

Das Modell zur Bestellsuche in der Commerce-Modulbibliothek wird verwendet, um das Formular zu rendern, das Gastbenutzer zur Auftragssuche verwenden. Das Modul zur Auftragssuche kann in den Text-Slot jeder Seite eingefügt werden, für die keine Kundenanmeldung erforderlich ist. Informationen zur Konfiguration des Moduls finden Sie unter [Auftragssuchmodul](order-lookup-module.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Auftragssuchmodul](order-lookup-module.md)

[E-Mail-Benachrichtigungsprofil einrichten](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
