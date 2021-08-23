---
title: Liveschaltung für Human Resources vorbereiten
description: Diese Seite enthält Anleitungen zur Vorbereitung für eine Liveschaltung mit Dynamics 365 Human Resources.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 196d843ce3ccacc203896439b8c66f168c75bdc945c9b2cd5f9bdd46a2cc3ddd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744893"
---
# <a name="prepare-for-human-resources-go-live"></a>Liveschaltung für Human Resources vorbereiten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie sich darauf vorbereiten, mit Dynamics 365 Human Resources Projekt mit Microsoft Dynamics Lifecycle Services (LCS) live zu gehen. 

Diese Grafik zeigt die Phasen des Liveschaltungsprozesses. 

![Liveschaltungsprozess.](./media/hr-admin-go-live-prepare-process.png)

In der folgenden Tabelle sind alle Schritte des Prozesses, die erwartete Dauer und die für die Aktion verantwortlichen Personen aufgeführt.

| Phase | Vorgang | Dauer/Wann | Wer | Notizen |
| --- | --- | --- | --- |--- |
| 1 | Aktualisieren Sie die Liveschaltung in LCS | Spätestens 2-3 Monate im Voraus | Partner/Kunde | Die Meilensteintermine sollten laufend auf dem neuesten Stand gehalten werden. |
| 2 | Checkliste ausfüllen und senden | Nachdem der Benutzerakzeptanztest (UAT) abgeschlossen ist | Partner/Kunde | Befolgen Sie die Anweisungen in [FastTrack Liveschaltungs-Bewertung](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Projektbewertung (FastTrack) | FastTrack Architect* | Der Architekt liefert nach Erhalt der Checkliste eine Bewertung und setzt die Überprüfung fort, bis die Fragen geklärt sind und gegebenenfalls Abhilfemaßnahmen getroffen wurden. |
| 4 | Projektworkshop (FastTrack) | FastTrack Architect* | |
| 5 | Importieren eines Datenpakets | Kommt auf das Projekt an | Partner/Kunde | Folgen Sie den Anweisungen in [Datenverwaltungsübersicht](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).|
| 6 | Produktion bereit | Nachdem alle vorherigen Schritte abgeschlossen wurden | Partner/Kunde | Partner/Kunde kann die Kontrolle über die Produktionsumgebung übernehmen.|
| 7 | Cutover-Aktivitäten | Kommt auf das Projekt an | Partner/Kunde | |
| 8 | Liveschaltung | Kommt auf das Projekt an | Debitor | |

> [!IMPORTANT]
> *Schritte 3 und 4 werden nur für Kunden ausgeführt, die sich für FastTrack qualifizieren.

## <a name="completing-the-lcs-methodology"></a>Vervollständigung der LCS-Methodik

Ein wichtiger Meilenstein in jedem Implementierungsprojekt ist die Umstellung auf die Produktionsumgebung. Der Vorgang zum Ausführen eines Schritts besteht aus zwei Teilen: 

- Führen Sie die eigentliche Arbeit aus, z. B. eine Anpassungs-Lückenanalyse oder einen Benutzerakzeptanztest (UAT). 
- Markieren Sie den entsprechenden Schritt in der LCS-Methodik als abgeschlossen. 

Es ist eine gute Praxis, die Schritte in der Methodik abzuschließen, während Sie Fortschritte bei der Implementierung machen. Warten Sie nicht bis zur letzten Minute. Es liegt im Interesse des Kunden, eine solide Implementierung zu haben. 

## <a name="uat-for-your-solution"></a>UAT für Ihre Lösung

Während der UAT-Phase müssen Sie alle von Ihnen implementierten Geschäftsprozesse und vorgenommenen Anpassungen in einer Sandbox-Umgebung im Implementierungsprojekt testen. Um eine erfolgreiche Inbetriebnahme sicherzustellen, sollten Sie beim Abschluss der UAT-Phase Folgendes berücksichtigen: 

- Wir empfehlen, dass Ihr UAT-Prozess mit einer sauberen und frischen Umgebung beginnt, in der die Daten aus Ihrer GOLD-Konfiguration vor dem Start des UAT-Prozesses in die Umgebung kopiert werden. Wir empfehlen, dass Sie die Produktionsumgebung bis zur Inbetriebnahme als GOLD-Umgebung verwenden. Ab diesem Zeitpunkt wird die Umgebung zur Produktion.
- Testfälle decken den gesamten Anforderungsumfang ab. 
- Testen Sie mit migrierten Daten. Dazu sollten Daten wie Arbeitskräfte, Stellen und Positionen gehören. Schließen Sie auch Eröffnungssalden wie Urlaubs- und Abwesenheitsrückstellungen ein. Schließen Sie schließlich offene Transaktionen ein, z. B. aktuelle Leistungsregistrierungen. Schließen Sie die Tests mit allen Datentypen ab, auch wenn der Datensatz noch nicht abgeschlossen ist. 
- Testen Sie mit den richtigen Sicherheitsrollen (Standardrollen und benutzerdefinierte Rollen), die Benutzern zugewiesen sind. 
- Stellen Sie sicher, dass die Lösung allen unternehmens- und branchenspezifischen gesetzlichen Anforderungen entspricht. 
- Dokumentieren Sie alle Funktionen und lassen Sie sich vom Kunden genehmigen und abmelden. 

## <a name="mock-go-live"></a>Pseudo-Inbetriebnahme

Vor Ihrer Inbetriebnahme müssen Sie eine Pseudo-Inbetriebnahme durchführen, um die Schritte zu testen, die für die Umstellung von Ihren Altsystemen auf das neue System erforderlich sind. Sie sollten Ihr Pseudo-Inbetriebnahme in einer Sandboxumgebung durchführen und alle Schritte in Ihren Umstellungsplan aufnehmen.

- Wir empfehlen, dass Sie die Produktionsumgebung bis zur Inbetriebnahme als GOLD-Konfigurationsumgebung verwenden.
- Stellen Sie sicher, dass Sie über einen starken Governance-Prozess verfügen, um die Produktionsumgebung vor der Inbetriebnahme vor versehentlichen Transaktionen oder Aktualisierungen zu schützen.
- Wenn Sie bereit sind, UAT oder die Pseudo-Inbetriebnahme durchzuführen, aktualisieren Sie die Sandboxumgebung aus der Produktionsumgebung. Weitere Informationen finden Sie unter [Kopieren einer Instanz](hr-admin-setup-copy-instance.md).
- Testen Sie jeden Schritt Ihres Umstellungsplans in der Sandboxumgebung und validieren Sie dann die Sandboxumgebung, indem Sie Stichproben oder Tests mit Ihren UAT-Skripten in der Umgebung durchführen.
  - Die Tests sollten alle Datenmigrationen umfassen, einschließlich der für die Inbetriebnahme erforderlichen Transformationen.
  - Der Prozess sollte eine Unterbrechung der Praxis aller Legacy-Systeme beinhalten.
  - Stellen Sie sicher, dass alle Schritte der Integrationsumstellung oder externen Systemschritte in Ihrer Pseudo-Umstellung enthalten sind.
- Wenn Sie während der Pseudo-Umstellung Probleme feststellen, ist möglicherweise eine zweite Pseudo-Umstellung erforderlich. Aus diesem Grund empfehlen wir, dass Sie in Ihrem Projektplan zwei Pseudo-Umstellungen einplanen.

## <a name="fasttrack-go-live-assessment"></a>FastTrack Liveschaltungs-Bewertung

Kunden, die für FastTrack qualifiziert sind und mit einem FastTrack Lösungsarchitekt zusammenarbeiten, führen eine Liveschaltungs-Überprüfung mit Microsoft FastTrack durch. Für weitere Informationen siehe [Microsoft FastTrack](/dynamics365/fasttrack/). 

Ungefähr acht Wochen vor der Inbetriebnahme werden Sie vom FastTrack-Team gebeten, eine [Liveschaltungs-Checkliste](https://go.microsoft.com/fwlink/?linkid=2146013) auszufüllen.

Der Projektmanager oder ein wichtiges Projektmitglied muss die Liveschaltungs-Checkliste während der Phase vor der Liveschaltung des Projekts ausfüllen. In der Regel wird die Checkliste vier bis sechs Wochen vor dem vorgeschlagenen Liveschaltungsdatum ausgefüllt, wenn die UAT abgeschlossen oder fast abgeschlossen ist. 

Wenn Sie die Liveschaltungs-Checkliste ausgefüllt haben, senden Sie sie per E-Mail an Ihren FastTrack Lösungsarchitekt. Fügen Sie der E-Mail immer einen wichtigen Stakeholder des Kunden und des Implementierungspartners hinzu. 

Nachdem Sie die Checkliste eingereicht haben, überprüft Ihr FastTrack Lösungsarchitekt das Projekt und erstellt eine Bewertung, in der die potenziellen Risiken, Best Practices und Empfehlungen für eine erfolgreiche Inbetriebnahme des Projekts beschrieben werden. In einigen Fällen kann der Lösungsarchitekt Risikofaktoren hervorheben und einen Minderungsplan anfordern. 

## <a name="see-also"></a>Siehe auch

[FAQ live schalten](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
