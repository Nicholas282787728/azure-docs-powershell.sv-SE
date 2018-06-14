---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 9a40eae86b60afb5e04dd6a6074b60e82731578f
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854638"
---
# <a name="release-notes"></a><span data-ttu-id="0b213-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="0b213-103">Release notes</span></span>

<span data-ttu-id="0b213-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="0b213-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-170"></a><span data-ttu-id="0b213-105">Version 1.7.0</span><span class="sxs-lookup"><span data-stu-id="0b213-105">Version 1.7.0</span></span>

* <span data-ttu-id="0b213-106">**Beteendet har ändrats för parametrarna -Force, –Confirm och $ConfirmPreference för alla cmdletar. Vi håller på att ändra den här implementeringen så att den följer riktlinjerna för PowerShell. För de flesta cmdletarna innebär detta borttagning av parametern Force och att ShouldProcess-meddelandet hoppas över. Användarna måste ta med parametern -Confirm:$false i sina PowerShell-skript.**</span><span class="sxs-lookup"><span data-stu-id="0b213-106">**Behavioral change for -Force, –Confirm and $ConfirmPreference parameters for all cmdlets. We are changing this implementation to be in line with PowerShell guidelines. For most cmdlets, this means removing the Force parameter and to skip the ShouldProcess prompt, users will need to include the parameter: ‘-Confirm:$false’ in their PowerShell scripts.**</span></span> <span data-ttu-id="0b213-107">Den här ändringarna åtgärdar följande problem:</span><span class="sxs-lookup"><span data-stu-id="0b213-107">This changes are addressing following issues:</span></span>
  - <span data-ttu-id="0b213-108">Rätt implementering av –WhatIf-funktioner, vilket gör att en användare att bestämma effekterna av en cmdlet eller ett skript utan att göra ändringar</span><span class="sxs-lookup"><span data-stu-id="0b213-108">Correct implementation of –WhatIf functionality, allowing a user to determine the effects of a cmdlet or script without making any actual changes</span></span>
  - <span data-ttu-id="0b213-109">Kontroll över uppmaningar med sessionsomfattande $ConfirmPreference, så att användaren får en uppmaning baserat på en presumtiv ändring (såsom rapporteras i inställningen ConfirmImpact i cmdleten)</span><span class="sxs-lookup"><span data-stu-id="0b213-109">Control over prompting using a session-wide $ConfirmPreference, so that the user is prompted based on the impact of a prospective change (as reported in the ConfirmImpact setting in the cmdlet)</span></span>
  - <span data-ttu-id="0b213-110">Cmdlet-specifik kontroll över bekräftelseuppmaningar med parametern –Confirm</span><span class="sxs-lookup"><span data-stu-id="0b213-110">Cmdlet-specific control over confirmation prompts using the –Confirm parameter</span></span>
  - <span data-ttu-id="0b213-111">Konsekvent användning av ShouldContinue och parametern –Force i cmdletar, endast för de åtgärder som kräver uppmaning från användaren på grund av ändringarnas särskilda karaktär (till exempel borttagning av dolda filer)</span><span class="sxs-lookup"><span data-stu-id="0b213-111">Consistent use of ShouldContinue and the –Force parameter across cmdlets, for only those actions that would require prompting from the user due to the special nature of the changes (for example, deleting hidden files)</span></span>
  - <span data-ttu-id="0b213-112">Konsekvens med andra PowerShell-cmdletar, så att PowerShell-skriptkunskaper från andra cmdletar är direkt tillämpliga på Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="0b213-112">Consistency with other PowerShell cmdlets, so that PowerShell scripting knowledge from other cmdlets is immediately applicable to the Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="0b213-113">**Observera att användaren nu måste ange två parametrar för *Azure PowerShell-cmdletar för att* automatiskt hoppa över alla uppmaningar (gäller samtliga fall):**</span><span class="sxs-lookup"><span data-stu-id="0b213-113">**Notice that now to *automatically skip all Prompts in all Circumstances* Azure PowerShell cmdlets require the user to supply two parameters:**</span></span>
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* <span data-ttu-id="0b213-114">Azure Compute</span><span class="sxs-lookup"><span data-stu-id="0b213-114">Azure Compute</span></span>
  - <span data-ttu-id="0b213-115">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0b213-115">Set-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="0b213-116">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0b213-116">Get-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="0b213-117">Parametern -Redeploy för Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0b213-117">-Redeploy parameter for Restart-AzureVM</span></span>
  - <span data-ttu-id="0b213-118">Parametern -Validate för Move-AzureService, Move-AzureStorageAccount och Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0b213-118">-Validate parameter for Move-AzureService, Move-AzureStorageAccount, and Move-AzureVirtualNetwork</span></span>
  - <span data-ttu-id="0b213-119">Parametrarna för namn och version för cmdletar för tillägg är valfria som tidigare.</span><span class="sxs-lookup"><span data-stu-id="0b213-119">Name and version parameters for extension cmdlets are optional as before.</span></span>
  - <span data-ttu-id="0b213-120">New-AzureVM kan få en licenstyp från VM-objektet.</span><span class="sxs-lookup"><span data-stu-id="0b213-120">New-AzureVM can get a license type from VM object.</span></span>
* <span data-ttu-id="0b213-121">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="0b213-121">Azure Storage</span></span>
  - <span data-ttu-id="0b213-122">Ändra parametern Tags till Tag och lägg till parameteralias Tags</span><span class="sxs-lookup"><span data-stu-id="0b213-122">Change Tags Parameter to Tag, and add parameter alias Tags</span></span>
    + <span data-ttu-id="0b213-123">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b213-123">New-AzureRmStorageAccount</span></span>
    + <span data-ttu-id="0b213-124">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b213-124">Set-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0b213-125">Azure-nätverk</span><span class="sxs-lookup"><span data-stu-id="0b213-125">Azure Network</span></span>
  - <span data-ttu-id="0b213-126">Ny cmdlet har lagts till för virtuell nätverkspeering</span><span class="sxs-lookup"><span data-stu-id="0b213-126">New cmdlet added for Virtual Network Peering</span></span>
* <span data-ttu-id="0b213-127">Azure Redis Cache</span><span class="sxs-lookup"><span data-stu-id="0b213-127">Azure Redis Cache</span></span>
  - <span data-ttu-id="0b213-128">Ny cmdlet har lagts till för Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0b213-128">New cmdlet added for Reset-AzureRmRedisCache</span></span>
  - <span data-ttu-id="0b213-129">Ny cmdlet har lagts till för Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0b213-129">New cmdlet added for Export-AzureRmRedisCache</span></span>
  - <span data-ttu-id="0b213-130">Ny cmdlet har lagts till för Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0b213-130">New cmdlet added for Import-AzureRmRedisCache</span></span>
  - <span data-ttu-id="0b213-131">Cmdleten New-AzureRmRedisCache har ändrats för att innefatta parameterändring för vNet</span><span class="sxs-lookup"><span data-stu-id="0b213-131">Modified cmdlet New-AzureRmRedisCache to include parameter change for vNet</span></span>
* <span data-ttu-id="0b213-132">Säkerhetskopiering och återställning av Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="0b213-132">Azure SQL DB Backup/Restore</span></span>
  - <span data-ttu-id="0b213-133">Cmdletar för säkerhetskopieringsfunktionen för långsiktig kvarhållning</span><span class="sxs-lookup"><span data-stu-id="0b213-133">Cmdlets for LTR (Long Term Retention) backup feature</span></span>
  - <span data-ttu-id="0b213-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="0b213-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="0b213-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b213-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="0b213-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="0b213-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="0b213-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b213-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="0b213-138">Restore-AzureRmSqlDatabase stöder nu återställning till tidpunkt för en borttagen databas</span><span class="sxs-lookup"><span data-stu-id="0b213-138">Restore-AzureRmSqlDatabase now supports point-in-time restore of a deleted database</span></span>
  - <span data-ttu-id="0b213-139">Restore-AzureRmSqlDatabase stöder nu återställning från en säkerhetskopiering med långsiktig kvarhållning</span><span class="sxs-lookup"><span data-stu-id="0b213-139">Restore-AzureRmSqlDatabase now supports restoring from a Long Term Retention backup</span></span>
* <span data-ttu-id="0b213-140">Azure LogicApp</span><span class="sxs-lookup"><span data-stu-id="0b213-140">Azure LogicApp</span></span>
  - <span data-ttu-id="0b213-141">Cmdletar har lagts till för LogicApp-integreringskonton.</span><span class="sxs-lookup"><span data-stu-id="0b213-141">Added LogicApp Integration accounts cmdlets.</span></span>
  - <span data-ttu-id="0b213-142">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0b213-142">Get-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="0b213-143">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="0b213-143">Get-AzureRmIntegrationAccountCallbackUrl</span></span>
  - <span data-ttu-id="0b213-144">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="0b213-144">Get-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="0b213-145">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0b213-145">Get-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="0b213-146">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0b213-146">Get-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="0b213-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0b213-147">Get-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="0b213-148">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0b213-148">Get-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="0b213-149">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0b213-149">New-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="0b213-150">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="0b213-150">New-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="0b213-151">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0b213-151">New-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="0b213-152">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0b213-152">New-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="0b213-153">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0b213-153">New-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="0b213-154">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0b213-154">New-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="0b213-155">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0b213-155">Remove-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="0b213-156">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="0b213-156">Remove-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="0b213-157">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0b213-157">Remove-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="0b213-158">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0b213-158">Remove-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="0b213-159">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0b213-159">Remove-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="0b213-160">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0b213-160">Remove-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="0b213-161">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0b213-161">Set-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="0b213-162">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="0b213-162">Set-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="0b213-163">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0b213-163">Set-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="0b213-164">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="0b213-164">Set-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="0b213-165">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0b213-165">Set-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="0b213-166">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0b213-166">Set-AzureRmIntegrationAccountSchema</span></span>
* <span data-ttu-id="0b213-167">Azure Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="0b213-167">Azure Data Lake Store</span></span>
  - <span data-ttu-id="0b213-168">Kraftig förbättring av prestanda för uppladdning och nedladdning av filer och mappar.</span><span class="sxs-lookup"><span data-stu-id="0b213-168">Drastically improve performance of file and folder upload and download.</span></span>
  - <span data-ttu-id="0b213-169">Detta innefattar en liten ändring i parameternamnen för nedladdning och två nya parametrar för uppladdning:</span><span class="sxs-lookup"><span data-stu-id="0b213-169">This includes a slight change to the parameter names for download and inclusion of two new parameters for upload:</span></span>
    + <span data-ttu-id="0b213-170">NumThreads -> PerFileThreadCount, används för att ange antal trådar som ska användas i en enskild fil</span><span class="sxs-lookup"><span data-stu-id="0b213-170">NumThreads -> PerFileThreadCount, used to indicate the number of threads to use in a single file</span></span>
    + <span data-ttu-id="0b213-171">ConcurrentFileCount, används för att ange antal filer som ska överföras/ladda ned parallellt vid uppladdning/nedladdning av mappar.</span><span class="sxs-lookup"><span data-stu-id="0b213-171">ConcurrentFileCount, used to indicate the number of files to upload/download in parallel for folder upload/download.</span></span>
  - <span data-ttu-id="0b213-172">Standardtrådkörningsvärden har utformats för att ge ett bättre dataflöde för de flesta filstorlekar.</span><span class="sxs-lookup"><span data-stu-id="0b213-172">Default threading values are now designed to give a better all around throughput for most file sizes.</span></span> <span data-ttu-id="0b213-173">Om önskade prestanda inte uppnås kan värdena ovan ändras för att uppfylla kraven.</span><span class="sxs-lookup"><span data-stu-id="0b213-173">If performance is not as desired, the values above can be modified to meet requirements.</span></span>
* <span data-ttu-id="0b213-174">Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="0b213-174">Azure Data Lake Analytics</span></span>
  - <span data-ttu-id="0b213-175">Nu returnerar Get-AzureRMDataLakeAnalyticsDataSource alla datakällor vid anrop utan argument.</span><span class="sxs-lookup"><span data-stu-id="0b213-175">Get-AzureRMDataLakeAnalyticsDataSource now returns all data sources when called with no arguments.</span></span>
  - <span data-ttu-id="0b213-176">Med denna ändring tas också parametern för datakälltyp bort från cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b213-176">This change also removes the data source type parameter from the cmdlet.</span></span>
  - <span data-ttu-id="0b213-177">Den här ändringen gör att ett nytt objekt returneras för liståtgärden med följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="0b213-177">This change results in a new object being returned for the list operation with the following properties:</span></span>
    + <span data-ttu-id="0b213-178">Type (typ av datakälla)</span><span class="sxs-lookup"><span data-stu-id="0b213-178">Type, the type of data source</span></span>
    + <span data-ttu-id="0b213-179">Name (namnet på datakällan)</span><span class="sxs-lookup"><span data-stu-id="0b213-179">Name, the name of the data source</span></span>
    + <span data-ttu-id="0b213-180">IsDefault (har värdet true om detta är standarddatakällan för kontot)</span><span class="sxs-lookup"><span data-stu-id="0b213-180">IsDefault, set to true if this is the default data source for the account</span></span>
  - <span data-ttu-id="0b213-181">Get-AzureRMDataLakeAnalyticsJob har åtgärdats. Detta gäller vissa förskjutningsvärden för datum och tid i listan vid filtrering på submittedBefore och submittedAfter.</span><span class="sxs-lookup"><span data-stu-id="0b213-181">Get-AzureRMDataLakeAnalyticsJob fixed for list for certain date time offset values when filtering on submittedBefore and submittedAfter.</span></span>
* <span data-ttu-id="0b213-182">Web Apps</span><span class="sxs-lookup"><span data-stu-id="0b213-182">Web Apps</span></span>
  - <span data-ttu-id="0b213-183">Lägg till cmdleten Swap-AzureRmWebAppSlot för vanlig växling och växling med förhandsgranskning</span><span class="sxs-lookup"><span data-stu-id="0b213-183">Add Swap-AzureRmWebAppSlot cmdlet for regular swap and swap with preview</span></span>
  - <span data-ttu-id="0b213-184">Utöka cmdleten Set-AzureRmWebAppSlot för att stödja automatisk växling</span><span class="sxs-lookup"><span data-stu-id="0b213-184">Extend Set-AzureRmWebAppSlot cmdlet to support auto swap</span></span>
* <span data-ttu-id="0b213-185">Azure API Management</span><span class="sxs-lookup"><span data-stu-id="0b213-185">Azure API Management</span></span>
  - <span data-ttu-id="0b213-186">Cmdletar för Azure Api-hanteringsdistribution har åtgärdats för AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="0b213-186">Fixed Azure Api Management Deployment cmdlets for AzureChinaCloud.</span></span>
  - <span data-ttu-id="0b213-187">Cmdleten Set-AzureRmApiManagementTenantGitAccess har tagits bort eftersom Git-åtkomst är aktiverat som standard.</span><span class="sxs-lookup"><span data-stu-id="0b213-187">Removed cmdlet Set-AzureRmApiManagementTenantGitAccess as Git Access is enabled by Default.</span></span>
* <span data-ttu-id="0b213-188">Azure Recovery Services Backup</span><span class="sxs-lookup"><span data-stu-id="0b213-188">Azure Recovery Services Backup</span></span>
  - <span data-ttu-id="0b213-189">Stöd för Azure SQL-arbetsbelastningen har lagts till</span><span class="sxs-lookup"><span data-stu-id="0b213-189">Added support for the Azure SQL workload</span></span>
  - <span data-ttu-id="0b213-190">Stöd för att säkerhetskopiera och återställa krypterade virtuella Azure-datorer har lagts till</span><span class="sxs-lookup"><span data-stu-id="0b213-190">Added support for backing up and restoring encrypted Azure VMs</span></span>
  - <span data-ttu-id="0b213-191">Backup-AzureRmRecoveryServicesBackupItem – funktion för valfri kvarhållningstid har lagts till för återställningspunkter</span><span class="sxs-lookup"><span data-stu-id="0b213-191">Backup-AzureRmRecoveryServicesBackupItem - Added optional retention time feature for recovery points</span></span>
  - <span data-ttu-id="0b213-192">Mindre filterrelaterade fel har åtgärdats i cmdletarna Get-AzureRmRecoveryServicesBackupContainer och Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0b213-192">Minor filter-related bug fixes in Get-AzureRmRecoveryServicesBackupContainer and Get-AzureRmRecoveryServicesBackupItem cmdlets</span></span>
* <span data-ttu-id="0b213-193">Azure Automation</span><span class="sxs-lookup"><span data-stu-id="0b213-193">Azure Automation</span></span>
  - <span data-ttu-id="0b213-194">Get-AzureRmAutomationHybridWorkerGroup har lagts till</span><span class="sxs-lookup"><span data-stu-id="0b213-194">Added Get-AzureRmAutomationHybridWorkerGroup</span></span>
