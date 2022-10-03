---
title: Proaktive Qualitätsupdates
description: Dieser Artikel enthält Informationen zur proaktiven Bereitstellung von Qualitätsupdates.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c2d26b7c5e110d05806c064e15a3ad2af34d0fbd
ms.sourcegitcommit: fde2867524b6a851628185cbdeee60a6ad918d08
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2022
ms.locfileid: "9592045"
---
# <a name="proactive-quality-updates"></a>Proaktive Qualitätsupdates

[!include[banner](../includes/banner.md)]

In den letzten Jahren hat Microsoft kontinuierliche Fortschritte bei dem gemacht, was wir als [One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md) bezeichnen. Die Prämisse von One Version ist einfach: Je näher wir dem Ziel kommen, dass alle Kunden die gleiche Softwareversion zu haben, desto höher ist die Qualität, die wir liefern können. Wir finden und beheben Probleme einmal und geben diese Lösungen schneller an mehr Kunden weiter.

Die Ergebnisse bestätigen diese Prämisse: geringere Vorfallzahlen bei unseren Produkten. Wenn Kunden nicht dieselbe Version verwenden, stellen wir regelmäßig fest, dass sie Problemen haben, für die bereits eine Lösung vorliegt. Wir haben bereits große Fortschritte mit Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations und Dynamics 365 Commerce gemacht und dank der jüngsten technischen Fortschritte ist es jetzt möglich, den nächsten Schritt zu tun. Die folgenden Informationen beschreiben, was wir tun werden, was wir bereits getan haben, um die Voraussetzungen zu schaffen, und wie und wann wir die neuen Funktionen störungsfrei einführen werden.

## <a name="focus-on-quality-updates"></a>Schwerpunkt Qualitätsupdates

Wir bieten derzeit pro Jahr sieben [Dienstupdates](public-preview-releases.md) an. Version 10.0.29 ist zum Beispiel ein Dienstupdate. Bis vor Kurzem gab es acht Updates pro Jahr. Wir haben jedoch ein Update abgeschafft, da Kundenfeedback nahelegte, dass unsere Kunden Änderungen gegen Ende des Kalenderjahres lieber vermeiden möchten.

Wir werden die Intervalle der Dienstupdates nicht ändern. Stattdessen konzentrieren wir uns bei unserem nächsten Schritt auf dem Weg zu One Vision auf *Qualitätsupdates*. Qualitätsupdates sind kumulative Builds von Hotfixes. Sie enthalten keine neuen Funktionen. Unsere gesamte Kunden-Community ist zu jedem Zeitpunkt auf die drei oder vier neuesten Dienstupdates verteilt. Es kann jedoch ein, dass innerhalb der Gruppe für ein bestimmtes Dienstupdate Dutzende verschiedener Qualitätsupdateversionen verwendet werden, je nach den Daten, an denen die Personen bereitgestellt wurden. Im nächsten Schritt werden wir Qualitätsupdates proaktiv bereitstellen. Wir verwenden dieses Modell bereits für unsere Dataverse-basierten Anwendungen und konnten die erwarteten Ergebnisse im Hinblick auf verbesserte Qualität und weniger Supportfälle erreichen.

Natürlich könnte eine Reduzierung von Fehlern die Notwendigkeit von Qualitätsupdates verringern oder vollständig eliminieren. Es laufen mehrere Initiativen, um die Fehler zu reduzieren, für die Qualitätsupdates notwendig sind. Selbst wenn die Nutzlasten im Qualitätsupdate reduziert werden, verbessert die Konsistenz im gesamten Kundenstamm die Supportfähigkeit, bringt Kunden schneller Verbesserungen und verringert die Häufigkeit, mit der Kunden auf Probleme stoßen, für die bereits Lösungen vorliegen.

## <a name="making-proactive-distribution-possible"></a>Proaktive Bereitstellung möglich machen

Es wurden bereits mehrere Fortschritte umgesetzt, die eine proaktive Bereitstellung von Qualitätsupdates ermöglichen:

- **Aktualisierung nahezu ohne Downtime**: Um häufigere Umgebungen zu fördern, ist es wichtig, dass die Auswirkungen auf die Verfügbarkeit der Umgebung reduziert werden, um Vereinbarungen zum Servicelevel (SLAs) für Dynamics 365 aufrechtzuerhalten. Die Aktualisierung nahezu ohne Downtime wurde ursprünglich eingeführt, um das monatliche Betriebssystem-Patching zu verbessern, indem ein Cluster-Failover verwendet wird, um das aktualisierte Image mit minimaler Unterbrechung zu aktivieren. Der Mechanismus zum Anwenden von Updates wird verbessert, sodass er noch weniger störend ist, und er deckt dann sowohl das Betriebssystem-Patching als auch die Bereitstellung hochwertiger Updates ab.

    Bei interaktiven Benutzern wird eine aktive Sitzung möglicherweise unterbrochen, und die Wiederholung erfolgt in der jetzt aktualisierten Umgebung. Mit der Einführung von [prioritätsbasierten Stapelplanung](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), das jetzt auf Opt-in-Basis verfügbar ist, wird die Stapelplanung und -verarbeitung sofort nach dem Update wiederhergestellt und fortgesetzt. Für Kunden wird eine prioritätsbasierte Stapelplanung eingerichtet, bevor sie an der proaktiven Verteilung von Qualitätsupdates für ihre Produktionsumgebungen teilnehmen.

- **Nutzungsschwache Zeiten**: Nutzungsschwache Zeiten sind für jede Azure-Region festgelegt und während der Dark Hour-Periode werden Aktualisierungen nahezu ohne Downtime werden in diesem Zeitraum durchgeführt.

## <a name="the-proactive-update-process"></a>Der proaktive Updateprozess

Die Bereitstellung proaktiver Qualitätsupdates folgt einem sicheren Bereitstellungsprozess (SDP). Die Besonderheiten des SDP werden sich weiterentwickeln, aber Qualitätsupdates werden zunächst in Sandbox-Umgebungen bereitgestellt. Der Prozess beginnt mit Umgebungen, die sich für eine frühe Bereitstellung entscheiden. Wenn der Prozentsatz der erfolgreich bereitgestellten Sandboxes zunimmt, beginnt die Bereitstellung in Produktionsumgebungen. Noch einmal: Der Prozess beginnt mit Umgebungen, die sich bewusst für eine frühe Bereitstellung entscheiden. Überwachungssysteme überwachen Systemtelemetrie- und Live-Website-Vorfälle und stoppen die Einführung einer bestimmten Version, wenn eine Regression erkannt wird. Kunden können die Qualitätsupdates weiterhin vor der proaktiven Bereitstellung abrufen, wenn sie dies wünschen.

Aktuelle Versionsverwaltungsdaten zeigen, dass weniger als 3 Prozent der Regressionen in Qualitätsupdates eingeführt werden. Mit einem verstärkten Fokus auf die Eliminierung von Regressionen und einem verbesserten SDP werden die potenziellen Auswirkungen von Regressionen erheblich geringer sein als die Gewinne bei der Qualität, die durch eine schnellere Bereitstellung von Fixes für Kunden auf breiter Basis erzielt werden.

## <a name="process-changes"></a>Änderungen verarbeiten

Vor der Aktivierung der proaktiven Bereitstellung von Qualitätsupdates wird eine Reihe von Prozessänderungen implementiert:

- **Schema**: Tools stellen sicher, dass hochwertige Update-Builds nur Schemaänderungen enthalten, die angewendet werden können, während der Dienst online ist. Dieser Ansatz trägt dazu bei, die Möglichkeit zu bewahren, das Update nahezu ohne Ausfallzeit anzuwenden.
- **Verstärkte Änderungsprüfung**: Derzeit gibt es bereits einen zusätzlichen Prozessschritt, um Änderungen für die Aufnahme in ein Qualitätsupdate zu genehmigen. Die Prüfung im zusätzlichen Schritt wird verstärkt, um das Potenzial für Regressionen zu verringern. Breaking Changes sind in Qualitätsupdates nicht zulässig, und die verstärkte Änderungsprüfung wird dazu beitragen, dass wir dieses Ziel erreichen.
- **Sichtbarkeit**: Wir senden Benachrichtigungen für bevorstehende proaktive Qualitätsupdates per E-Mail und Lifecycle Services (LCS). Darüber hinaus haben Supportteams und Vorfallleiter Einblick darin, wo Qualitätsupdates proaktiv bereitgestellt wurden.
- **Fail Safe via Flighting** - Flighting wird verwendet, um Codeänderungen zu schützen, wo immer dies in einem Qualitätsupdate-Fehlerbehebung möglich ist, oder die bestehende Funktion Flighting zu verwenden, die für die Korrektur relevant ist. Wenn nach einer proaktiven Bereitstellung ein Fallback oder das Ausschalten einer Änderung erforderlich ist, kann dies über das Flighting-System erfolgen, um weitere Fehler zu vermeiden.
- **Sandbox-Synchronisierungsbezeichnung**: Weniger als 20 Prozent der Kunden haben heute mehrere Sandboxes und halten eine Sandbox bereit, in der die Version mit der Produktion übereinstimmt, um bei der Fehlerbehebung zu helfen. Wenn ein Kunde eine Sandbox verwendet, um eine neuere Version als seine Produktion zu testen, erhält diese Sandbox Qualitätsupdates für die neuere Version.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Wie sieht die Rollout-Roadmap für Qualitätsupdates aus?

Die Verteilung von proaktiven Qualitätsupdates für Sandbox-Umgebungen beginnt voraussichtlich Ende September oder Oktober 2022 für Azure Public Cloud-Kunden. Testumgebungen erhalten ab diesem Zeitpunkt auch eine proaktive Updatebereitstellung. Im September wird eine Benachrichtigung an alle Kunden gesendet, um sie über den erwarteten Zeitplan für seine Umgebungen zu informieren. Ausnahmen vom proaktiv aktualisierten Bereitstellungsprozess sind nur für FDA-regulierte Kunden zulässig. Wir arbeiten noch daran, wie regulierte Umgebungen und staatliche Cloud-Kunden verwaltet werden sollen.

In den Nächsten sechs Monaten steigern wir schrittweise den Prozentsatz der Sandbox-Umgebungen, die proaktive Updates erhalten, bis alle designierten Umgebungen enthalten sind, und fahren dann mit der Aktualisierung von Produktionsumgebungen fort. Wir überwachen den gesamten Zeitraum, um sicherzustellen, dass der Bereitstellungsprozess nahtlos verläuft und wir unser Ziel von unterbrechungsfreien Nutzlasten erreichen.

Da Kunden regelmäßig kleinere Nutzlasten erhalten, erwarten wir, dass es einfacher wird, auf dem Laufenden zu bleiben. Wir werden die Häufigkeit der Update-Bereitstellung anpassen, wenn wir den Prozess nachweislich ohne Unterbrechung ausführen können. Dieser Prozess funktioniert für unsere Dataverse-Plattform und -Anwendungen bereits effektiv und liefert die erwarteten Verbesserungen der Servicequalität. Wir möchten den gleichen Schritt nach vorne unbedingt auch für Finanz- und Betriebsanwendungen machen.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Wann beginnen Qualitätsupdates für Produktionsumgebungen?
Derzeit zielen Qualitätsupdates nur auf Sandboxes ab. Wir werden diesen Bereich mit einem Startdatum für Produktionsumgebungen aktualisieren, sobald wir konkretere Daten und Metriken von proaktiven Updates für Sandboxen haben, um die Bereitschaft für Prod.

## <a name="what-is-the-schedule-for-sandbox-quality-updates"></a>Wie sieht der Zeitplan für die Aktualisierung der Sandkastenqualität aus?
Informationen zu den nutzungsschwachen Zeiten für jede Region finden Sie unter [Wie sieht der Zeitplan für proaktive Qualitätsaktualisierungen aus?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-is-the-schedule-for-proactive-quality-updates).

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Wie werden die dunklen Stunden für Kunden gehandhabt, die über eine Finanz- und Betriebs-App-Instanz verfügen, aber in mehreren Zeitzonen aktiv sind? 
Es gibt keine speziellen Zeitpläne außerhalb der nutzungsschwachen Zeiten, in denen eine Instanz von Finanz- und Betriebs-Apps vorhanden ist, da wir planen, Qualitätsupdates auf minimal störende Weise mit [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean) einzuführen.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Wie stellt Microsoft die Qualität dieser Updates sicher?
Microsoft ist bestrebt, die Release-Pipeline effizient genug zu halten, um kleine Nutzlasten bereitzustellen, um die Validierungskosten niedrig zu halten. Jeder Fix in einem Qualitätsupdate durchläuft einen strengen und sicheren Bereitstellungsprozess, der dazu beiträgt, die Qualität und Zuverlässigkeit zu verbessern und dadurch die Auswirkungen auf den Kunden zu reduzieren. Die Bereitstellung erfolgt schrittweise zuerst in Sandbox-Umgebungen, gefolgt von der Produktion. Gestaffelte Bereitstellungen ermöglichen eine ordnungsgemäße Überwachung, um festzustellen, ob eine weitere Bereitstellung sicher ist. Wir stoppen die Einführung, wenn Probleme bei jeder bereitgestellten Kundengruppe festgestellt werden, und stellen sicher, dass jeder Schritt der Einführung genügend Zeit hat, damit Probleme auftauchen. Für jedes anstehende Qualitätsupdate bieten wir durch Aktualisierungen der öffentlichen Dokumentation und E-Mails Einblick in den Zeitplan, damit Kunden vorausplanen können.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Können Kunden ein Qualitätsupdate verzögern, verschieben oder anhalten?
Nein Das Hauptziel von Qualitätsupdates besteht darin, sicherzustellen, dass sich Grundlagen wie Sicherheit, Datenschutz, Zuverlässigkeit, Verfügbarkeit und Leistung für unsere Kunden kontinuierlich verbessern. Durch das Verzögern oder Anhalten eines Updates werden Sicherheit, Verfügbarkeit und Zuverlässigkeit gefährdet.

## <a name="how-can-one-know-the-set-of-changes-that-went-into-a-quality-update-payload"></a>Wie kann man den Satz von Änderungen erkennen, die in eine Qualitätsupdate-Nutzlast eingeflossen sind?
Sie können alle KB-Artikel in einem Qualitätsupdate-Build auf der Seite **Umgebungsdetails** in LCS einsehen, indem Sie zum Abschnitt **Qualitätsupdate** navigieren. 

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Wie ist der Prozess, wenn nach einem Qualitätsupdate ein kritisches Problem gefunden wird?
Ein kritisches Problem oder eine Regression sind ein oder mehrere Ereignisse, die normalerweise dazu führen, dass mehrere Kunden eine verschlechterte Erfahrung mit einem oder mehreren unserer Dienste haben. Diese Probleme können zu ungeplanten Ausfallzeiten führen, einschließlich Nichtverfügbarkeit, Leistungseinbußen und Störungen des Dienstmanagements. Wenn es aufgrund solcher Regressionen zu einer breiten Kundenauswirkung kommt, stoppen wir die Einführung eines Qualitätsupdates, bis wir das Problem kommunizieren und beheben können. In der Regel enthält das nächste Qualitätsupdate die erforderliche Korrektur, um die Einführung fortzusetzen.

Wenn eine einzelne Kundenumgebung betroffen ist, wenden Sie sich an den Microsoft-Support, um ein Ticket zu eröffnen. Basierend auf der Begründung werden wir die Einführung des Qualitätsupdates in allen anderen Umgebungen in diesem Projekt stoppen, bis das Problem behoben ist.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Können Kunden weiterhin manuell Hotfix-Updates von LCS anwenden?
Ja. Um sicherzustellen, dass Hotfixes dauerhaft gleich funktionieren, können Hotfix-Updates weiterhin auf Kundenumgebungen in LCS angewendet werden. Es ist jedoch wichtig zu beachten, dass Hotfixes, die als Teil eines Qualitätsupdates bereitgestellt werden, den Standard-SDP durchlaufen, bevor das Update bereitgestellt wird. Dadurch wird das Risiko von Regressionen aufgrund höherer Qualität reduziert. Wir empfehlen, dass Sie sich für eine Qualitätsaktualisierung entscheiden, anstatt Hotfixes manuell anzuwenden, um die Zuverlässigkeit zu erhöhen.

## <a name="can-customers-self-install-a-quality-update-build-by-themselves-ahead-of-the-schedule"></a>Können Kunden ein selbst erstelltes Qualitätsupdate vor dem Zeitplan selbst installieren?
Ja. Sie können ein Qualitätsupdate proaktiv installieren. Microsoft überspringt das Update, wenn die aktuelle Build-Version der Umgebung gleich oder höher als das betreffende Qualitätsupdate ist.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Wenn für eine Umgebung innerhalb einer Woche ein geplantes monatliches Service-Update ansteht, erhält sie dann immer noch Qualitätsupdates?
- Qualitätsupdates werden nicht angewendet, wenn ein bevorstehendes Dienstupdate innerhalb einer Woche nach dem geplanten Zeitpunkt des Qualitätsupdates geplant ist.
- Wenn eine Sandbox-Umgebung dieselbe oder eine höhere Build-Version als das bevorstehende Qualitätsupdate hat, wird sie übersprungen.
- Wenn eine Produktionsumgebung dieselbe oder eine höhere Build-Version als das bevorstehende Qualitätsupdate hat, wird sie übersprungen.
- Wenn eine Sandbox aufgrund eines Qualitätsupdates oder eines manuellen Updates für die Produktion die gleiche oder eine höhere Build-Version hat, erhält die Produktion dennoch die geplante Version des monatlichen Dienstupdates. Wenn Sie nicht möchten, dass die geplante Produktionsumgebung auf die Dienstaktualisierungsversion aktualisiert wird, können Sie die Dienstaktualisierung von LCS aus anhalten. 
- Wir empfehlen, dass Sie den neuesten Qualitätsupdate-Build verwenden, um Ihre Änderungen für ein bevorstehendes Service-Update für bessere Stabilität und Ergebnisse zu testen.

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Kann eine Umgebung in ihren vorherigen Zustand zurückversetzt werden, wenn es Probleme gibt, nachdem ein Qualitätsupdate angewendet wurde?
Nachdem ein Qualitätsupdate angewendet wurde, gibt es unter keinen Umständen ein Rollback. Es sind nur Patch-Forward-Optionen verfügbar, um Probleme zu mindern.

## <a name="what-about-fda-regulation-and-gpx"></a>Was ist mit der FDA-Verordnung und GPX?
Der Plan für Kunden, die der FDA-Validierung und -Regulierung unterliegen, befindet sich noch in der Entwicklung. Erwarten Sie bald weitere Updates in diesem Bereich. Vorerst sind alle diese Kunden von Qualitätsaktualisierungen ausgenommen.

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Welche Versionen von Dienstupdates werden für diese Qualitätsupdates unterstützt?
Kunden mit niedrigeren Versionen als N-2 erhalten keine Qualitätsupdates. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Die Bereitstellung von Finanz- und Betriebs-Apps mit Einzelhandelskomponenten erfordert neben der erneuten Bereitstellung von MPOS in der Regel zusätzliche Arbeit. Wie wirken sich diese Qualitätsupdates auf das RetailSDK aus? 
Da sich die Art der Hotfixes selbst in der Nutzlast der Qualitätsupdates nicht ändert, erwarten wir derzeit keine zusätzlichen Auswirkungen, die sich speziell auf Einzelhandelskomponenten beziehen.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che-"></a>Gibt es Auswirkungen auf Cloud Hosted Environments (CHE)? ? 
Nein

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Gibt es Integrationsprobleme mit Microsoft Dataverse? 
Nein

