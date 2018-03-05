---
title: "Anforderungen an die Hardwarekalkulation für lokale Umgebungen"
description: "Dieses Thema listet die Anforderungen an die Hardwarekalkulation für eine lokale Umgebung auf."
author: kfend
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fecffd83f32c8424e3ddcd77fb0651631f73c055
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="hardware-sizing-for-on-premises-environments"></a>Hardwarekalkulation für lokale Umgebungen

[!include[banner](../includes/banner.md)]

Bevor Sie mit der Hardware- und Infrastrukturkalkulation für eine lokale Umgebung beginnen, machen Sie sich mit den [Systemanforderungen](system-requirements.md) und den [Anweisungen für die Einrichtung und Bereitstellung](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) vertraut, um die zugrundeliegende Infrastruktur wirklich zu verstehen. 

  **Hinweis:** Achten Sie auf die optimalen Leistungsverfahren für die Systemeinrichtung. 

Nachdem Sie die Dokumentation gelesen haben, können Sie damit beginnen, das Volumen Ihrer transaktionalen und parallel arbeitenden Benutzer zu schätzen und Ihre Umgebung basierend auf dem durchschnittlichen Kerndurchsatz auszulegen.

## <a name="factors-that-affect-sizing"></a>Faktoren, die sich auf die Kalkulation auswirken
Alle in der folgenden Abbildungen gezeigten Faktoren wirken sich auf die Kalkulation aus. Je detailliertere Informationen erfasst werden, desto genauer können Sie die Kalkulation durchführen. Eine Hardwarekalkulation ohne zugrundeliegende Daten wird sehr wahrscheinlich unpräzise sein. Die absolute Mindestanforderung im Hinblick auf die benötigten Daten ist die Spitzentransaktionsleitungslast pro Stunde. 

[![Hardwarekalkulation für lokale Umgebungen](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Von links nach rechts betrachtet, ist der erste und wichtigste Faktor, den Sie brauchen, um eine präzise geschätzte Kalkulation durchzuführen, ein Transaktionsprofil oder eine Transaktionscharakterisierung. Es ist wichtig, immer das Spitzentransaktionsvolumen pro Stunde zu ermitteln. Wenn es mehrere Spitzenintervalle gibt, müssen diese Intervalle präzise definiert werden. 

Genau wie die Last, die sich auf Ihre Infrastruktur auswirkt, müsse Sie auch die folgenden Faktoren genau verstehen: 

- **Transaktionen** – Typische Transaktionen haben über den Tag/die Woche bestimmte Spitzen. Dies hängt hauptsächlich vom Transaktionstyp ab. Zeit- und Speseneinträge weisen normalerweise einmal pro Woche Spitzen auf, während Vertriebsauftragseinträge häufig gruppiert über eine Integration oder während des Tages nacheinander eintreffen. 

- **Anzahl der parallel arbeitenden Benutzer** – Die Anzahl parallel arbeitender Benutzer ist der zweitwichtigste Faktor für die Größenauslegung. Basierend auf der Anzahl parallel arbeitender Benutzer ist keine zuverlässige Größenschätzung möglich. Wenn Ihnen nur diese Daten zur Verfügung stehen, schätzen Sie vorläufig und wiederholen die Schätzung, sobald Ihnen mehr Daten zur Verfügung stehen. Eine präzise Definition parallel arbeitender Benutzer bedeutet: 
  - Benannte Benutzer sind keine parallel arbeitenden Benutzer.
  - Parallel arbeitende Benutzer sind immer eine Untermenge der benannten Benutzer. 
  - Die Spitzenarbeitslast definiert die maximale Parallelität für die Größenauslegung.
 
- Kriterien für parallel arbeitende Benutzer sind, dass die Benutzer alle folgenden Kriterien erfüllen: 
  - Angemeldet. 
  - Bearbeitung von Transaktionen/Abfragen während der Zeit der Zählung. 
  - Keine untätige Sitzung. 
 
- **Datenzusammensetzung** – Dabei geht es hauptsächlich darum, wie Ihr System eingerichtet und konfiguriert wird. Beispielsweise, wie viele juristische Entitäten Sie haben, wie viele Artikel, wie viele BOM-Ebenen, und wie komplex Ihr Sicherheitssystem ist. Jeder dieser Faktoren kann sich leicht auf die Leistung auswirken, sie können also durch eine geschickte Auswahl der Infrastruktur kompensiert werden. 

- **Erweiterungen** – Anpassungen können einfach oder komplex sein. Die Anzahl der Anpassungen sowie ihre jeweilige Komplexität und Nutzung wirkt sich unterschiedlich auf die Größe der benötigten Infrastruktur aus. Für komplexe Anpassungen wird empfohlen, Leistungsauswertungen durchzuführen. Dabei soll nicht nur ihre Effizienz getestet werden, sondern sie sollen auch dazu beitragen, die Anforderungen im Hinblick auf die Infrastruktur besser zu verstehen. Das ist vor allem dann kritisch, wenn die Erweiterungen nicht unter Anwendung der optimalen Verfahren für Leistung und Skalierbarkeit codiert wurden. 

- **Berichterstellung und Analyse** – Diese Faktoren umfassen häufig umfangreiche Abfragen der verschiedenen Datenbanken in den Datenbanksystemen von Finance and Operations. Diese Kenntnis und die Reduzierung der Häufigkeit, in der umfangreiche Berichte erstellt werden, hilft Ihnen, den Einfluss zu erkennen. 

- **Lösungen von Drittanbietern** – Für diese Lösungen, wie ISVs, gelten dieselben Auswirkungen und Empfehlungen wie für Erweiterungen. 

## <a name="sizing-your-finance-and-operations-environment"></a>Größenauslegung Ihrer Finance and Operations-Umgebung
Um die Größenanforderungen zu verstehen, müssen Sie das Spitzenvolumen der Transaktionen kennen, die Sie verarbeiten müssen. Die meisten Hilfssysteme, wie beispielsweise Management Reporter oder SSRS, sind weniger kritisch für den Betrieb. Aus diesem Grund konzentriert sich dieses Dokument hauptsächlich auf AOS und SQL Server. 

**Hinweis:** Im Allgemeinen sollten die Schichten nach dem Prinzip N+1 ausgelegt werden. Wenn Sie also drei AOS schätzen, sollten Sie ein viertes AOS bereitstellen. Die Datenbankschicht sollte so eingerichtet werden, dass sie immer verfügbar ist. 


## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Größenauslegung

- 3K- bis 15K-Transaktionsleitungen pro Stunde pro Kern auf dem DB-Server.
- Typisches AOS/SQL-Kern-Verhältnis von 3:1 für den primären SQL Server. Abhängig von der gewählten Konfiguration für höchste Verfügbarkeit sind zusätzliche Kerne erforderlich. 
  - Die Verarbeitung sehr datenbankintensiver Operationen kann dies auf 2:1 vermindern. 
- Die folgenden Faktoren beeinflussen die Variationen: 
  - Verwendete Parametereinstellungen. 
  - Erweiterungsniveaus. 
  - Verwendung zusätzlicher Funktionalität, wie beispielsweise Datenbankprotokolle und Alarme. Extrem viele Datenbankanmeldungen reduzieren den Durchsatz pro Stunde pro Kern weiter unter 3K-Leitungen. 
  - Komplexität der Datenzusammensetzung – Der Durchsatz ändert sich abhängig davon, ob eine einfache Kontentabelle verwendet wird, oder eine sehr detaillierte Kontentabelle (als Beispiel). 
  - Transaktionscharakterisierung.
  - 2 GB bis 4 GB Speicher für jeden Kern. 
  - Zusatzdatenbanken auf dem DB-Server, wie beispielsweise Management Reporter- und SSRS-Datenbanken.
  - Temporäre DB = 15 % der DB-Größe, mit so vielen Dateien wie physischen Prozessoren. 
  - SAN-Größe und Durchsatz basierend auf dem gesamten parallelen Transaktionsvolumen/der gesamten parallel stattfindenden Nutzung. 

### <a name="high-availability"></a>Höchste Verfügbarkeit 
Wir empfehlen, SQL Server immer in einer Cluster- oder Mirroring-Einrichtung zu verwenden. Der zweite SQL-Knoten sollte dieselbe Anzahl an Kernen haben wie der primäre Knoten. 

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory Federation Services (AD FS)
Weitere Informationen zur Größenauslegung von AD FS finden Sie in der [Dokumentation für die AD FS Server-Kapazität](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

Für die Planung der Instanzenanzahl in Ihrer Bereitstellung steht ein [Tabellenkalkulationsblatt](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) für die Größenauslegung zur Verfügung.

<a name="aos-online-and-batch"></a>AOS (Online und Batch)
----------------------

### <a name="sizing"></a>Größenauslegung

- Größenauslegung nach Transaktionsvolumen/Nutzung
  - 2K- bis 6K-Leitungen pro Kern
  - 16 GB pro Instanz
  - Standardgehäuse – 4 bis 24 Kerne
  - 10 bis 15 Unternehmensbenutzer pro Kern
  - 15 bis 25 Aktivitätsbenutzer pro Kern
  - 25 bis 50 Teammitglieder pro Kern
- Stapel
   - 1 bis 4 Batch-Threads pro Kern
   - Größe basierend auf der Charakterisierung des Batch-Fensters
- Beachten Sie, dass AOS, Datenverwaltung und Batch auf dem Service Fabric dieselbe Rolle einnehmen. Sie müssen die Größe auf die Kombination der drei Arbeitslasten auslegen, und nicht separat dafür, wie in Microsoft Dynamics AX 2012.
- Hier gelten dieselben Variabilitätsfaktoren für SQL Server.

### <a name="high-availability"></a>Höchste Verfügbarkeit
- Stellen Sie sicher, dass Ihnen mindestens 1 bis 2 weitere AOS zur Verfügung stehen, als Ihre Schätzung vorgibt.
- Stellen Sie sicher, dass Ihnen mindestens 3 bis 4 virtuelle Hosts zur Verfügung stehen.

## <a name="management-reporter"></a>Management Reporter
Größtenteils sollten die empfohlenen Mindestanforderungen mit zwei Knoten ausreichend gut funktionieren, wenn keine extensive Nutzung stattfindet. Sie brauchen nur in Fällen mit sehr starker Nutzung mehr als zwei Knoten. Bitte führen Sie eine Skalierung nach Bedarf durch.

## <a name="sql-server-reporting-services"></a>SQL Server Reporting Services
Für die allgemeine Verfügbarkeit kann nur ein SSRS-Knoten bereitgestellt werden. Überwachen Sie Ihren SSRS-Knoten beim Test und erhöhen Sie die Anzahl der Kerne für SSRS bei Bedarf. Stellen Sie sicher, dass Ihnen auf einem virtuellen Host, der nicht die SSRS VM ist, ein vorkonfigurierter sekundärer Knoten zur Verfügung steht. Das ist wichtig, falls es Probleme mit der virtuellen Maschine gibt, auf der SSRS oder der virtuelle Host untergebracht sind. In diesem Fall müssten sie ersetzt werden. 

## <a name="environment-orchestrator"></a>Environment Orchestrator
Der Orchestrator-Service verwaltet Ihre Bereitstellung und die entsprechende Kommunikation mit LCS. Dieser Service wird als primärer Service Fabric-Service bereitgestellt und benötigt mindestens drei VMs. Dieser Services befindet sich am selben Standort wie die Service Fabric-Orchestrierungsservices. Dieser sollte auf die Spitzenlast des Clusters ausgelegt werden. Weitere Informationen finden Sie unter [Aspekte zur Service Fabric-Clusterkapazitätsplanung](/azure/service-fabric/service-fabric-cluster-capacity).  


## <a name="virtualization-and-oversubscription"></a>Virtualisierung und Überabonnement
Aufgabenkritische Services wie AOS sollten auf virtuellen Hosts mit speziell dafür vorgesehenen Ressourcen untergebracht werden, wie beispielsweise Kerne, Speicher und Festplatten.   


