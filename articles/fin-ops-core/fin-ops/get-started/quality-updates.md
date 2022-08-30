---
title: Proaktive Qualitätsupdates
description: Dieser Artikel enthält Informationen zur proaktiven Bereitstellung von Qualitätsupdates.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338135"
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
- **Versionsfallback**: Flighting wird verwendet, um alle Änderungen in einem proaktiven Qualitätsupdate zusammenzufassen. Wenn nach einer proaktiven Bereitstellung ein Fallback erforderlich ist, kann dies über das Flighting-System erfolgen.
- **Sandbox-Synchronisierungsbezeichnung**: Weniger als 20 Prozent der Kunden haben heute mehrere Sandboxes und halten eine Sandbox bereit, in der die Version mit der Produktion übereinstimmt, um bei der Fehlerbehebung zu helfen. In naher Zukunft werden wir Kunden die Möglichkeit geben, eine Sandbox-Umgebung anzugeben, die die proaktive Bereitstellung von Qualitätsupdates nicht zusammen mit anderen Sandboxen erhalten soll, sondern später zusammen mit der Produktionsumgebung. Beachten Sie, dass, wenn ein Kunde eine Sandbox verwendet, um eine neuere Version als seine Produktion zu testen, diese Sandbox Qualitätsupdates für die neuere Version erhält.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Ab wann werden proaktive Qualitätsupdates genutzt?

Die Verteilung von proaktiven Qualitätsupdates für Sandbox-Umgebungen beginnt voraussichtlich Ende September oder Oktober 2022 für Azure Public Cloud-Kunden. Testumgebungen erhalten ab diesem Zeitpunkt auch eine proaktive Updatebereitstellung. Im September wird eine Benachrichtigung an alle Kunden gesendet, um sie über den erwarteten Zeitplan für seine Umgebungen zu informieren. Ausnahmen vom proaktiv aktualisierten Bereitstellungsprozess sind nur für FDA-regulierte Kunden zulässig. Wir arbeiten noch daran, wie regulierte Umgebungen und staatliche Cloud-Kunden verwaltet werden sollen.

In den Nächsten sechs Monaten steigern wir schrittweise den Prozentsatz der Sandbox-Umgebungen, die proaktive Updates erhalten, bis alle designierten Umgebungen enthalten sind, und fahren dann mit der Aktualisierung von Produktionsumgebungen fort. Wir überwachen den gesamten Zeitraum, um sicherzustellen, dass der Bereitstellungsprozess nahtlos verläuft und wir unser Ziel von unterbrechungsfreien Nutzlasten erreichen.

Da Kunden regelmäßig kleinere Nutzlasten erhalten, erwarten wir, dass es einfacher wird, auf dem Laufenden zu bleiben. Wir werden die Häufigkeit der Update-Bereitstellung anpassen, wenn wir den Prozess nachweislich ohne Unterbrechung ausführen können. Dieser Prozess funktioniert für unsere Dataverse-Plattform und -Anwendungen bereits effektiv und liefert die erwarteten Verbesserungen der Servicequalität. Wir möchten den gleichen Schritt nach vorne unbedingt auch für Finanz- und Betriebsanwendungen machen.
