---
title: Asynchroner Debitorerstellungsmodus
description: Dieser Artikel beschreibt den asynchronen Debitorerstellungsmodus in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b2926339021991f87dd3eadef94da3b500c954cf
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690288"
---
# <a name="asynchronous-customer-creation-mode"></a>Asynchroner Debitorerstellungsmodus

[!include [banner](includes/banner.md)]

Dieser Artikel beschreibt den asynchronen Debitorerstellungsmodus in Microsoft Dynamics 365 Commerce.

In Commerce gibt es zwei Arten der Debitorerstellung: synchron (oder sync) und asynchron (oder async). Standardmäßig werden Debitoren synchron erstellt. Mit anderen Worten, sie werden in Echtzeit in den Commerce headquarters erstellt. Der sync-Modus für die Debitorerstellung ist von Vorteil, da neue Debitoren sofort kanalübergreifend durchsucht werden können. Es hat jedoch auch einen Nachteil. Weil es [Commerce Data Exchange: Echtzeitservice](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)-Aufrufe an die Commerce-Zentrale erzeugt, kann die Leistung beeinträchtigt werden, wenn viele Aufrufe zur Debitorerstellung gleichzeitig getätigt werden.

Wenn die Option **Debitor im asynchronen Modus erstellen** auf **Ja** gesetzt ist im Funktionsprofil des Geschäfts (**Retail und Commerce \> Kanaleinrichtung \> Einrichtung Onlineshop \> Funktionsprofile**), werden Echtzeit-Serviceaufrufe nicht zum Erstellen von Debitordatensätzen in der Debitordatenbank verwendet. Der asynchrone Debitorerstellungsmodus wirkt sich nicht auf die Leistung der Commerce-Zentrale aus. Jedem neuen asynchrone Debitordatensatz wird eine temporäre GUID (Globally Unique Identifier) zugewiesen und als Debitorenkontokennung verwendet. Diese GUID wird Benutzern der Verkaufsstelle (POS) nicht angezeigt. Stattdessen werden diese Benutzer **Ausstehende Synchronisierung** als Debitorenkontokennung sehen.

> [!IMPORTANT]
> Wann immer der POS offline geschaltet wird, erstellt das System die Debitoren selbst dann automatisch asynchron, wenn der asynchrone Debitorenerstellungsmodus deaktiviert ist. Daher müssen Administratoren der Commerce headquarters ungeachtet Ihrer Auswahl bei der Ersteller synchroner und asynchroner Debitoren wiederkehrenden Stapelverarbeitungsauftrag für den **P-Einzelvorgang**, den Einzelvorgang **Debitoren und Geschäftspartner im asynchronen Modus synchronisieren** und den Einzelvorgang **1010** erstellen und planen, sodass alle asynchrone Debitoren im Commerce headquarters in synchrone Debitoren konvertiert werden.

## <a name="async-customer-limitations"></a>Asynchrone Debitorenbeschränkungen

Die asynchrone Debitorenfunktionalität weist derzeit die folgende Einschränkung auf:

- Kundenkarten können nur dann an asynchrone Debitoren ausgegeben werden, wenn die neue Debitorenkonto-ID wieder mit dem Kanal synchronisiert wurde.

## <a name="async-customer-enhancements"></a>Verbesserungen bei asynchronen Debitoren

Um Organisationen bei der Verwendung des asynchronen Debitorenerstellungsmodus zum Verwalten von Debitoren zu unterstützen und die Echtzeitkommunikation mit den Commerce headquarters zu reduzieren, wurden die folgenden Verbesserungen eingeführt, um Parität zwischen synchronen und asynchronen Modi in Kanälen herzustellen. 

| Funktionsverbesserung | Commerce-Version | Funktionsdetails |
|---|---|---|
| Leistungsverbesserungen beim Abrufen von Debitoreninformationen aus der Kanaldatenbank | 10.0.20 und höher | Um die Leistung zu verbessern, wird die Debitorenentität in kleinere Einheiten aufgeteilt. Das System ruft dann nur die erforderlichen Informationen aus der Kanaldatenbank ab. |
| Möglichkeit zum asynchronen Erstellen von Adressen während des Bezahlvorgangs | 10.0.22 und höher | <p>Funktionsschalter: **Asynchrone Erstellung für Debitorenadressen aktivieren**</p><p>Funktionsdetails:</p><ul><li>Möglichkeit, Adressen hinzuzufügen, ohne Dienstaufrufe in Echtzeit an die Commerce headquarters zu tätigen</li><li>Möglichkeit, Adressen in der Kanaldatenbank eindeutig zu identifizieren, ohne eine Datensatz-ID zu verwenden (**RecId**-Wert)</li><li>Nachverfolgungs-Zeitstempel für die Adresserstellung</li><li>Synchronisierung von Adressen in Commerce headquarters</li></ul><p>Diese Funktion betrifft sowohl synchrone als auch asynchrone Debitoren. Um Adressen zusätzlich zum asynchronen Erstellen asynchron zu bearbeiten, müssen Sie die Funktion **Debitoren im asynchronen Modus bearbeiten** aktivieren.</p> |
| Aktivieren Sie die Parität zwischen der Erstellung synchroner und asynchroner Debitoren. | 10.0.24 und höher | <p>Funktionsschalter: **Erweiterte asynchrone Debitorenerstellung aktivieren**</p><p>Funktionsdetails: Möglichkeit, zusätzliche Informationen zu erfassen, z. B. den Titel, Zugehörigkeiten des Standarddebitors und sekundäre Kontaktinformationen (Telefonnummer und E-Mail-Adresse), während Sie Debitoren asynchron erstellen</p> |
| Benutzerfreundliche Fehlermeldungen | 10.0.28 und höher | Diese Verbesserungen helfen, benutzerfreundliche Fehlermeldungen zu verbessern, wenn ein Benutzer Informationen nicht sofort bearbeiten kann, während die Synchronisierung läuft. Sie aktivieren diese Verbesserungen mit der Einstellung **Zulassen, dass bestimmte Benutzeroberflächenelemente von einem asynchronen Debitor nicht geändert werden können** im Commerce-Seitengenerator **Seiteneinstellungen \> Erweiterungen**. |
| Möglichkeit, Debitorinformationen asynchron zu bearbeiten | 10.0.29 und höher | <p>Funktionsschalter: **Bearbeitung von Debitoren im asynchronen Modus ermöglichen**</p><p>Funktionsdetails: Möglichkeit, Debitorendaten asynchron zu bearbeiten</p><p>Antworten auf häufig gestellte Fragen zu Problemen im Zusammenhang mit der asynchronen Bearbeitung von Debitoreninformationen finden Sie unter [Häufig gestellte Fragen zum asynchronen Debitorenerstellungsmodus](async-customer-mode-faq.md).</p> |
| Möglichkeit, die Synchronisierung von Kundenverwaltungsvorgängen zu prüfen | 10.0.31 und höher | Diese Verbesserung ermöglicht es Benutzern, die Synchronisierung von Kundenverwaltungsvorgängen in der Commerce Headquarters zu prüfen. Außerdem können Benutzer bei Bedarf Änderungen vornehmen und die Daten synchronisieren. |

### <a name="feature-switch-hierarchy"></a>Funktionsschalterhierarchie

Aufgrund der Hierarchie der Funktionsschalter müssen Sie, bevor Sie die Funktion **Bearbeitung von Debitoren im asynchronen Modus ermöglichen** aktivieren, die folgenden Funktionen aktivieren: 

- **Leistungsverbesserungen bei Debitorenaufträgen und Debitorentransaktionen**: Diese Funktion ist seit der Commerce-Version 10.0.28 obligatorisch. 
- **Erweiterte asynchrone Debitorenerstellung aktivieren**
- **Asynchrone Erstellung für Kundenadressen aktivieren**

Antworten auf häufig gestellte Fragen zur Problembehandlung finden Sie unter [Häufig gestellte Fragen zum asynchronen Debitorenerstellungsmodus](async-customer-mode-faq.md). 

Nachdem Sie die zuvor erwähnten Funktionen aktiviert haben, müssen Sie einen wiederkehrenden Batchauftrag für den **P-Einzelvorgang**, den Einzelvorgang **Debitoren und Geschäftspartner im asynchronen Modus synchronisieren** und den Einzelvorgang **1010** erstellen und planen, sodass alle asynchrone Debitoren in der Commerce-Zentrale in synchrone Debitoren konvertiert werden.

### <a name="customer-creation-in-pos-offline-mode"></a>Debitorenerstellung im POS-Offlinemodus

Wie zuvor erwähnt: wann immer das POS offline geschaltet wird, erstellt das System die Debitoren selbst dann automatisch asynchron, wenn der asynchrone Debitorenerstellungsmodus deaktiviert ist. Daher müssen Administratoren der Commerce-Zentrale einen wiederkehrenden Batchauftrag für den **P-Einzelvorgang**, den Einzelvorgang **Debitoren und Geschäftspartner im asynchronen Modus synchronisieren** und den Einzelvorgang **1010** erstellen und planen, sodass alle asynchrone Debitoren in der Commerce-Zentrale in synchrone Debitoren konvertiert werden.

> [!NOTE]
> Wenn die Option **Gemeinsam genutzte Debitorendatentabellen filtern** auf **Ja** auf der Seite **Handelskanalschema** (**Retail und Commerce \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Kanaldatenbankgruppe**) gesetzt ist, werden Debitorendatensätze nicht im POS-Offlinemodus erstellt. Weitere Informationen finden Sie unter [Ausschluss von Offlinedaten](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Debitorenverwaltung in Geschäften](customer-mgmt-stores.md)

[Asynchrone Debitoren in synchrone Debitoren konvertieren](convert-async-to-sync.md)

[Debitorattribute](dev-itpro/customer-attributes.md)

[Ausschluss von Offlinedaten](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
