---
title: Für das globale Adressbuch und andere Adressbücher planen
description: Dieser Artikel beschreibt die Überlegungen und Entscheidungen, die Sie während des Planungsprozesses machen müssen.
author: msftbrking
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288c96d8c877f5e3b3101080294b2f6cdeb39882
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863158"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Für das globale Adressbuch und andere Adressbücher planen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Überlegungen und die Entscheidungen, die Sie während des Planungsprozesses vornehmen müssen, bevor Sie das globale Adressbuch und alle zusätzlichen Adressbücher einrichten und konfigurieren. Einige der Entscheidungen erfordern, dass Sie die Entscheidungen bestätigen, die für andere Bereiche des Produkts getroffen wurden, wie die Organisationshierarchie.

## <a name="global-address-book"></a>Globales Adressbuch

Bevor Sie beginnen mit dem globalen Adressbuch zu arbeiten, müssen Sie die dafür notwendigen Standardwerte bestimmen. Diese Standardwerte werden dann für weitere Adressbücher verwendet, die Sie erstellen.

**Entscheidungen**

- In welcher Reihenfolge sollen die Namen der Parteidatensätze vom Typ **Person** angezeigt werden? So kann beispielsweise eine Reihenfolge Nachname, zweiter Vorname, Vorname sein.
- Müssen Parteidatensätze aus dem Adressbuch gelöscht werden, wenn die Rolle Datensatz gelöscht wird? Sollte der Parteidatensatz auch gelöscht werden, wenn beispielsweise ein Debitorendatensatz gelöscht wird?
- Sollten Benutzer benachrichtigt werden, sobald ein doppelter Datensatz im globalen Adressbuch gefunden wird, wenn ein neuer Datensatz erstellt wird?
- Sollte die Data Universal Numbering System (DUNS)-Nummer in den Informationen eines Parteidatensatzes angezeigt werden?
- Wenn die DUNS-Nummer in einem Parteidatensatz enthalten ist, sollte die Eindeutigkeit der Nummer überprüft werden?
- Möchten Sie einen standardmäßigen Parteityp, -person oder -Organisation einrichten, wenn ein Parteidatensatz im globalen Adressbuch erstellt wird?
- Welche Benutzerrollen sollen Zugriff auf private Adress- und Kontaktinformationen der Parteidatensätze haben?

## <a name="additional-address-books"></a>Zusätzliche Adressbücher

Nachdem Sie das globale Adressbuch erstellt haben, können Sie, wenn nötig, zusätzliche Adressbücher, wie z. B. ein separates Adressbuch für jedes Unternehmen in der Organisation oder für jede einzelne Sparte, erstellen. Fabrikam beispielsweise ist eine internationale Organisation mit mehreren Unternehmen und Sparten. Fabrikam plant die Erstellung eines Adressbuchs für jede Sparte. Für Sparten mit mehreren Standorten wie der für pneumatische Werkzeuge, erstellt Fabrikam ein Adressbuch für jeden Standort. Heiko, der IT-Manager bei Fabrikam, hat die folgende Liste von Adressbüchern erstellt, die erforderlich sind. Diese Liste beschreibt auch die Parteidatensätze, die jedes Adressbuch enthalten muss.

- **Verträge Öffentlicher Sektor (PubSC)** – Parteidatensätze für alle Parteien, die an Verträgen im öffentlichen Sektor von Fabrikam beteiligt sind.
- **Verträge Privatkundenbereich (PriSC)** – Parteidatensätze für alle Parteien, die an Verträgen im Privatkundenbereich von Fabrikam beteiligt sind.
- **Elektronische Werkzeuge (ET)** – Parteidatensätze für alle Parteien, die am Einkauf oder Verkauf von elektronischen Werkzeugen beteiligt sind oder anderweitig mit den durch Fabrikam bereitgestellten oder für Fabrikam im Unternehmen Fabrikam-Japan eingekauften elektronischen Werkzeugen interagieren.
- **Pneumatische Werkzeuge (PTJPN)** – Parteidatensätze für alle Parteien, die am Einkauf oder Verkauf von pneumatischen Werkzeugen beteiligt sind oder anderweitig mit den durch Fabrikam bereitgestellten oder für Fabrikam im Unternehmen Fabrikam-Japan eingekauften pneumatischen Werkzeugen interagieren.
- **Pneumatische Werkzeuge (PTUSA)** – Parteidatensätze für alle Parteien, die am Einkauf oder Verkauf von pneumatischen Werkzeugen beteiligt sind oder anderweitig mit den durch Fabrikam bereitgestellten oder für Fabrikam im Unternehmen Fabrikam-USA eingekauften pneumatischen Werkzeugen interagieren.

**Entscheidung:**

- Wie viele zusätzliche Adressbücher wollen Sie erstellen?


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]