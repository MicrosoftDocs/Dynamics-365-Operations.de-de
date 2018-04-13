---
title: "Startseite für die Organisationsverwaltung"
description: "Auf dieser Seite wird auf Ressourcen verwiesen, die Sie bei der Verwendung von Microsoft Dynamics 365 Finance and Operations in Ihrer Organisation unterstützen."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: a2c1d846527eac4db0a043c7f1c51da0e73bd796
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="organization-administration-home-page"></a>Startseite für die Organisationsverwaltung

[!INCLUDE [banner](../includes/banner.md)]

In diesem Thema wird auf Inhalt verwiesen, mit dessen Hilfe Poweruser und Administratoren Microsoft Dynamics 365 for Finance and Operations konfigurieren können. Dieser Inhalt hilft, das System so zu konfigurieren, dass es für Ihre Organisation und die Geschäfte effektiv läuft.

Ein Großteil des Inhalts, der hier aufgeführt wird, gilt für die Funktionen im Modul **Verwaltung ud**. Jedoch gibt es einige Aufgaben wie die Erstellung und Verwendung einer Datensatzvorlage, die in einem beliebigen Modul ausgeführt werden, um Ihre Organisation zu unterstützen, problemlos zu laufen. 

<a name="number-sequences"></a>Nummernkreise
----------------
Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Bezeichnern für Masterdatensätze und Buchungsdatensätze, die Bezeichner benötigen. Ein Masterdatensatz oder Buchungsdatensatz, der eine Kennung erfordert, wird als *Referenz* bezeichnet. Bevor neue Datensätze für eine Referenz erstellt werden können, muss ein Nummernkreis eingerichtet und der Referenz zugeordnet werden.

-   [Nummernkreise – Überblick](number-sequence-overview.md)
-   [Einrichten von Nummernsequenzen mit einem Assistenten](tasks/set-up-number-sequences-wizard.md)(Aufgabenleitfaden)
-   [Richten Sie Nummernkreise auf einzelner Basis ein](tasks/set-up-number-sequences-individual-basis.md)(Aufgabenleitfaden)

## <a name="organizations"></a>Organisation
Eine Organisation ist eine Gruppe von Personen, die zusammenarbeiten, um einen Geschäftsprozess durchzuführen oder ein Ziel zu erreichen. Organisationshierarchien stellen die Beziehungen zwischen den Organisationen dar, aus denen das Unternehmen besteht.

Bevor Sie Organisationen und Organisationshierarchien in Finance and Operations einrichten, sollten Sie sicherstellen, dass Sie planen, wie das Unternehmen modelliert wird. Das Organisationsmodell hat bedeutende Auswirkungen auf die Implementierung von Finance and Operations sowie auf Unternehmensprozesse.

-   [Organisationen und Organisationshierarchien](organizations-organizational-hierarchies.md)
-   [Planen Ihrer Organisationshierarchie](plan-organizational-hierarchy.md)
-   [Erstellen oder Ändern einer Organisationshierarchie](tasks/create-organization-hierarchy.md) (Aufgabenleitfaden)
-   [Juristische Person erstellen](tasks/create-legal-entity.md) (Aufgabenleitfaden)
-   [Erstellen oder Ändern einer Organisationseinheit](tasks/create-operating-unit.md)(Aufgabenleitfaden)

## <a name="address-books"></a>Adressbücher
Das globale Adressbuch ist ein zentralisiertes Repository für Masterdaten, die für alle externen und internen Personen und Organisationen gespeichert werden müssen, mit denen das Unternehmen interagiert. Die Daten, die Parteidatensätzen zugeordnet sind, umfassen Name, Adresse und Kontaktinformationen. 

Nachdem Sie das globale Adressbuch erstellt haben, können Sie, wenn nötig, zusätzliche Adressbücher, wie z. B. ein separates Adressbuch für jedes Unternehmen in der Organisation oder für jede einzelne Sparte, erstellen. 

-   [Globales Adressbuch](overview-global-address-book.md)
-   [Konfiguration des globalen Adressbuchs und zusätzlicher Adressbücher planen](plan-configuration-global-address-book-additional-address-books.md)
- [Das globale Adressbuch konfigurieren](tasks/configure-global-address-book.md)
-   [Adressbücher – FAQ](qa-address-books.md)


## <a name="workflow"></a>Workflow
Das Workflowsystem das in Finance and Operations installiert wird und das Sie nutzen können, um einzelne Workflows oder Geschäftsprozesse zu erstellen. Wenn Sie einen Workflow definieren, können Sie definieren, wie ein Dokument das System durchläuft, indem angezeigt wird, wer eine Aufgabe abschließen, eine Entscheidung treffen oder ein Dokument genehmigen muss. 

-   [Workflowüberblick](overview-workflow-system.md)
-   [Workflowelemente](workflow-elements.md)
-   [Workflowaktivitäten](workflow-actions.md)
-   [Erstellen eines Workflows](create-workflow.md)

## <a name="electronic-signatures"></a>Elektronische Signaturen
Eine elektronische Signatur bestätigt die Identität einer Person, die im Begriff ist, einen Datenverarbeitungsprozess zu starten oder zu genehmigen. In einigen Branchen ist eine elektronische Signatur ebenso rechtskräftig wie eine handschriftliche Signatur. Elektronische Signaturen sind eine Konformitätsanforderung für verschiedene behördlich regulierte Branchen. Dazu zählen z. B. die Arzneimittel-, Lebensmittel- und Getränke-, Luftfahrt- und Rüstungsindustrie.

In Finance and Operations können Sie elektronische Signaturen für wichtige Geschäftsprozesse verwenden. Einige Prozesse verfügen über integrierte Funktionen der elektronischen Signatur. Darüber hinaus können Sie benutzerdefinierte Signaturanforderungen für Datenbanktabellen und -felder erstellen.

-   [Elektronische Signatur – Überblick](electronic-signature-overview.md)
-   [Einrichten von Parametern für elektronische Signaturen](tasks/set-up-electronic-signatures.md)(Aufgabenleitfaden)

## <a name="case-management"></a>Anfragenverwaltung
Indem Sie Anfragen planen, nachverfolgen und analysieren, können Sie effiziente Lösungen entwickeln, die für ähnliche Probleme wiederverwendet werden können. Wenn Mitarbeiter des Kundendiensts oder der Personalverwaltung Anfragen erstellen, können sie die Informationen in den Knowledge-Artikeln zur Handhabung bzw. zur effizienteren Lösung einer Anfrage verwenden. 

-   [Anfragenverwaltung – Überblick](cases.md)
-   [Anfragensicherheit, -prozesse und -kategorien konfigurieren](plan-case-management.md)

## <a name="record-templates"></a>Datensatzvorlagen
Mithilfe von Datensatzvorlagen können Sie Datensätze schneller erstellt werden. Diese Prozedur zeigt, wie eine Datensatzvorlge erstellt wird, sodass Feldwerte, die oft verwendet werden, nicht explizit für jeden neuen Datensatz eingegeben werden müssen. 

-   [Datensatzvorlagen](record-templates.md)
- [Eine Datensatzvorlage erstellen, um die Dateneingabe zu erleichtern](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Aufgabenleitfaden)
- [Datensatzvorlage zum Erstellen eines neuen Datensatzes verwenden](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Aufgabenleitfaden)

## <a name="general-organization-administration"></a>Allgemeine Organisationsverwaltung
-   [Ändern Sie das Banner oder das Logo](../get-started/tasks/change-banner-or-logo.md) (Aufgabenleitfaden)
- [Dokumentverwaltung konfigurieren](configure-document-management.md)
- [E-Mail konfigurieren und senden](configure-email.md)
-   [Datums-/Uhrzeitdaten und Zeitzonen](date-time-zones.md)








