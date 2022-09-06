---
title: Massenbereitstellung versiegelter Commerce-Self-Service-Komponenten
description: In diesem Artikel wird erläutert, wie Sie das Framework für Self-Service-Komponenteninstallationsprogramme verwenden, um Bereitstellungen im Hintergrund zu installieren und zu warten.
author: jashanno
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 66a711aff90221e594f4b2a0df3735eac93d0c9b
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387018"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Massenbereitstellung versiegelter Commerce-Self-Service-Komponenten

[!include [banner](../includes/banner.md)]

Dieser Artikel gilt für das versiegelte Framework, Komponenteninstallationsprogramme, die jeden Monat veröffentlicht werden, beginnend mit der Version 10.0.18, und die in der Bibliothek freigegebener Anlagen in Microsoft Dynamics Lifecycle Services (LCS) zur Verfügung gestellt werden. Beachten Sie, dass die ersten Versionen dieser neuen Installationsprogramme als **(Vorschauversion)** gekennzeichnet sind. Der einzige Zweck dieser Bezeichnung besteht jedoch darin, die neuen Installationsprogramme zu unterscheiden, während Microsoft bestimmt, ob es zusätzliche funktionale Anforderungen gibt, um sie zu verwenden. Dies bedeutet nicht, dass die Installationsprogramme nicht für die Produktion gültig sind. Basierend auf der Veröffentlichung dieser neuen Installationsprogramme plant Microsoft, die alten (Legacy-) Installationsprogramme im oder um den Oktober 2023 als veraltet zu markieren. 

In diesem Artikel wird erläutert, wie die neuen Installationsprogramme verwendet werden, um unbeaufsichtigte Installationen durchzuführen und Aktualisierungen über Befehlszeilenargumente zu warten. Mit diesen Argumenten können Sie eine Massenbereitstellung auf verschiedene Arten durchführen.

> [!NOTE]
> Die neuen versiegelten Self-Service-Installationsprogramme werden nicht in Headquarters zur Verfügung gestellt und können nur über LCS heruntergeladen werden.

## <a name="delimiters-for-mass-deployment"></a>Trennzeichen für die Massenbereitstellung

Die folgende Tabelle zeigt die Trennzeichen, die bei der Befehlszeilenausführung verwendet werden können.


| Trennzeichen                 | Description |
|---------------------------|-------------|
| -AadTokenIssuerPrefix | Das Präfix für den Microsoft Azure Active Directory (Azure AD)-Token-Emittent. |
| -AsyncClientAadClientId | Die Azure AD-Client-ID, die Async Client während der Kommunikation mit Headquarters verwenden soll. |
| -AsyncClientAppInsightsInstrumentationKey | Der Instrumentierungsschlüssel für Async Client AppInsights. |
| -AsyncClientCertFullPath | Der vollständig formatierte URN-Pfad, der den Fingerabdruck als Suchmetrik für den Speicherort des Async Client-Identitätszertifikats verwendet, das für die Authentifizierung mit Azure AD für die Kommunikation mit Headquarters verwendet werden soll. Zum Beispiel ist `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` ein korrekt formatierter URN. Der Wert **\<MyThumbprint\>** wird durch den Fingerabdruck des zu verwendenden Zertifikats ersetzt. Verwenden Sie diesen Parameter nicht zusammen mit dem **-AsyncClientCertThumbprint**-Parameter. |
| -AsyncClientCertThumbprint | Der Fingerabdruck des Async Client-Identitätszertifikats, das zur Authentifizierung mit Azure AD für die Kommunikation mit Headquarters verwendet werden soll. Dieser Fingerabdruck wird verwendet, um den Speicherort **LocalMachine/Mein Shop** und Namen zu durchsuchen, um das richtige zu verwendende Zertifikat zu finden. Verwenden Sie diesen Parameter nicht zusammen mit dem **-AsyncClientCertFullPath**-Parameter. |
| -ClientAppInsightsInstrumentationKey | Der Instrumentierungsschlüssel für Client AppInsights. |
| -CloudPosAppInsightsInstrumentationKey | Der Instrumentierungsschlüssel für Cloud POS AppInsights. |
| -Config | Die Konfigurationsdatei, die während der Installation verwendet werden soll. Ein Beispiel für einen Dateinamen ist **Contoso.CommerceScaleUnit.xml**. |
| -CposAadClientId | Die Azure AD-Client-ID, die Cloud POS während der Geräteaktivierung verwenden soll. Dieser Parameter ist für lokale Bereitstellungen nicht erforderlich. |
| -Device | Die Geräte-ID, wie auf der **Geräte**-Seite in Headquarters angezeigt. |
| - EnvironmentId | Die Umgebungs-ID. |
| -HardwareStationAppInsightsInstrumentationKey | Der Instrumentierungsschlüssel für Hardware Station-AppInsights. |
| Installieren | Ein Parameter, der angibt, ob die von diesem Installationsprogramm bereitgestellte Komponente installiert werden soll. Dieser Parameter ist erforderlich, um eine Installation durchzuführen, und hat keinen führenden Bindestrich. |
| -InstallOffline | Für Modern POS gibt dieser Parameter an, dass auch die Offlinedatenbank installiert und konfiguriert werden soll. Verwenden Sie auch den **-SQLServerName**-Parameter. Andernfalls versucht das Installationsprogramm, eine Standardinstanz zu finden, die die Voraussetzungen erfüllt. |
| -Port | Der Port, der dem virtuellen Retail Server-Verzeichnis zugeordnet und von diesem verwendet werden soll. Wenn kein Port festgelegt wird, wird der Standardport 443 verwendet. |
| -Register | Die Registerkennung, wie auf der **Register**-Seite in Headquarters angezeigt. |
| -RetailServerAadClientId | Die Azure AD-Client-ID, die Retail Server während der Kommunikation mit Headquarters verwenden soll. |
| -RetailServerAadResourceId | Die Retail Server Azure AD-App-Ressourcen-ID, die während der Geräteaktivierung verwendet werden soll. Dieser Parameter ist für lokale Bereitstellungen nicht erforderlich. |
| -RetailServerCertFullPath | Der vollständig formatierte URN-Pfad, der den Fingerabdruck als Suchmetrik für das Retail Server-Identitätszertifikats verwendet, das für die Authentifizierung mit Azure AD für die Kommunikation mit Headquarters verwendet werden soll. Zum Beispiel ist `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` ein korrekt formatierter URN, wobei der Wert **\<MyThumbprint\>** durch den zu verwendenden Zertifikatfingerabdruck ersetzt wird. Verwenden Sie diesen Parameter nicht zusammen mit dem **-RetailServerCertThumbprint**-Parameter. |
| -RetailServerCertThumbprint | Der Fingerabdruck des Retail Server-Identitätszertifikats, das zur Authentifizierung mit Azure AD für die Kommunikation mit Headquarters verwendet werden soll. Dieser Fingerabdruck wird verwendet, um den Speicherort **LocalMachine/Mein Shop** und Namen zu durchsuchen, um das richtige zu verwendende Zertifikat zu finden. Verwenden Sie diesen Parameter nicht zusammen mit dem **-RetailServerCertFullPath**-Parameter. |
| -RetailServerURL | Die Retail Server-URL, die das Installationsprogramm verwenden soll. (Diese URL wird auch als Commerce Scale Unit bezeichnet \[CSU\]-URL.) Für Modern POS wird dieser Wert während der Geräteaktivierung verwendet. |
| -SkipAadCredentialsCheck| Ein Schalter, der angibt, ob Voraussetzungsprüfungen für Azure AD-Anmeldeinformationen übersprungen werden sollen. Der Standardwert ist **Falsch**. |
| -SkipCertCheck | Ein Schalter, der angibt, ob Voraussetzungsprüfungen für Zertifikate übersprungen werden sollen. Der Standardwert ist **Falsch**. |
| -SkipIisCheck | Ein Schalter, der angibt, ob Voraussetzungsprüfungen für Internet Information Services (IIS) übersprungen werden sollen. Der Standardwert ist **Falsch**. |
| -SkipNetFrameworkCheck | Ein Schalter, der angibt, ob Voraussetzungsprüfungen für .NET Framework übersprungen werden sollen. Der Standardwert ist **Falsch**. |
| -SkipScaleUnitHealthcheck | Ein Schalter, der angibt, ob die Integritätsprüfung installierter Komponenten übersprungen werden soll. Der Standardwert ist **Falsch**. |
| -SkipSChannelCheck | Ein Schalter, der angibt, ob Voraussetzungsprüfungen für sichere Kanäle übersprungen werden sollen. Der Standardwert ist **Falsch**. |
| -SkipSqlFullTextCheck | Ein Schalter, der angibt, ob die Überprüfung der SQL Server-Voraussetzung, die eine Volltextsuche erfordert, übersprungen werden soll. Der Standardwert ist **Falsch**. |
| -SkipSqlServerCheck | Ein Schalter, der angibt, ob Voraussetzungsprüfungen für SQL Server übersprungen werden sollen. Der Standardwert ist **Falsch**. |
| -SqlServerName | Der SQL Server-Name. Wenn der Name nicht angegeben ist, versucht das Installationsprogramm, die Standardinstanz zu finden. |
| -SslcertFullPath | Der vollständig formatierte URN-Pfad, der den Fingerabdruck als Suchmetrik des Speicherorts des Zertifikats verwendet, das zum Verschlüsseln des HTTP-Datenverkehrs zur Skalierungseinheit verwendet werden soll. Zum Beispiel ist `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` ein korrekt formatierter URN, wobei der Wert **\<MyThumbprint\>** durch den zu verwendenden Zertifikatfingerabdruck ersetzt wird. Verwenden Sie diesen Parameter nicht zusammen mit dem **-SslCertThumbprint**-Parameter. |
| -SslCertThumbprint | Der Fingerabdruck des Zertifikats, das zum Verschlüsseln des HTTP-Datenverkehrs zur Skalierungseinheit verwendet werden soll. Dieser Fingerabdruck wird verwendet, um den Speicherort **LocalMachine/Mein Shop** und Namen zu durchsuchen, um das richtige zu verwendende Zertifikat zu finden. Verwenden Sie diesen Parameter nicht zusammen mit dem **-SslCertFullPath**-Parameter. |
| -StoreSystemAosUrl | Die Headquarters (AOS)-URL. |
| -StoreSystemChannelDatabaseId | Die Kanaldatenbankkennung (Name). |
| -TenantId | Die Azure AD-Mandanten-ID. |
| -TransactionServiceAzureAuthority | Die Transaction Service Azure AD-Autorität. |
| -TransactionServiceAzureResource | Die Transaction Service Azure AD-Ressource. |
| -TrustSqlServerCertificate | Ein Schalter, der angibt, ob dem Serverzertifikat vertraut werden soll, während eine Verbindung mit SQL Server hergestellt wird. Um Sicherheitsrisiken zu vermeiden, sollten Produktionsbereitstellungen hier niemals einen Wert von **wahr** liefern. Der Standardwert ist **Falsch**. |
| -Verbosity | Die Protokollierungsebene, die während der Installation angefordert wird. In der Regel sollte dieser Wert nicht verwendet werden. |
| -WindowsPhoneAppInsightsInstrumentationKey | Der Instrumentierungsschlüssel für Hardware Station-AppInsights. |

## <a name="general-overview"></a>Allgemeiner Überblick

Das neue Framework für Self-Service-Installationsprogramme verfügt über verschiedene Funktionen und Verbesserungen. Das neue Framework generiert derzeit nur Installationsprogramme für Modern POS, Hardware Station und CSU (selbst gehostet). Es ist wichtig, die grundlegende Befehlszeilenverwendung der versiegelten Installationsprogramme zu verstehen, die ähnlich wie im folgenden Beispiel aussehen sollte. 
 
```Console
<Component Installer Name>.exe install -<Parameter Name> "<Parameter Information>"
```

Das Installationsprogramm benötigt den Parameter **install** (oder **uninstall** zum Entfernen der Installation) und alle Parameter, die für diese Installation spezifisch sind. **Parametername** sollte alle erforderlichen Parameter wie Registrierung, CSU-URL oder Zertifikatsinformationen enthalten. **Parameterinformationen** sollte zusätzliche Informationen zu den Parametern enthalten.

Das versiegelte Framework wurde erstellt, um die folgenden Änderungen zu ermöglichen:
- **Versiegelt** – Das neue Installationsprogramm-Framework trennt von Microsoft verteilte Basiskomponenten-Installationsprogramme vollständig von den erweiterbarkeitsbasierten Anpassungen. Die Anpassungen werden anschließend installiert, sind dann aber in Bezug auf Updates entkoppelt (sodass Updates nur für die Microsoft-Basiskomponente, nur für die Anpassungen oder für beide zulässig sind).
- **GUI-los** – Es gibt keine Benutzeroberfläche (UI) mehr. Stattdessen gibt es für jedes Komponenteninstallationsprogramm eine vollständig befehlszeilengesteuerte ausführbare Datei. Diese Änderung ist eine von mehreren wichtigen Änderungen oder Funktionen, die verwendet werden, um das neue Installationsprogramm-Framework für die Verwendung mit Massenbereitstellungen zu fokussieren.
- **Tiefere Protokollierung** – Verbesserte Installationsprotokolle ermöglichen eine bessere Überprüfung des Installationsabschlusses oder -fehlers, der durchgeführten Schritte und aller Warnungen oder Fehler, die generiert wurden.
- **Aufräumen** – Im neuen Framework arbeiten die Installationsprogramme für Komponenten härter, um die Sauberkeit der Installationsverzeichnisse aufrechtzuerhalten, indem sie den gesamten Inhalt des Komponentenordners löschen, bevor sie die neueren Komponenten installieren. Diese Bereinigung stellt sicher, dass keine Dateien übrig bleiben, die Probleme verursachen und eine erfolgreiche Installation verhindern könnten.

Drei Komponenten wurden nicht in das neue Framework migriert: der Virtual Peripheral Simulator, der Async Server Connector Service (verwendet für Dynamics AX 2012 R3-Unterstützung) und der Serviceersatz in Echtzeit (verwendet für Dynamics AX 2012 R3-Unterstützung).

> [!NOTE]
> Installationsprogramme werden lokal gespeichert und beibehalten.  Im Laufe der Zeit ist es wichtig, die aufbewahrten Installationsprogramme zu verwalten oder zu löschen, um keinen Speicherplatz zu verschwenden. Es wird empfohlen, das aktuelle Installationsprogramm für die Basiskomponente(n) und alle Erweiterungsinstallationsprogramme für die neueste(n) Version(en) für die Wiederherstellung nach extremen Situationen beizubehalten.

## <a name="migration"></a>Migration

Die Migration von den alten Self-Service-Framework-Komponenteninstallationsprogrammen zu den neuen Framework-Komponenteninstallationsprogrammen erfordert die Deinstallation der alten Komponenten.

- **Modern POS** – Das neue Installationsprogramm-Framework bewirkte, dass die Anwendung eine neue Anwendungssignatur-ID erhielt. Daher ist eine vollständige Deinstallation alter Komponenten erforderlich, bevor die neue Modern POS-Framework-Komponente installiert wird. Da eine vollständige Deinstallation erforderlich ist, ist eine erneute Geräteaktivierung erforderlich. (Diese Gerätereaktivierung ist eine einmalige Anforderung, vorausgesetzt, dass die Deinstallation nicht erneut erfolgt.)
- **Hardware Station** – Als IIS-Website erfordert das neue Installationsprogramm-Framework eine Überarbeitung der Basisordnerstruktur. Daher ist eine vollständige Deinstallation alter Komponenten erforderlich, bevor die neue Hardware Station-Framework-Komponente installiert wird.
- **Commerce Scale Unit (CSU, selbst gehostet)** – Als eine Reihe von IIS-Websites erfordert das neue Installationsprogramm-Framework eine Überarbeitung der Basisordnerstruktur.  Daher ist eine vollständige Deinstallation alter Komponenten erforderlich, bevor die neue Framework-Komponente für CSU (selbst gehostet) installiert wird.

## <a name="modern-pos"></a>Modern POS

### <a name="before-you-begin"></a>Bevor Sie beginnen

Es ist wichtig, dass Sie die alte Self-Service-Komponente von Modern POS entfernen. Weitere Informationen finden Sie in den Migrationsschritten weiter oben in diesem Artikel.

> [!NOTE]
> Auf einem Einzelcomputersystem wie einer Entwicklertopologie oder einer Demoumgebung oder wenn Commerce Scale Unit und Modern POS auf demselben Computer installiert sind, kann Store Commerce die Geräteaktivierung möglicherweise nicht abschließen. Dieses Problem tritt auf, weil Store Commerce keine Netzwerkaufrufe an den gleichen Computer (d. h. Aufrufe an sich selbst) tätigen kann. Während dies niemals ein Szenario in einer Produktionsumgebung sein sollte, kann das Problem eingedämmt werden, indem eine AppContainer-Loopback-Ausnahme aktiviert wird, sodass die Kommunikation mit demselben Computer erfolgen kann. Verschiedene Anwendungen sind öffentlich verfügbar, um dieses Loopback zu ermöglichen. Weitere Informationen zum Loopback finden Sie unter [Loopback aktivieren und Probleme mit der Netzwerkisolation beheben](/previous-versions/windows/apps/hh780593(v=win.10)). Es ist wichtig zu verstehen, dass ein Loopback ein Sicherheitsrisiko darstellen kann, daher wird davon abgeraten, ein Loopback zu verwenden, falls dies nicht absolut notwendig ist.

### <a name="examples-of-silent-deployment"></a>Beispiele für unbeaufsichtigte Bereitstellung

Dieser Abschnitt zeigt Beispiele für Befehle, die zum Installieren von Modern POS verwendet werden.

#### <a name="silently-install-modern-pos"></a>Modern POS automatisch installieren

Der folgende Befehl installiert (oder aktualisiert) Modern POS im Hintergrund. Er verfügt über die Standardbefehlsstruktur, die für die unbeaufsichtigte Wartung von derzeit installierten Komponenten verwendet wird. Die Struktur verwendet die Grundwerte von **&lt;InstallerName&gt;.exe**.

Der folgende grundlegende Befehl zeigt die verfügbaren Optionen, wenn eine Installation angefordert wird. Es wird dringend empfohlen, diesen Befehl beim ersten Testen oder Verwenden des Installationsprogramms zu verwenden.

```Console
CommerceModernPOS.exe -help install
```

> [!NOTE]
> Für Modern POS ist keine Konfigurationsdatei erforderlich. Das Installationsprogramm verfügt jetzt über Parameter (weiter oben in diesem Artikel gezeigt) für die verschiedenen Werte, die während der Geräteaktivierung verwendet werden.

Der folgende Befehl gibt alle Parameter an, die während der Geräteaktivierung verwendet werden sollten, nachdem die Modern POS-Anwendung installiert wurde. Dieses Beispiel verwendet das **Houston-3**-Register, ein häufig verwendeter Wert in Dynamics 365 Commerce-Demodaten.

```Console
CommerceModernPOS.exe install -Register "Houston-3" -Device "Houston-3" -RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Der folgende Befehl gibt die Parameter an, die zum Installieren und Konfigurieren der Offlinedatenbank verwendet werden sollen. Der SQL Server wird zusammen mit der zu verwendenden Konfigurationsdatei angegeben.

```Console
CommerceModernPOS.exe install -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

Sie können diese Konzepte kombinieren, um die gewünschten Installationsergebnisse zu erzielen.

## <a name="hardware-station"></a>Hardwarestation

### <a name="before-you-begin"></a>Bevor Sie beginnen

Es ist wichtig, dass Sie die alte Self-Service-Komponente von Hardware Station entfernen. Weitere Informationen finden Sie in den Migrationsschritten weiter oben in diesem Artikel. Es gibt kein Händlerkonto-Informationstool mehr. Stattdessen werden die Händlerkontoinformationen installiert, wenn ein POS-Terminal mit der Hardware Station gekoppelt wird. Es wird dringend empfohlen, den folgenden Befehl beim ersten Testen des Installationsprogramms auszuführen:

```Console
CommerceHardwareStation.exe -help install
```

### <a name="examples-of-silent-deployment"></a>Beispiele für unbeaufsichtigte Bereitstellung

Dieser Abschnitt zeigt Beispiele für Befehle, die zum Installieren von Hardware Station verwendet werden.

#### <a name="silently-install-hardware-station"></a>Hardware Station automatisch installieren

Der folgende Befehl installiert (oder aktualisiert) Hardware Station im Hintergrund. Er verfügt über die Standardbefehlsstruktur, die für die Wartung von derzeit installierten Komponenten verwendet wird. Die Struktur verwendet die Grundwerte von **&lt;InstallerName&gt;.exe**.

Der folgende grundlegende Befehl führt das ausführbare Dateiinstallationsprogramm aus.

```Console
HardwareStation.exe install -Port 443 -StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" -StoreSystemChannelDatabaseID "Houston" -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> Für Hardware Station ist keine Konfigurationsdatei erforderlich. Das Installationsprogramm verfügt jetzt über Parameter (weiter oben in diesem Artikel gezeigt) für die verschiedenen erforderlichen Werte.

Der folgende Befehl gibt alle Parameter an, die erforderlich sind, um die Voraussetzungsprüfungen während einer Standardinstallation zu überspringen. 

> [!NOTE]
> Das Überspringen von Überprüfungen wird nicht ohne gründliche Tests im Voraus oder in Entwicklungssituationen empfohlen.

```Console
HardwareStation.exe install -SkipFirewallUpdate -SkipOPOSCheck -SkipVersionCheck -SkipURLCheck -Config "HardwareStation.Houston.xml"
```

Wie üblich können diese Konzepte üblicherweise kombiniert werden, um die gewünschten Installationsergebnisse zu erzielen.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (selbst gehostet)

Es wird dringend empfohlen, den folgenden Befehl beim ersten Testen des Installationsprogramms auszuführen:

```Console
CommerceStoreScaleUnitSetup.exe -help install
```

### <a name="before-you-begin"></a>Bevor Sie beginnen

Es ist wichtig, dass Sie die alte Self-Service-Komponente von CSU (selbst gehostet) entfernen. Weitere Informationen finden Sie in den Migrationsschritten weiter oben in diesem Artikel.

### <a name="examples-of-silent-deployment"></a>Beispiele für unbeaufsichtigte Bereitstellung

Dieser Abschnitt zeigt Beispiele für Befehle, die zum Installieren von CSU (selbst gehostet) verwendet werden.

#### <a name="silently-install-csu-self-hosted"></a>CSU (selbst gehostet) im Hintergrund installieren

Der folgende Befehl installiert (oder aktualisiert) CSU (selbst gehostet) im Hintergrund. Er verfügt über die Standardbefehlsstruktur, die für die unbeaufsichtigte Wartung von derzeit installierten Komponenten verwendet wird. Die Struktur verwendet die Grundwerte von **&lt;InstallerName&gt;.exe**.

Im Vergleich zu den anderen Self-Service-Installationsprogrammen ist Commerce Scale Unit (CSU) komplexer und erfordert eine ziemlich große Menge zusätzlicher Informationen. Der folgende Befehl ist der Mindestbefehl (mit Parametern), der zum Ausführen des Installationsprogramms für ausführbare Dateien erforderlich ist, wenn keine Konfigurationsdatei vorhanden ist.

```Console
CommerceScaleUnit.exe install -port 446 -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> Für CSU (selbst gehostet) ist weiterhin eine Konfigurationsdatei erforderlich.

Der folgende Befehl ist ein gründlicherer Befehl, der das Installationsprogramm für ausführbare Dateien mit einigen alternativen Parametern ausführt.

```Console
CommerceScaleUnit.exe install -Port 446 -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Verbosity 0 -Config "Contoso.StoreSystemSetup.xml"
```

Der folgende Befehl gibt Parameter an, die erforderlich sind, um die Voraussetzungsprüfungen während einer Standardinstallation zu überspringen. 

> [!NOTE]
> Das Überspringen von Überprüfungen wird nicht ohne gründliche Tests im Voraus oder in Entwicklungssituationen empfohlen.


```Console
CommerceScaleUnit.exe installer -skipscaleunithealthcheck -skipcertcheck -skipaadcredentialscheck -skipschannelcheck -skipiischeck -skipnetcorebundlecheck -skipsqlservercheck -skipnetframeworkcheck -skipversioncheck -skipurlcheck -Config "Contoso.StoreSystemSetup.xml" -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate
```

Sie können diese Konzepte kombinieren, um die gewünschten Installationsergebnisse zu erzielen.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
