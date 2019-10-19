---
title: Erweitern von Talent mit PowerApps und Microsoft Flow – Beispielfälle
description: In diesem Thema werden einige Beispiele von Erweiterbarkeitsszenarien für Microsoft Dynamics 365 Talent beschrieben, die Microsoft PowerApps und Microsoft Flow verwenden.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 7bc3a18327f2d32770176eddcb7200681f0fb0da
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008058"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>Erweitern von Talent mit PowerApps und Microsoft Flow – Beispielfälle

In diesem Thema werden einige Beispiele von Erweiterbarkeitsszenarien für Microsoft Dynamics 365 Talent beschrieben, die Microsoft PowerApps und Microsoft Flow verwenden. Sie können das Lösungspaket importieren, das jedem Beispiel in der PowerApps-Umgebung zugeordnet ist. Sie können entweder die Pakete als Anleitung oder als Startpunkte zu den Werkzeugszenarien verwenden, die der Organisation zugeordnet sind.

> [!IMPORTANT]
> Wenn Sie die Vorlagen und Apps verwenden möchten, die in diesem Thema als "wie vorliegend" beschrieben sind, müssen Sie diese unbedingt testen, um sicherzustellen, dass sie alle Szenarien beinhalten, die für Ihre Implementierung bestimmt sind.


## <a name="prerequisites"></a>Voraussetzungen

- Um Pakete zu importieren, müssen Benutzer die Berechtigung **Umgebungs-Hersteller** haben.
- Um Apps zu exportierenden oder zu importieren, müssen Benutzer eine Lizenz für PowerApps Plan 2 oder eine Testlizenz für PowerApps-Plan 2 haben.

## <a name="flow--form-connect"></a>Ablauf - Formular schließen

Die Vorlage **Ablauf - Formular verbinden** kann verwendet werden, wenn Daten aus Microsoft Formularen gelesen und in einer Common Data Service Entität gespeichert werden.

Diese Vorlage kann auch erweitert werden, sodass sie für andere Szenarien verwendet werden kann. Nachfolgend finden Sie einige Beispiele:

- Kandidatenbewertungen aufzeichnen.
- Zeichnen Sie Ergebnisse aus Kursfragebögen auf.
- Kompilieren Sie eine Bibliothek von Gesprächsfragen für die Personalverwaltungs (HR)-Administratoren.
- Zeichnen Sie die Bewertung des Kandidaten aus dem Gesprächsprozess auf

In Microsoft Dynamics 365:  Attract Formulare können in Kandidatenprofilen angezeigt werden und der Kandidat kann die Details ausfüllen. Formulare können als Aktivitäten auch in einer Stellenvorlage eingebettet werden.

Wenn ein Kandidat ein Formular sendet, zeichnet Microsoft Flow die Formularübermittlung auf, liest die Daten und speichert sie in der Common Data Service Entität.

Um die Vorlage **Ablauf - Formular verbinden** und die benutzerdefinierte Entitäts-Struktur herunterzuladen, gehen Sie zu [Ablauf - Formular verbinden](https://go.microsoft.com/fwlink/?linkid=2081988) im Microsoft Download Center.

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>Parameter, die an Powerapps übergeben werden, auslösen und extrahieren

Die Vorlage **An PowerApps übergebene Parameter einleiten und extrahieren** kann als Ausgangspunkt für alle PowerApps-Szenarien verwendet werden, die für Attract spezfisch sind. Dies umfasst alle Standardparameter, die von Attract weitergegeben werden, wie beispielsweise **Stellenbewerbung**, **Kandidaten-ID** und **JobID**.

Diese Vorlage kann verwendet werden, um einen Kandidatenbewertungsbogen abzurufen, damit ein zukünftiger Vorgesetzter die Bewertung sehen kann, die ein Kandidat ausfüllte.

Apps, die mithilfe von PowerApps erstellt wurden, können in die Stellenvorlage in Attract eingebettet werden.

Wenn Sie die Vorlage **Parameter, die die Powerapps durchlaufen einleiten und extrahieren** und die benutzerdefinierte Entitätsstruktur herunterladen, gehen Sie im Microsoft Download Center auf [Parameter,di die Powerapps durchlaufen einleiten und extrahieren](https://go.microsoft.com/fwlink/?linkid=2081991).

## <a name="integration-with-office-365"></a>Integration mit Office 365

Die **Integration mit Office 365** App kann verwendet werden, um Teaminformationen für angemeldete Benutzer von Microsoft Office 365 zu extrahieren. Sie verweist Arbeitskräfte in Talent dahingehend, Ausstempeldetails und Ausnahmeaufzeichnungen zu extrahieren. Ein- und Ausstempelndetails werden in den benutzerdefinierten Common Data Service Entitäten gespeichert. Die Voraussetzung ist, dass diese Details von einem System von einem Fremdanbietern über die Integration ausgefüllt werden.

Diese App kann auch erweitert werden, sodass sie für andere Szenarien verwendet werden kann. Sie kann zum Beispiel dazu verwendet werden, Teamferieninformationen, Kalenderereignisse und weitere Team spezifische Ereignisse anzuzeigen.

Wenn Sie die App**Integration mit Office 365** und die benutzerdefinierte Entitäts-Struktur herunterladen, gehen Sie zu [Integration mit Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) im Microsoft Download Center.

## <a name="flow--email-notification"></a>Fluss – E-Mail-Benachrichtigung

Die Vorlage **Fluss - E-Mail-Benachrichtigung** kann für E-Mail-Benachrichtigungsszenarien verwendet werden. Sie kann verwendet werden, um Benachrichtigungs-E-Mails zu den Kandidaten zu starten, die das Einstellungsteam während jeder Phase des Rekrutierungsprozesses abgelehnt hat.

Diese Vorlage kann erweitert werden, um Änderungen an der Kandidatenphase während des Rekrutierungsprozesses nachzuverfolgen und, Benachrichtigungen an das Einstellungsteam und die Kandidaten zu senden.

Im Allgemeinen gilt für Entitäten, die in Common Data Service gespeichert werden, dass Fluss eingerichtet werden kann, um Benachrichtigungen für Ereignisse zu versenden, die in Core HR Attract oder Onboard auftreten.

Um die Vorlage **Flussf - E-Mail-Benachrichtigung** herunterzuladen gehen Sie zu [Fluss - E-Mail-Benachrichtigung](https://go.microsoft.com/fwlink/?linkid=2082103) im Microsoft Download Center.

## <a name="flow--sql-connect-and-execute"></a>Fluss - SQL Connect und ausführen

Die Vorlage **Fluss - SQL Connect und ausführen** verbindet mit  Microsoft SQL Server und aktiviert die SQL Abfrage, die dann ausgeführt wird.

Obwohl diese Vorlage dazu entwickelt wurde, SQL-Tabellen zu lesen und zu aktualisieren, kann sie auch erweitert werden, sodass sie für andere Szenarien verwendet werden kann. Sie kann beispielsweise dazu verwendet werden, um eine Stagingtabelle in Common Data Service mit Datensätzen vom SQL Server zu füllen und um die Stagingtabelle regelmäßig zu synchronisieren, indem ein inkrementeller Push von SQL Server verwendet wird.

Um die Vorlage **Ablauf - SQL verbinden und ausführen** herunterzuladen, gehen Sie zu [Ablauf - Formular verbinden](https://go.microsoft.com/fwlink/?linkid=2081789) im Microsoft Download Center.

## <a name="flow--sharepoint-integration"></a>Fluss SharePoint-Integration

Die Vorlage **Fluss – SharePoint Integration** kann verwendet werden, um Daten aus einer Microsoft SharePoint  Liste zu lesen, die Liste mit Feldwerten für jede beliebige Common Data Service Entität zu vergleichen und die Ergebnisse des Vergleichs als Benachrichtigungs-E-Mail zu versenden. 

Eine Organisation hat möglicherweise eine Reihe von Fähigkeiten, die sie dringend benötigt. Diese Qualifikationen können in SharePoint als Liste SharePoint gespeichert werden. Wenn sich ein Kandidat für eine Stelle bewirbt, die Qualifikationen verlangt, die aufgelistet sind und wenn es eine erhebliche Übereinstimmung zwischen den Fähigkeiten des Kandidaten und den Qualifikationen gibt, die in SharePoint gespeichert sind, wird eine  Benachrichtigungs-E-Mail übermittelt. Auf diese Weise werden Positionen, die dringend erforderlich sind, schneller gefüllt, da die Benachrichtigungen den Personalbeschaffern hilft, Kandidaten aus der gesamten Organisation zu finden.

Diese Vorlage kann auch erweitert werden, sodass sie für ein beliebiges Szenario verwendet werden kann, das die SharePoint Integration betrifft.

Um die Vorlage **Fluss – SharePoint Integration**herunterzuladen, gehen Sie zu [Fluss SharePoint Integration ](https://go.microsoft.com/fwlink/?linkid=2082109) im Microsoft Download Center.

## <a name="referral-app"></a>Bezugs-App
Sie können die Empfehlungs-App verwenden, um Kandidaten einer freigegebene Talentschmiede hinzuzufügen. Der Empfehler kann **Vorname**, **Lastname**, **E-Mail** und **Linkedln-URL** eingeben, wenn er den Kandidaten übermittelt. Die Kandidatenquellenmetadaten werden dann mit den Informationen des Empfehlers ausgefüllt.

Sie können dieser App im Mitarbeiter-Self-Service (ESS) für das Übermitteln von Empfehlungen eingeben, oder Sie können sie als Verknüpfung im Unternehmensportal und als eigenständige App ausführen.

Um die **Empfehlungs-App** herunterzuladen, gehen Sie zur [Dynamics 365 Talent Erweiterbarkeitslösung: Empfehlungs-App](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) im  Microsoft Download Center. Sie können diese App importieren und anpassen, um weitere Funktionen hinzuzufügen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Das Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Migrieren der App zwischen Mandanten und Umgebung](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
