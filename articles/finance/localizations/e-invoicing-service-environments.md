---
title: Dienstumgebungen
description: Dieser Artikel enthält Informationen über Dienstumgebungen für die elektronische Rechnungsstellung und erklärt, wie Sie diese festlegen.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8c743c5b2fbc7dcc3ae04fa4d7ca0e65de6c2507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901246"
---
# <a name="service-environments"></a>Dienstumgebungen

[!include [banner](../includes/banner.md)]

Serviceumgebungen sind logische Partitionen, die erstellt werden, um die Funktionen der Globalisierung und die entsprechenden Belege, die im Dienst für die elektronische Rechnungsstellung verarbeitet werden, zu unterstützen. Die Sicherheitsgeheimnisse und digitalen Zertifikate sowie die Berechtigungen für den Zugriff (Governance) müssen auf der Ebene der Serviceumgebung konfiguriert werden.

Sie können so viele Service-Umgebungen erstellen, wie Sie benötigen. Alle von Ihnen erstellten Serviceumgebungen sind voneinander unabhängig. Als bewährtes Verfahren empfehlen wir Ihnen, mindestens zwei Umgebungen für den Service zu erstellen:

- Eine Umgebung für Hauptentwicklungs- und Validierungszwecke. Bei dieser Umgebung handelt es sich in der Regel um eine Umgebung für Benutzerakzeptanztests (UAT).
- Eine Umgebung für Produktionszwecke. Bei dieser Umgebung handelt es sich in der Regel um eine Produktionsumgebung.

Diese Art der Partitionierung trägt dazu bei, dass die E-Invoicing-Prozesse in der Sandbox validiert und angepasst werden, bevor sie in die Produktion gehen.

Serviceumgebungen müssen im Regulatory Configuration Service (RCS) erstellt und verwaltet werden. Wenn sie dann fertig sind, müssen sie im Dienst für die elektronische Rechnungsstellung veröffentlicht werden. Der Veröffentlichungsprozess sendet die Parameter der Umgebung des Services von der RCS-Instanz an den Dienst für die elektronische Rechnungsstellung.

Wenn Sie den Veröffentlichungsprozess nicht abschließen, nachdem Sie eine neue Umgebung erstellt oder eine bestehende Umgebung angepasst haben (z.B. durch Hinzufügen oder Entfernen von Benutzern oder Microsoft Azure Key Vault-Geheimnissen), werden die Änderungen nicht wirksam. Nur auf veröffentlichte Umgebungen kann über Dynamics 365 Finance oder Dynamics 365 Supply Chain Management zugegriffen werden.

## <a name="service-environment-statuses"></a>Status der Service-Umgebung

Serviceumgebungen können über ihren Status verwaltet werden. Sie können den Status einer Umgebung auf der Seite **Serviceumgebungen** einsehen. Die folgenden Status sind verfügbar:

- **Nicht veröffentlicht** – Die Umgebung wurde erstellt, aber noch nicht veröffentlicht.
- **Veröffentlicht** - Die Umgebung wurde für den Dienst für die elektronische Rechnungsstellung veröffentlicht.
- **Geändert** – Die Attribute einer veröffentlichten Umgebung wurden geändert, die Änderungen wurden jedoch noch nicht veröffentlicht.

## <a name="users"></a>Benutzer

In jeder Umgebung müssen die Benutzer aufgeführt werden, die eine Verbindung zur Elektronischen Rechnungsstellung von Finance oder Supply Chain Management aus herstellen können.

## <a name="applications"></a>Bewerbungen

In einigen Szenarien müssen möglicherweise andere Anwendungen als Finance oder Supply Chain Management eine Verbindung zum Dienst für die elektronische Rechnungsstellung herstellen, um elektronische Belege zur weiteren Verarbeitung zu senden oder um Informationen wie den Einreichungsstatus eines Belegs abzurufen. In diesen Szenarien sollte die Anwendung in der Liste der Anwendungen definiert sein. Auf diese Weise erhält sie Zugriff auf den Dienst für die elektronische Rechnungsstellung. Die Anwendung muss auch als Anwendung in Azure Active Directory (Azure AD) registriert werden und die Objekt-ID muss zu ihrer Identifizierung verwendet werden. 

Da Microsoft ein hohes Maß an Steuerelementen für Anwendungen verlangt, die sich mit dem Dienst für die elektronische Rechnungsstellung verbinden können, müssen Sie Microsoft unter <DGXRegulatoryservicesengineering@service.microsoft.com> kontaktieren und die folgenden Details zu Ihrer Anwendung angeben:

- Azure AD-Mandanten-ID
- Microsoft Dynamics Lifecycle Services (LCS) Umgebungs-ID
- Anwendungs-ID (Client ID)
- Objektkennung
- Begründung und eine ausführliche Beschreibung der Anwendung

Microsoft prüft die Anfrage und registriert die Anwendung im Sicherheitsregister, um sicherzustellen, dass sie mit Elektronischer Rechnungsstellung arbeiten kann.

## <a name="number-sequences"></a>Nummernkreise

Wenn Ihre Szenarien Nummernkreise erfordern (z.B. in Dateinamen), können Sie Nummernkreise verwenden, die für eine bestimmte Umgebung definiert sind, aber entweder für alle Globalisierungsfunktionen oder für eine bestimmte Globalisierungsfunktion verwendet werden können. Nachdem ein Nummernkreis definiert ist, können Sie ihn in Variablen und Verarbeitungs-Pipelines verwenden. Um die Verwendung zu verfolgen, suchen Sie auf der Seite **Nummernkreise** nach einem Wert von **Aktuell** für den Parameter **In Verwendung**.

### <a name="working-with-number-sequences"></a>Arbeiten mit Nummernkreisen
Auf der Seite **Nummernkreise**: 

- Wählen Sie **Neu**, um eine Sequenz zu erstellen. Geben Sie dann einen Namen und eine Beschreibung ein. 
- Wählen Sie **Löschen**, um eine Sequenz zu löschen, wenn sie nicht mehr verwendet wird.
- Sie müssen nicht **Veröffentlichen** im Aktionsbereich wählen, um die Änderungen an einer Sequenz zu veröffentlichen. Die Aktualisierung wird automatisch durchgeführt.

## <a name="create-a-key-vault-reference"></a>Erzeugen Sie eine Key Vault-Referenz

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie auf der Seite **Einrichtung der Umgebung** im Aktionsbereich **Dienstumgebungen**.
4. Wählen Sie auf der Seite **Dienstumgebungen** im Aktionsbereich **Key Vault Parameter**.
5. Wählen Sie auf der Seite **Schlüsseltresor-Parameter** die Option **Neu**, um einen Verweis auf den Key Vault zu erstellen.
6. Geben Sie in das Feld **Name** den Namen der Key Vault Referenz ein.
7. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
8. Fügen Sie in das Feld **Key Vault URI** die Key Vault URI aus dem Key Vault ein (`https://<your key vault>.vault.azure.net/`). Weitere Informationen finden Sie unter [Erstellen eines Azure Key Vault im Azure-Portal](e-invoicing-create-azure-key-vault-azure-portal.md).
9. Wählen Sie **Speichern** aus.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Erzeugen Sie ein Geheimnis für den geheimen Token des Lagerkontos

1. Wählen Sie auf der Seite **Key Vault-Parameter** die Key Vault-Referenz aus, die Sie im vorherigen Verfahren erstellt haben, und wählen Sie dann im Abschnitt **Zertifikate** die Option **Hinzufügen**.
2. Geben Sie im Feld **Name** den Namen des Speicherkontogeheimnisses ein. Dieser Name sollte mit dem Namen des Key Vault-Geheimnisses übereinstimmen, das das Token für den gemeinsamen Zugriff auf den Speicher (SAS) enthält. Weitere Informationen finden Sie unter [Erstellen eines Azure-Speicherkontos im Azure-Portal](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
4. Wählen Sie im Feld **Typ** **Geheimnis** aus.
5. Wählen Sie **Speichern** aus.
    
## <a name="create-a-service-environment"></a>Eine Service-Umgebung erstellen

1. Wählen Sie auf der Seite **Dienstumgebungen** die Option **Neu**, um eine Dienstumgebung zu erstellen.
2. Geben Sie in das Feld **Name** den Namen der Umgebung für die Elektronische Rechnungsstellung ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
4. Wählen Sie im Feld **Storage SAS-Tokengeheimnis** den Namen des Speicherkontogeheimnisses aus, das zur Authentifizierung des Zugriffs auf das Speicherkonto verwendet werden muss.
5. Wählen Sie im Bereich **Benutzer** die Option **Hinzufügen**, um einen Benutzer hinzuzufügen, der elektronische Rechnungen über die Umgebung senden und sich mit dem Speicherkonto verbinden darf.
6. Geben Sie im Feld **Benutzer-ID** den Alias des Benutzers ein. 
7. Geben Sie im Feld **E-Mail** die E-Mail-Adresse des Benutzers ein.
8. Wählen Sie **Speichern** aus.
9. Wählen Sie im Aktionsbereich **Veröffentlichen**, um die Umgebung für den Dienst für die elektronische Rechnungsstellung zu veröffentlichen. Überprüfen Sie, ob der Wert des Feldes **Status** auf **Veröffentlicht** geändert wurde.
