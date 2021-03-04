---
title: Elektronische Berichterstellung (ER) – Erweiterte Formatsuche
description: In diesem Thema wird beschrieben, wie eine ER-Formatreferenz in der ER-Formatsuche eingerichtet werden kann, wenn das erforderliche Format im globalen Repository gespeichert ist.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7c6cb99a6c5cc6fb92ce52041296af2d0c6722e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679485"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Benutzern ermöglichen, eine ER-Formatreferenz einzurichten, die ein Format aus dem globalen Repository abfragt

[!include [banner](../includes/banner.md)]

Sie können das [Elektronische Berichterstattung](general-electronic-reporting.md) (ER)-Framework zum Konfigurieren von [Formaten](general-electronic-reporting.md#FormatComponentOutbound) für ausgehende Dokumente gemäß den rechtlichen Anforderungen für verschiedene Länder/Regionen verwenden. Sie können das ER-Framework auch zum Konfigurieren von [Formaten](general-electronic-reporting.md#FormatComponentInbound) für die Analyse eingehender Dokumente verwenden und die Informationen aus diesen Dokumenten nutzen, um Anwendungsdaten anzuhängen oder zu aktualisieren. Jedes dieser Formate kann in Ihrer Dynamics 365 Finance-Instanz für die Bearbeitung eingehender oder ausgehender Geschäftsdokumente im Rahmen eines bestimmten Geschäftsprozesses verwendet werden.

In der Regel müssen Sie angeben, welches ER-Format in einem bestimmten Geschäftsprozess verwendet werden muss. Wählen Sie dazu ein einzelnes ER-Format in einem Suchfeld aus, das als Teil von Geschäftsprozess-spezifischen Parametern konfiguriert ist. Diese Suchfelder werden normalerweise mithilfe der entsprechenden API des ER-Frameworks implementiert. Weitere Informationen finden Sie unter [ER-Framework-API – Code zum Anzeigen einer Formatzuordnungssuche](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Beispiel: Wenn Sie [Außenhandelsparameter](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters) konfigurieren, müssen Sie die Verweise auf einzelne Formate einrichten, die zum Generieren der Intrastat-Meldung und des Intrastat-Meldungskontrollberichts verwendet werden. Die folgenden Screenshots zeigen, wie das Suchfeld für die ER-Formate auf der Seite **Außenhandelsparameter** aussieht.

Wenn die aktuelle Finance-Instanz keine auf den Intrastat-Geschäftsprozess bezogenen EB-Formate enthält, ist dieses Suchfeld leer.

[![Außenhandelsparameter-Seite](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Wenn die aktuelle Finance-Instanz auf den Intrastat-Geschäftsprozess bezogenen ER-Formate enthält, bietet das Suchfeld die ER-Formate an.

[![Außenhandelsparameter-Seite](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Diese Suche bietet nur die ER-Formate an, die bereits in die aktuelle Finance-Instanz importiert wurden. Zum [Importieren](./tasks/er-import-configuration-lifecycle-services.md) von ER-Lösungen in die aktuelle Finance-Instanz benötigen Sie Berechtigungen, um die entsprechende Funktion des ER-Frameworks auszuführen, die den [Lebenszyklus](general-electronic-reporting-manage-configuration-lifecycle.md) von ER-Lösungen unterstützt, die ER-Formate enthalten.

Ab Finance-Version 10.0.9 (Release April 2020) wurde die Benutzeroberfläche der Suche im ER-Format, die mithilfe der ER-Framework-API implementiert wird, erweitert. Sie können weiterhin die vorhandenen ER-Formate auswählen, die auf dem Inforegister für **Formatkonfiguration auswählen** vorhanden sind. Darüber hinaus bietet die erweiterte Suche die neue Option, das globale Repository (GR) nach bestimmten EB-Formaten zu durchsuchen. Alle ER-Formate des GR werden auf dem Inforegister für **Aus globalem Repository importieren** angeboten.

[![Außenhandelsparameter-Seite](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Ähnlich wie das Inforegister für **Formatkonfiguration auswählen** zeigt das Inforegister für **Aus globalem Repository importieren** nur die ER-Formate an, die für den Geschäftsprozess gelten, für den in diesem Suchfeld ein ER-Format ausgewählt wurde. In diesem Beispiel die Generierung der Intrastat-Meldung. Das ER-Format gilt für das Unternehmen, bei dem der Benutzer derzeit angemeldet ist, abhängig vom Kontext des Unternehmenslandes.

Wenn Sie ein ER-Format auf dem Inforegister für **Aus globalem Repository importieren** auswählen, wird die ausgewählte ER-Format-[Konfiguration](general-electronic-reporting.md#Configuration) aus dem GR in die aktuelle Finance-Instanz importiert.

[![Außenhandelsparameter-Seite](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Wenn der Import erfolgreich abgeschlossen wurde, wird der Verweis auf das importierte ER-Format in diesem Suchfeld gespeichert. Beim erstmaligen Zugriff auf das GR müssen Sie dem angegebenen Link folgen, um sich für den [Regulatory Configuration Service](https://aka.ms/rcs) (RCS) anzumelden, mit dem der Zugriff auf den GR-Speicher verwaltet wird.

[![Außenhandelsparameter-Seite](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Standardmäßig zeigt das Inforegister für **Aus globalem Repository importieren** die Liste der ER-Formate aus dem temporären Speicher an, die basierend auf dem GR-Inhalt zur Leistungsverbesserung automatisch erstellt wird. Dies passiert, wenn das Inforegister für **Aus globalem Repository importieren** zum ersten Mal geöffnet wird, was einige Sekunden dauern kann.

Wenn Sie das erforderliche ER-Format auf dem Inforegister **Aus globalem Repository importieren** nicht sehen, aber sicher sind, dass es im GR gespeichert ist, wählen Sie die Option **Synchronisieren** aus. Durch diese Option wird der temporäre Speicher mit dem aktuellen Inhalt des GR synchronisiert.

## <a name="feature-activation"></a>Funktionsaktivierung

Die Verfügbarkeit dieser Funktionalität wird von der Funktion für die **Erweiterte Suche nach ER-Formatkonfigurationen mit Abfrage des globalen Respository** in der **Funktionsverwaltung** gesteuert. Diese Funktion ist standardmäßig aktiviert.

[![Funktionsverwaltung-Seite](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Sicherheitsaspekte

Das Recht **Verwalten von Konfigurations-Repositorys** (**ERMaintainSolutionRepositories**) steuert den Zugriff auf den GR für einen Benutzer, der die ER-Formatsuche mit aktiviertem Inforegister für **Aus globalem Repository importieren** öffnet. Um Benutzern den Zugriff auf den GR-Inhalt über die ER-Formatsuche zu ermöglichen, müssen Sie die Sicherheitseinstellungen ändern, indem Sie Benutzern das Recht **ERMaintainSolutionRepositories** gewähren, entweder direkt oder unter Verwendung bereits zugewiesener Rollen und Aufgaben.

Der folgende Screenshot zeigt, wie dieses Recht Benutzern gewährt werden kann, die der **Buchhalter**-Rolle zugewiesen sind. Diese Rolle ermöglicht es Benutzern, Außenhandelsparameter zu konfigurieren und Verweise auf die EB-Formate in den Feldern **Dateiformatzuordnung** und **Berichtformatzuordnung** auf der Seite **Außenhandelsparameter** einzurichten.

[![Sicherheitskonfiguration-Seite](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Einschränkungen

Der Zugriff auf den GR in der ER-Formatsuche wird derzeit nur für die Auswahl von ER-Formaten unterstützt, die zum Generieren ausgehender Dokumente verwendet werden.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Warum kann ich über die ER-Formatsuche nicht auf das globale Repository zugreifen?

Wenn Sie die Funktion für **Erweiterte Suche nach ER-Formatkonfigurationen mit Abfrage des globalen Respository** auf der Seite **Funktionsverwaltung** aktiviert haben, Benutzer die ER-Formate auf dem Inforegister für **Aus globalem Repository importieren** aber nicht sehen und die Option **Synchronisieren** zwar sichtbar, aber deaktiviert ist, stellen Sie sicher, dass das Recht **Verwalten von Konfigurations-Repositorys** (**ERMaintainSolutionRepositories**) dem Benutzer gewährt wurde. Wenden Sie sich an Ihren Systemadministrator, um dieses Recht zu erhalten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung (ER)](general-electronic-reporting.md)
- [ER-Framework-API](er-apis-app73.md)
- [Den Lebenszyklus der Konfiguration der elektronischen Berichterstellung verwalten](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]