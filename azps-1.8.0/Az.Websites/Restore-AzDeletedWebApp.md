---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a90a56417ab8b1b08d72cb9d00ebe7411a6f075c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746030"
---
# <span data-ttu-id="79fc8-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="79fc8-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="79fc8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="79fc8-103">Återställer en borttagen webbapp till en ny eller befintlig webbapp.</span><span class="sxs-lookup"><span data-stu-id="79fc8-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="79fc8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79fc8-104">SYNTAX</span></span>

### <span data-ttu-id="79fc8-105">FromDeletedResourceName (standard)</span><span class="sxs-lookup"><span data-stu-id="79fc8-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79fc8-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="79fc8-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79fc8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79fc8-107">DESCRIPTION</span></span>
<span data-ttu-id="79fc8-108">Cmdleten **restore-AzDeletedWebApp** återställer en borttagen webbapp.</span><span class="sxs-lookup"><span data-stu-id="79fc8-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="79fc8-109">Webb programmet som anges av TargetResourceGroupName, TargetName och TargetSlot kommer att skrivas över med innehållet och inställningarna för det borttagna webb programmet.</span><span class="sxs-lookup"><span data-stu-id="79fc8-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="79fc8-110">Om mål parametrarna inte anges fylls de automatiskt i med webb programmets resurs grupp, namn och plats.</span><span class="sxs-lookup"><span data-stu-id="79fc8-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="79fc8-111">Om mål webb programmet inte finns kommer det att skapas automatiskt i den app service-plan som anges av TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="79fc8-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="79fc8-112">Växeln RestoreContentOnly kan bara användas för att återställa de borttagna apparnas filer utan appinställningar.</span><span class="sxs-lookup"><span data-stu-id="79fc8-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="79fc8-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79fc8-113">EXAMPLES</span></span>

### <span data-ttu-id="79fc8-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79fc8-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="79fc8-115">Återställer en borttagen app som heter ContosoApp som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="79fc8-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="79fc8-116">En ny app med samma namn och resurs grupp kommer att skapas i App Service-planen med namnet ContosoPlan och den borttagna appens filer och inställningar återställs.</span><span class="sxs-lookup"><span data-stu-id="79fc8-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="79fc8-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="79fc8-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="79fc8-118">Återställer mellanlagrings platsen för en borttagen app som heter ContosoApp som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="79fc8-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="79fc8-119">Webb programmet som heter ContosoRestore som tillhör resurs gruppens standard-webeast skrivs över.</span><span class="sxs-lookup"><span data-stu-id="79fc8-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="79fc8-120">De borttagna webbappens inställningar återställs inte.</span><span class="sxs-lookup"><span data-stu-id="79fc8-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="79fc8-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79fc8-121">PARAMETERS</span></span>

### <span data-ttu-id="79fc8-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79fc8-122">-AsJob</span></span>
<span data-ttu-id="79fc8-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="79fc8-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79fc8-124">-DefaultProfile</span></span>
<span data-ttu-id="79fc8-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79fc8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-126">-Force</span><span class="sxs-lookup"><span data-stu-id="79fc8-126">-Force</span></span>
<span data-ttu-id="79fc8-127">Utför återställningen utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="79fc8-127">Do the restore without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79fc8-128">-InputObject</span></span>
<span data-ttu-id="79fc8-129">Den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="79fc8-129">The deleted Azure Web App.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="79fc8-130">-Name</span></span>
<span data-ttu-id="79fc8-131">Namnet på den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="79fc8-131">The name of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79fc8-132">-ResourceGroupName</span></span>
<span data-ttu-id="79fc8-133">Resurs gruppen för den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="79fc8-133">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="79fc8-134">-RestoreContentOnly</span></span>
<span data-ttu-id="79fc8-135">Återställ webbappens filer, men Återställ inte inställningarna.</span><span class="sxs-lookup"><span data-stu-id="79fc8-135">Restore the web app's files, but do not restore the settings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="79fc8-136">-Slot</span></span>
<span data-ttu-id="79fc8-137">Den borttagna Azure Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="79fc8-137">The deleted Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="79fc8-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="79fc8-139">App Service-abonnemanget för den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="79fc8-139">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="79fc8-140">-TargetName</span></span>
<span data-ttu-id="79fc8-141">Namnet på den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="79fc8-141">The name of the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79fc8-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="79fc8-143">Resurs gruppen som innehåller den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="79fc8-143">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="79fc8-144">-TargetSlot</span></span>
<span data-ttu-id="79fc8-145">Namnet på den nya Azure Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="79fc8-145">The name of the new Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-146">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="79fc8-146">-UseDisasterRecovery</span></span>
<span data-ttu-id="79fc8-147">Använd det här alternativet om du vill återställa en borttagen app från en enhet som är offline.</span><span class="sxs-lookup"><span data-stu-id="79fc8-147">Use to recover a deleted app from a scale unit that is offline.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79fc8-148">-Confirm</span></span>
<span data-ttu-id="79fc8-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79fc8-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79fc8-150">-WhatIf</span></span>
<span data-ttu-id="79fc8-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79fc8-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79fc8-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79fc8-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fc8-153">CommonParameters</span></span>
<span data-ttu-id="79fc8-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79fc8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fc8-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79fc8-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fc8-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79fc8-156">INPUTS</span></span>

### <span data-ttu-id="79fc8-157">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="79fc8-157">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="79fc8-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79fc8-158">OUTPUTS</span></span>

### <span data-ttu-id="79fc8-159">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="79fc8-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="79fc8-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79fc8-160">NOTES</span></span>

## <span data-ttu-id="79fc8-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79fc8-161">RELATED LINKS</span></span>

[<span data-ttu-id="79fc8-162">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="79fc8-162">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)