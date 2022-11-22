---
title: Sicherheitskonfigurationskonzepte für virtuelle tabellenbasierte Integrationen
description: In diesem Artikel wird eine Architektur zum Erstellen einer Integration zwischen Microsoft Dynamics 365 Human Resources und anderen Systemen erklärt.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759653"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Sicherheitskonfigurationskonzepte für virtuelle tabellenbasierte Integrationen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt eine Architektur für die Verwendung von [Microsoft Dataverse virtuelle Tabellen (Entitäten)](/dev-itpro/power-platform/virtual-entities-overview) zum Erstellen einer Integration zwischen Dynamics 365 Human Resources und einem Drittanbietersystem. Der Fokus des Artikels liegt auf der Sicherheitskonfiguration und den Authentifizierungs- und Autorisierungsaspekten, die zwischen den Systemgrenzen erforderlich sind, um ein funktionierendes, sicheres System aufzubauen.

## <a name="prerequisite-reference-articles"></a>Erforderliche Referenzartikel

Die folgenden Artikel informieren Sie über die Konzepte in diesem Artikel:

- [Übersicht über virtuelle Entitäten](/dev-itpro/power-platform/virtual-entities-overview)
- [Erste Schritte mit virtuellen Tabellen (Entitäten)](/developer/data-platform/virtual-entities/get-started-ve)
- [Verwenden Sie die mehrinstanzenfähige Server-zu-Server-Authentifizierung (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [Verwenden der OAuth-Authentifizierung mit Microsoft Dataverse (Dataverse)](/developer/data-platform/authenticate-oauth)
- [OAuth 2.0-Clientanmeldeinformationen-Flow auf der Microsoft Identity Platform](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Authentifizierung und Autorisierung](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Architektur 

Das folgende Architekturdiagramm zeigt die Hauptkonzepte, die an einer Integration beteiligt sind, die virtuelle Tabellen (Entitäten) verwendet.

![Virtuelle tabellenbasierte Integration.](./media/Hosts.jpg)

Hier ist eine Erklärung von einigen der nummerierten Elemente im vorherigen Diagramm:

- **Microsoft** – Microsoft hostet und betreibt die verschiedenen Dynamics 365-Produkte im Kundenauftrag.

    - **Azure Active Directory (Azure AD) Mandant C** – Ein Azure AD Mandant, der Microsoft gehört. Es ist der Mandant, in dem die Dynamics 365-Anwendungen registriert sind.

- **Integrationspartner**

    - **Integrierendes System** – Das System, das in Dynamics 365 integriert wird. Es kann sich um ein Gehaltsabrechnungssystem oder ein beliebiges System handeln, das sich auf Daten stützt, die in Dynamics 365 gespeichert sind.
    - **Adapter** – Die Software oder der Dienst, der für die Interaktion mit Dynamics 365 und dem integrierenden System verantwortlich ist.

        > [!NOTE]
        > Wenn ein Adapter von mehreren Dynamics 365-Kunden verwendet werden soll, wird erwartet, dass er als mehrinstanzenfähige Anwendung in Azure AD registriert wird.

    - **Azure AD Mandant A** – Ein Azure AD Mandant, der dem Integrationspartner gehört. Es ist der Mandant, in dem die Anwendungskennung des Adapters registriert ist.

- **Gemeinsamer Kunde** – Ein Kunde, der Dynamics 365 Human Resources und die Lösung des integrierenden Partners implementiert.

    - **Dynamics 365 Finance oder Human Resources** – Die kundenspezifische Instanz von Dynamics 365 Finance oder Human Resources, die die Kundendaten enthält, die das integrierende System benötigt.
    - **Dataverse**– Die kundenspezifische Dataverse Umgebung, die entweder mit Finance oder Human Resources verbunden ist. Dataverse stellt eine Web-API für die Interaktion mit Dynamics 365-Daten bereit.
    - **Azure AD Mandant B** – Der Azure AD Mandant des Kunden. Er fungiert als Identitätsanbieter (Autorisierungsserver) und gibt Token aus, die Anrufer autorisieren, die Dataverse Instanz des Kunden aufzurufen.

## <a name="basic-request-flow"></a>Grundlegender Anforderungsflow

In diesem Abschnitt wird der grundlegende Ablauf einer typischen Anforderung beschrieben, die an einer Integration beteiligt ist. Es verweist auf das Architekturdiagramm weiter oben in diesem Artikel.

Eine typische Anforderung erfordert, dass der Adapter Dynamics 365 nach Daten abfragt und diese Daten dann speichert und mit dem integrierenden System synchronisiert.

1. Der Adapter ruft die Dataverse Web-API zur Abfrage relevanter Daten auf.

    > [!NOTE]
    > Die Authentifizierung ist eine Voraussetzung, und die Token-Erfassung ist ein wichtiger Teil des Prozesses. Die Authentifizierung wird im Abschnitt [Authentifizierung und Autorisierung an Systemgrenzen](#authentication-and-authorization-at-system-boundaries) beschrieben.

    Dieser Aufruf erfolgt gegen die Dataverse Web-API zum Abfragen von Anwendungsdaten, die über eine virtuelle Tabelle verfügbar gemacht werden. (Siehe „2. Erstsynchronisierung“ und „3. Delta Sync“ im Diagramm.)

2. Dataverse verarbeitet die Anforderung, indem es die virtuelle Tabelle über das Plug-In für virtuelle Entitäten abfragt („Virtual Table Proxy“ im Diagramm). Die Dataverse Anforderung wird an den virtuellen Entitätsdienst Finance oder Human Resources weitergeleitet, um die Daten abzufragen, die physisch in der Finance- oder Human Resources-Datenbank gespeichert sind.
3. Der Dienst für virtuelle Entitäten von Finance oder Human Resources übersetzt die Anforderung an die virtuelle Entität in eine Abfrage an die Entität der Finanz- oder Personalabteilung, die die Dataverse virtuelle Entität unterstützt. Die Daten werden aus der Datenbank abgerufen und in die Dataverse Entitätsdarstellung zurückübersetzt und an den Aufrufer zurückgegeben.
4. Der Adapter vervollständigt alle erforderlichen Abbildungen und Datenübersetzungen und ruft das Integrationssystem auf, um die Daten in der Datenbank des Integrationssystems zu speichern. (Siehe „4. Daten speichern“ im Diagramm.)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Authentifizierung und Autorisierung an Systemgrenzen

*Authentifizierung* validiert, dass die Identität eines Benutzers oder einer Anwendung nachgewiesen wurde, und bestätigt, dass der Benutzer oder die Anwendung derjenige ist, für den sie sich ausgeben. *Genehmigung* gewährt dem Benutzer oder der Anwendung das Recht, auf bestimmte Berechtigungen auf Anwendungsebene zuzugreifen. Weitere Informationen finden Sie unter [Authentifizierung vs. Autorisierung](/azure/active-directory/develop/authentication-vs-authorization).

Die meisten systemübergreifenden Aufrufe im Architekturdiagramm weiter oben in diesem Artikel betreffen den Adapter. Der Adapter muss sich selbst authentifizieren, um die folgenden Aufrufe zu tätigen:

- Der Anruf an Dataverse
- Der Aufruf an das integrierende System

Betrachten Sie die Systemgrenzen im Diagramm. Jede Webanforderung zwischen Systemen muss authentifiziert werden, und Autorisierungsprüfungen auf Anwendungsebene müssen bestanden werden, bevor Daten an den Aufrufer zurückgegeben werden. Für eine Anforderung an eine virtuelle Dynamics 365-Tabelle, die von Finance oder Human Resources unterstützt wird, werden Authentifizierungs- und Autorisierungsprüfungen an den folgenden Systemgrenzen erzwungen:

- Der Anruf zwischen dem Adapter und dem Dataverse Endpunkt der Web-API (OData)
- Der Anruf zwischen dem Dataverse Plug-In für virtuelle Einheiten und dem Dienst für virtuelle Einheiten von Finance oder Human Resources

In beiden Fällen werden zuerst Authentifizierungsprüfungen durchgeführt. Anschließend werden Autorisierungsprüfungen auf Anwendungsebene durchgeführt, um sicherzustellen, dass der authentifizierte Benutzer oder die Anwendung über die richtigen Berechtigungen auf Anwendungsebene verfügt, um die angeforderten Daten abzurufen.

Authentifizierung zum Anrufen von Dataverse wird über ein Bearer-Token abgewickelt, das als HTTP-Header in die Webanforderung an Dataverse eingefügt werden muss. Der Adapter muss ein Token von Mandant B Azure AD Instanz enthalten. (Siehe „1. Get Token“ im Diagramm.) Azure AD fungiert als Identitätsanbieter im Authentifizierungsfluss.

Der Adapter authentifiziert sich, indem er seine Anwendungsidentität bereitstellt (nicht geheim, wie in Azure AD Mandant A registriert) und ein Anwendungsgeheimnis oder Zertifikat, das nur die Adapteranwendung hat.

Nachdem der Benutzer oder die Anwendung authentifiziert wurde, um Anrufe an Dataverse zu tätigen, werden Berechtigungsprüfungen auf Dataverse-Ebene für jede Anfrage durchgeführt. Diese Überprüfungen stellen sicher, dass der Aufrufer (die Identität der Adapteranwendung, die als „\<guid A\>“ im Diagramm bezeichent) über die entsprechenden Anwendungsberechtigungen verfügt. Die Autorisierung auf Anwendungsebene wird in Dataverse über einen Anwendungsbenutzer verwaltet, der die Anwendungs-ID des Adapters darstellt. Berechtigungen auf Anwendungsebene werden verwaltet, indem Zugriff auf bestimmte Dataverse-definierte Anwendungsrollen gewährt wird. Diese Rollen bieten der Anwendung granulare Berechtigungen.

Detailliertere Anleitungen finden Sie unter [Verwenden Sie die Server-zu-Server-Authentifizierung für mehrere Mandanten](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication)

Wenn Dataverse-Level-Anwendungsberechtigungsprüfungen bestanden werden, ruft das Plug-In für virtuelle Entitäten den Dienstendpunkt für virtuelle Entitäten in der Finanz- oder Personalumgebung auf. Für diesen Anruf wird Server-zu-Server-Authentifizierung (S2S) verwendet. Es verwendet die Identität und das Geheimnis, die im Konfigurationsdatensatz der virtuellen Datenquelle von Finanzen und Betrieb konfiguriert sind.

![Konfigurationsdatensatz für die virtuelle Datenquelle von Finanzen und Betrieb in der Sandbox-Umgebung.](./media/sandbox.jpg)

Weitere Informationen finden Sie unter [virtuelle Dataverse-Entitäten konfigurieren](/dev-itpro/power-platform/admin-reference).

Der Anruf vom Dataverse Plug-In für virtuelle Entitäten für Finance oder Human Resources enthält die Adapteridentität des ursprünglichen Aufrufs an Dataverse vom Adapter (die Identität, die als „\<guid A\>“ im Architekturdiagramm bezeichnet wird). Wenn die Datenquelle der virtuellen Entität korrekt konfiguriert ist und die S2S-Authentifizierungsprüfungen bestanden sind, führt der Dienst der virtuellen Entität in Finance oder Human Resources die Abfrage im Kontext des ursprünglichen Aufrufers aus (der Adapter, \<guid A\>). Anwendungsberechtigungsprüfungen (Autorisierung) auf Finanz- oder Personalebene werden durchgeführt, um sicherzustellen, dass der Adapter über die Berechtigungen verfügt, die für den Zugriff auf die Datenentitäten erforderlich sind, die durch die Abfrage angefordert werden.

Die Sicherheit von Finance und Human Resources wird auf folgende Weise verwaltet:

1. Durch Zuordnen der Adapteridentität (\<guid A\>) an einen bestimmten Benutzer aus der Finanz- oder Personalabteilung. Diese Zuordnung erfolgt auf der **Azure Active Directory-Anwendungen** Seite. Weitere Informationen finden Sie unter [Registrieren Ihrer externen Anwendung](/dev-itpro/data-entities/services-home-page.md#register-your-external-application).
2. Indem Sie dem Benutzer von Finance oder Human Resources die entsprechenden Rollen, Pflichten und Berechtigungen auf Anwendungsebene gewähren. Weitere Informationen finden Sie unter [Rollenbasierte Sicherheit](/dev-itpro/sysadmin/role-based-security).

Wenn der Adapteranwendung (\<guid A\>) die Berechtigungen erteilt werden, die für den Zugriff auf die angeforderten Daten erforderlich sind, treten die folgenden Ereignisse ein:

1. Die Anforderung wird ausgeführt.
2. Die Daten werden in ihre Dataverse Entitätsseite zurückübersetzt.
3. Die Daten werden an den Adapter zurückgegeben.

> [!IMPORTANT]
> Während der Entwicklung kann der Adapter von einem Benutzer von Finance oder Human Resources ausgeführt werden, der die Administratorrolle hat. In einer Produktionsumgebung sollte der Adapter jedoch niemals mit Administratorrechten ausgeführt werden.

## <a name="key-takeaways"></a>Die zentralen Thesen

Hier sind einige wichtige Auswirkungen der virtuellen Tabellen- oder Entitätsarchitektur:

- Die Sicherheitskonfiguration für virtuelle Tabellen, die von Human Resources unterstützt werden, wird in Human Resources verwaltet.
- Der Kunde („Gegenseitiger Kunde“ im Architekturdiagramm weiter oben in diesem Artikel) hat die volle Kontrolle darüber, welche Berechtigungen der Identität des integrierenden Adapters (bezeichnet als „\<guid A\>“ im Diagramm).
- Der Kunde ist für die korrekte Sicherheitskonfiguration seiner Human Resources-Umgebung verantwortlich. Der Integrationspartner, der den Adapter erstellt, muss Anleitungen zu den Berechtigungen geben, die der Adapter benötigt.
