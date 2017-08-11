---
title: Lokale Umgebungen einrichten und bereitstellen
description: "Dieses Thema enthält Informationen dazu, wie eine On-Premises-Umgebung geplant, eingerichtet und bereitgestellt wird."
author: sarvanisathish
manager: AnnBe
ms.date: 08/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations, Unified Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d100f6dbcbdf8f4c12ab04670fb598a88d48d84b
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: de-de
ms.lasthandoff: 08/10/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Lokale Umgebungen einrichten und bereitstellen

In diesem Dokument wird beschrieben, wie Sie Ihre Bereitstellung planen, die Infrastruktur einrichten und Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (on-premises), bereitstellen.

## <a name="finance-and-operations-components"></a>Finance and Operations-Komponenten

Die Anwendung Finance and Operations besteht aus drei Hauptkomponenten:

- Anwendungsobjektserver (AOS)
- Business Intelligence (BI)
- Financial Reporting/Management Reporter

Diese Komponenten sind von der folgenden Systemsoftware abhängig:

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1, das folgende Funktionen hat:

    - Volltext-Indexsuche ist aktiviert.
    - SQL Server Reporting Services (SSRS).
    - SQL Server Integration Services (SSIS).
    
     > [!NOTE]
     > Die Anwendung wird nicht ausgeführt, wenn „Volltextsuche” nicht aktiviert ist.

- SQL Server Management Studio
- Eigenständiges Microsoft Azure Service Fabric
- Windows PowerShell 5.0 oder höher
- Active Directory-Verbunddienste (AD FS) auf Windows Server 2016

  Der Domänencontroller muss Windows Server 2012 R2 oder höher sein, mit einer Domänenfunktionsebene von 2012 R2 oder höher

  Weitere Informationen zu Domänenfunktionsebenen finden Sie unter: 
  - [Was sind Active Directory-Funktionsebenen](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Grundlegendes zu Active Directory Domain Services-Funktionsebenen](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

Finance and Operations-Bits werden über Microsoft Dynamics Lifecycle Services (LCS) veteilt. Vor der Bereitstellung müssen Sie Lizenzschlüssel über den Kanal [Unternehmensvereinbarungen](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) erwerben und ein On-Premises-Projekt in LCS einrichten. Bereitstellungen können nur durch LCS initiiert werden. Weitere Informationen dazu, wie lokale Projekte in LCS eingerichtet werden, finden Sie unter [Ein On-Premises-Projekt in Lifecycle Services erstellen](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Authentifizierung

Die On-Premises-Anwendung funktioniert mit AD FS. Um mit LCS zu interagieren, müssen Sie auch Azure Active Directory (Azure AD) konfigurieren.

## <a name="standalone-service-fabric"></a>Eigenständiges Service Fabric

Finance and Operations verwendet eingenständiges Service Fabric. Weitere Informationen finden Sie in der [Service Fabric-Dokumentation](/azure/service-fabric/).

## <a name="infrastructure"></a>Infrastruktur

Finance and Operations ist dazu konzipiert, in einer hyperkonvergenten Architektur zu funktionieren. Die Hardwarekonfiguration umfasst die folgenden Komponenten:

- Eigenständiger Service Fabric-Cluster, der auf virtuellen Computern (VMs) von Windows Server 2016 basiert.
- SQL Server (sowohl „Gruppierter SQL” als auch „Immer aktiviert” werden unterstützt)
- AD FS zur Authentifizierung
- Server Message Block (SMB) Version 3 – Dateifreigabe zum Speichern
- Optional: Microsoft Office Server 2017

Weitere Informationen finden Sie unter [Systemanforderungen](../get-started/system-requirements.md) und Größenanpassungsrichtlinien.

### <a name="hardware-layout"></a>Hardwarelayout

Planen Sie Ihre Infrastrutkur und Ihr Service Fabric-Cluster, basierend auf der empfohlenen Größenanpassung in [Hardware-Größenanpassung für On-Premises-Umgebungen](../get-started/hardware-sizing-on-premises-environments.md). Weitere Informationen dazu, wie der Service Fabric-Cluster zu planen ist, finden unter [Planen und Vorbereiten Ihrer eigenständigen Service Fabric-Clusterbereitstellung](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)

In der folgenden Tabelle wird ein Beispiel des Hardwarelayouts angezeigt. Dieses Beispiel wird in diesem gesamten Thema verwendet, um das Setup zu veranschaulichen.

> [!NOTE]
> Der Primärknoten des Service Fabric-Cluster muss mindestens drei Knoten haben. In diesem Beispiel wird **OrchestratorType** als Primärknotentyp festgelegt.

| Computerzweck                                 | Computername    | IP-Adresse    |
|-------------------------------------------------|-----------------|---------------|
| Domänencontroller                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Dateiserver                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL – immer aktivierter Cluster                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Kunde                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric-Cluster/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric-Cluster/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric-Cluster/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric-Cluster/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric-Cluster/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric-Cluster/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Service Fabric-Cluster/Management Reporter-Knoten | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric-Cluster/SSRS-Knoten                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Einstellung

### <a name="prerequisites"></a>Voraussetzungen

Bevor Sie mit den Einstellungen beginnen, müssen die folgenden Voraussetzungen erfüllt sein. Die Einstellungen dieser Voraussetzungen liegt außerhalb des Rahmens dieses Dokuments.

- Active Directory Domain Services (AD DS) ist in Ihrem Netzwerk installiert und konfiguriert.
- AD FS ist bereitgestellt.
- SQL Server, SSRS und Management Studio sind installiert.

### <a name="overview"></a>Überblick

Die folgenden Schritte müssen abgeschlossen sein, um die Infrastruktur für Finance and Operations einzurichten.

1. Ihren Domänennamen und DNS-Zonen planen
2. Ihre Zertifikate planen und abrufen
3. Ihre Benutzer und Servicekonten planen
4. DNS-Zonen erstellen und A-Datensätze hinzufügen
5. VMs mit der Domäne verknüpfen
6. Vorausgesetzte Software den VMs hinzufügen
7. Einstellungsskripts von LCS herunterladen
8. Ihre Konfiguration beschreiben
9. Zertifikate installieren
10. Einen eigenständigen Service Fabric-Cluster einrichten
11. LCS-Konnektivität für den Mandanten konfigurieren
12. Dateispeicher einrichten
13. SQL Server einrichten
14. Die Datenbanken konfigurieren
15. Anmeldeinformationen verschlüsseln
16. SSRS einrichten
17. AD FS konfigurieren

### <a name="plan-your-domain-name-and-dns-zones"></a>Ihren Domänennamen und DNS-Zonen planen

Es wird empfohlen, dass Sie einen öffentlich registrierten Domänennamen für Ihre Produktionsinstallation von Microsoft Dynamics AX Application Object Server (AOS) verwenden. Auf diese Weise kann auf sie von außerhalb des Netzwerks zugegriffen werden, wenn der Zugriff von außen erforderlich ist.

Wenn beispielsweise die Domäne Ihres Unternehmens contoso.com ist, könnte Ihre Zone für Finance and Operations (on-premises) d365ffo.onprem.contoso.com sein, und die Hostnamen könnten folgende sein:

- ax.d365ffo.onprem.contoso.com für AOS-Computer
- sf.d365ffo.onprem.contoso.com für den Service Fabric-Cluster

### <a name="plan-and-acquire-your-certificates"></a>Ihre Zertifikate planen und abrufen

Secure Sockets Layer (SSL)-Zertifikate werden benötigt, um einen Service Fabric-Cluster und alle die Anwendungen zu sichern, die bereitgestellt werden. Für die Produktions- und Sandbox-Workloads empfehlen wir, dass Sie Zertifikate von einer Zertifizierungsstelle (CA) abrufen, wie beispielsweise [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) oder [GlobalSign](https://www.globalsign.com/en/ssl/). Wenn Ihre Domäne mit [Active Directory-Zertifikatdienste](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS) eingerichtet ist, können Sie die Zertifikate durch AD CS erstellen. Jedes Zertifikat muss einen privaten Schlüssel enthalten, der für den Schlüsselaustausch erstellt wurde, und es muss in eine Datei für den privaten Informationsaustausch (.pfx) exportiert werden können.

Selbstsignierte Zertifikate können nur für Testzwecke verwendet werden. Für die Benutzerfreundlichkeit enthalten die Einstellungsskripts Skripts, die selbstsignierte Zertifikate generieren und exportieren. Wie wir erwähnt haben, dürfen diese Bescheinigungen nur für Testzwecke verwendet werden.

| Kostenträger                                      | Erläuterung | Zusätzliche Anforderungen |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL-Zertifikat                   | Dieses Zertifikat wird verwendet, um Daten zu verschlüsseln, die innerhalb eines Netzwerks zwischen einer Instanz von SQL Server und einer Client-Anwendung übertragen werden. | <p>Der Domänenname des Zertifikats sollte mit dem vollqualifizierten Domänennamen (FQDN) von SQL Server-Instanz oder -Listener übereinstimmen.</p><p>Wenn beispielsweise der SQL-Listener auf dem Computer DAX7SQLAOSQLA gehostet wird, ist der DNS-Name des Zertifikats DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| Service Fabric Server-Zertifikat            | Dieses Zertifikat wird verwendet, um damit die Knoten-zu-Knoten-Kommunikation zwischen den Service Fabric-Knoten zu sichern. Dieses Zertifikat wird auch als das Server-Zertifikat verwendet, das dem Client präsentiert wird, der sich mit dem Cluster verbindet. | <p>Der Domännenname des Zertifikats muss mit der DNS-Zone übereinstimmen, in der Microsoft Dynamics AX Application Object Server (AOS) und Service Fabric gehostet werden.</p><p>Beispielsweise könnte der Domänenname des Zertifikats \*.onprem.contoso.com or \*.contoso.com sein.</p><p>Wenn Sie ein Platzhalterzertifikat verwenden, gilt das Platzhalterzeichen nur für eine Ebene. Eine Unterdomäne, alternativer Antragstellername (SAN), muss auf das Zertifikat angewendet werden, wenn es sich dabei um mehr als eine Ebene handelt, wie beispielsweise \*.contoso.com im vorherigen Beispiel.</p> |
| Service Fabric Client-Zertifikat            | Dieses Zertifikat wird von Clients verwendet, um das Service Fabric-Cluster anzuzeigen und zu verwalten. | |
| Verschlüsselungszertifikat                     | Dieses Zertifikat wird verwendet, um vertrauliche Informationen zu verschlüsseln, wie beispielsweise das SQL Server-Kennwort und Benutzerkontenkennwörter. | <p>Die Zertifikatschlüsselverwendung muss Datenverschlüsselung (10) verwenden und sollte nicht Serverauthentifizierung oder Clientauthentifizierung enthalten.</p><p>Weitere Informationen finden Sie unter [Geheimnisse in Service Fabric-Anwendungen verwalten](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| AOS SSL-Zertifikat                          | <p>Dieses Zertifikat wird auch als das Server-Zertifikat verwendet, das dem Client für die AOS-Website präsentiert wird. Es wird auch verwendet, um Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP)-Zertifikate zu aktivieren.</p><p>Das Service Fabric Server-Zertifikat kann hier verwendet werden, wenn es ein Platzhalterzertifikat ist.</p> | <p>Der Domännenname des Zertifikats muss mit der DNS-Zone übereinstimmen, in der Microsoft Dynamics AX Application Object Server (AOS) und Service Fabric gehostet werden.</p><p>Beispielsweise könnte der Domänenname des Zertifikats \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com oder \*.contoso.com sein.</p><p>Wenn Sie ein Platzhalterzertifikat verwenden, gilt der Platzhalter nur für eine Ebene. Eine Unterdomäne, SAN, muss auf das Zertifikat angewendet werden, wenn es sich dabei um mehr als eine Ebene handelt, wie beispielsweise \*.contoso.com im vorherigen Beispiel.</p> |
| Sitzungsauthentifizierungszertifikat           | Dieses Zertifikat wird von AOS verwendet, um die Sitzungsinformationen eines Benutzers zu sichern. | Dies ist auch das **Dateifreigabe**-Zertifikat, das zum Zeitpunkt der Bereitstellung von LCS verwendet wird. |
| Datenverschlüsselung und Datensignierungszertifikat | Diese Zertifikat werden von AOS verwendet, um vertrauliche Informationen zu verschlüsseln. | |
| Financial Reporting-Clientzertifikat       | Dieses Zertifikat wird verwendet, um damit die Kommunikation zwischen den Financial Reporting-Services und AOS zu sichern. | |
| Reporting-Zertifikat                        | Dieses Zertifikat wird verwendet, um damit die Kommunikation zwischen SSRS und AOS zu sichern. | |
| Lokales On-Premise-Agentzertifikat           | <p>Dieses Zertifikat wird verwendet, um die Kommunikation zwischen einem lokalen Agent, der on-premises verwaltet wird und LCS sicherzustellen.</p><p>Dieses Zertifikat ermöglicht es dem lokalen Agent im Auftrag Ihres Azure AD-Mandanten zu handeln und mit LCS zu kommunizieren, um Bereitstellungen zu orchestrieren und zu überwachen.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Ihre Benutzer und Servicekonten planen

Sie müssen mehrere Benutzer- oder Servicekonten für Finance and Operations (on-premises) erstellen, um zu arbeiten. Sie müssen eine Kombination aus gruppenverwalteten Servicekonten (gMSAs), Domänenkonten und SQL-Konten erstellen. In der folgenden Tabelle werden die Benutzerkonten angezeigt, ihr Zwecke und Beispielnamen, die in diesem Thema verwendet werden.

| Benutzerkonto                                            | Typ           | Kostenträger | Benutzername |
|---------------------------------------------------------|----------------|---------|-----------|
| Dienstkonto der Finanzberichterstattungsanwendung         | gMSA           |         | Contoso\\svc-FRAS$ |
| Dienstkonto des Finanzberichterstattungsprozesses             | gMSA           |         | Contoso\\svc-FRPS$ |
| Dienstkonto für Einfachklick-Designer für Finanzberichterstattung | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS-Dienstkonto                                     | gMSA           | Dieser Benutzer sollte für die Zukunftssicherheit erstellt werden. Wir planen, die Zusammenarbeit von AOS mit der gMSA bei zukünftigen Versionen zu ermöglichen. Durch das Erstellen dieses Benutzers zum Zeitpunkt des Setup tragen zur Sicherstellung eines nahtlosen Übergangs zur gMSA bei. | Contoso\\svc-AXSF$ |
| AOS-Dienstkonto                                     | Domänenkonto | AOS verwendet diesen Benutzer in der GA-Version. | Contoso\\AXServiceUser |
| AOS SQL-Datenbankadministrator-Benutzer                                   | SQL-Benutzer       | Finance and Operations verwendet diesen Benutzer für die Authentifizierung bei SQL\*. Dieser Benutzer wird auch vom gMSA-Benutzer in den bevorstehenden Versionen ersetzt. | AXDBAdmin |
| Dienstkonto für lokalen Bereitstellungsagent                  | gMSA           | Dieses Konto wird vom lokalen Agenten verwendet, um die Bereitstellung in verschiedenen Knoten zu orchestrieren. | Contoso\\Svc-LocalAgent$ |

\* Der SQL-Benutzername und das Kennwort für die SQL-Authentifizierung werden gesichert, da sie in der Dateifreigabe verschlüsselt und gespeichert werden.

### <a name="create-dns-zones-and-add-a-records"></a>DNS-Zonen erstellen und A-Datensätze hinzufügen

DNS wird mit AD DS integriert und Sie können damit Ressourcen in einem Netzwerk organisieren, verwalten und suchen. Erstellen Sie eine DNS-Forward-Lookup-Zone und A-Datensätze für den AOS-Hostnamen und den Service Fabric-Cluster. In dieser Beispieleinstellung ist der DNS-Zonenname d365ffo.onprem.contoso.com und die A-Datensatz-/Hostnamen sind folgende:

- **ax**.d365ffo.onprem.contoso.com für AOS-Computer
- **sf**.d365ffo.onprem.contoso.com für den Service Fabric-Cluster

#### <a name="add-a-dns-zone"></a>Eine DNS-Zone hinzufügen

Gehen Sie dazu folgendermaßen vor, um eine DNS-Zone hinzuzufügen.

1. Melden Sie sich beim Domänencontrollercomputer an, klicken Sie auf **Start**, und starten Sie DNS-Manager, indem Sie **dnsmgmt.msc** eingeben.
2. Klicken Sie mit der rechten Maustaste auf den Domänencontrollername, und klicken Sie dann auf Neue Zone und anschließend auf **Neue Zone** \> **Weiter**.
3. Wählen Sie **Primäre Zone** aus.
4. Lassen Sie das Kontrollkästchen **Die Zone in Active Directory speichern (nur verfügbar, wenn der DNS Server ein beschreibbarer Domänencontroller ist)** aktiviert, und klicken Sie dann auf **Weiter**.
5. Wählen Sie **An alle DNS-Server, die auf Domänencontrollern in dieser Domäne ausgeführt werden: Contoso.com** aus, und klicken Sie dann auf **Weiter**.
6. Wählen Sie **Forward Lookup-Zone** aus, und klicken Sie dann auf **Weiter**.
7. Geben Sie den Zonennamen für die Einstellungen ein, und klicken Sie dann auf **Weiter** Geben Sie beispielsweise **d365ffo.onprem.contoso.com** ein.
8. Wählen Sie **Keine dynamischen Updates zulassen** aus, und klicken Sie dann auf **Weiter**.

#### <a name="set-up-an-a-record-for-aos"></a>Einrichten eines A-Datensatzes für AOS

In der neuen DNS-Zone erstellen Sie einen A-Datensatz mit der Bezeichnung **ax.d365ffo.onprem.contoso.com** für **jeden** Service Fabric-Clusterknoten des Typs **AOSNodeType**. Erstellen Sie keinen A-Datensatz für die anderen Knotentypen.

1. Klicken Sie mit der rechten Maustaste auf die neue Zone, und klicken Sie anschließend auf **Neuer Host**.
2. Geben Sie den Namen und die IP-Adresse des Service Fabric-Knotens ein (z. B. 10.179.108.12), und klicken Sie dann auf **Host hinzufügen**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Einrichten eines A-Datensatzes für den Orchestrator

In der neuen DNS-Zone erstellen Sie einen A-Datensatz mit der Bezeichnung **sf.d365ffo.onprem.contoso.com** für **jeden** Service Fabric-Clusterknoten des Typs **OrchestratorType**. Erstellen Sie keinen A-Datensatz für die anderen Knotentypen.

1. Klicken Sie mit der rechten Maustaste auf die neue Zone, und klicken Sie anschließend auf **Neuer Host**.
2. Geben Sie den Namen und die IP-Adresse des Service Fabric-Knotens ein (z. B. 10.179.108.15), und klicken Sie dann auf **Host hinzufügen**.

#### <a name="join-vms-to-the-domain"></a>VMs mit der Domäne verknüpfen

Verknüpfen Sie jede der VMs mit der Domäne, indem Sie die Schritte in [Vorgehensweise bei der Verknüpfung von Windows Server 2016 mit einer Active Directory-Domäne](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html) ausführen. Alternativ können Sie das Windows PowerShell-Skript verwenden.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
Sobald die VMs mit der Domäne verknüpft sind, fügen Sie die AOS-Dienstkonten (Contoso\svc-AXSF$ , Contoso\svc-AXSF$ ) der lokalen Administratorengruppe hinzu. Sie können im Artikel [Der lokalen Gruppe ein Mitglied hinzufügen](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) nachlesen, wie Sie dabei vorgehen.

#### <a name="disable-user-access-control"></a>Benutzerzugriffssteuerung deaktivieren 

Führen Sie das folgende Skript aus, um die Benutzerzugriffssteuerung in **jedem** Service Fabric-Knoten zu deaktivieren.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> Sie müssen den Knoten neu starten, nachdem das Skript erfolgreich abgeschlossen wurde.

#### <a name="add-prerequisite-software-to-vms"></a>Vorausgesetzte Software den VMs hinzufügen

In der folgenden Tabelle wird die erforderliche Software aufgelistet, die auf den Computern jedes Knotentyps eingerichtet werden muss.

> [!NOTE]
> Sie müssen Ihren Computer neu starten, nachdem Sie die Komponenten installieren.

| Knotentyp | Bestandteil | Befehl |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC-Treiber | Siehe [Microsoft ODBC Driver 13.1 for SQL Server - Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Die Microsoft .NET Framework-Version 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Die Microsoft .NET Framework-Version 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Internetinformationsdienste (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual C++ Redistributable Packages für Microsoft Visual Studio 2013 | Siehe [Microsoft Visual C++ Redistributable Packages für Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Microsoft Access Database Engine 2010 Redistributable | Siehe [Microsoft Access Database Engine 2010 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | Die .NET Framework-Version 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | Die .NET Framework-Version 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Server Reporting Services 2016 im **einheitlichen** Modus | |
| MR        | Die .NET Framework-Version 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | Die .NET Framework-Version 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual C++ Redistributable Packages für Visual Studio 2013 | Siehe [Microsoft Visual C++ Redistributable Packages für Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Einstellungsskripts von LCS herunterladen

Wir haben mehrere Skripts bereitgestellt, um damit die Benutzerfreundlichkeit des Setup zu erhöhen. Gehen Sie folgendermaßen vor, um die Setupskripts von LCS herunterzuladen.

1. Melden Sie sich bei LCS an (<https://lcs.dynamics.com/v2>).
2. Klicken Sie im Dashboard auf die Kachel **Bibliothek freigegebener Anlagen**.
3. Klicken Sie auf die Registerkarte **Modell**.
4. Im Raster wählen Sie die Zeile **Dynamics 365 for Operations – On-Premises-Bereitstellungsskripts** aus.
5. Klicken Sie auf **Versionen**, und laden Sie die neueste Version der Skripts herunter.

### <a name="describe-your-configuration"></a>Ihre Konfiguration beschreiben

Dieser Abschnitt enthält Informationen über die Skripts, die Sie ausführen müssen. Die Skripts werden in der Reihenfolge behandelt, in der Sie diese ausführen müssen. Um die Skripts auszuführen, füllen Sie die Vorlagendatei in $(downloadPath)\\ConfigTemplate.xml aus. Die ConfigTemplate.xml-Datei beschreibt die Service Fabric-Cluster, die Zertifikate, die verwendet werden, um sie zu konfigurieren und die Konten, für die Zugriff auf die relevanten Zertifikate gewährt werden muss. Im angegebenen Beispiel werden die Werte für die Beispielinfrastruktur ausgefüllt, die in diesem Thema beschrieben wird. Die Vorlagendatei wird im nächsten Abschnitt verwendet.

#### <a name="create-the-domain-account-for-a-service-user"></a>Erstellen des Domänenkontos für einen Servicebenutzer

Führen Sie den folgenden Befehl aus, um das Domänenbenutzerkonto contoso\\AXServiceUser zu erstellen.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>gMSAs erstellen

1. Ändern Sie das Verzeichnis zu **$(DownloadPath)**, und führen Sie den folgenden aus Windows PowerShell-Befehl aus.

    > [!NOTE]
    > Durch dieses Skript werden nicht die Benutzer erstellt. Stattdessen druckt das Skript die Befehle, die manuell im Domänencontrollercomputer ausgeführt werden müssen.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Kopieren Sie die Ausgabe des Befehls in ein Windows PowerShell-Fenster. Stellen Sie sicher, dass die Zeilenumbrüche entfernt werden, und führen Sie die Zeilen im Active Directory-Domänencontrollercomputer aus, indem Sie erhöhte Rechte verwenden (Rechtsklick und klicken Sie dann auf **Als Administrator ausführen**).
3. Führen Sie das folgende Skript im Active Directory-Domänencontrollercomputer aus, um zu überprüfen, dass die Konten erfolgreich erstellt wurden. Stellen Sie sicher, dass Sie das Skript ausführen, nachdem Sie das Muster ersetzt haben, das mit der Namenskonvention der Dienstkonten übereinstimmt.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Führen Sie das Skript Export-AddGMSAsONVMScript.ps1 auf dem Clientcomputer aus. Dieses Skript generiert Skripts, die in jedem virtuellen Sevice Fabric-Computer ausgeführt werden und fügt sie einem Ordner hinzu, der jedem Name eines virtuellen Computers entspricht.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>IIS beenden

Verwenden Sie das Remotedesktopprotokoll (RDP), um mit jedem virtuellen Service Fabric-Computer eine Verbindung herzustellen, und schließen Sie die manuellen Schritte in [Den Webserver (IIS 7) starten und beenden](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx) ab. Alternativ können Sie das folgende Windows PowerShell-Skript mithilfe von RDP verwenden, um eine Verbindung mit jedem virtuellen Service Fabric-Computer herzustellen.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_IIS-Funktion sollten eingerichtet aber deaktiviert werden, da es einige Abhängigkeiten zu den IIS-dlls im Produkt gibt._

### <a name="install-certificates"></a>Zertifikate installieren

1. Wenn Sie die Zertifikate, die zuvor in diesem Thema aufgelistet waren, von einer gültigen Zertifizierungsstelle abgerufen haben, füllen Sie den Namen der PFX-Datei und den Fingerabdruck für die Zertifikate in der Datei ConfigTemplate.xml aus. Legen Sie das Attribut **generateSelfSignedCert** auf **FALSE** und das Attribut **exportable** auf **FALSE** fest. Kopieren Sie die PFX-Dateien in den Ordner $(DownloadPath)\\InfrastructureScripts\\Certs.
2. Wenn Sie selbstsignierte Zertifikate verwenden (nur zu Testzwecken), führen Sie das folgende Skript aus. Um selbstsignierte Zertifikate in der Datei ConfigTemplate.xml zu erstellen, stellen Sie sicher, dass **generateSelfSignedCert** auf **TRUE** und **exportable** auf **TRUE** festgelegt ist. Das Skript aktualisiert die XML mit dem Fingerabdruck für die Zertifikate.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Exportieren Sie die neuen Zertifikate mit dem privaten Schlüssel (die PFX-Datei). Verwenden Sie folgendes Skript, um die Exportbefehle in Windows PowerShell zu generieren und auszuführen. Die PFX-Dateien werden in den Ordner „Certs” abgelegt.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Die Zertifikate müssen installiert sein und müssen in cert:\\CurrentUser\\My vorhanden sein. Die Zertifikate müssen auch exportierbar sein.

    Wenn Sie selbstsignierte Zertifikate verwenden, fahren Sie mit dem nächsten Abschnitt fort. Sie müssen diese Prozedur nicht abschließen.

4. Nachdem Sie die PFX-Dateien in den Ordner $(DownloadPath)\\InfrastructureScripts\\Certs exportieren oder kopieren, führen Sie die folgenden Befehle aus, um Skripte zu generieren, die in den Ordnern abgelegt werden, die den virtuellen Computern entsprechen.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Kopieren Sie die Skripts in jedem Ordner zu den virtuellen Computern, die dem Ordnername entsprechen.
6. Führen Sie in jedem virtuellen Computer die folgenden Schritte in der Reihenfolge aus, in der sie angezeigt werden.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Einrichten eines eigenständigen Service Fabric-Cluster

1. Führen Sie den folgenden Befehl aus, um die Datei ClusterConfig.json zu generieren.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Weitere Informationen finden Sie unter [Schritt 1B: Erstellen eines Clusters für mehrere Computer](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Sichern eines eigenständigen Clusters in Windows mithilfe von X.509-Zertifikaten](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) und [Erstellen eines eigenständigen Clusters, der auf Windows Server ausgeführt wird](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Laden Sie das [Eigenständige Service Fabric-Installationspaket](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) zu einem Ihrer Service Fabric-Knoten herunter. Nachdem die ZIP-Datei heruntergeladen ist, entsperren Sie diese, indem Sie mit der rechten Maustaste auf die ZIP-Datei klicken und dann auf **Eigenschaften** klicken. Aktivieren Sie im Dialogfeld das Kontrollkästchen **Entsperren** unten rechts.
3. Kopieren Sie die ZIP-Datei zu einem der Knoten im Service Fabric-Cluster, und entzippen Sie sie.
4. Führen Sie die folgenden Befehle aus, um eine eingehende Firewallregel für Ports 443 und 445 in allen Knoten zu erstellen.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Führen Sie die folgenden Befehle aus, um eine eingehende Firewallregel für Port 80 ausschließlich für den SSRS-Knoten zu erstellen.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Kopieren Sie die Datei ClusterConfig.json zu Ihrem entzippten Installationsspeicherort des eigenständigen Service Fabric.
7. Navigieren Sie zum entzippten Installationsspeicherort in Windows PowerShell, indem Sie erweiterte Rechte verwenden, und führen Sie den folgenden Befehl aus, um ClusterConfig zu testen.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Wenn der Test erfolgreich ist, führen Sie den folgenden Befehl aus, um den Cluster bereitzustellen.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Nachdem der Cluster erstellt ist, öffnen Sie den Service Fabric-Explorer auf irgendeinem Clientcomputer, um die Installation zu überprüfen:

    1. Installieren Sie das Service Fabric-Clientzertifikat in certificate in CurrentUser\\My, wenn es nicht bereits installiert ist.
    2. Wechseln Sie zu **IE-Einstellungen** \> **Kompatibilitätsmodus**, und deaktivieren Sie das Kontrollkästchen **Intranet-Websites im Kompatibilitätsmodus anzeigen**.
    3. Navigieren Sie zu `https://sf.d365ffo.onprem.contoso.com:19080`, wo sf.d365ffo.onprem.contoso.com der Hostname des Service Fabric-Clusters ist, der in der Zone angegeben ist. Wenn die DNS-Namensauflösung nicht konfiguriert ist, verwenden Sie die IP-Adresse des Computers.
    4. Wählen Sie das Clientzertifikat aus. Die Seite **Service Fabric-Explorer** wird angezeigt.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>LCS-Konnektivität für den Mandanten konfigurieren

Bereitstellung und Wartung von Finance and Operations werden durch LCS orchestriert, indem ein lokaler On-Premises-Agent verwendet wird. Um die Konnektivität zwischen LCS und dem Finance and Operations-Mandanten herzustellen, müssen Sie ein Zertifikat konfigurieren, mit dem der lokale Agent im Auftrag Ihres Azure AD-Mandanten agieren kann (beispielsweise Contoso.Onmicrosoft.com).

Verwenden Sie das On-Premises-Agentzertifikat, das Sie von einer Zertifizierungsstelle abgerufen haben oder das selbstsignierte Zertifikat, das Sie mithilfe von Skripts generiert haben.

Nur Benutzerkonten, die die Verzeichnisrolle Globaler Administrator haben, können Zertifikate hinzufügen, um LCS zu autorisieren. Standardmäßig ist die Person, die sich für Ihre Organisation für Microsoft Office 365 registriert, der globale Administrator für das Verzeichnis.

> [!NOTE]
> Sie müssen das Zertifikat genau einmal pro Mandant konfigurieren. Alle On-Premises-Umgebungen können dasselbe Zertifikat verwenden, um eine Verbindung mit LCS herzustellen.

1. Laden Sie die neueste Version von Azure PowerShell auf einen Clientcomputer herunter und installieren Sie sie dort. Weitere Informationen finden Sie unter [Azure PowerShell installieren und konfigurieren](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Melden Sie sich beim [Azure-Portal des Debitors](https://portal.azure.com) an, um zu überprüfen, ob Sie die Verzeichnisrolle „Globaler Administrator” haben.
3. Führen Sie das folgende Skript von $(DownloadPath)\\InfrastructureScripts aus.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Dateispeicher einrichten

Sie müssen zwei hoch verfügbare SMB 3.0-Dateifreigaben einrichten. Weitere Informationen zum Aktivieren von SMB 3.0 finden Sie unter[SMB-Sicherheitsverbesserungen](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Sichere Dialektaushandlung kann Herabstufungen von SMB 2.0 oder 3.0 nach SMB 1.0 nicht entdecken oder verhindern. Deshalb und um die volle Funktionalität der SMB-Verschlüsselung auszunutzen, wird dringend empfohlen, dass Sie den SMB 1.0-Server deaktivieren

> [!NOTE]
> Zur Sicherstellung, dass Ihre Daten geschützt sind, während sie sich in Ihrer Umgebung befinden, muss BitLocker-Laufwerkverschlüsselung auf jedem Computer aktiviert sein. Informationen darüber, wie BitLocker aktiviert wird, finden Sie unter [BitLocker: Vorgehensweise bei der Bereitstellung auf Windows Server 2012 und später](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- Eine Dateifreigabe, die Benutzerdokumente speichert, die nach AOS hochgeladen werden (beispielsweise \\\\DAX7SQLAOFILE1\\aos-storage).
- Eine Dateifreigabe, die die aktuellsten Build- und Konfigurationsdateien speichert, um die Bereitstellung zu orchestrieren (beispielsweise \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > Halten Sie diesen Dateifreigabepfad so kurz wie möglich, um zu vermeiden, dass die maximale Pfadlänge bei den Dateien überschritten wird, die in der Freigabe abgelegt werden.

1. Führen Sie auf dem Dateifreigabecomputer den folgenden Befehle aus.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>Einrichten der Dateifreigabe \\\\DAX7SQLAOFILE1\\aos-storage

2. Im Server Manager wählen Sie **Datei- und Speicherdienste** \> **Freigaben** aus.
3. Klicken Sie auf **Aufgaben** \> **Neue Freigabe**, um eine neue Freigabe mit Namen **aos-storage** zu erstellen.
4. Gewähren Sie Berechtigungen zum **Ändern** für jeden Computer im Service Fabric-Cluster, mit Ausnahme von **OrchestratorNodeType**.
5. Gewähren Sie Berechtigungen zum **Ändern** für den Benutzer der Benutzer-AOS-Domäne (contoso\\AXServiceUser) und den gMSA-Benutzer (contoso\\svc-AXSF).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>Einrichten der Dateifreigabe \\\\DAX7SQLAOFILE1\\agent

6. Kehren Sie zurück zum Server Manager, wählen Sie **Datei- und Speicherdienste** \> **Freigaben** aus.
7. Klicken Sie auf **Aufgaben** \> **Neue Freigabe**, um eine neue Freigabe mit Namen **agent** zu erstellen.
8. Gewähren Sie dem gMSA-Benutzer Berechtigungen zum **Vollzugriff** für den lokalen Bereitstellungsagent (contoso\\svc-LocalAgent$).

### <a name="set-up-sql-server"></a>SQL Server einrichten

1. Installieren Sie SQL Server 2016 SP1 mit hoher Verfügbarkeit, entweder als SQL-Cluster, die ein Storage Area Network (SAN) umfassen, oder in einer „Always-On”-Konfiguration.  Überprüfen Sie, ob die **Datenbankmodul, Reporting Services, Volltextsuche** und **Verwaltungstools** bereits installiert sind.
> [!NOTE]
> Stellen Sie bitte sicher, dass SQL Always On gemäß folgender Anleitung eingerichtet ist [Anfangsseite der Datensynchronisierung auswählen (Always-On-Verfügbarkeitsgruppen-Assistenten)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) und folgen Sie den Anleitungen in [Vorgehensweise beim manuellen Vorbereiten sekundärer Datenbanken](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. Führen Sie den SQL-Dienst als Domänenbenutzer aus.
3. Rufen Sie ein SSL-Zertifikat von einer Zertifizierungsstelle ab, um Finance and Operations zu konfigurieren. Zu Testzwecken können Sie ein selbstsigniertes Zertifikat erstellten und verwenden.

**Selbstsigniertes Zertifikat für gruppierte SQL-Instanz**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Selbstsigniertes Zertifikat für Always-On-SQL-Instanz**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. Führen Sie unter Verwendung des Zertifikats die Schritte aus in [Vorgehensweise bei der Aktivierung der SSL-Verschlüsselung für eine Instanz von SQL Server mithilfe von Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console), um SSL in SQL Server zu konfigurieren.
5. Führen Sie für jeden Knoten des Clusters diese Schritte aus. Stellen Sie sicher, dass Sie die Änderungen am inaktiven Knoten vornehmen und zu ihm einen Failover ausführen, nachdem Änderungen vorgenommen wurden.

    1. Importieren Sie das Zertifikat in LocalMachine\\My.
    2. Gewähren Sie dem Dienstkonto, das zum Ausführen des SQL-Diensts verwendet wird, Zertifikatsberechtigungen. In der Microsoft Management Console (MMC) klicken Sie mit der rechten Maustaste auf das Zertifikat (certlm.msc), und klicken Sie dann auf **Aufgaben** \> **Private Schlüssel verwalten**.
    3. Fügen Sie den Zertifikatsfingerabdruck zu HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate hinzu.
    4. Legen Sie in Microsoft SQL Server-Konfigurations-Manager **ForceEncryption** auf **Ja** fest.

6. Exportieren Sie den öffentlichen Schlüssel des Zertifikats (die CER-Datei), und installieren Sie diesen im vertrauenswürdigen Stamm von jedem Service Fabric-Knoten.

### <a name="configure-the-orchestratordata-database"></a>Konfigurieren der OrchestratorData-Datenbank

1.  Erstellen Sie eine leere Datenbank und nennen Sie diese **OrchestratorData**. Diese Datenbank wird vom lokalen On-Premises-Agenten verwendet, um Bereitstellungen zu orchestrieren.
2.  Gewähren Sie dem lokalen Agenten gMSA-(svc-LocalAgent$) **db\_owner**-Berechtigungen für die Datenbank:

    1. In der Struktur erweitern Sie den Servernamen, erweitern Sie **Sicherheit** \> **Anmeldungen**, und klicken Sie dann mit der rechten Maustaste auf **Neue Anmeldung**.

        ![Befehl „Neue Anmeldung”](./media/OPSetup_01_NewLogin.png)


    2. Suchen Sie das Dienstkonto **svc-LocalAgent$**. Klicken Sie auf **Speicherorte**, und wählen Sie **Gesamtes Verzeichnis** aus, und klicken Sie dann auf **Objekttypen**, und wählen Sie **Dienstkonto** aus.

        ![Wählen Sie das Dialogfeld „Benutzer”, „Dienstkonto” oder „Gruppe” aus](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Legen Sie **ServerRole zuweisen** auf **Öffentlich** fest.
    4. Weisen Sie die Rollenberechtigung **db\_owner** der Datenbank „OrchestratorData” zu.

### <a name="configure-the-finance-and-operations-database"></a>Konfigurieren der Finance and Operations-Datenbank

1. Melden Sie sich bei LCS an (<https://lcs.dynamics.com/v2>).
2. Klicken Sie im Dashboard auf die Kachel **Bibliothek freigegebener Anlagen**.
3. Auf die Registerkarte **Modell** klicken 
4. Klicken Sie im Raster auf die Zeile **Dynamics 365 for Operations on-premises, Enterprise Edition – Demodaten**, um das ZIP herunterzuladen.
5. ZIP enthält leere BAK-Dateien und solche mit Demodaten. Auf Basis Ihrer Anforderungen entnehmen Sie die entsprechende BAK-Datei. Wenn Sie beispielsweise Demodaten benötigen, stellen Sie die Datei AxBootstrapDB_Demodata.bak wieder her. 
6. Stellen Sie die Datenbank AxBootstrapDB_DemoData.bak wieder her.
7. Benennen Sie die Datenbank **AXDBRAIN** um.
8. Führen Sie die folgenden Abfragen bei der wiederhergestellten Datenbank aus.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Aktualisieren Sie die Datenbankdateien:

    1. Klicken Sie mit der rechten Maustaste auf die Datenbank, und klicken Sie dann auf **Eigenschaften**.
    2. Klicken Sie auf **Dateien**, um die Datenbankdateieigenschaften zu ändern.
    3. Geben Sie im Feld **Ausgangsgröße (MB)** einen Wert ein, der größer als 5.120 ist.

        ![Dialogfeld „Datenbankeigenschaften”](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. Für **AXDBBuild\_Data** legen Sie das Feld **Automatische Vergrößerung/Maximierung** auf **200** Megabytes (MB) fest.
    5. Für **AXDBBuild\_Log** legen Sie das Feld **Automatische Vergrößerung/Maximierung** auf **500** MB fest.

        ![Ändern des Dialogfelds „Automatische Vergrößerung”](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Erstellen Sie einen neuen Benutzer, bei dem die SQL-Authentifizierung aktiviert ist (axdbadmin).
6. Verwenden Sie die Informationen in der folgenden Tabelle, um die Benutzer und Datenbankrollen zuzuordnen.

    | Benutzer             | Typ    | Datenbankrolle |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. Geben Sie dem „svc-AXSF$”-Benutzer und dem „axdbadmin SQL”-Benutzer Zugriff auf die folgenden Rollen in der Datenbank „tempdb”:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. In Management Studio führen Sie die folgenden „Transact SQL (T-SQL)”-Befehle aus:

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Führen Sie den folgenden Befehl aus:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Konfigurieren der „Financial Reporting”-Datenbank

1.  Erstellen Sie eine leere Datenbank und nennen Sie diese **FinancialReporting**.
2.  Verwenden Sie die Informationen in der folgenden Tabelle, um die Benutzer und Datenbankrollen zuzuordnen.

    | Benutzer             | Typ | Datenbankrolle |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>Anmeldeinformationen verschlüsseln

1. Auf jedem Clientcomputer installieren Sie das Verschlüsselungszertifikat im Zertifikatsspeicher LocalMachine\\My.
2. Gewähren Sie dem aktuellen Benutzer Lesezugriff auf den privaten Schlüssel dieses Zertifikats.
3. Erstellen Sie die Datei Credentials.json, wie hier angezeigt.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** ist das verschlüsselte Domänenbenutzerkennwort für den AOS-Domänenbenutzer (contoso\\axserviceuser).
    - **SqlUser** ist der verschlüsselte SQL-Benutzer (axdbadmin), der Zugriff auf die Finance and Operations-Datenbank (AXDBRAIN) hat, und **SqlPassword** ist das verschlüsselte SQL-Kennwort.

4. Kopieren Sie die JSON-Datei der SMB-Dateifreigabe, \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Aktualisieren Sie die Datei Credentials.json mit verschlüsselten Werten.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. In Credentials.json ersetzen Sie **\<encryptedDomainUserPassword\>** durch das verschlüsselte Domänenkennwort.
    2. Ersetzen Sie **\<encryptedSqlUser\>** durch den verschlüsselten Finance and Operations SQL-Benutzer.
    3. Ersetzen Sie **\<encryptedSqlPassword\>** durch das Finance and Operations SQL-Kennwort.
    
### <a name="set-up-ssrs"></a>SSRS einrichten

1.  Bevor Sie beginnen, stellen Sie sicher, dass die erforderlichen Komponenten, die am Anfang dieses Themas aufgeführt sind, installiert sind.
2.  Folgen Sie den Schritten, damit Sie [SQL Server Reporting Services für eine On-Premises-Bereitstellung konfigurieren](../analytics/configure-ssrs-on-premises.md).

### <a name="configure-ad-fs"></a>AD FS konfigurieren

Bevor Sie diese Prozedur ausführen können, muss AD FS auf Windows Server 2016 bereitgestellt sein. Informationen darüber, wie Sie AD FS bereitstellen, finden Sie unter [Bereitstellungsleitfaden für Windows Server 2016 und 2012 R2 AD FS-Bereitstellungsleitfaden](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Finance and Operations benötigt zusätzliche Konfiguration, die über die standardmäßige, vorgegebene Konfiguration von AD FS hinausgeht. Für die folgenden Schritte wird Windows PowerShell auf einem Computer ausgeführt, auf dem ein AD FS-Rollendienst installiert wurde. Das Benutzerkonto muss über genügend Berechtigungen verfügen, um AD FS zu verwalten. So muss der Benutzer beispielsweise ein Domänenadministratorkonto haben.

1. Konfigurieren Sie den AD FS-Bezeichner, sodass er mit dem AD FS-Tokenaussteller übereinstimmt.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Sie sollten die Integrierte Windows-Authentifizierung (Windows Integrated Authentication, WIA) für Intranetauthentifizierungsverbindungen deaktivieren, sofern Sie nicht AD FS für gemischte Umgebungen konfiguriert haben. Weitere Informationen dazu, wie WIA konfiguriert wird, sodass es mit AD FS verwendet werden kann, finden Sie unter [Browser für die Verwendung der Integrierten Windows-Authentifizierung (Windows Integrated Authentication, WIA) mit AD FS konfigurieren](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. Für die Anmeldung muss die E-Mail-Adresse des Benutzers eine akzeptierte Authentifizierungseingabe sein.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

Damit AD FS Finance and Operations für den Austausch der Authentifizierung vertraut, müssen mehrere Anwendungseingaben in AD FS unter einer AD FS-Anwendungsgruppe registriert sein. Um den Setupprozess zu beschleunigen und Fehler zu verringern, können Sie das folgende Skript zur Registrierung verwenden. Kopieren Sie das Skript Publish-ADFSApplicationGroup.ps1 und das Verzeichnis D365FO-OP in einen Computer, auf dem der AD FS-Rollendienst installiert ist. Führen Sie dann das Skript aus, indem Sie ein Benutzerkonto verwenden, wie beispielsweise ein Administratorkonto, das über genügend Berechtigungen verfügt, um AD FS zu verwalten. Weitere Informationen dazu, wie Sie das Skript verwenden, finden Sie in der Dokumentation, die im Skript aufgeführt ist. Notieren Sie die Client-IDs, die in der Ausgabe angegeben sind, da Sie nach diesen Informationen in LCS in einem späteren Schritt gefragt werden.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

Die AD FS-Verwaltungskonsole sollte der folgenden Abbildung ähneln. Um Server-Manager zu öffnen, klicken Sie auf **Extras** \> **AD FS-Verwaltung**, und klicken Sie dann im unteren Bereich der Strukturansicht auf der linken Seite auf **Anwendungsgruppen**. Doppelklicken Sie auf die Anwendungsgruppe, um weitere Details anzuzeigen.

![Eigenschaften der Anwendungsgruppe](./media/OPSetup_05_ApplicatioGroupProperties.png)

Stellen Sie schließlich für eine Integritätsprüfung sicher, dass Sie auf die AD FS OpenID-Konfigurations-URL auf einem Service Fabric-Knoten des Typs **AOSNodeType** zugreifen können, indem Sie zu `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` in einem Webbrowser gehen. Wenn Sie eine Meldung erhalten, die aussagt, dass die Website nicht sicher ist, haben Sie Ihr AD FS SSL-Zertifikat nicht dem Speicher vertrauenswürdiger Stammzertifizierungsstellen hinzugefügt. Dieser Schritt wird im AD FS-Bereitstellungsleitfaden beschrieben. Wenn Sie erfolgreich auf die URL zugreifen, wird eine JavaScript Object Notation (JSON)-Datei zurückgegeben, die Ihre AD FS-Konfiguration enthält, und Sie sehen, dass Ihrer AD FS-URL vertraut wird.

Damit ist das Setup der Infrastruktur abgeschlossen. In den folgenden Abschnitten wird beschrieben, wie Sie zu [LCS](https://lcs.dynamics.com) navigieren, um Ihren Konnektor einzurichten und Ihre Dynamics 365 for Finance and Operations-Umgebung bereitzustellen.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Konnektor konfigurieren und lokalen On-Premises-Agent installieren

1. Melden Sie sich bei [LCS](https://lcs.dynamics.com/) an, und öffnen Sie das On-Premises-Implementierungsprojekt.
2. Klicken Sie im Hamburgermenü auf **Projekteinstellungen**.

    ![Befehl „Projekteinstellungen”](./media/OPSetup_06_ProjectSettings.png)

3. Klicken Sie auf **On-premises-Konnektoren**.
4. Klicken Sie auf **Hinzufügen**, um einen neuen Konnektor zu erstellen
5. Laden Sie in der Registerkarte **Hostinfrastruktur einrichten** das Agent-Installationsprogramm herunter.

    ![Laden Sie die Schaltfläche des Agent-Installationsprogramms auf der Registerkarte „Hostinfrastruktur einrichten” herunter](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Überprüfen Sie, dass die ZIP-Datei entsperrt ist. Klicken Sie mit der rechten Maustaste auf **Eigenschaften**, und wählen Sie dann **Entsperren** aus.
7. Entzippen Sie das Agent-Installationsprogramm auf einem der Service Fabric-Knoten des Typs **OrchestratorType**.
8. Auf der Registerkarte **Agent konfigurieren** geben Sie die Konfigurationseinstellungen ein.
9. Speichern Sie die Konfiguration, und klicken Sie dann auf **Konfigurationen herunterladen**, um die Konfigurationsdatei localagent-config.json herunterzuladen.

    ![Herunterladen der Konfigurationsschaltfläche auf der Registerkarte „Agent konfigurieren”](./media/OPSetup_08_DownloadConfigurations.png)

10. Kopieren Sie die Datei localagent-config.json auf den Computer, auf dem sich das Agent-Installationsprogrammpaket befindet.
11. Führen Sie in einem Eingabeaufforderungsfenster den folgenden Befehl aus, indem Sie zum Ordner navigieren, der das Agent-Installationsprogramm enthält.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Der Benutzer, der diesen Befehl ausführt, muss über **db\_owner**-Berechtigungen für die OrchestratorData-Datenbank verfügen.
    
12. Sobald lokaler Agent erfolgreich installiert ist, navigieren Sie zurück zu Ihrem On-Premises-Konnektor in LCS.
13. Klicken Sie auf der Registerkarte **Setup überprüfen** auf die Schaltfläche **Nachrichten-Agent**. Dadurch wird die LCS-Konnektivität Ihres lokalen Agenten überprüft. Wenn die Verbindung erfolgreich eingerichtet ist, sieht die Seite wie die Grafik unten aus.

     ![Agent überprüfen](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Bereitstellen Ihrer Dynamics 365 for Finance and Operations (on-premises)-Umgebung

1. Navigieren Sie zu Ihrem On-Premises-Projekt in LCS, wechseln Sie zu **Umgebung**, **Sandkasten**, und klicken Sie auf **Konfigurieren**
2. Wählen Sie Ihre **Umgebungstopologie** aus, und verwenden Sie den Assistenten, um Ihre Bereitstellung zu initiieren.
3. Der lokale Agent wird die Bereitstellungsanforderung entnehmen, die Bereitstellung auslösen und LCS benachrichtigen, sobald der Vorgang abgeschlossen ist.

