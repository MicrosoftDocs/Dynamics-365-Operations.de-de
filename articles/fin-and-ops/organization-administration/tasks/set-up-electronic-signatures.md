---
title: Einrichten elektronischer Signaturen
description: Verwenden Sie diese Prozedur, um elektronische Signaturen einzurichten.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb6bf529b1e94d598e219482f182140402f2928a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "318579"
---
# <a name="set-up-electronic-signatures"></a>Einrichten elektronischer Signaturen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Verwenden Sie diese Prozedur, um elektronische Signaturen einzurichten. Eine elektronische Signatur bestätigt die Identität einer Person, die im Begriff ist, einen Datenverarbeitungsprozess zu starten oder zu genehmigen. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DAT.


## <a name="enable-the-electronic-signature-configuration-key"></a>Konfigurationsschlüssel "Elektronische Signatur " aktivieren
1. Gehen Sie zu "Systemadministration" > "Einstellungen" > "Lizenzkonfiguration".
2. Erweitern Sie 'Administration' in der Struktur.
    * Vergewissern Sie sich, dass das Kontrollkästchen Elektronische Signatur aktiviert ist.  
    * Wenn das Kontrollkästchen für elektronische Signatur nicht aktiviert ist, müssen Sie Wartungsmodus aktivieren. Sie können den Wartungsmodus in dieser Umgebung aktivieren, indem Sie den Wartungsvorgang über Lifecycle Services durchführen oder das Deployment.Setup-Tool lokal verwenden.  
3. Schließen Sie die Seite.

## <a name="set-up-electronic-signature-parameters"></a>Einrichten von Parametern für elektronische Signaturen
1. Wechseln Sie zu "Organisationsverwaltung" > "Einrichten" > "Elektronische Signatur" > "Parameter für elektronische Signatur".
2. Klicken Sie auf "Bearbeiten".
3. Geben Sie im Feld Hinweis einen Wert ein.
    * Geben Sie den Hinweis ein, den Signaturgeber empfangen, wenn eine Signatur angefordert wird. Sie können einen beliebigen Text eingeben. In der Regel informiert dieser Text den Benutzer über die Bedeutung des elektronischen Signierens eines Dokuments.  
    * Klicken Sie auf die Schaltfläche Übersetzungen, um den Hinweistext in weiteren Sprachen einzugeben.  
4. Klicken Sie auf "Speichern".
5. Schließen Sie die Seite.

## <a name="set-up-reason-codes-for-electronic-signatures"></a>Einrichten von Ursachencodes für elektronische Signaturen
1. Wechseln Sie zu "Organisationsverwaltung" > "Elektronische Signatur einrichten" > "Gründe für elektronische Signatur".
2. Klicken Sie auf "Neu".
    * Ursachencodes müssen vor der Verwendung elektronischer Signaturen eingerichtet werden. Zum Signieren eines Dokuments ist ein gültiger Ursachencode erforderlich.     Ein Signaturgeber wählt einen Ursachencode aus, um den Zweck einer elektronischen Signatur anzugeben. Mit einem Ursachencode könnte z. B. eine rechtliche Genehmigung angezeigt werden.  
3. Geben Sie im Feld "Grundcode" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Geben Sie Ursachencodes, nach Bedarf ein.  
5. Klicken Sie auf "Speichern".
6. Schließen Sie die Seite.

## <a name="require-electronic-signatures-for-existing-processes"></a>Anfordern elektronischer Signaturen für vorhandene Prozesse
1. Wechseln Sie zu "Organisationsverwaltung" > "Einrichtung" > "Elektronische Signatur einrichten" > "Anforderungen für elektronische Signatur".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Auswählen eines Prozesses, der elektronische Signaturen erfordert.  
3. Aktivieren oder deaktivieren Sie das Kontrollkästchen Signatur erforderlich.
    * Wiederholen Sie diese Schritte für jeden Prozess, der elektronische Signaturen erfordert.  
4. Klicken Sie auf "Speichern".

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>Erstellen einer benutzerdefinierten Anforderung für elektronische Signaturen
1. Klicken Sie auf "Neu".
2. Aktivieren oder deaktivieren Sie das Kontrollkästchen Signatur erforderlich.
3. Geben Sie im Feld Name einen eindeutigen Namen für den Prozess ein, der elektronische Signaturen erfordert.
4. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Suchen und wählen Sie in der Liste die Tabelle aus, in der die zu signierenden Daten gespeichert sind.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie im Feld "Feldname" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Wählen Sie in der Liste das Feld in der Tabelle aus, das überwacht werden soll.
9. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Geben Sie an, wann eine Signatur erforderlich ist.     Wählen Sie Immer aus, wenn eine Signatur erforderlich ist, wenn sich die Felddaten ändern.     Wählen Sie Nur aus, wenn eine Signatur nur unter bestimmten Bedingungen erforderlich ist. Wenn Sie Nur auswählen, müssen Sie eine der folgenden Optionen auch auswählen: Wenn ein Datensatz eingefügt wird, wenn ein Datensatz aktualisiert wird oder wenn ein Datensatz gelöscht wird.  
10. Klicken Sie auf "Speichern".
11. Schließen Sie die Seite.

