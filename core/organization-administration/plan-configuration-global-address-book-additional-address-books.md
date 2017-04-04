---
title: "Konfigurieren Sie globale Adressbücher"
description: "In diesem Artikel wird beschrieben die Überlegungen und der getroffenen Entscheidungen, die während des Planungsvorgangs vornehmen müssen, bevor Sie das globale Adressbuch und zusätzliche Adressbücher in Microsoft Dynamics 365 für Arbeitsgänge einrichten und konfigurieren. Einige der Entscheidungen erfordern, dass Sie die Entscheidungen bestätigen, die für andere Bereiche des Produkts getroffen wurden, wie die Organisationshierarchie."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: abd9ec44530522657f758b35e8f987aa92c3b0e3
ms.lasthandoff: 03/31/2017


---

# <a name="configure-global-address-books"></a>Konfigurieren Sie globale Adressbücher

In diesem Artikel wird beschrieben die Überlegungen und der getroffenen Entscheidungen, die während des Planungsvorgangs vornehmen müssen, bevor Sie das globale Adressbuch und zusätzliche Adressbücher in Microsoft Dynamics 365 für Arbeitsgänge einrichten und konfigurieren. Einige der Entscheidungen erfordern, dass Sie die Entscheidungen bestätigen, die für andere Bereiche des Produkts getroffen wurden, wie die Organisationshierarchie.

<a name="global-address-book"></a>Globales Adressbuch
-------------------

Bevor Sie beginnen mit dem globalen Adressbuch zu arbeiten, müssen Sie die dafür notwendigen Standardwerte bestimmen. Diese Standardwerte werden dann für weitere Adressbücher verwendet, die Sie erstellen. **Entscheidung:**

-   In welcher Reihenfolge sollen die Namen der Parteidatensätze vom Typ **Person** angezeigt werden? So kann beispielsweise eine Reihenfolge Nachname, zweiter Vorname, Vorname sein.
-   Müssen Parteidatensätze aus dem Adressbuch gelöscht werden, wenn die Rolle Datensatz gelöscht wird? Sollte der Parteidatensatz auch gelöscht werden, wenn beispielsweise ein Debitorendatensatz gelöscht wird?
-   Sollten Benutzer benachrichtigt werden, sobald ein doppelter Datensatz im globalen Adressbuch gefunden wird, wenn ein neuer Datensatz erstellt wird?
-   Sollte die Data Universal Numbering System (DUNS)-Nummer in den Informationen eines Parteidatensatzes angezeigt werden?
-   Wenn die DUNS-Nummer in einem Parteidatensatz enthalten ist, sollte die Eindeutigkeit der Nummer überprüft werden?
-   Möchten Sie einen standardmäßigen Parteityp, -person oder -Organisation einrichten, wenn ein Parteidatensatz im globalen Adressbuch erstellt wird?
-   Welche Benutzerrollen sollen Zugriff auf private Adress- und Kontaktinformationen der Parteidatensätze haben?

## <a name="additional-address-books"></a>Zusätzliche Adressbücher
Nachdem Sie das globale Adressbuch erstellt haben, können Sie, wenn nötig, zusätzliche Adressbücher, wie z. B. ein separates Adressbuch für jedes Unternehmen in der Organisation oder für jede einzelne Sparte, erstellen. Fabrikam beispielsweise ist eine internationale Organisation mit mehreren Unternehmen und Sparten. Fabrikam plant die Erstellung eines Adressbuchs für jede Sparte. Für Sparten mit mehreren Standorten wie der für pneumatische Werkzeuge, erstellt Fabrikam ein Adressbuch für jeden Standort. Heiko, der IT-Manager bei Fabrikam, hat die folgende Liste von Adressbüchern erstellt, die erforderlich sind. Diese Liste beschreibt auch die Parteidatensätze, die jedes Adressbuch enthalten muss.

-   **Verträge Öffentlicher Sektor (PubSC)** – Parteidatensätze für alle Parteien, die an Verträgen im öffentlichen Sektor von Fabrikam beteiligt sind.
-   **Verträge Privatkundenbereich (PriSC)** – Parteidatensätze für alle Parteien, die an Verträgen im Privatkundenbereich von Fabrikam beteiligt sind.
-   **Elektronische Werkzeuge (ET)** – Parteidatensätze für alle Parteien, die am Einkauf oder Verkauf von elektronischen Werkzeugen beteiligt sind oder anderweitig mit den durch Fabrikam bereitgestellten oder für Fabrikam im Unternehmen Fabrikam-Japan eingekauften elektronischen Werkzeugen interagieren.
-   **Pneumatische Werkzeuge (PTJPN)** – Parteidatensätze für alle Parteien, die am Einkauf oder Verkauf von pneumatischen Werkzeugen beteiligt sind oder anderweitig mit den durch Fabrikam bereitgestellten oder für Fabrikam im Unternehmen Fabrikam-Japan eingekauften pneumatischen Werkzeugen interagieren.
-   **Pneumatische Werkzeuge (PTUSA)** – Parteidatensätze für alle Parteien, die am Einkauf oder Verkauf von pneumatischen Werkzeugen beteiligt sind oder anderweitig mit den durch Fabrikam bereitgestellten oder für Fabrikam im Unternehmen Fabrikam-USA eingekauften pneumatischen Werkzeugen interagieren.

**Entscheidung:**

-   Wie viele zusätzliche Adressbücher wollen Sie erstellen?

### <a name="address-book-security"></a>Adressbuch-Sicherheit

Adressbücher können jederzeit erstellt werden, und auch Sicherheitsparameter für die Adressbücher können jederzeit festgelegt werden. Sie müssen keine Sicherheitsrechte für ein Adressbuchfestlegen. Wenn Sie es aber nicht tun, können alle Arbeitskräfte in der Organisation alle Parteidatensätze im Adressbuch anzeigen. Sie können Sicherheitsrechte für Parteidatensätze über das Adressbuch festlegen. Sicherheitsrechte basieren auf Teams. Dieser Ansatz garantiert, dass Arbeitskräfte, die einem Team zugewiesen sind, das Zugriff auf ein Adressbuch hat, die Parteidatensätze in diesem Adressbuch anzeigen können. Sie müssen die Teams auswählen, die Zugriff auf jedes Adressbuch haben. Für jedes Adressbuch können Sicherheitsrechte festgelegt werden, die den Zugriff auf bestimmte Teams gestatten oder verweigern. Werden einem Team Rechte für ein Adressbuch gewährt, können alle Mitglieder dieses Teams die Datensätze im Adressbuch anzeigen. Wird einem Team kein Zugriff auf ein Adressbuch gewährt, kann die Mitglieder des Teams das Adressbuch oder dessen Inhalt nicht anzeigen. **Entscheidung:**

-   Welches Team soll Zugriff auf jedes neue Adressbuch haben, das Sie erstellen?



