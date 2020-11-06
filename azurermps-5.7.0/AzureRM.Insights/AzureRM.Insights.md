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
# <span data-ttu-id="b3b6d-101">AzureRM. Insights-modul</span><span class="sxs-lookup"><span data-stu-id="b3b6d-101">AzureRM.Insights Module</span></span>
## <span data-ttu-id="b3b6d-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="b3b6d-102">Description</span></span>
<span data-ttu-id="b3b6d-103">I det här avsnittet visas hjälp avsnitt för dina Azure Insights-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-103">This topic displays help topics for the Azure Insights Cmdlets.</span></span>

## <span data-ttu-id="b3b6d-104">AzureRM. Insights-cmdletar</span><span class="sxs-lookup"><span data-stu-id="b3b6d-104">AzureRM.Insights Cmdlets</span></span>
### [<span data-ttu-id="b3b6d-105">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b3b6d-105">Add-AzureRmAutoscaleSetting</span></span>](Add-AzureRmAutoscaleSetting.md)
<span data-ttu-id="b3b6d-106">Skapar en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-106">Creates an Autoscale setting.</span></span>

### [<span data-ttu-id="b3b6d-107">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3b6d-107">Add-AzureRmLogAlertRule</span></span>](Add-AzureRmLogAlertRule.md)
<span data-ttu-id="b3b6d-108">Lägger till eller ersätter en regel för loggnings aviseringar.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-108">Adds or replaces a log alert rule.</span></span>

### [<span data-ttu-id="b3b6d-109">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b3b6d-109">Add-AzureRmLogProfile</span></span>](Add-AzureRmLogProfile.md)
<span data-ttu-id="b3b6d-110">Skapar en ny aktivitets logg profil.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-110">Creates a new activity log profile.</span></span> <span data-ttu-id="b3b6d-111">Denna profil används till att antingen arkivera aktivitets loggen på ett Azure Storage-konto eller strömma den till en Azure Event Hub i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-111">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="b3b6d-112">**Lagrings konto** – det finns inget standard lagrings konto (Premium Storage-konto stöds inte).</span><span class="sxs-lookup"><span data-stu-id="b3b6d-112">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="b3b6d-113">Det kan antingen vara av typen ARM eller klassiskt.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-113">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="b3b6d-114">Om den är inloggad på ett lagrings konto debiteras kostnaden för att lagra aktivitets loggen med normal standard lagrings taxa.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-114">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="b3b6d-115">Det kan bara finnas en enda logg profil per prenumeration som bara är ett lagrings konto per prenumeration som kan användas för att exportera aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-115">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="b3b6d-116">**Händelsehubben-det** kan bara finnas en enda logg profil per prenumeration som bara en händelse gren per prenumeration kan användas för att exportera aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-116">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="b3b6d-117">Om aktivitets loggen strömmas till en händelsehubben tillämpas standard Event Hub-priser.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-117">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="b3b6d-118">I aktivitets loggen kan händelser gälla en region eller kan vara "globalt".</span><span class="sxs-lookup"><span data-stu-id="b3b6d-118">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="b3b6d-119">Global innebär detta att dessa händelser är region agnostics och att de är oberoende av regionen, i de flesta händelser hamnar i den kategorin.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-119">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="b3b6d-120">Om aktivitets loggnings profilen är inställd från portalen lägger den implicit till "global" tillsammans med alla andra regioner som är markerade i användar gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-120">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="b3b6d-121">När du använder en cmdlet måste platsen som "global" anges explicit från valfri annan region.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-121">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="b3b6d-122">**Obs!** **om du inte anger "globalt" i platserna kommer det att leda till att huvud aktivitets loggen inte exporteras.**</span><span class="sxs-lookup"><span data-stu-id="b3b6d-122">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

### [<span data-ttu-id="b3b6d-123">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3b6d-123">Add-AzureRmMetricAlertRule</span></span>](Add-AzureRmMetricAlertRule.md)
<span data-ttu-id="b3b6d-124">Lägger till eller uppdaterar en Metric-baserad notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-124">Adds or updates a metric-based alert rule.</span></span>

### [<span data-ttu-id="b3b6d-125">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3b6d-125">Add-AzureRmWebtestAlertRule</span></span>](Add-AzureRmWebtestAlertRule.md)
<span data-ttu-id="b3b6d-126">Lägger till eller uppdaterar en aviserings regel för en webtest.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-126">Adds or updates a webtest alert rule.</span></span>

### [<span data-ttu-id="b3b6d-127">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b3b6d-127">Disable-AzureRmActivityLogAlert</span></span>](Disable-AzureRmActivityLogAlert.md)
<span data-ttu-id="b3b6d-128">Inaktiverar en aktivitets loggs varning och anger dess taggar.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-128">Disables an activity log alert and sets its tags.</span></span>

### [<span data-ttu-id="b3b6d-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b3b6d-129">Enable-AzureRmActivityLogAlert</span></span>](Enable-AzureRmActivityLogAlert.md)
<span data-ttu-id="b3b6d-130">Aktiverar en aktivitets logg varning och anger dess taggar.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-130">Enables an activity log alert and sets its Tags.</span></span>

### [<span data-ttu-id="b3b6d-131">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b3b6d-131">Get-AzureRmActionGroup</span></span>](Get-AzureRmActionGroup.md)
<span data-ttu-id="b3b6d-132">Hämtar åtgärds grupper.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-132">Gets action group(s).</span></span>

### [<span data-ttu-id="b3b6d-133">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b3b6d-133">Get-AzureRmActivityLogAlert</span></span>](Get-AzureRmActivityLogAlert.md)
<span data-ttu-id="b3b6d-134">Hämtar en eller flera aktivitets logg varningar.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-134">Gets one or more activity log alert resources.</span></span>

### [<span data-ttu-id="b3b6d-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b3b6d-135">Get-AzureRmAlertHistory</span></span>](Get-AzureRmAlertHistory.md)
<span data-ttu-id="b3b6d-136">Hämtar historiken över aviseringar.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-136">Gets the history of alerts.</span></span>

### [<span data-ttu-id="b3b6d-137">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3b6d-137">Get-AzureRmAlertRule</span></span>](Get-AzureRmAlertRule.md)
<span data-ttu-id="b3b6d-138">Hämtar notifieringsregler.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-138">Gets alert rules.</span></span>

### [<span data-ttu-id="b3b6d-139">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="b3b6d-139">Get-AzureRmAutoscaleHistory</span></span>](Get-AzureRmAutoscaleHistory.md)
<span data-ttu-id="b3b6d-140">Hämtar den automatiska skalnings historiken.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-140">Gets the Autoscale history.</span></span>

### [<span data-ttu-id="b3b6d-141">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b3b6d-141">Get-AzureRmAutoscaleSetting</span></span>](Get-AzureRmAutoscaleSetting.md)
<span data-ttu-id="b3b6d-142">Hämtar inställningar för Autoskala.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-142">Gets Autoscale settings.</span></span>

### [<span data-ttu-id="b3b6d-143">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="b3b6d-143">Get-AzureRmDiagnosticSetting</span></span>](Get-AzureRmDiagnosticSetting.md)
<span data-ttu-id="b3b6d-144">Hämtar de protokollförda kategorierna och tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-144">Gets the logged categories and time grains.</span></span>

### [<span data-ttu-id="b3b6d-145">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="b3b6d-145">Get-AzureRmLog</span></span>](Get-AzureRmLog.md)
<span data-ttu-id="b3b6d-146">Hämtar en logg över händelser.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-146">Gets a log of events.</span></span>

### [<span data-ttu-id="b3b6d-147">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b3b6d-147">Get-AzureRmLogProfile</span></span>](Get-AzureRmLogProfile.md)
<span data-ttu-id="b3b6d-148">Hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-148">Gets a log profile.</span></span>

### [<span data-ttu-id="b3b6d-149">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="b3b6d-149">Get-AzureRmMetric</span></span>](Get-AzureRmMetric.md)
<span data-ttu-id="b3b6d-150">Hämtar metriska värden för en resurs.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-150">Gets the metric values of a resource.</span></span>

### [<span data-ttu-id="b3b6d-151">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b3b6d-151">Get-AzureRmMetricDefinition</span></span>](Get-AzureRmMetricDefinition.md)
<span data-ttu-id="b3b6d-152">Hämtar mått definitioner.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-152">Gets metric definitions.</span></span>

### [<span data-ttu-id="b3b6d-153">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="b3b6d-153">Get-AzureRmUsage</span></span>](Get-AzureRmUsage.md)
<span data-ttu-id="b3b6d-154">Hämtar användnings måtten för en resurs.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-154">Gets the usage metrics for a resource.</span></span>

### [<span data-ttu-id="b3b6d-155">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b3b6d-155">New-AzureRmActionGroup</span></span>](New-AzureRmActionGroup.md)
<span data-ttu-id="b3b6d-156">Skapar ett ActionGroup-referens objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-156">Creates an ActionGroup reference object in memory.</span></span>

### [<span data-ttu-id="b3b6d-157">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b6d-157">New-AzureRmActionGroupReceiver</span></span>](New-AzureRmActionGroupReceiver.md)
<span data-ttu-id="b3b6d-158">Skapar en ny mottagare av åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-158">Creates an new action group receiver.</span></span>

### [<span data-ttu-id="b3b6d-159">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="b3b6d-159">New-AzureRmActivityLogAlertCondition</span></span>](New-AzureRmActivityLogAlertCondition.md)
<span data-ttu-id="b3b6d-160">Skapar ett nytt aviserings villkor för aktivitets loggen i minnet.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-160">Creates an new activity log alert condition object in memory.</span></span>

### [<span data-ttu-id="b3b6d-161">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="b3b6d-161">New-AzureRmAlertRuleEmail</span></span>](New-AzureRmAlertRuleEmail.md)
<span data-ttu-id="b3b6d-162">Skapar en e-poståtgärd för en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-162">Creates an email action for an alert rule.</span></span>

### [<span data-ttu-id="b3b6d-163">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="b3b6d-163">New-AzureRmAlertRuleWebhook</span></span>](New-AzureRmAlertRuleWebhook.md)
<span data-ttu-id="b3b6d-164">Skapar en aviserings regel med webhook.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-164">Creates an alert rule webhook.</span></span>

### [<span data-ttu-id="b3b6d-165">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="b3b6d-165">New-AzureRmAutoscaleNotification</span></span>](New-AzureRmAutoscaleNotification.md)
<span data-ttu-id="b3b6d-166">Skapar ett e-postmeddelande med Autoskala.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-166">Creates an Autoscale email notification.</span></span>

### [<span data-ttu-id="b3b6d-167">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="b3b6d-167">New-AzureRmAutoscaleProfile</span></span>](New-AzureRmAutoscaleProfile.md)
<span data-ttu-id="b3b6d-168">Skapar en Autoskala-profil.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-168">Creates an Autoscale profile.</span></span>

### [<span data-ttu-id="b3b6d-169">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="b3b6d-169">New-AzureRmAutoscaleRule</span></span>](New-AzureRmAutoscaleRule.md)
<span data-ttu-id="b3b6d-170">Skapar en Autoskala-regel.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-170">Creates an Autoscale rule.</span></span>

### [<span data-ttu-id="b3b6d-171">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="b3b6d-171">New-AzureRmAutoscaleWebhook</span></span>](New-AzureRmAutoscaleWebhook.md)
<span data-ttu-id="b3b6d-172">Skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-172">Creates an Autoscale webhook.</span></span>

### [<span data-ttu-id="b3b6d-173">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b3b6d-173">Remove-AzureRmActionGroup</span></span>](Remove-AzureRmActionGroup.md)
<span data-ttu-id="b3b6d-174">Tar bort en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-174">Removes an action group.</span></span>

### [<span data-ttu-id="b3b6d-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b3b6d-175">Remove-AzureRmActivityLogAlert</span></span>](Remove-AzureRmActivityLogAlert.md)
<span data-ttu-id="b3b6d-176">Tar bort en aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-176">Removes an activity log alert.</span></span>

### [<span data-ttu-id="b3b6d-177">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b3b6d-177">Remove-AzureRmAlertRule</span></span>](Remove-AzureRmAlertRule.md)
<span data-ttu-id="b3b6d-178">Tar bort en varnings regel.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-178">Removes an alert rule.</span></span>

### [<span data-ttu-id="b3b6d-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b3b6d-179">Remove-AzureRmAutoscaleSetting</span></span>](Remove-AzureRmAutoscaleSetting.md)
<span data-ttu-id="b3b6d-180">Tar bort en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-180">Removes an Autoscale setting.</span></span>

### [<span data-ttu-id="b3b6d-181">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b3b6d-181">Remove-AzureRmLogProfile</span></span>](Remove-AzureRmLogProfile.md)
<span data-ttu-id="b3b6d-182">Tar bort en logg profil.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-182">Removes a log profile.</span></span>

### [<span data-ttu-id="b3b6d-183">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b3b6d-183">Set-AzureRmActionGroup</span></span>](Set-AzureRmActionGroup.md)
<span data-ttu-id="b3b6d-184">Skapar en ny eller uppdaterar en befintlig åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-184">Creates a new or updates an existing action group.</span></span>

### [<span data-ttu-id="b3b6d-185">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b3b6d-185">Set-AzureRmActivityLogAlert</span></span>](Set-AzureRmActivityLogAlert.md)
<span data-ttu-id="b3b6d-186">Skapar en ny eller anger en befintlig aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-186">Creates a new or sets an existing activity log alert.</span></span>

### [<span data-ttu-id="b3b6d-187">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="b3b6d-187">Set-AzureRmDiagnosticSetting</span></span>](Set-AzureRmDiagnosticSetting.md)
<span data-ttu-id="b3b6d-188">Ange inställningar för loggar och mått för resursen.</span><span class="sxs-lookup"><span data-stu-id="b3b6d-188">Sets the logs and metrics settings for the resource.</span></span>

