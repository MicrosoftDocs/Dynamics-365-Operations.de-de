---
title: "Handelsgrundlagenüberblick"
description: "Dieser Artikel wird Informationen zu Handelsgrundlagen festgelegt, die eine Kleinverkaufsstelle (POS) und E-Commerce-Konfigurationsoption für Microsoft Dynamics 365 für Arbeitsgänge ist. Handelsgrundlagen stellen eine vordefinierte Einzelhandelsauslastung bereit, die Einzelhändler dabei unterstützen können, rasch mit einer Microsoft Dynamics basierten Einzelhandelslösung in den Markt einzutreten, damit sie sich auf Einzelhandels-spezifische Funktionen fokussieren können."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16121
ms.assetid: 61dced3e-8b6b-4c1f-af39-d20f4ab48659
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 6d16a0ebf84b217df0c2cd022ba5bf46e5ca61b2
ms.lasthandoff: 03/31/2017


---

# <a name="commerce-essentials-overview"></a>Handelsgrundlagenüberblick

Dieser Artikel wird Informationen zu Handelsgrundlagen festgelegt, die eine Kleinverkaufsstelle (POS) und E-Commerce-Konfigurationsoption für Microsoft Dynamics 365 für Arbeitsgänge ist. Handelsgrundlagen stellen eine vordefinierte Einzelhandelsauslastung bereit, die Einzelhändler dabei unterstützen können, rasch mit einer Microsoft Dynamics basierten Einzelhandelslösung in den Markt einzutreten, damit sie sich auf Einzelhandels-spezifische Funktionen fokussieren können. 

<a name="overview"></a>Überblick
--------

Geschäftssoftwareumgebungen umfassen viele häufig Systeme, von denen jedes sehr spezielle Funktionen ausführt. Häufig möchten Einzelhändler die Kleinverwaltungsaspekte von Microsoft Dynamics 365 für Arbeitsgänge nutzen möchten, nicht aber wertmäßig oder ihr vorhandenen Personalverwaltung (HR)- System. Für diese Einzelhändler ist eine Arbeitsauslastung, die spezifisch für den Einzelhandel ist, obligatorisch. Handelsgrundlagen stellt diesen als Einzelhandelbesonderefunktionen Konfigurationsoption für Dynamics 365 für Arbeitsgänge. Nachdem die Konfiguration abgeschlossen ist, werden alle Nicht-Einzelhandelsaspekte der Lösung von der Ansicht ausgeblendet, damit der Fokus darauf gelegt werden kann, was wichtig ist: das Verwalten einer Einzelhandelsorganisation. Handelsgrundlagen wurden zunächst als Konfigurationsoption in Microsoft Dynamics AX 2012 R3 CU8 eingeführt. Seitdem wurden zahlreiche Verbesserungen vorgenommen, um es eine Lösung werden zu lassen, die für Mehrkanaleinzelhändler funktioniert, und nicht nur für physische Organisationen.

## <a name="configuration"></a>Variante
Um Handelszu konfigurieren Grundlagen, wechseln ** Systemverwaltung ** ** &gt; Einstellungen ** ** &gt; Lizenzkonfiguration ** und zurücksetzen Sie unten ** Einzelhandel **. Erweitern Sie den **Einzelhandel**-Knoten, und aktivieren Sie das Kontrollkästchen für **Handelsgrundlagen**. Klicken Sie auf **Speichern**, überprüfen Sie die Änderungen, und aktualisieren Sie die Seite. Um wieder in die vollständigen Lösung zu wechseln, fahren ** Handelsgrundlagen ** ** &gt; die Einrichtung Headquarter ** ** &gt; Lizenzkonfiguration ** und zurücksetzen Sie unten ** Einzelhandel **. Erweitern Sie den **Einzelhandel**-Knoten, und deaktivieren Sie das Kontrollkästchen für **Handelsgrundlagen**. Klicken Sie auf **Speichern**, überprüfen Sie die Änderungen, und aktualisieren Sie die Seite.

## <a name="what-is-included"></a>Was ist enthalten?
Handelsgrundlagen enthält alle Kleinbackofficefunktionen, die den in Kernsatz Dynamics 365 für Arbeitsgangskleinlösung aufgebaut werden, außer Callcenterfunktionen. Alle Kanal-, Arbeitskraft-, Produkt-, Geschäfts-, Register- und Geräteverwaltungsfunktionen sind in einem einzelnen Navigationsknoten einbezogen. Darüber hinaus wurden alle vollständigen Einzelhandelsarbeitsbereiche einbezogen, um vordefinierte rollenspezifische Angebotsseiten bereitzustellen. Handelsgrundlagen-Zieleinzelhändler, die ein Ziegelstein-undmörtel- oder Mobileszenario haben, das von modernen KleinKanälen POS (MPOS) und des E-Commerce Vorteil sein kann. Indem Handelsgrundlagen verwendet werden, können Einzelhändler diese Kanäle an einem einzigen Ort verwalten und dadurch echte Mehrkanalfunktionen nutzen.

## <a name="how-is-commerce-essentials-different"></a>Inwiefern unterscheiden sich Handelsgrundlagen?
Neben der Ermöglichung der einheitlichen Navigation und Nur-Einzelhandel-Seiten, blenden Handelsgrundlagen alle Nicht-Einzelhandelsseitenelemente wie Felder und Kontrollen aus. Das Ergebnis ist eine optimierte Benutzeroberfläche, die Einzelhändlern hilft, sich auf ihre eigentliche Arbeit zu konzentrieren. Einzelhändler, die eine vollständige Produktlizenz haben, können Handelsgrundlagen als Ausgangspunkt für Einzelhandel-ausgerichtete Benutzer verwenden. Andere Elemente, wie erweiterten Verwendung, können den Handelsgrundlagen, während diese gefordert sind, gemäß den Bedingungen des Lizenzvertrags werden, der hinzugefügt vorhanden ist. Im Rahmen der Optimierung und Vereinfachung, die Handelsgrundlagen bereitstellen, können Einzelhändler mit Buchhaltungsexportfunktionen Summen zuordnen, die in den Handelsgrundlagen für die Kontonummern in ihrem vorhandenen Buchhaltungssystem antizipiert werden. Da das Einzelhandelssystem Finanzdaten generiert, können diese Daten leicht aus den Handelsgrundlagen in das Buchhaltungssystem des Einzelhändlers exportiert werden. Wenn Integrationsfunktionen weiter reichende erforderlich sind, enthält Handelsgrundlagen auch das vollständige Import-/Exportframework, das in Dynamics 365 für Arbeitsgänge einbezogen ist. Die Hunderte von Datenentitäten, die standardmäßig enthalten sind, geben Handelsgrundlagen die Flexibilität, sich einer Umgebung mit mehreren Ebenen, in der mehrere spezielle Systeme verwendet werden, bequem anzupassen.


