---
title: Skalierungseinheiten in einer verteilten Hybridtopologie
description: Dieses Thema enthält Informationen über Cloud- und Edge-Scale-Einheiten für Arbeitsauslastungen in der Fertigung und Lagerortverwaltung.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 30f455f37b5161878cf9c864b92966aa74da051f
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376181"
---
# <a name="scale-units-in-a-distributed-hybrid-topology"></a>Skalierungseinheiten in einer verteilten Hybridtopologie

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Die Skalierungseinheit für Microsoft Dynamics 365 Supply Chain Management wird Ihnen unter den Bedingungen zur Verfügung gestellt, die für die Nutzung des Dienstes gelten. Weitere Informationen finden Sie in den [rechtlichen Hinweisen zu Microsoft Dynamics](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Wenn Sie Cloud- und Edge-Scale-Einheiten aktivieren, werden Sie aufgefordert, zu bestätigen, dass Sie verstehen, dass einige Daten, die mit der Konfiguration und Verarbeitung von Cloud- und Edge-Scale-Einheiten zusammenhängen, möglicherweise in einem Rechenzentrum gespeichert werden, das sich in den USA befindet. Weitere Informationen zur Datenverarbeitung für Cloud- und Edge-Skalierungseinheiten finden Sie weiter unten in diesem Thema im Abschnitt [Datenverarbeitung während der Verwaltung von Skalierungseinheiten](#data-processing-management).

## <a name="core-value-proposition-for-a-distributed-hybrid-topology"></a>Kernwertversprechen für eine verteilte Hybridtopologie

Unternehmen, die mit Fertigung und Vertrieb arbeiten, müssen in der Lage sein, wichtige Geschäftsprozesse rund um die Uhr, ohne Unterbrechung und in großem Umfang auszuführen. Eine verteilte Hybridtopologie ermöglicht es Unternehmen, wichtige geschäftskritische Fertigungs- und Lagerortprozesse ohne Unterbrechung laufen zu lassen, selbst bei gelegentlichen Problemen mit der Netzwerkkonnektivität oder Latenz.

Eine verteilte Hybridtopologie führt das Konzept von *Skalierungseinheiten* ein, die in der Werkstatt und am Lagerort eine Verteilung der Arbeitslasten auf verschiedene Umgebungen ermöglichen. Diese Funktionalität kann dazu beitragen, die Leistung zu verbessern, Serviceunterbrechungen zu verhindern und die Betriebszeit zu maximieren. Skalierungseinheiten werden über die folgenden Add-Ins für Ihr Supply Chain Management-Abonnement bereitgestellt:

- Cloud Scale Unit Add-in für Dynamics 365 Supply Chain Management
- Edge Scale Einheit Add-in für Dynamics 365 Supply Chain Management

Die Arbeitsauslastungsfunktionen werden kontinuierlich durch schrittweise Verbesserungen freigegeben.

## <a name="scale-units-and-dedicated-workloads"></a>Skalierungseinheiten und dedizierte Arbeitsauslastungen

Skalierungseinheiten erweitern Ihre zentrale Supply Chain Management Hub-Umgebung, indem sie dedizierte Verarbeitungskapazität hinzufügen. Skalierungseinheiten können in der Cloud laufen. Sie können sie auch am [Rand](cloud-edge-edge-scale-units-lbd.md), lokal in Ihrer Einrichtung ausführen.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 mit Skalierungseinheiten.":::

Skalierungseinheiten bieten Resilienz, Zuverlässigkeit und Skalierbarkeit für die zugewiesenen Arbeitsauslastungen. Edge-Skalierungseinheiten können vorübergehend von der Cloud-Hub-Umgebung getrennt werden, und die Mitarbeiter arbeiten weiterhin in den zugewiesenen Arbeitsauslastungen am Edge.

Eine *Arbeitsauslastung* ist eine festgelegte Menge an Geschäftsfunktionalität, die an eine Skalierungseinheit delegiert werden kann. Obwohl die Arbeitsauslastung für die Lagerortverwaltung freigegeben wurde, befindet sich die Arbeitsauslastung für die Fertigungssteuerung noch in der Vorschau.

Sie können Ihre Hub-Umgebung und Cloud-Skalierungseinheiten für ausgewählte Arbeitsauslastungen konfigurieren, indem Sie das [Scale Unit Manager-Portal](https://sum.dynamics.com) verwenden. Sie können auch mehrere Arbeitsauslastungen pro Skalierungseinheit zuweisen. Weitere Informationen zu den Voraussetzungen und Einschränkungen für Cloud-Skalierungseinheiten in der aktuellen Version finden Sie weiter unten in diesem Thema im Abschnitt [Voraussetzungen und Einschränkungen für Cloud-Skalierungseinheiten](#cloud-scale-unit-prerequisites).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Dedizierte Arbeitsauslastungen für die Lagerortverwaltung in einer Scale Unit

Mit der Arbeitsauslastung der Lagerortverwaltung können Sie Ihre Lagervorgänge skalieren und in einer stabilen Umgebung ausführen, indem Sie isolierte Wartungsfenster verwenden. Der Workload Lagerverwaltung unterstützt die meisten Prozesse der Lagerverwaltung im Enterprise Hub. Weitere Informationen finden Sie unter [Arbeitsauslastungen in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Dedizierte Funktionalitäten für die Arbeitsauslastung bei der Fertigungsausführung in einer Skalierungseinheit

Die Fertigungsarbeitsauslastung bietet die folgenden Fähigkeiten:

- Maschinenbediener und Werkstattleiter können auf den operativen Produktionsplan zugreifen.
- Maschinenbediener können den Plan auf dem neuesten Stand halten, indem sie diskrete und Prozessfertigungsaufträge ausführen.
- Der Fertigungsleiter kann den Betriebsplan anpassen.
- Die Arbeitskräfte können auf die Zeiterfassung zugreifen, um die korrekte Berechnung der Löhne sicherzustellen.

Weitere Informationen finden Sie unter [Arbeitsauslastungen bei der Fertigungsausführung für Cloud- und Edge-Skalierungseinheiten](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Überlegungen, bevor Sie die verteilte Hybridtopologie für Supply Chain Management aktivieren

Indem Sie die verteilte Hybridtopologie aktivieren, stellen Sie Ihre Supply Chain Management Cloud Umgebung so um, dass sie als Hub fungiert. Sie können auch zusätzliche Umgebungen zuordnen, die als Skalierungseinheiten in der Cloud oder am Edge konfiguriert sind.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>Voraussetzungen und Einschränkungen für Cloud-Skalierungseinheiten

In der aktuellen Version für Skalierungseinheiten sind einige Funktionen noch nicht verfügbar, können jedoch im Laufe der Zeit schrittweise hinzugefügt werden.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Sie müssen ein lizenzierter Kunde von Supply Chain Management sein

Für das Onboarding in die verteilte Topologie benötigen Sie eine Lizenz für Supply Chain Management. Ihre vorhandene Cloud-Umgebung wird zum Hub in Ihrer Hybridtopologie. Sie können sowohl Sandbox-Umgebungen als auch Produktionsumgebungen als Hub-Umgebungen deklarieren und Skalierungseinheiten entsprechend den von Ihnen erworbenen Add-Ins hinzufügen.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Ihr bestehendes Projekt muss über die globale kommerzielle Version von LCS verwaltet werden

Ihr bestehendes Microsoft Dynamics Lifecyle Services-Projekt (LCS-Projekt) muss die folgenden Versionsanforderungen erfüllen:

- Das bestehende Projekt muss über die globale kommerzielle Version von LCS unter [lcs.dynamics.com](https://lcs.dynamics.com) verwaltet werden.
- Lokale Versionen von LCS (wie [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) und [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) werden nicht unterstützt.
- Behördliche Cloud-Versionen von LCS werden nicht unterstützt.
- Die Mooncake-Version von LCS wird nicht unterstützt.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Ihre aktuelle Produktionsumgebung muss den Self-Service-Typ in LCS haben

Ihre aktuelle Produktionsumgebung muss den in LCS als Typ **Self-Service** gekennzeichnet sein. Dieser Typ gibt an, dass der Mandant Ihres LCS-Projekts bereits konvertiert wurde, sodass er das Azure Service Fabric Hosting-Modell unterstützt.

> [!IMPORTANT]
> Umgebungstypen, die als Infrastructure-as-a-Service (IaaS) ausgeführt werden, werden nicht unterstützt. Diese Umgebungen sind normalerweise mit dem Typ **Von Microsoft verwaltet** in LCS gekennzeichnet. Wenn Sie über Umgebungen dieses Typs verfügen, informieren Sie sich bei Ihrem Ansprechpartner bei Microsoft über den Migrationszeitplan zum Typ **Self-Service**.

Microsoft ist dabei, alle Cloud-Umgebungen von Supply Chain Management von einem IaaS-Modell auf eine Topologie umzustellen, die in Service Fabric gehostet wird. Dieser Schritt bringt eine bessere Skalierbarkeit und erleichtert die Dienstverwaltung. Daher sind Bereitstellungs- und Wartungsvorgänge schneller. Ebenso werden Dienstkomponenten auf das Konzept der Microservices migriert und das Dienst-Hosting-Modell wird von einem VM-Modell (virtuelle Maschine) auf eine schlanke Containerarchitektur [umgestellt](/virtualization/windowscontainers/about/containers-vs-vm).

Letztendlich versorgt dieselbe Service-Fabric-basierte containerisierte Dienstinfrastruktur sowohl Cloud- als auch Edge-Instanzen des Dienstes, unabhängig davon, ob eine Instanz ein Hub in der Cloud oder eine Skalierungseinheit in der Cloud oder am Edge ist.

Bevor Sie das Onboarding in die Hybridtopologie durchführen können, die Skalierungseinheiten unterstützt, muss Ihr Projektmandant auf das von Service Fabric gehostete Modell umgestellt werden. Darüber hinaus muss jede Umgebung, die als Hub fungiert, konvertiert werden.

> [!TIP]
> Um den Status Ihres LCS-Projektmandanten abzufragen, suchen Sie nach dem Typ Ihrer Umgebung in [LCS](https://lcs.dynamics.com/) oder wenden Sie sich an Ihren Partner oder Ansprechpartner bei Microsoft.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Lokale Geschäftsdatenumgebungen (lokal) werden nicht als Hubs für Skalierungseinheiten unterstützt

Lokale Umgebungen können nicht als Hubs für Skalierungseinheiten fungieren. Hub-Umgebungen müssen immer in der Cloud gehostet werden.

#### <a name="scale-unit-management-capabilities-are-limited"></a>Die Funktionen zur Verwaltung von Skalierungseinheiten sind begrenzt

Die Verwaltungsfunktionen, die beim Verschieben von Arbeitsauslastungen helfen können, sind begrenzt. Einige Verwaltungsvorgänge werden nicht als Self-Service unterstützt, und Sie müssen möglicherweise Unterstützung über Ihren Partner oder Ansprechpartner bei Microsoft anfordern. Beispiele hierfür sind einige Arbeitsauslastungsbewegungen zwischen Skalierungseinheiten und temporäre Ad-hoc-Bewegungen in Katastrophenfallszenarien.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Metriken und Messungen sind noch nicht verfügbar

Metriken und Kennzahlen, die Ihnen bei der Auswahl der besten Anwendung für Ihre Skalierungseinheiten helfen könnten, sind noch nicht verfügbar. Arbeiten Sie mit Ihrem Ansprechpartner bei Microsoft oder Ihrem Implementierungspartner zusammen, um die vorteilhafteste Anwendung auszuwählen.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>Datenverarbeitung während der Verwaltung von Skalierungseinheiten

Wenn Sie Ihre Dynamics 365 Umgebung aktivieren, um die verteilte hybride Topologie für Cloud- und Edge-Scale-Einheiten zu unterstützen, werden einige Verwaltungsdienste nur in den Vereinigten Staaten gehostet, wie für LCS. Dieses Verhalten wirkt sich auf die Übertragung und Speicherung einiger Verwaltungs- und Konfigurationsinformationen aus, die vom [Scale Unit Manager-Portal](https://sum.dynamics.com) genutzt werden. Im Folgenden finden Sie einige Beispiele hierfür:

- Ihre Mandanten-Namen und IDs
- Ihre LCS-Projekt-IDs
- E-Mail-Adressen von Administratoren und Projektbesitzern, die für die Anmeldung verwendet werden
- Umgebungs-IDs für die Hub und Skalierungseinheiten
- Arbeitsauslastungskonfigurationen, einschließlich der Namen und physischen Adressen von juristischen Personen und Einrichtungen, damit Ihre Topologie auf einer geografischen Karte angezeigt werden kann
- Gesammelte Metriken (wie Wartezeit und Durchsatz), die auf der Seite zur Kartenanalyse angezeigt werden, um Ihnen bei der Auswahl der vorteilhaftesten Verwendung Ihrer Skaleneinheiten zu helfen

Daten, die an US-Rechenzentren übertragen und dort gespeichert werden, werden gemäß den Richtlinien für die Datenaufbewahrung von Microsoft gelöscht. Ihre Privatsphäre ist für Microsoft wichtig. Weiteres erfahren Sie in unserer [Datenschutzerklärung](https://go.microsoft.com/fwlink/?LinkId=521839).

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Onboarding in die verteilte Hybridtopologie für Supply Chain Management

### <a name="try-out-the-distributed-hybrid-topology"></a>Probieren Sie die verteilte hybride Topologie aus

Das Onboarding für die verteilte Hybridtopologie erfolgt in zwei Schritten. In der ersten Phase sollten Sie die Lösung [ausprobieren](cloud-edge-try-out.md) und Ihre Anpassungen validieren, um sicherzustellen, dass sie in einer verteilten Topologie mit Scale-Units funktionieren. (Für die Validierung können Sie vorhandene Entwicklungsumgebungen verwenden.) Anschließend können Sie mit der zweiten Stufe fortfahren, in der Sie Produktionsumgebungen erwerben.

## <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>Ihren LCS-Projekt-Mandanten und den detaillierten Onboarding-Prozess auswählen

Skalierungseinheiten werden in mehreren Lagermengeneinheiten (SKUs) und Preisoptionen angeboten. Daher können Sie die Option auswählen, die Ihrem geplanten monatlichen Transaktionsvolumen und Ihren Leistungsanforderungen am besten entspricht.

> [!TIP]
> Um die Größe zu ermitteln, die Ihren Anforderungen am besten entspricht, arbeiten Sie mit Ihrem Implementierungspartner und Microsoft zusammen, um die von Ihnen benötigte monatliche Transaktionsgröße zu ermitteln.

Die Einstiegs-SKU heißt *Basic* und die leistungsfähigere SKU *Standard*. In jeder SKU ist eine bestimmte Anzahl monatlicher Transaktionen vorinstalliert. Sie können das monatliche Transaktionsbudget jedoch erhöhen, indem Sie für jede SKU Überschreitungs-Add-Ins hinzufügen.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Add-Ins für Cloud-Skalierungseinheiten.":::

> [!NOTE]
> Scale-Unit Add-Ins sind nicht an eine begrenzte Anzahl von Benutzern gekoppelt. Sie stehen jedem Benutzer in Ihrem bestehenden Abonnement zur Verfügung (vorausgesetzt, Ihr Administrator hat ihm die erforderlichen Benutzerrollen zugewiesen).

Durch den Kauf jedes Add-Ins für Skalierungseinheiten erhalten Sie nicht nur ein monatliches Transaktionsvolumen, sondern auch eine bestimmte Anzahl von Umgebungsslots in LCS. Für jedes Add-In für eine Cloud-Skalierungseinheit haben Sie Anspruch auf einen neuen Produktionsslot und einen neuen Sandbox-Slot. Während des Onboarding-Prozesses wird ein neues LCS-Projekt mit diesen Slots hinzugefügt. Die Nutzungsrechte für die Slots sind gebunden, sodass die Slots als Skalierungseinheiten mit einem Cloud-Hub verwendet werden müssen.

Überschreitungs-Add-Ins geben Ihnen keinen Anspruch auf neue Umgebungsslots.

Wenn Sie mehr Sandbox-Umgebungen erwerben möchten, können Sie zusätzliche reguläre Sandbox-Slots erwerben. Microsoft kann Ihnen dann dabei helfen, diese Slots als Sandbox-Skalierungseinheiten für die Hybridtopologie zu aktivieren.


Nachdem Sie die Planung abgeschlossen haben, wie Sie in die verteilte hybride Topologie für Supply Chain Management einsteigen wollen, verwenden Sie das Portal [Scale-Unit-Manager](https://aka.ms/SCMSUM), um mit dem Onboarding zu beginnen. Wählen Sie im Portal die Registerkarte **Dynamics 365-Mandanten**. Diese Registerkarte zeigt die Mandanten an, zu denen Ihr Konto gehört und bei denen Sie Besitzer oder Umgebungs-Administrator für ein LCS-Projekt sind.

Wenn der gesuchte Mandant nicht in der Liste enthalten ist, gehen Sie zu [LCS](https://lcs.dynamics.com/v2) und stellen Sie sicher, dass Sie entweder ein Umgebungs-Admininstrator oder Besitzer des LCS-Projekts für diesen Mandanten sind. Nur Azure Active Directory-Konten (Azure AD-Konten) aus dem ausgewählten Mandanten sind berechtigt, die Anmeldung abzuschließen.

> [!NOTE]
> Nachdem Sie Änderungen an LCS vorgenommen haben, braucht die Liste der Mandanten bis zu 30 Minuten, um die Änderungen widerzuspiegeln.

Für jeden Mandanten zeigt die Liste den Onboardingstatus an.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Liste der Mandanten in der Registerkarte „Dynamics 365-Mandanten“,":::

Wählen Sie **Zum Anfangen hier klicken**, um das Onboarding für den LCS-Mandanten anzufordern. Sie müssen die Bedingungen akzeptieren. Sie müssen auch eine geschäftliche E-Mail-Adresse angeben, an die Microsoft Mitteilungen senden kann, die mit dem Onboardingprozess zusammenhängen.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Sign-up-Antrag für einen Mandanten.":::

Microsoft prüft Ihren Antrag und informiert Sie über eine E-Mail an die Adresse, die Sie im Anmeldeformular angegeben haben, über die nächsten Schritte. Microsoft arbeitet eng mit Ihnen zusammen, um Skalierungseinheiten in der Hybridtopologie für Ihr Geschäftsszenario zu aktivieren.

Nach Abschluss des Onboarding können Sie über den Port Skalierungseinheiten und Arbeitsauslastungen konfigurieren.

### <a name="manage-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Verwalten Sie Skalierungseinheiten und Arbeitsauslastungen mithilfe des Scale Unit Manager-Portals

Gehen Sie zum [Scale Unit Manager-Portal](https://aka.ms/SCMSUM), und melden Sie sich mit Ihrem Mandanten-Konto an. Auf der Seite **Skalierungseinheiten konfigurieren** können Sie eine Hub Umgebung hinzufügen, wenn sie nicht bereits aufgelistet ist. Sie können dann den Hub auswählen, den Sie mit Skalierungseinheiten und Arbeitsauslastungen konfigurieren möchten.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Scale Unit Manager Portal, Seite „Skalierungseinheiten konfigurieren“.":::

Um eine oder mehrere Skalierungseinheiten hinzuzufügen, die in Ihrem Abonnement verfügbar sind, wählen Sie **Skalierungseinheiten hinzufügen**.

Verwenden Sie auf der Registerkarte **Definierte Arbeitsauslastungen** die Schaltfläche **Arbeitsauslastung erstellen**, um einer Ihrer Skalierungseinheiten eine Arbeitsauslastung hinzuzufügen. Für jede Arbeitsauslastung müssen Sie den Kontext der Prozesse angeben, die zur Arbeitsauslastung gehören sollen. Bei Arbeitsauslastungen für die Lagerortverwaltung ist der Kontext ein bestimmtes Lager an einem bestimmten Standort und einer bestimmten juristischen Entität.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Dialogfeld „Arbeitsauslastungen definieren“.":::

#### <a name="manage-workloads"></a><a name="manage-workloads"></a>Arbeitsauslastungen verwalten

Wenn eine oder mehrere Arbeitsauslastungen aktiviert sind, verwenden Sie die Option **Arbeitsauslastungen verwalten** zum Initiieren und Verwalten von Prozessen, wie sie in der folgenden Tabelle aufgeführt sind.

| Bearbeiten | Description |
|---|---|
| Skalierungseinheitenkommunikation anhalten | Pipelinenachrichten zwischen dem Hub und einer Skalierungseinheit anhalten. Dieser Prozess stoppt die Kommunikation und entleert die Datenpipeline zwischen dem Hub und den Skalierungseinheiten. Sie müssen diesen Prozess ausführen, bevor Sie einen Supply Chain Management-Wartungsvorgang entweder auf dem Hub oder der Skalierungseinheit ausführen, aber Sie können dies auch in anderen Situationen verwenden. |
| Skalierungseinheitenkommunikation fortsetzen | Pipelinenachrichten zwischen dem Hub und einer Skalierungseinheit fortsetzen. Möglicherweise müssen Sie diesen Prozess verwenden, nachdem Sie beispielsweise einen Supply Chain Management-Wartungsvorgang auf dem Hub oder der Skalierungseinheit ausgeführt haben. |
| Arbeitsauslastungen aktualisieren | Synchronisieren Sie neue Funktionen zwischen den Arbeitsauslastungen von Hub und Skalierungseinheiten. Sie müssen diesen Prozess beispielsweise verwenden, wenn die Wartung dazu geführt hat, dass sich die Datenaustauschabfragen geändert haben und/oder der Arbeitsauslastung neue Tabellen oder Felder hinzugefügt wurden. |
| Arbeitsauslastung auf eine Skalierungseinheit übertragen | Planen Sie die Verschiebung einer Arbeitsauslastung, die derzeit auf dem Hub ausgeführt wird, in eine Skalierungseinheit. Wenn dieser Prozess ausgeführt wird, erfolgt die Synchronisierung der Daten, und sowohl der Hub als auch die Skalierungseinheit werden so eingestellt, dass sie die Eigentümerschaft der Arbeitsauslastung ändern. |
| Skalierungseinheit zu Hub übertragen | Planen Sie die Verschiebung einer Arbeitsauslastung, die derzeit auf der Skalierungseinheit ausgeführt wird, in die Hub. Wenn dieser Prozess ausgeführt wird, erfolgt die Synchronisierung der Daten, und sowohl der Hub als auch die Skalierungseinheit werden so eingestellt, dass sie die Eigentümerschaft der Arbeitsauslastung ändern.
| Notfallübergang zum Hub | <p>Übertragen Sie sofort eine vorhandene Arbeitsauslastung an den Hub. *Dieser Prozess ändert nur die Eigentümerschaft der Daten, die derzeit auf dem Hub verfügbar sind.*</p><p><strong>Warnung:</strong> Dieser Prozess kann zu Datenverlust bei nicht synchronisierten Daten und zum Ausfall der Geschäftsverarbeitung führen. Daher sollte er nur in Notfällen verwendet werden, wenn Geschäftsprozesse auf dem Hub verarbeitet werden müssen, da es in der Skalierungseinheit einen Ausfall gibt, der nicht innerhalb einer angemessenen Zeit behoben werden kann.</p> |
| Nutzung der verteilten Topologie einstellen | Entfernen Sie eine Skalierungseinheitenbereitstellung und führen Sie sie nur auf dem Hub aus, ohne Verarbeitung der Arbeitsauslastung. |

:::image type="content" source="media/sum-manage-workloads.png" alt-text="Erfahrung mit Skalierungseinheiten und Arbeitsauslastung.":::

> [!TIP]
> Im Laufe der Zeit werden der Scale Unit Manager-Umgebung schrittweise Verbesserungen hinzugefügt, um das Lebenszyklusverwaltung zu vereinfachen. Die spezifischen Funktionen für die aktuelle Version sind in einem Onboarding-Handbuch dokumentiert, das Kunden zur Verfügung steht, die gerade das Onboarding der verteilten Hybridtopologie für Supply Chain Management durchführen. <!-- KFM: Add a link to the handbook when it is published -->

## <a name="feature-management-considerations-for-workloads"></a>Überlegungen zur Funktionsverwaltung für Arbeitsauslastungen

In diesem Abschnitt werden einige wichtige Aspekte erläutert, die Sie berücksichtigen sollten, wenn Sie Arbeitsauslastungen installieren, Funktionen hinzufügen oder Funktionen in einer Bereitstellung mit verteilter Hybridtopologie entfernen. Mehrere Szenarien können Einfluss darauf haben, ob Sie ein [Arbeitsauslastungsupgrade](#manage-workloads) durchführen müssen, nachdem Sie Änderungen vorgenommen haben. Normalerweise müssen Sie dies jedoch tun, wenn Sie neue Datenaustauschabfragen aktualisieren oder hinzufügen und/oder wenn Sie einer zuvor installierten Arbeitsauslastung neue Tabellen oder Felder hinzufügen.

### <a name="mandatory-features-for-installing-a-workload"></a>Obligatorische Funktionen für die Installation einer Arbeitsauslastung

Wenn Sie eine Arbeitsauslastung installieren, erstellt der Installationsprozess eine Arbeitsauslastungsdefinition, die Informationen zu den Datentabellen enthält, die verwendet werden, wenn Daten zwischen den beiden Bereitstellungen synchronisiert werden. Die Erstellung einer Arbeitsauslastungsdefinition wird automatisch basierend auf den derzeit in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktivierten Funktionen durchgeführt. In der folgenden Tabelle sind die Funktionen aufgeführt, die aktiviert werden müssen, um die Arbeitsauslastungsdefinitionen zu generieren, die zum Ausführen einer Lager- oder Fertigungsarbeitsauslastung erforderlich sind.

| Obligatorisches Funktionen | Workload |
|---|---|
| Automatische Zuweisung der GUIDs für die WHS-Benutzererstellung | Lager |
| Organisationsweite Arbeitssperrung | Lager |
| Lieferartdetails für Lieferungszyklus | Lager |
| Skalierungseinheitenunterstützung für Lagerort-App-Arbeitslisten | Lager |
| Produktionsumgebungsausführung | Fertigung |

Wenn Sie eine Arbeitsauslastung mithilfe von [Tools zur Bereitstellung von Skalierungseinheiten für Entwicklungsumgebungen mit einem Feld](https://github.com/microsoft/SCMScaleUnitDevTools) oder des [Scale Unit Manager Portals](https://sum.dynamics.com) bereitstellen, werden alle obligatorischen Funktionen automatisch aktiviert. Wenn Sie jedoch eine manuelle Testbereitstellung durchführen, bei der mindestens eine obligatorische Funktion fehlt, schlägt die Installation der Arbeitsauslastung fehl, und Sie erhalten eine Meldung, in der die fehlenden Funktionen aufgeführt sind. Sie müssen diese Funktionen dann manuell aktivieren und die Installation der Arbeitsauslastung erneut auslösen.

### <a name="enabling-or-disabling-features-that-have-data-synchronization-dependencies"></a>Funktionen, die Datensynchronisierungsabhängigkeiten haben, aktivieren oder deaktivieren

Funktionen, die sich auf die Auswahl von Daten auswirken, die zwischen dem Hub und seinen Skalierungseinheiten synchronisiert werden, wirken sich auch darauf aus, wie die Arbeitsauslastungsdefinition erstellt wird. Daher ist es wichtig, dass diese Funktionen aktiviert werden, bevor Sie die Arbeitsauslastung installieren. Wenn Sie diese Art von Funktion aktivieren, während Sie eine Arbeitsauslastung ausführen, müssen Sie die Arbeitsauslastungsdefinition neu generieren, indem Sie ein [Arbeitsauslastungupgrade](#manage-workloads) ausführen, nachdem Sie die Funktion aktiviert haben. Wenn Sie eine Funktion deaktivieren, die Datensynchronisierungsabhängigkeiten aufweist, während Sie eine Arbeitsauslastung ausführen, müssen Sie entsprechend ein [Arbeitsauslastungsupgrade](#manage-workloads) ausführen, um die relevanten Datensynchronisierungsinformationen aus der Arbeitsauslastungsdefinition entfernen.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
