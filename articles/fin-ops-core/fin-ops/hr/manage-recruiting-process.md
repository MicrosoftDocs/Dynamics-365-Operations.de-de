---
title: Personalbeschaffungsprozesse verwalten
description: Dieses Thema beschreibt ein Konzept, mit dem Personalvermittler die Schritte in einem Personalbeschaffungsprozess verfolgen können.
author: twheeloc
ms.date: 01/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb7cc1db906ba0cd07caaa1d82a12182f78b19ba
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735373"
---
# <a name="manage-recruiting-processes"></a>Personalbeschaffungsprozesse verwalten

> [!IMPORTANT]
> Die Personalbeschaffungsfunktionen in diesem Thema werden als Personalbeschaffungsprojekte bezeichnet und konzentrieren sich auf Bewerber, Bewerbungen und Personalbeschaffungsprojekte. 


In diesem Artikel wird ein Konzept beschrieben, das Personalbeschaffungssachbearbeiter verwenden können, um die Schritte in einem Personalbeschaffungsprozess nachzuverfolgen. Dazu gehören Bemühungen, offene Positionen zu annoncieren und Bewerber anzuwerben, die Informationen zu Bewerber und Bewerbung nachzuverfolgen, Gespräche mit Bewerbern zu führen und einen oder mehrere Kandidaten auszuwählen, um offene Positionen in Ihrer Organisation zu besetzen.

## <a name="overview"></a>Überblick

Personalbeschaffungsprojekte können helfen, die Schritte zu organisieren, die Sie abschließen, wenn Sie offene Positionen in einer juristischen Person besetzen. Ein Bewerber ist eine Person, die für eine Anstellung auf Ihr Unternehmen gilt. Eine Bewerbung ist der Seite auf die Teilnahme eines Bewerbers gebunden werden, der in einem Unternehmen verwendet werden und ist mit einem Personalbeschaffungsprojekt, Zinsen in einer bestimmten Anzahl auszudrücken. Einzelner Bewerber können mehrere Bewerbungen in derselben juristischen Person oder für mehrere Unternehmen in der Organisation.

## <a name="recruitment-projects"></a>Personalbeschaffungsprojekte

Personalbeschaffungsprojekte können Werbeoffiziere zur Nachverfolgung für den Fortschritt für das Ausfüllen einer oder mehreren offenen Stellen. Das Personalbeschaffungsprojekt identifiziert die Abteilung und die Stelle, für welches oder mehr Positionen geprüft wird geöffnet. Personalbeschaffungsprojekte verfolgen auch die folgenden Informationen für offene Positionen nach:

- Die spezifische Anzahl offener Positionen
- Der einstellende Manager und ein alternativer Ansprechpartner für die Position
- Das Datum, an dem die Anforderung genehmigt wurde
- Die Bewerbungsfrist
- Das voraussichtliche Startdatum

Das Personalbeschaffungsprojekt enthält den Wert **Stellenanzeige**, der auf der Seite **Employee Self-Service** verwendet wird, um die offene Stelle zu annoncieren. Die offenen Stellen können Mitarbeitern nur angezeigt werden, wenn das Personalbeschaffungsprojekt einen Wert **Stellenanzeige** hat, das Feld **Employee Self-Service** auf **Ja** festgelegt ist, das Feld **Bewerbungsfrist** ein zukünftiges Datum festgelegt wurde und das Personalbeschaffungsprojekt den **Projektstatus** den Wert **Gestartet** hat. In der folgenden Tabelle werden die möglichen Personalbeschaffungsprojektstatus und deren Beschreibung aufgelistet.

| Status    | Zeigt an:                                                                         |
|-----------|-----------------------------------------------------------------------------------------|
| Geplant | Rekrutierungsaufwände wurden vorbereitet. Die Personalbeschaffung für dieses Projekt ist noch nicht gestartet worden. |
| Gestartet   | Bewerbungen werden nun für die offenen Stellen in diesem Projekt angenommen.                   |
| Abgeschlossen  | Alle offenen Stellen für dieses Projekt sind besetzt worden.                                         |
| Abgebrochen  | Die Personalbeschaffung für dieses Projekt ist storniert worden.                                          |

Personalbeschaffungsmitarbeiter können sowohl die **Medien** erfassen, die verwendet werden, um die offenen Stellen durch externe Outlet-Geschäfte zu annoncieren, als auch **Entwicklungen** in Bezug auf das Projekt oder die Bewerbungen nachverfolgen.

## <a name="applicants"></a>Bewerber

Ein Bewerber ist eine Person, die für eine Anstellung auf Ihr Unternehmen gilt. Bewerber werden in allen juristischen Personen in Ihrer Organisation freigegeben. Daher haben Sie einen großen Pool an Talenten, in dem Sie suchen können. Sie können die Kompetenzen, Referenzen, Arbeitsplatzhilfsmittel-Anforderungen sowie die persönlichen Daten für Bewerber verwalten. Wenn Sie einen Bewerberdatensatz erstellen, wird ein Personendatensatz für diesen Bewerber im globalen Adressbuch erstellt. Sie können die Seite **Bewerber** verwenden, um die folgenden Informationen für das globale Adressbuch für Personen zu aktualisieren, die Bewerber sind:

- Adressdaten
- Kontaktinformationen
- Identifizierungsdaten
- Namensdetails
- Persönliche Informationen

## <a name="applications"></a>Anträge

Verwenden Sie zum Erfassen von Informationen zu eingegangenen Bewerbungen die Seite **Bewerbung**. Die Anwendung kommuniziert der Seite auf die Teilnahme des Bewerbers in ein Stellenangebot in der Organisation. Wenn Sie eine Bewerbung erstellen, muss der Bewerber als Bewerber oder für Personen im System vorhanden sein.

Die Mitarbeiterbewerbungen, die von Bewerbern über das Web gesendet werden, sind entweder angeforderte Bewerbungen, die als Antwort auf eine Stellenanzeige gesendet werden, oder nicht angeforderte Bewerbungen. Angeforderte Bewerbungen werden automatisch dem Personalbeschaffungsprojekt zugeordnet, für das die Stellenanzeige erstellt wurde. Nicht angeforderte Bewerbungen werden dem Personalbeschaffungsprojekt zugeordnet, das im Bereich **Personalbeschaffung** der Seite **Personalverwaltungsparameter** angegeben ist.

### <a name="application-status"></a>Bewerbungsstatus

Der Bewerbungsstatus gibt an, in welcher Phase des Personalbeschaffungsprozesses sich die Bewerbung befindet. In der folgenden Tabelle werden die möglichen Bewerbungsstatus und deren Beschreibung aufgelistet.

| Status    | Zeigt an:                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Empfangen  | Die Bewerbung wurde empfangen.                                                             |
| Bestätigt | An den Bewerber kann eine Benachrichtigung gesendet werden, um den Bewerbungseingang zu bestätigen.            |
| Gespräch | Eine Einladung zum Bewerbungsgespräch kann an den Bewerber gesendet werden.                                     |
| Ablehnung | An den Bewerber kann ein Ablehnungsschreiben gesendet werden.                                          |
| Abgebrochen  | An den Bewerber kann eine Widerrufsbestätigung gesendet werden. Dieser Status wird manuell zugewiesen. |
| Eingestellt  | An den Bewerber kann ein Stellenangebot gesendet werden.                                         |

### <a name="correspondence-actions"></a>Korrespondenzaktivitäten

Die Korrespondenzaktivität einer Bewerbung bestimmt das Dokument oder die E-Mail-Vorlage, die Sie verwenden, um mit dem Bewerber zu kommunizieren, der die Bewerbung eingereicht hat. Durch Zuordnung von **Bewerbungslesezeichen** zu Korrespondenzaktivitäten können Sie Werte aus den Seiten **Anwendungen**, **Bewerber**, **Gespräch** und **Personalbeschaffungsprojekt** in Ihrer Kommunikation mit Bewerbern verwenden. Durch die Erstellung von **Bewerbungs-E-Mail-Vorlagen** für die Korrespondenzaktivitäten können Sie schnell E-Mails an Bewerber senden, deren Bewerbung eine bestimmte Kombination aus einem Status und einer Korrespondenzaktivität aufweisen. Beispielsweise können Sie allen Bewerbungen mit dem **Status**-Wert **Erhalten** und dem **Korrespondenzaktivität**-Wert **Empfangen** eine Bestätigungs-E-Mail senden. Nachdem Sie die E-Mail gesendet haben, haben Sie die Möglichkeit, den Status der Bewerbungen automatisch zu aktualisieren.

## <a name="application-routing"></a>Weiterleitung von Bewerbungen

Wenn eine Bewerbung von mehreren Arbeitskräften geprüft werden muss, können Sie die Seite **Weiterleitung von Bewerbungen** verwenden, um eine Umlaufliste zur Verwaltung des Vorgangs zu erstellen.

## <a name="interviews"></a>Gespräche

**Bewerbergespräche** können geplant werden **Bewerbungen** Seite. Verwenden Sie die **Besprechungsinformationen übermitteln** Schaltfläche, um eine Kalenderdatei mit den Gesprächszeitplaninformationen dem Bewerber und zur Befragungsperson zu senden.

## <a name="skill-mapping"></a>Qualifikationszuordnung

**Qualifikationszuordnung** und **Qualifikationszuordnungsprofile** können verwendet werden, um Kandidaten zu identifizieren, die für eine offene Stelle möglicherweise gut geeignet sind.

## <a name="hiring-applicants"></a>Einstellen von Bewerbern

Verwenden Sie die Seite **Bewerbungen**, um einen Bewerber einzustellen. Wird ein Bewerber eingestellt, erhält der Bewerbungsdatensatz den Status **Eingestellt**, und der Personendatensatz des globalen Adressbuchs des Bewerbers wird dem neuen Arbeitskraftdatensatz zugeordnet. Die Änderungen an den Informationen des globalen Adressbuchs für den neuen Arbeitskraftdatensatz werden auch im Bewerberdatensatz angezeigt. Dies kann dazu beitragen, die Dateneingaben zu reduzieren, sollte sich die neue Arbeitskraft um eine andere Stelle innerhalb des Unternehmens bewerben. Um eine vorhandene Arbeitskraft in eine neue Position einstellen, klicken Sie auf **Änderungsposition** in **Bewerbungsstatus** ablegen unten um den Übergangsprozess zu initiieren.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
