---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571164"
---
# AzureRM. Insights-modul
## Problembeskrivning
I det här avsnittet visas hjälp avsnitt för dina Azure Insights-cmdletar.

## AzureRM. Insights-cmdletar
### [Add-AzureRmAutoscaleSetting](Add-AzureRmAutoscaleSetting.md)
Skapar en autoskalningsinställning.

### [Add-AzureRmLogAlertRule](Add-AzureRmLogAlertRule.md)
Lägger till eller ersätter en regel för loggnings aviseringar.

### [Add-AzureRmLogProfile](Add-AzureRmLogProfile.md)
Skapar en ny aktivitets logg profil. Denna profil används till att antingen arkivera aktivitets loggen på ett Azure Storage-konto eller strömma den till en Azure Event Hub i samma prenumeration. 

- **Lagrings konto** – det finns inget standard lagrings konto (Premium Storage-konto stöds inte). Det kan antingen vara av typen ARM eller klassiskt. Om den är inloggad på ett lagrings konto debiteras kostnaden för att lagra aktivitets loggen med normal standard lagrings taxa. Det kan bara finnas en enda logg profil per prenumeration som bara är ett lagrings konto per prenumeration som kan användas för att exportera aktivitets loggen. 

- **Händelsehubben-det** kan bara finnas en enda logg profil per prenumeration som bara en händelse gren per prenumeration kan användas för att exportera aktivitets loggen. Om aktivitets loggen strömmas till en händelsehubben tillämpas standard Event Hub-priser. 

I aktivitets loggen kan händelser gälla en region eller kan vara "globalt". Global innebär detta att dessa händelser är region agnostics och att de är oberoende av regionen, i de flesta händelser hamnar i den kategorin. Om aktivitets loggnings profilen är inställd från portalen lägger den implicit till "global" tillsammans med alla andra regioner som är markerade i användar gränssnittet. När du använder en cmdlet måste platsen som "global" anges explicit från valfri annan region. 

**Obs!** **om du inte anger "globalt" i platserna kommer det att leda till att huvud aktivitets loggen inte exporteras.** 

### [Add-AzureRmMetricAlertRule](Add-AzureRmMetricAlertRule.md)
Lägger till eller uppdaterar en Metric-baserad notifieringsregel.

### [Add-AzureRmWebtestAlertRule](Add-AzureRmWebtestAlertRule.md)
Lägger till eller uppdaterar en aviserings regel för en webtest.

### [Disable-AzureRmActivityLogAlert](Disable-AzureRmActivityLogAlert.md)
Inaktiverar en aktivitets loggs varning och anger dess taggar.

### [Enable-AzureRmActivityLogAlert](Enable-AzureRmActivityLogAlert.md)
Aktiverar en aktivitets logg varning och anger dess taggar.

### [Get-AzureRmActionGroup](Get-AzureRmActionGroup.md)
Hämtar åtgärds grupper.

### [Get-AzureRmActivityLogAlert](Get-AzureRmActivityLogAlert.md)
Hämtar en eller flera aktivitets logg varningar.

### [Get-AzureRmAlertHistory](Get-AzureRmAlertHistory.md)
Hämtar historiken över aviseringar.

### [Get-AzureRmAlertRule](Get-AzureRmAlertRule.md)
Hämtar notifieringsregler.

### [Get-AzureRmAutoscaleHistory](Get-AzureRmAutoscaleHistory.md)
Hämtar den automatiska skalnings historiken.

### [Get-AzureRmAutoscaleSetting](Get-AzureRmAutoscaleSetting.md)
Hämtar inställningar för Autoskala.

### [Get-AzureRmDiagnosticSetting](Get-AzureRmDiagnosticSetting.md)
Hämtar de protokollförda kategorierna och tids kornig het.

### [Get-AzureRmLog](Get-AzureRmLog.md)
Hämtar en logg över händelser.

### [Get-AzureRmLogProfile](Get-AzureRmLogProfile.md)
Hämtar en logg profil.

### [Get-AzureRmMetric](Get-AzureRmMetric.md)
Hämtar metriska värden för en resurs.

### [Get-AzureRmMetricDefinition](Get-AzureRmMetricDefinition.md)
Hämtar mått definitioner.

### [Get-AzureRmUsage](Get-AzureRmUsage.md)
Hämtar användnings måtten för en resurs.

### [New-AzureRmActionGroup](New-AzureRmActionGroup.md)
Skapar ett ActionGroup-referens objekt i minnet.

### [New-AzureRmActionGroupReceiver](New-AzureRmActionGroupReceiver.md)
Skapar en ny mottagare av åtgärds gruppen.

### [New-AzureRmActivityLogAlertCondition](New-AzureRmActivityLogAlertCondition.md)
Skapar ett nytt aviserings villkor för aktivitets loggen i minnet.

### [New-AzureRmAlertRuleEmail](New-AzureRmAlertRuleEmail.md)
Skapar en e-poståtgärd för en notifieringsregel.

### [New-AzureRmAlertRuleWebhook](New-AzureRmAlertRuleWebhook.md)
Skapar en aviserings regel med webhook.

### [New-AzureRmAutoscaleNotification](New-AzureRmAutoscaleNotification.md)
Skapar ett e-postmeddelande med Autoskala.

### [New-AzureRmAutoscaleProfile](New-AzureRmAutoscaleProfile.md)
Skapar en Autoskala-profil.

### [New-AzureRmAutoscaleRule](New-AzureRmAutoscaleRule.md)
Skapar en Autoskala-regel.

### [New-AzureRmAutoscaleWebhook](New-AzureRmAutoscaleWebhook.md)
Skapar en Autoskala-webhook.

### [Remove-AzureRmActionGroup](Remove-AzureRmActionGroup.md)
Tar bort en åtgärds grupp.

### [Remove-AzureRmActivityLogAlert](Remove-AzureRmActivityLogAlert.md)
Tar bort en aktivitets loggs avisering.

### [Remove-AzureRmAlertRule](Remove-AzureRmAlertRule.md)
Tar bort en varnings regel.

### [Remove-AzureRmAutoscaleSetting](Remove-AzureRmAutoscaleSetting.md)
Tar bort en autoskalningsinställning.

### [Remove-AzureRmLogProfile](Remove-AzureRmLogProfile.md)
Tar bort en logg profil.

### [Set-AzureRmActionGroup](Set-AzureRmActionGroup.md)
Skapar en ny eller uppdaterar en befintlig åtgärds grupp.

### [Set-AzureRmActivityLogAlert](Set-AzureRmActivityLogAlert.md)
Skapar en ny eller anger en befintlig aktivitets loggs avisering.

### [Set-AzureRmDiagnosticSetting](Set-AzureRmDiagnosticSetting.md)
Ange inställningar för loggar och mått för resursen.

