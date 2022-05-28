---
title: Versiegeltes Angebot für Angebotsanforderungen
description: In diesem Thema wird beschrieben, wie Sie versiegelte Angebote einrichten, um die Angebotsantworten von Kreditoren geheim zu halten, bis die Versiegelung vom Einkaufspersonal aufgehoben wird.
author: GalynaFedorova
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: dfc19646d6724627c8a25bcfc8a6b2a70a73c261
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675148"
---
# <a name="sealed-bidding-for-rfqs"></a>Versiegeltes Angebot für Angebotsanforderungen

[!include [banner](../includes/banner.md)]

Durch versiegelte Angebote bleiben Angebotsantworten von Kreditoren geheim, bis die Versiegelung vom Einkaufspersonal aufgehoben wird. Alle Angebote, die sich auf eine Angebotsanforderung (RFQ) beziehen, können erst nach Ablauf des Angebots entsiegelt werden. Bevor die Versiegelung eines Angebots aufgehoben wird, können nur Benutzer mit dedizierten Benutzerrollen und die den Kreditor vertreten darauf zugreifen.

> [!IMPORTANT]
> Das Ändern oder Erweitern von Formularen oder das Erstellen neuer Formulare oder Geschäftslogik kann den Schutz, den Microsoft für versiegelte Angebotsabgaben bietet, zunichte machen. Sie tragen das Risiko der Verwendung von Änderungen, Erweiterungen, neuen Formularen oder Geschäftslogik oder der Unfähigkeit, die Funktion für die versiegelte Angebotsabgabe aufgrund solcher Änderungen, Erweiterungen, neuer Formulare oder Geschäftslogik zu verwenden.  Microsoft ist nicht verantwortlich für Schäden, die sich aus Änderungen oder Erweiterungen von Formularen oder neuen Formularen oder Geschäftslogiken ergeben, die Sie oder ein Dritter für Sie erstellen. Microsoft bietet keinen technischen oder sonstigen Support für Änderungen, Erweiterungen, neue Formulare oder Geschäftslogiken, die von Ihnen oder Dritten in Ihrem Namen vorgenommen werden. Sie allein sind für die Einhaltung aller geltenden Gesetze oder Vorschriften in Bezug auf versiegelte Angebotsabgaben verantwortlich.

## <a name="how-bids-are-kept-secure"></a>So werden Angebote geschützt

Versiegelte Angebote verwenden eine asymmetrische Verschlüsselung zum Verschlüsseln des Verschlüsselungsschlüssels (KEK) des Angebots und eine symmetrische Verschlüsselung zum Verschlüsseln des tatsächlichen Angebots. Das System ist mit Microsoft Azure Key Vault integriert, um die Verschlüsselungsschlüssel, die zum Verschlüsseln versiegelter Angebote verwendet werden, zu generieren und zu verwalten. Jedes Angebot hat seinen eigenen Verschlüsselungsschlüssel. Diese Verschlüsselung wird sicher in einem Schlüsseltresor aufbewahrt, der sich im Besitz der Organisation befindet, die Dynamics 365 Supply Chain Management ausführt. Das System greift bei Bedarf auf den Schlüsseltresor zu, wenn eine Verschlüsselung erforderlich ist oder aufgehoben werden soll.

## <a name="setup-and-configuration"></a>Einrichtung und Konfiguration

In diesem Abschnitt werden die Voraussetzungen beschrieben, die erfüllt sein müssen, bevor Sie Angebotsanforderungen versenden können, die eine versiegelte Angebotsabgabe erfordern.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>Schritt 1: Nutzerzugriff auf versiegelte Angebote festlegen

Wenn Sie versiegelte Angebote verwenden, können nur Benutzer, die als Kontaktperson eines Kreditors festgelegt sind, Angebote für diesen Kreditor anzeigen, bearbeiten und abgeben, bis die Angebotsfrist abgelaufen ist. Diese Benutzer müssen die Rolle **Kreditor (extern)** haben, und sie müssen als Kontaktperson für das Kreditorenkonto festgelegt werden. Die Kontaktperson muss auch die Berechtigung zur Zusammenarbeit mit Kreditoren haben, wie in [Kreditorenzusammenarbeit einrichten und verwalten](set-up-maintain-vendor-collaboration.md) beschrieben.

Da Benutzer mit entsprechenden Berechtigungen, die als Kreditorenkontakte eingerichtet sind, auf die versiegelten Angebote für einen Kreditoren zugreifen können, ist es wichtig, nachzuverfolgen, wer diese Benutzer sind. Der Systemadministrator, der Benutzer und Sicherheitsrollen einrichtet, ist dafür verantwortlich, den Zugriff auf versiegelte Angebote auf die Benutzer zu beschränken, die sie wirklich sehen dürfen.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>Schritt 2: Die Funktion für versiegelte Angebote aktivieren

Bevor Sie mit der Einrichtung oder Verwendung dieser Funktion beginnen, müssen Sie sicherstellen, dass sie in Ihrem System verfügbar ist. Administratoren können den Arbeitsbereich **[Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** verwenden, um den Status der Funktion zu prüfen und sie einzuschalten. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Beschaffung*
- **Funktionsname:** *Versiegeltes Angebote für Angebotsanforderungen*

### <a name="step-3-set-up-azure-key-vault"></a>Schritt 3. Azure Key Vault einrichten

Supply Chain Management verwendet Verschlüsselungsschlüssel, um alle versiegelten Angebote zu schützen und sie bis zum entsprechenden Zeitpunkt geheim zu halten. Es nutzt die Funktionen von Key Vault, um die erforderlichen Schlüssel zu generieren und zu verwalten. Daher müssen Sie eine Verbindung von Supply Chain Management zu einem Schlüsseltresor einrichten, um das System zu aktivieren.

> [!IMPORTANT]
> Die Schlüsseltresore, die Sie für versiegelte Gebote verwenden, müssen die folgenden Anforderungen erfüllen:
>
> - Wenn Sie eine Sandbox zum Entwickeln und Testen verwenden, benötigen Sie einen dedizierten Schlüsseltresor für die Sandbox und einen separaten für die Produktion.
> - Jeder Schlüsseltresor muss in einem Azure-Abonnement erstellt werden, das sich im Besitz Ihrer Organisation befindet (nicht das Abonnement, in dem Sie Supply Chain Management ausführen).
> - Jeder Schlüsseltresor darf ausschließlich für versiegelte Gebote verwendet werden. Sie dürfen Ihre versiegelten Gebotsschlüsseltresore nicht für andere Zwecke verwenden.

Jedes Angebot ruft seinen eigenen geheimen Schlüssel ab. Dieser Schlüssel wird jedes Mal verwendet, wenn ein Benutzer das Angebot anzeigt, aktualisiert oder die Versiegelung aufhebt.

Key Vault generiert den Schlüssel, der verwendet wird, um das Geheimnis abzurufen, wenn der Kreditor **Angebot** in der Kreditorzusammenarbeitsschnittstelle auswählt. Der Schlüssel verfällt dann nach einer festen Zeit, die der Beschaffungsmanager auf der Seite **Beschaffungsparameter** im Supply Chain Management festlegt. Nach Ablauf des Schlüssels kann niemand das Angebot anzeigen, bearbeiten oder seine Versiegelung aufheben. Daher ist es wichtig, den Ablauf des Schlüssels so zu konfigurieren, dass genügend Zeit bleibt, um den Angebotsprozess abzuschließen.

In den nächsten drei Schritten richten Sie die Verbindung zu Key Vault ein. Zuerst richten Sie einen Schlüsseltresor ein, der mit versiegelten Angeboten verwendet wird. Als Nächstes konfigurieren Sie Supply Chain Management für die Kommunikation mit dem Schlüsseltresor. Schließlich legen Sie die Ablaufzeit für den Schlüssel fest.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>Schritt 4: Einen Schlüsseltresor einrichten, der mit versiegelten Angeboten verwendet wird

Um Ihren Schlüsseltresor einzurichten, gehen Sie wie folgt vor. Die Reihenfolge der Schritte ist wichtig.

1. Wenn Sie noch kein Azure-Abonnement eingerichtet haben, das von dem Abonnement getrennt ist, in dem Sie Supply Chain Management ausführen, richten Sie es ein.
1. Richten Sie einen Schlüsseltresor in Ihrem separaten Azure-Speicher ein. Weitere Informationen finden Sie unter [Verwalten von Azure Key Vault-Speicher](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage).
1. Richten Sie Ihre Supply Chain Management-App als Client für Ihren Schlüsseltresor ein. Weitere Informationen finden Sie unter [Einen Azure Key Vault-Client einrichten](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>Schritt 5: Key Vault-Parametern im Supply Chain Management konfigurieren

Führen Sie die folgenden Schritte aus, um Supply Chain Management für die Kommunikation mit dem Schlüsseltresor während der versiegelten Angebotsabgabe zu konfigurieren.

1. Melden Sie sich bei Supply Chain Management an und gehen Sie zu **Systemadministration \> Setup \> Key Vault-Parameter**.
1. Wählen Sie **Neu**, um einen Datensatz zu erstellen, und legen Sie die folgenden Felder dafür fest:

    - **Name**: Geben Sie einen Namen ein.
    - **Beschreibung**: Geben Sie eine Beschreibung ein.
    - **Key Vault-URL**: Geben Sie die Standard-URL für Ihren Schlüsseltresor ein.
    - **Key Vault-Client**: Geben Sie die interaktive Client-ID der Active Directory-Anwendung ein, die einem Schlüsseltresor zur Authentifizierung zugeordnet ist.
    - **Key Vault geheimer Schlüssel**: Geben Sie die Geheimreferenz für das Zertifikat ein.
    - **Für versiegelte Angebote aktiviert**: Setzen Sie diese Option auf *Ja*.

![Seite „Key Vault-Parameter“](media/sealed-bidding-key-vault-param.png "Seite „Key Vault-Parameter“")

> [!NOTE]
> Sie können jeweils nur eine Schlüsseltresorkonfiguration für versiegelte Angebote aktivieren. Bevor Sie eine vorhandene Schlüsseltresorkonfiguration deaktivieren, müssen Sie sicherstellen, dass die Versiegelung für alle versiegelten Anebote, die sie verwenden, aufgehoben ist. Überprüfen Sie jede Angebotsaufforderung vom Typ *Versiegelt* und stellen Sie sicher, dass die Versiegelung für alle Antworten aufgehoben ist.

### <a name="step-6-set-the-key-expiration-time"></a>Schritt 6: Die Ablaufzeit des Schlüssels festlegen

Gehen Sie folgendermaßen vor, um die Ablaufzeit festzulegen, die auf den Schlüssel angewendet wird, der für jedes neue Angebot generiert wird.

1. Gehen Sie zu **Beschaffungsparameter \> Setup \> Beschaffungsparameter**.
1. Geben Sie auf der Registerkarte **Angebotsanforderung** im Feld **Verschiebung in Tagen** die Anzahl der Tage ein, die Angebotsanforderung dauern soll. Wenn eine Angebotsanforderung erstellt wird, wird die hier eingegebene Anzahl von Tagen zum Systemdatum addiert, um das Standardablaufdatum für die Angebotsanforderung zu definieren.
1. Im Feld **Verschiebung in Tagen Ablauf Verschlüsselungsschlüssel** geben Sie die Anzahl der Tage ein, die jeder Verschlüsselungsschlüssel nach seiner Ausgabe gültig sein soll. Nach Ablauf des Verschlüsselungsschlüssels kann niemand das Angebot anzeigen, bearbeiten oder die Versiegelung des dazugehörigen Angebots aufheben.

> [!TIP]
> Der Wert des Felds **Verschiebung in Tagen Ablauf Verschlüsselungsschlüssel** sollte nicht kleiner sein als der Wert des Feld **Verschiebung in Tagen**.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>Schritt 7: Standardangebotstyp festlegen

Jeder Angebotsanforderungsfall hat eine Angebotsart. Der Angebotstyp definiert, ob dieser Angebotsanforderungfall offene oder versiegelte Angebote bereitstellt.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>Angebotsanforderungsfälle ohne Anforderungstyp

Führen Sie die folgenden Schritte aus, um den Standardangebotstyp festzulegen, der neuen Angebotsanforderungen zugewiesen wird, denen beim Erstellen kein Anforderungstyp zugewiesen wird.

1. Gehen Sie zu **Beschaffungsparameter \> Setup \> Beschaffungsparameter**.
1. Legen Sie auf der Registerkarte **Angebotsanforderung** das Feld **Angebotstyp** auf *Versiegelt* fest.

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>Angebotsanforderungsfälle mit Anforderungstyp

Führen Sie die folgenden Schritte aus, um den Standardangebotstyp festzulegen, der neuen Angebotsanforderungen zugewiesen wird, denen beim Erstellen ein Anforderungstyp zugewiesen wird.

1. Gehen Sie zu **Beschaffung \> Setup \> Angebotsanforderung \> Anforderungstyp**.
1. Erstellen Sie einen neuen Anforderungstyp oder wählen Sie einen vorhandenen Anforderungstyp aus, für den Sie den Angebotstyp *Versiegelt* verwenden möchten.
1. Legen Sie das Feld **Angebotstyp** auf *Versiegelt* fest.
1. Wiederholen Sie diese Schritte für jeden weiteren Anforderungstyp, bei dem Sie versiegelte Angebote implementieren möchten.

> [!TIP]
> Beim Anlegen einer neuen Angebotsanforderung muss kein Anforderungstyp zugewiesen werden. Wenn eine Anforderungsart zugewiesen ist, kann der Standardangebotstyp einer Angebotsanforderung diese abrufen. Andernfalls kann der Standardanforderungstyp verwendet werden, der in den Beschaffungsparametern festgelegt ist.

## <a name="the-sealed-bidding-process"></a>Der Prozess für versiegelte Angebotsabgaben

Versiegelte Angebote folgen fast dem gleichen Prozess, der in [Übersicht über Angebotsanforderungen](request-quotations.md) beschrieben wird. Der Hauptunterschied besteht darin, dass die Angebotsdaten und ihre Anhänge verschlüsselt bleiben, bis die Versiegelung des Angebots aufgehoben wird.

> [!IMPORTANT]
> [Fragebögen](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) sind nicht verschlüsselt und sollten nicht zum Sammeln vertraulicher Informationen verwendet werden.

Hier ein Überblick über den Prozess:

1. Sie erstellen und senden eine Angebotsanforderung an einen oder mehrere Kreditoren.
1. Die Kreditoren antworten, indem sie ihr versiegeltes Angebot abgeben.
1. Sie heben die Versiegelung der Angebote nach der Ablaufzeit der Angebotseingabe auf.
1. Die Angebote werden sichtbar, Sie können sie bewerten und vergleichen.
1. Nachdem ein Angebot angenommen wurde, generieren Sie eine Bestellung, einen Kaufvertrag oder aktualisieren eine Bestellanforderung.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Einen Angebotsanforderungsfall erstellen, der versiegelte Angebote verwendet

Der Prozess zum Erstellen eines Angebotsanforderungfalls für versiegelte Angebote ist fast der gleiche wie der Prozess für nicht versiegelte Angebote. Informationen zum Erstellen beider Typen von Angebotsanforderungsfälle finden Sie unter [Eine Angebotsanforderung erstellen](tasks/create-request-quotation.md). In diesem Abschnitt werden einige wichtige Überlegungen erläutert, wenn Sie eine RFQ für versiegelte Angebote erstellen.

Angebotsanforderungsfälle für versiegelte Angebote müssen den **Angebotstyp** *Versiegelt* haben. Es gibt drei Möglichkeiten, diesen Wert einem Angebotsanforderungsfall zuzuweisen:

- Legen Sie den Wert direkt im Angebotsanforderungsfall fest, nachdem Sie ihn erstellt haben.
- Legen Sie versiegelte Angebote als Standardangebotstyp für alle Angebotsanforderungsfälle in Beschaffungsparametern fest. (Siehe Abschnitt [Standardangebotstyp festlegen](#set-default-bid-type) weiter oben in diesem Thema.)
- Wenn Sie einen neuen Angebotsanforderungsfall erstellen, wählen Sie einen Anforderungstyp aus, für den versiegelte Angebote eingerichtet sind. (Siehe Abschnitt [Standardangebotstyp festlegen](#set-default-bid-type).)

Für versiegelte Angebote legt der Wert **Ablaufdatum und -uhrzeit** des Angebotsanforderungsfalls fest, wann die Versiegelung der abgegebenen Angebote aufgehoben werden kann. Der Wert **Ablaufdatum und -uhrzeit** in jeder Position entspricht dem Wert in der Kopfzeile.

Sie können den Angebotstyp nicht mehr ändern, nachdem ein Angebotsanforderungsfall gesendet wurde.

### <a name="vendors-respond-to-an-rfq"></a>Kreditoren antworten auf eine Angebotsanforderung

Kreditoren, die auf ein versiegeltes Angebot antworten, verwenden das gleiche Verfahren, wie bei der Antwort auf offene Angebote, wie in [Arbeiten mit Angebotsanforderungen im Arbeitsbereich für Kreditorenangebotsabgabe](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace) beschrieben. Ausführliche Anweisungen zum Arbeiten mit offenen und versiegelten Angeboten finden Sie unter [Angebotsanforderungsangebote eingeben und vergleichen und Verträge vergeben](tasks/enter-compare-rfq-bids-award-contracts.md). Der einzige Unterschied zwischen der Verarbeitung für versiegelte Angebote und der Verarbeitung für offene Angebote besteht darin, dass Beschaffungsspezialisten das versiegelte Angebot eines Kreditors erst nach Ablauf der Angebotsfrist öffnen können. Nur eine Kontaktperson des Kreditors kann das versiegelte Angebot dieses Kreditors öffnen.

> [!IMPORTANT]
> Bei versiegelten Abgeboten können Kreditoren Anhänge nur im PDF-Format hochladen. Andere Formate werden nicht akzeptiert.

Nachdem ein registrierter Kreditorenbenutzer **Angebot** bei einer versiegelten Angebotsanforderung ausgewählt hat, können er seine Angebotsdaten eingeben, und diese Daten werden sicher aufbewahrt. Kreditoren können ihre Arbeit während der Angebotserstellung speichern, beliebig oft zurückkehren und sie dann abgeben, wenn sie fertig ist. Kreditoren können ihr Angebot auch nach der Abgabe einsehen. Wenn Kreditoren ihr Angebot nach der Abgabe ändern müssen, können sie es bis zum Ablauf der Angebotsfrist jederzeit zurückrufen, aktualisieren und erneut einreichen.

Bei versiegelten Angeboten gelten folgende Bedingungen:

- Während der Versiegelung erstellt das System eine *Angebotsanforderungs* erfassung.
- Wenn ein Kreditor ein Angebot abgibt, werden Angebotsanforderungserfassungen ohne Positionen mit einem versiegelten Preis erstellt.
- Nachdem die Versiegelung des Falls aufgehoben wurde, werden Angebotsanforderungserfassungen mit einem Preis und einem Betrag erstellt. Sie können auf diese Erfassung zugreifen, indem Sie **Angebotsanforderungerfassungen** auf der Seite **Alle Angebotsanforderungen** auswählen.
- Das System speichert ein Protokoll jeder Aktivität, die Benutzer bei einem versiegelten Angebot ausführen. Zu diesen Aktivitäten gehören das Anzeigen, Bearbeiten und Speichern des Angebots. Dieses Protokoll ist sowohl für den Kreditor als auch für Beschaffungsspezialisten sichtbar, die Zugriff auf das Angebot haben.
- Während das Angebot fortschreitet, können Beschaffungsspezialisten seinen Status einsehen. Der Status ist entweder *Kreditor aktualisiert* oder *Versendet durch Kreditor*.
- Der Status der Positionen in einem versiegelten Angebot bleibt *Gesendet* bis die Versiegelung aufgehoben wird.
- Wenn der Kreditor ein Angebot ablehnt, hat das Angebot unter **Antwortfortschritt** den Status *Von Kreditor abgelehnt*. Dieser Status ist für das Beschaffungspersonal sichtbar.
- Antworten in Fragebögen werden **nicht** verschlüsselt in der Datenbank gespeichert. Daher sind sie nicht versiegelt. Sie werden jedoch erst in der Angebotsanforderungs-Benutzeroberfläche angezeigt, wenn die Verschlüsselung des Falls aufgehoben wird.

### <a name="all-sealed-bid-activities-are-logged"></a>Alle versiegelten Angebotsaktivitäten werden protokolliert

Ein detailliertes Protokoll zeichnet alle Benutzeraktivitäten und -aktionen für ein Angebot auf. Mithilfe des Aktivitätsprotokolls können Organisationen feststellen, wer ein Angebot während seiner Lebensdauer aktualisiert hat und welche Aktualisierungen es waren. Es ermöglicht Organisationen auch zu bestätigen, dass nur autorisierte Personen auf ein versiegeltes Angebot zugegriffen haben. Das Aktivitätsprotokoll ist auf der Seite **Aktivität** jedes Angebots.

### <a name="review-rfq-activity"></a>Angebotsanforderungsaktivität überprüfen

Jede Interaktion mit dem Angebot wird protokolliert und kann auf der Seite **Aktivität** eingesehen werden. Die folgende Abbildung zeigt ein Beispiel.

![Beispiel für die Aktivitätsseite](media/sealed-bidding-rfq-activity.png "Beispiel für die Aktivitätsseite")

Anbieter können auf die Seite **Aktivität** durch Auswahl von **Aktivität** auf der Seite **Angebotsanforderung versiegeltes Angebot** zugreifen. Das Beschaffungspersonal kann darauf zugreifen, indem es **Aktivität** auf der Seite **Angebotsanforderung** auswählt. Das Aktivitätsprotokoll bietet vollständige Transparenz von Kreditoren und Beschaffungspersonal, die auf das Angebot zugegriffen haben. Daher kann es jeden unbefugten Zugriff aufdecken.

### <a name="unseal-sealed-bids"></a>Versiegelung versiegelter Angebote aufheben

Wenn der Wert **Ablaufdatum und -uhrzeit**, der für einen Angebotsanforderungsfall mit versiegeltem Angebot konfiguriert wurde, überschritten wurde, wird die Schaltfläche **Versiegelung aufheben** verfügbar. Wählen Sie **Versiegelung aufheben** aus, um die Versiegelung aller Angebote für den ausgewählten Angebotsanforderungsfall aufzuheben. Anschließend werden alle Angebotsdaten und -anhänge sichtbar, sodass Antworten auf den Fall verwaltet werden können. Zusätzlich werden Erfassungen erstellt, die die übermittelten Angebotsdaten enthalten.

Die Aufhebung der Versiegelung wird protokolliert und kann auf der Seite **Aktivität** eingesehen werden.

### <a name="process-accepted-bids"></a>Akzeptierte Angebote verarbeiten

Der Prozess des Vergleichens und der Genehmigung zuvor versiegelter Angebote ist der gleiche wie der Prozess für offene Angebote. Informationen zum Bewerten, Vergleichen, Ablehnen und Akzeptieren nicht versiegelter Gebote finden Sie unter [Angebotsanforderungsangebote eingeben und vergleichen und Verträge vergeben](tasks/enter-compare-rfq-bids-award-contracts.md).

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>Das Aktivitätsprotokoll der Angebotsanforderung kann niemals gelöscht werden

Niemand, nicht einmal Administratoren und der Microsoft-Support, können das Aktivitätsprotokoll von Angebotsanforderungen bearbeiten oder löschen. Diese Einschränkung trägt dazu bei, die Fairness des geschlossenen Bieterverfahrens zu gewährleisten. Es trägt auch dazu bei, sicherzustellen, dass ein genauer Audit-Trail gepflegt wird.
