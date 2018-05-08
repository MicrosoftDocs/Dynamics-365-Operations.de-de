---
title: "Elektronische Signatur (Überblick)"
description: "Dieser Artikel enthält einen Überblick über elektronische Signaturen und erläutert ihre Verwendung in Microsoft Dynamics 365 for Finance and Operations."
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 698b938e515ff4755c2f111279cda244577ac9f3
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="electronic-signature-overview"></a>Elektronische Signatur (Überblick)

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält einen Überblick über elektronische Signaturen und erläutert ihre Verwendung in Microsoft Dynamics 365 for Finance and Operations.

<a name="what-is-an-electronic-signature"></a>Was ist eine elektronische Signatur?
--------------------------------

Eine elektronische Signatur bestätigt die Identität einer Person, die im Begriff ist, einen Datenverarbeitungsprozess zu starten oder zu genehmigen. In einigen Branchen ist eine elektronische Signatur ebenso rechtskräftig wie eine handschriftliche Signatur. 

Elektronische Signaturen sind eine Konformitätsanforderung für verschiedene behördlich regulierte Branchen. Dazu zählen z. B. die Arzneimittel-, Lebensmittel- und Getränke-, Luftfahrt- und Rüstungsindustrie. Sie sind auch erforderlich, um die Konformität mit den Bestimmungen in 21 CFR Teil 11 der Bundesbehörde zur Überwachung von Nahrungs- und Arzneimitteln in den USA (Food and Drug Administration, FDA) zu gewährleisten. 

**Hinweis:** Eine elektronische Signatur ist nicht das Gleiche wie eine digitale Signatur. Eine elektronische Signatur ist einfach ein Ersatz für eine handschriftliche Signatur, während eine digitale Signatur zusätzliche Sicherheitsmerkmale bietet. Mithilfe einer digitalen Signatur kann festgestellt werden, ob die Daten durch einen anderen Benutzer oder Prozess manipuliert wurden. Außerdem kann eine digitale Signatur überprüft werden, und diese Überprüfung kann nicht vom Besitzer des Zertifikats angefochten werden, das zum Signieren der Daten verwendet wurde. Wie nachfolgend erläutert, verfügen elektronische Signaturen in Microsoft Dynamics 365 for Finance and Operations über die integrierte Funktion für digitale Signaturen.

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a>Elektronische Signaturen in Microsoft Dynamics 365 for Finance and Operations
In Finance and Operations können Sie elektronische Signaturen für wichtige Geschäftsprozesse verwenden. Einige Prozesse verfügen über integrierte Funktionen der elektronischen Signatur. Darüber hinaus können Sie benutzerdefinierte Signaturanforderungen für Datenbanktabellen und -felder erstellen. 

Elektronische Signaturen verfügen über die integrierte Funktion für digitale Signatur. Jeder Benutzer, der Dokumente signiert, muss über ein gültiges kryptografisches Zertifikat verfügen. Beim Signieren eines Dokuments wird der diesem Zertifikat zugeordnete private Schlüssel geprüft. Finance and Operations zeichnet Daten der elektronischen Signatur in einem Protokoll auf, um Informationen für ein Audit-Trail bereitzustellen. Um elektronische Signaturen einzurichten, siehe [Einrichten elektronischer Signaturen (Aufgabenleitfaden)](tasks/set-up-electronic-signatures.md).

## <a name="users-who-require-access-to-electronic-signatures"></a>Benutzer, die Zugriff auf elektronische Signaturen benötigen
Drei Arten von Benutzern brauchen in der Regel Sicherheitszugriff auf elektronische Signaturen: Administratoren für elektronische Signaturen, Signaturgeber und Wirtschaftsprüfer für elektronische Signaturen.

### <a name="electronic-signature-administrator"></a>Administrator für elektronische Signatur

Der Administrator der elektronischen Signatur richtet Signaturanforderungen, allgemeine Parameter sowie genehmigende Personen ein und erhält Warnmeldungen, wenn die Signatur nicht überprüft werden kann. Standardmäßig hat ein Benutzer, der der Sicherheitsrolle **Leiter IT** angehört, die Berechtigung zum Verwalten elektronischer Signaturen.

### <a name="signer"></a>Signaturgeber

Ein Signaturgeber stellt elektronische Signaturen für Dokumente und Prozesse bereit, die Signaturen erfordern. Standardmäßig hat ein Benutzer, der der Sicherheitsrolle **Systembenutzer** angehört, die Berechtigung zum elektronischen Signieren von Dokumenten. 

**Hinweis:** Der Signaturgeber benötigt unter Umständen zusätzliche Berechtigungen bevor Zugriff auf die Daten genehmigt wird, die dem zu signierenden Dokument oder Vorgang zugeordnet sind. Ein Benutzer, der Daten ändert und dann für diese Änderungen signieren muss, benötigt die Berechtigung zum Ändern der Daten. Ein Benutzer, der im Auftrag eines anderen Benutzers signiert, benötigt unter Umständen keinen Zugriff auf die Daten. Ein Beispiel dieser Art von Benutzer ist ein Supervisor, der für die Änderungen eines Mitarbeiters signiert.

### <a name="electronic-signature-auditor"></a>Wirtschaftsprüfer für elektronische Signatur

Der Wirtschaftsprüfer für elektronische Signatur überprüft das Datenbankprotokoll und das über das Datenbankprotokoll verfügbare Signaturprüfungsprotokoll. Standardmäßig hat ein Benutzer, der der Sicherheitsrolle **Leiter IT** angehört, die Berechtigung zum Überwachen elektronischer Signaturen. 

Wenn Sie eine andere Rolle als **Leiter IT** verwenden, sollten Sie sicherstellen, dass der Rolle die folgenden Berechtigungen zugewiesen wurden:

-   Elektronische Signaturfehler anzeigen
-   Datenbankprotokoll anzeigen

## <a name="signing-documents-electronically"></a>Elektronisches Signieren von Dokumenten
### <a name="get-a-certificate"></a>Erhalten eines Zertifikats

Vor dem elektronischen Signieren von Dokumenten in Finance and Operations muss ein Zertifikat angefordert werden. 

**Hinweis:** Finance and Operations verwendet Microsoft SQL Server-Funktionen zum Erstellen von Zertifikaten und Aktivieren elektronischer Signaturen. Es ist keine zusätzliche Infrastruktur für Zertifikate oder öffentliche Schlüssel (PKI) erforderlich. 

Beim Anfordern eines Zertifikats werden für Sie ein öffentlicher Schlüssel und ein privater Schlüssel in der Finance and Operations-Datenbank erstellt. Der private Schlüssel wird mit einem nur Ihnen bekannten Kennwort verschlüsselt. Beim elektronischen Signieren eines Dokuments wird Ihre Identität überprüft, wenn Sie das Kennwort eingeben. 

Um ein Zertifikat anzufordern, klicken Sie **Zertifikat abrufen** auf der Registerkarte **Konten** der Seite **Optionen**. 

Sie müssen das Kennwort, das Sie für Signaturen verwenden möchten, eingeben und bestätigen. Mithilfe des Kennworts wird Ihr privater Schlüssel geschützt und die Verwendung Ihres Zertifikats autorisiert. Dieses Kennwort wird nicht in der Datenbank gespeichert und ist für keine andere Person verfügbar, auch nicht für den Finance and Operations-Administrator. 

Wenn Sie das mit dem Zertifikat verknüpfte Kennwort vergessen haben, muss das Zertifikat zurückgesetzt werden. Wenn Sie das Zertifikat zurücksetzen, wirkt sich dies nicht auf mit dem vorherigen Zertifikat signierte Dokumente aus. Um das Zertifikat zurückzusetzen, klicken Sie **Zertifikat zurücksetzen** auf der Seite **Optionen**.

### <a name="sign-a-document-electronically"></a>Elektronisches Signieren eines Dokuments

Die Seite **Dokument signieren** wird angezeigt, wenn Sie eine Änderung vornehmen, die eine elektronische Signatur erfordert.

1.  Klicken Sie auf der Seite **Dokument signieren** auf die Registerkarte **Dokument**, um die Änderungen am Dokument zu überprüfen.
2.  Wählen Sie auf der Registerkarte **Signatur** einen Ursachencode aus.
3.  Geben Sie einen Kommentar ein, wenn erforderlich.
4.  Wenn im Feld **Signaturgeber** nicht Ihre Benutzerkennung angezeigt wird, wählen Sie sie aus der Liste aus.
5.  Geben Sie Ihren Standort ein, wenn erforderlich.
6.  Klicken Sie auf **OK**.

### <a name="sign-for-another-users-changes"></a>Signieren für die Änderungen eines anderen Benutzers

Gelegentlich kann es sinnvoll sein, dass ein Benutzer für die Änderungen eines anderen Benutzers signiert. So kann es beispielsweise vorkommen, dass ein Supervisor Änderungen abzeichnen muss, die ein Mitarbeiter an einer Stückliste (BOM) vornimmt. Mit diesem Verfahren legen Sie einen Finance and Operations-Benutzer als Signaturgeber für einen anderen Benutzer fest. 

**Hinweis:** Wenn ein Benutzer die Änderungen eines anderen Benutzers abzeichnet, muss die Signatur auf der Arbeitsstation des Benutzers bereitgestellt werden, der die Änderung vorgenommen hat. Der Benutzer kann die Änderung erst speichern, wenn die Signatur vorliegt. 

Gehen Sie folgendermaßen vor, um einen Genehmiger festzulegen.

1.  Klicken Sie auf der Seite **Optionen**, auf der Registerkarte **Konten** auf **Genehmigende Person festlegen**.
2.  Wählen Sie im Feld **Benutzerkennung für genehmigende Person** die Kennung des Benutzers aus, der die Änderungen eines anderen Benutzers abzeichnen muss.
3.  Wählen Sie im Feld **Signatur für Benutzer (Kennung)** die Kennung des Benutzers aus, dessen Änderungen abgezeichnet werden müssen.





