---
title: Cloud- und Edge-Skalierungseinheiten für Arbeitsauslastungen in der Fertigung und Lagerortverwaltung
description: Dieses Thema enthält Informationen über Cloud- und Edge-Scale-Einheiten für Arbeitsauslastungen in der Fertigung und Lagerortverwaltung.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: fb0d8e0226b11e93503979c202da917de1df6319
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240436"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Cloud- und Edge-Skalierungseinheiten für Arbeitsauslastungen in der Fertigung und Lagerortverwaltung

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Cloud- und Edge-Scale-Einheiten ermöglichen die Verteilung von Arbeitsauslastungen in der Fertigung und im Lagerort auf verschiedene Umgebungen. Diese Funktionalität kann dazu beitragen, die Leistung zu verbessern, Serviceunterbrechungen zu verhindern und die Betriebszeit zu maximieren. Sie wird von den folgenden Add-Ins bereitgestellt:

- Cloud Scale Unit Add-in für Dynamics 365 Supply Chain Management
- Edge Scale Einheit Add-in für Dynamics 365 Supply Chain Management

Unternehmen, die mit Fertigung und Vertrieb arbeiten, müssen in der Lage sein, wichtige Geschäftsprozesse rund um die Uhr, ohne Unterbrechung und in großem Umfang auszuführen. Cloud- und Edge-Scale-Einheiten ermöglichen es Unternehmen, wichtige geschäftskritische Fertigungs- und Lagerort-Prozesse ohne Unterbrechung laufen zu lassen, selbst bei gelegentlichen Problemen mit der Netzwerkkonnektivität oder Latenz.

## <a name="public-preview-information"></a>Informationen zur öffentlichen Vorschau

Die Vorschau bietet eine Umgebung, die als Cloud-basierter Hub Ihrer Dynamics 365 Supply Chain Management-Umgebung fungiert und eine Umgebung, die als Cloud-Scale-Einheit fungiert.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Verfügbarkeit der Vorschau

Die Vorschau für Cloud- und Edge-Scale-Einheiten wird für bestehende Kunden von Supply Chain Management im Oktober 2020 verfügbar.

Um Zugriff auf das Oktober-Preview-Release 10.0.15/Plattform-Update 39 für die Bereitstellung in Ihrer [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) Umgebung zu erhalten, müssen Sie Teil des Preview Early Access Program (auch bekannt als PEAP) für Supply Chain Management sein. Sie können PEAP beitreten, wenn Sie bereits Mitglied des breiteren [Dynamics Insider Program](https://experience.dynamics.com/insider) sind. Wählen Sie einfach das spezifische Programm aus, das „Finance & Operations Preview early access program (PEAP)“ heißt.

> [!IMPORTANT]
> Die Funktionalität der Skalierungseinheit für Supply Chain Management wird nur zur Verfügung gestellt, wenn Sie den [Cloud + Edge Vorschau für Finance and Operations Bedingungen](https://Aka.ms/SCMCnETerms) zustimmen.

### <a name="data-processing-for-the-preview"></a>Datenverarbeitung für die Vorschau

Während der öffentlichen Vorschau werden einige Verwaltungsdienste nur in den Vereinigten Staaten gehostet. Wenn die Funktion jedoch allgemein verfügbar wird, werden diese Management-Services in allen vom Supply Chain Management unterstützten Geografien verfügbar sein. Dies betrifft die Übertragung und Speicherung von Verwaltungsinformationen, die vom Scale-Unit-Manager verwendet werden, einschließlich

- Ihre Mandanten-Namen und IDs
- Ihre LCS-Projekt-IDs
- Administrator-E-Mails, die zur Anmeldung verwendet werden
- Umgebungs-IDs für Hub und Scale Units
- Konfigurationen der Arbeitsauslastung
- Gesammelte Metriken (z. B. Latenz und Durchsatz), die auf der Seite zur Kartenanalyse angezeigt werden

Die in die US-Rechenzentren übertragenen und dort gespeicherten Daten werden gelöscht, wenn Ihre Vorschau-Umgebungen heruntergefahren werden.

### <a name="sign-up-for-the-preview"></a>Anmelden für eine Vorschau

Um sich für die Cloud- und Edge-Vorschau für Supply Chain Management anzumelden, muss Ihr Unternehmen bereits über eine aktive Supply Chain Management-Cloud-Umgebung verfügen.

Die Funktionalitäten der skalierbaren Einheiten befinden sich derzeit in der öffentlichen Vorschau. Wenn Sie sich anmelden, müssen Sie ein Benutzerkonto für den jeweiligen Mandanten verwenden. Außerdem müssen Sie ein Besitzer eines Projekts oder ein Admin der Umgebung in LCS für ein aktives Dynamics 365 LCS-Projekt in diesem Mandanten sein.

Wenn Sie sich für die Vorschau anmelden, wählen Sie einen Mandanten aus und durchlaufen die Anmeldeschritte. Sobald Microsoft Preview-Kapazitäten zuweisen kann, senden wir Ihnen eine E-Mail mit den Bereitstellungsdetails und den Promo-Codes für zwei Umgebungen (einen Hub und eine Scale Unit) für das entsprechende LCS Projekt. Sie können dann die beiden Umgebungen als Tier-2-Sandbox-Umgebungen bereitstellen. Diese Umgebungen werden 60 Tage ab dem Erstellungsdatum der Promo-Codes gültig sein. Sie sollten die beiden Umgebungen nicht verwenden, bevor der im nächsten Absatz beschriebene Schritt abgeschlossen ist.

Nachdem Sie mit Microsoft bestätigt haben, dass die beiden Umgebungen mit Hilfe der Promo-Codes bereitgestellt wurden, wird eine der Umgebungen so konfiguriert, dass sie als Hub arbeitet, und die andere wird so konfiguriert, dass sie als Scale Unit arbeitet. Sie können dann die Scale Units konfigurieren und ausgewählte Arbeitsauslastungen für die Lagerortverwaltung und die Fertigung bereitstellen, indem Sie das [Scale Unit Manager-Portal](https://aka.ms/SCMSUM) verwenden.

Vorschau-Umgebungen werden automatisch nach 60 Tagen gelöscht. Sie können jedoch auch früher gelöscht werden, wenn es den Anschein hat, dass sie nicht verwendet werden. Nachdem Ihre Vorschau-Umgebungen gelöscht worden sind, können Sie sich für eine neue Vorschau-Bereitstellung anmelden und in die Warteschlange stellen.

Um sich für die Vorschau anzumelden, gehen Sie zum [Scale Unit Manager Portal](https://aka.ms/SCMSUM).

### <a name="limitations-that-apply-during-the-preview-period"></a>Einschränkungen, die während der Vorschauzeit gelten

> [!IMPORTANT]
> In der Anfangsphase des Preview-Programms für diese Funktion unterstützt Microsoft nur Hubs, die über Cloud-Scale Units verfügen, nicht aber Hubs, die über Edge-Scale Units verfügen. Edge-Scale-Units werden lokal installiert und werden voraussichtlich in einer kommenden Phase des Programms verfügbar sein.

Da es sich bei Cloud- und Edge-Scale-Units um eine Vorschau-Funktion handelt, sind Dienste, die damit zusammenhängen, derzeit nur in begrenzten Ländern und Regionen verfügbar. Durch die Aktivierung von Cloud- und Edge-Scale-Einheiten bestätigen Sie, dass Sie verstehen, dass einige Daten, die mit der Konfiguration und Verarbeitung von Cloud- und Edge-Scale-Einheiten zusammenhängen, in einem Rechenzentrum gespeichert werden können, das sich in den Vereinigten Staaten befindet. Durch die Aktivierung von Cloud- und Edge-Scale-Units erklären Sie sich auch mit den [Bedingungen der Cloud + Edge Vorschau für Finance and Operations einverstanden](https://Aka.ms/SCMCnETerms). Um mehr über Cloud- und Edge-Scale-Units zu erfahren, lesen Sie die [Dokumentation](https://aka.ms/scmcne).

Ihre Privatsphäre ist für Microsoft wichtig. Um mehr zu erfahren, lesen Sie unsere [Datenschutzerklärung](https://aka.ms/privacy).

> [!IMPORTANT]
> Einige Geschäftsfunktionen werden in der öffentlichen Vorschau nicht vollständig unterstützt, wenn Arbeitsauslastungen auf Scale Units verwendet werden. Weitere Informationen zu den funktionalen Arbeitsauslastungen finden Sie in den Abschnitten weiter unten in diesem Thema.

## <a name="scale-units-and-dedicated-workloads"></a>Skalierungseinheiten und dedizierte Arbeitsauslastungen

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 mit Skalierungseinheiten":::

Skalierungseinheiten erweitern Ihre zentrale Supply Chain Management Hub-Umgebung, indem sie dedizierte Verarbeitungskapazität hinzufügen. Skalierungseinheiten können in der Cloud laufen. Alternativ können sie auf dem Edge in den Räumlichkeiten Ihrer lokalen Einrichtung laufen. Scale-Units können vorübergehend von der Hub-Umgebung getrennt werden. Wenn sie verbunden sind, erhalten die Skalierungseinheiten alle Informationen, die für die Ausführung der dedizierten Verarbeitung für zugewiesene Arbeitsauslastungen erforderlich sind.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Optionen für Scale-Units in der öffentlichen Vorschau":::

Für die öffentliche Vorschau können Sie eine Hub-Umgebung mit ausgewählten Arbeitsauslastungen auf einer Cloud-Skalierungseinheit konfigurieren, indem Sie das Portal Scale Unit Manager verwenden. Teilnehmer der Vorschau, die Zugriff auf eine lokale Business Data (LBD)-Umgebung haben, können die LBD-Umgebung auch als Edge Scale Unit konfigurieren.

Eine Arbeitsauslastung ist eine festgelegte Menge an Geschäftsfunktionalität, die an eine Scale Unit delegiert werden kann. Derzeit bietet die Vorschau zwei Arten von Arbeitsauslastungen:

- Fertigungssteuerung
- Lagerortverwaltung

Sie können jeweils eine Arbeitsauslastung pro Skalierungseinheit zuweisen. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Dedizierte Funktionalitäten für die Arbeitsauslastung bei der Fertigungsausführung in einer Skalierungseinheit

Für die Fertigungsausführung bieten die Cloud- und Edge-Scale-Units die folgenden Funktionalitäten, auch wenn die Edge-Units nicht mit der Cloud verbunden sind:

- Maschinenbediener und Werkstattleiter können auf den operativen Produktionsplan zugreifen.
- Maschinenbediener können den Plan auf dem neuesten Stand halten, indem sie diskrete und Prozessfertigungsaufträge ausführen.
- Der Fertigungsleiter kann den Betriebsplan anpassen.
- Die Arbeiter können auf die Zeiterfassung zugreifen, um die korrekte Berechnung der Löhne sicherzustellen.

Weitere Informationen finden Sie in den [Details zur Arbeitsauslastung von Fertigungswaagen-Einheiten](cloud-edge-workload-manufacturing.md).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Dedizierte Arbeitsauslastungen für die Lagerortverwaltung in einer Scale Unit

Für die Lagerortverwaltung bieten Cloud- und Edge-Scale-Units die folgenden Funktionalitäten, auch wenn die Edge-Einheiten nicht mit der Cloud verbunden sind:

- Die Verarbeitung ausgewählter Wave-Methoden ist für Verkaufsaufträge und Wiederbeschaffung von Bedarfen aktiviert.
- Lagerort-Mitarbeiter können den Verkauf und die Wiederbeschaffung von Waren über die Lagerort-App abwickeln.
- Lagerort-Mitarbeiter können über die Lagerort-App den Bestand abfragen.
- Lagerort-Mitarbeiter können mit der Lagerort App Bestandsbewegungen erstellen und ausführen.
- Lagerort-Mitarbeiter können mit der Lagerort-App Einkaufsbestellungen registrieren und Einlagerungen vornehmen.

Weitere Informationen finden Sie in den [Details zur Arbeitsauslastung von Lagerort-Scale-Units](cloud-edge-workload-warehousing.md).

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Skalierungseinheiten für Ihre Supply Chain Management-Umgebung einbinden

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>Vorschau für Cloud- und Edge-Scale-Einheiten bereitstellen

Die folgende Abbildung zeigt den Anmelde- und Bereitstellungs-Flow für die öffentliche Vorschau für Cloud-Scale-Units.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Schritte zur Anmeldung für die Vorschau":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>Wählen Sie Ihren LCS-Projekt-Mandanten und den detaillierten Ablauf der Vorschau

In der öffentlichen Vorschau zeigt das [Scale Unit Manager-Portal](https://aka.ms/SCMSUM) die Liste der Mandanten an, zu denen Ihr Konto gehört und bei denen Sie Besitzer oder Umgebungs-Admin für ein LCS-Projekt sind.

Wenn der gesuchte Mandant nicht in dieser Liste enthalten ist, gehen Sie zu [LCS](https://lcs.dynamics.com/v2) und stellen Sie sicher, dass Sie entweder ein Umgebungs-Admin oder ein Besitzer des LCS-Projekts für diesen Mandanten sind. Beachten Sie, dass nur Azure Active Directory (Azure AD) Konten aus dem ausgewählten Mandanten berechtigt sind, die Anmeldung abzuschließen.

> [!NOTE]
> Nachdem Sie Änderungen an LCS vorgenommen haben, kann es bis zu 30 Minuten dauern, bis die Liste der Mandanten die Änderungen widerspiegelt.

Für jeden Mandanten zeigt die Liste den Anmeldestatus an.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Anmeldemöglichkeit für einen Mandanten":::

Wählen Sie den Link **Klicken Sie hier, um sich anzumelden**, um Ihren LCS-Mandanten für die Teilnahme an der Vorschau anzumelden. Sie müssen die Bedingungen akzeptieren. Sie müssen auch eine geschäftliche E-Mail-Adresse angeben, an die Microsoft Mitteilungen senden kann, die mit dem Anmeldeprozess für die Vorschau zusammenhängen.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Sign-up-Antrag für einen Mandanten":::

Microsoft prüft Ihren Antrag und informiert Sie über die nächsten Schritte, indem es eine E-Mail an die Adresse sendet, die Sie auf dem Anmeldeformular angegeben haben.

Nachdem Ihnen der Zugriff auf das Preview-Programm gewährt wurde, erhalten Sie zwei Promo-Codes für Ihr LCS-Projekt. Sie können diese Promo-Codes nun verwenden, um zwei Umgebungen in LCS bereitzustellen. Die Umgebungen müssen die PEAP-Version 10.0.15 oder höher verwenden. Wenn Sie mit der Anwendung der Promo-Codes fertig sind, benachrichtigen Sie Microsoft (wie angewiesen), damit wir die Umgebungen für die Vorschau-Funktionen fertig aktivieren können. Microsoft wird Sie benachrichtigen, wenn dieser Konfigurationsschritt abgeschlossen ist.

Sie können nun damit beginnen, Skalierungseinheiten und Arbeitsauslastungen in Ihrer Vorschau-Umgebung zu konfigurieren.

> [!IMPORTANT]
> Wenn Sie Cloud-Skalierungseinheiten konfigurieren, können Sie [alle erforderlichen Schritte im Portal Scale Unit Manager](#scale-unit-manager-portal) durchführen.
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Verwalten Sie Cloud-Skalierungseinheiten und Arbeitsauslastungen mithilfe des Scale Unit Manager-Portals

Gehen Sie zum [Scale Unit Manager-Portal](https://aka.ms/SCMSUM), und melden Sie sich mit Ihrem Mandanten-Konto an. Auf der Seite **Skalierungseinheiten konfigurieren** können Sie eine Hub Umgebung hinzufügen, wenn sie nicht bereits aufgelistet ist. Sie können dann den Hub auswählen, den Sie mit Skalierungseinheiten und Arbeitsauslastungen konfigurieren möchten.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Erfahrung mit Skalierungseinheiten und Arbeitsauslastung":::

Um eine oder mehrere Scale Units hinzuzufügen, die in Ihrer Topologie verfügbar sind, wählen Sie **Scale Units hinzufügen**. In der Vorschau sollten Sie die Cloud-Skalierungseinheit sehen, die Sie mit einem der Promo-Codes bereitgestellt haben, die Sie im Rahmen des Vorschau-Programms erhalten haben.

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

Verwenden Sie auf der Registerkarte **Definierte Arbeitsauslastungen** die Schaltfläche **Arbeitsauslastung erstellen**, um einer Ihrer Skalierungseinheiten eine Arbeitsauslastung für die Lagerortverwaltung oder die Fertigungsausführung hinzuzufügen. Für jede Arbeitsauslastung müssen Sie den Kontext der Prozesse angeben, die zur Arbeitsauslastung gehören sollen. Bei Arbeitsauslastungen für die Lagerortverwaltung ist der Kontext ein bestimmtes Lager an einem bestimmten Standort und einer bestimmten juristischen Entität. Bei Arbeitsauslastungen für die Fertigungsausführung ist der Kontext ein bestimmter Standort in einer juristischen Entität.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Erstellung von Arbeitsauslastung":::

> [!IMPORTANT]
> Im Portal Scale Unit Manager in der Vorschau können Sie keine Arbeitsauslastungen aus Scale Units entfernen oder die Zuordnung einer Scale Unit zu einem Hub aufheben, nachdem die Zuordnung erfolgt ist. Wenn Sie eine Zuordnung aufheben müssen, wenden Sie sich an Ihren Ansprechpartner für die Programmverwaltung der Vorschau.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]