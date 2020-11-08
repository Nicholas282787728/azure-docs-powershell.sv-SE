---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a67fec3246d52122554f256dfeb4d0349e869573
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090641"
---
# <span data-ttu-id="9170a-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="9170a-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="9170a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9170a-102">SYNOPSIS</span></span>
<span data-ttu-id="9170a-103">Återställer en borttagen webbapp till en ny eller befintlig webbapp.</span><span class="sxs-lookup"><span data-stu-id="9170a-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="9170a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9170a-104">SYNTAX</span></span>

### <span data-ttu-id="9170a-105">FromDeletedResourceName (standard)</span><span class="sxs-lookup"><span data-stu-id="9170a-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9170a-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="9170a-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9170a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9170a-107">DESCRIPTION</span></span>
<span data-ttu-id="9170a-108">Cmdleten **restore-AzDeletedWebApp** återställer en borttagen webbapp.</span><span class="sxs-lookup"><span data-stu-id="9170a-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="9170a-109">Webb programmet som anges av TargetResourceGroupName, TargetName och TargetSlot kommer att skrivas över med innehållet och inställningarna för det borttagna webb programmet.</span><span class="sxs-lookup"><span data-stu-id="9170a-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="9170a-110">Om mål parametrarna inte anges fylls de automatiskt i med webb programmets resurs grupp, namn och plats.</span><span class="sxs-lookup"><span data-stu-id="9170a-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="9170a-111">Om mål webb programmet inte finns kommer det att skapas automatiskt i den app service-plan som anges av TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="9170a-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="9170a-112">Växeln RestoreContentOnly kan bara användas för att återställa de borttagna apparnas filer utan appinställningar.</span><span class="sxs-lookup"><span data-stu-id="9170a-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="9170a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9170a-113">EXAMPLES</span></span>

### <span data-ttu-id="9170a-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9170a-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="9170a-115">Återställer en borttagen app som heter ContosoApp som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="9170a-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="9170a-116">En ny app med samma namn och resurs grupp kommer att skapas i App Service-planen med namnet ContosoPlan och den borttagna appens filer och inställningar återställs.</span><span class="sxs-lookup"><span data-stu-id="9170a-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="9170a-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9170a-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="9170a-118">Återställer mellanlagrings platsen för en borttagen app som heter ContosoApp som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="9170a-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="9170a-119">Webb programmet som heter ContosoRestore som tillhör resurs gruppens standard-webeast skrivs över.</span><span class="sxs-lookup"><span data-stu-id="9170a-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="9170a-120">De borttagna webbappens inställningar återställs inte.</span><span class="sxs-lookup"><span data-stu-id="9170a-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="9170a-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9170a-121">PARAMETERS</span></span>

### <span data-ttu-id="9170a-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9170a-122">-AsJob</span></span>
<span data-ttu-id="9170a-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9170a-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9170a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9170a-124">-DefaultProfile</span></span>
<span data-ttu-id="9170a-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9170a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9170a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9170a-126">-Force</span></span>
<span data-ttu-id="9170a-127">Utför återställningen utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9170a-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9170a-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9170a-128">-InputObject</span></span>
<span data-ttu-id="9170a-129">Den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9170a-129">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="9170a-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="9170a-130">-Location</span></span>
<span data-ttu-id="9170a-131">Platsen för den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9170a-131">The location of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9170a-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="9170a-132">-Name</span></span>
<span data-ttu-id="9170a-133">Namnet på den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9170a-133">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="9170a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9170a-134">-ResourceGroupName</span></span>
<span data-ttu-id="9170a-135">Resurs gruppen för den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9170a-135">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="9170a-136">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="9170a-136">-RestoreContentOnly</span></span>
<span data-ttu-id="9170a-137">Återställ webbappens filer, men Återställ inte inställningarna.</span><span class="sxs-lookup"><span data-stu-id="9170a-137">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="9170a-138">-Plats</span><span class="sxs-lookup"><span data-stu-id="9170a-138">-Slot</span></span>
<span data-ttu-id="9170a-139">Den borttagna Azure Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="9170a-139">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="9170a-140">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="9170a-140">-TargetAppServicePlanName</span></span>
<span data-ttu-id="9170a-141">App Service-abonnemanget för den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9170a-141">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="9170a-142">-TargetName</span><span class="sxs-lookup"><span data-stu-id="9170a-142">-TargetName</span></span>
<span data-ttu-id="9170a-143">Namnet på den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9170a-143">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="9170a-144">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9170a-144">-TargetResourceGroupName</span></span>
<span data-ttu-id="9170a-145">Resurs gruppen som innehåller den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9170a-145">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="9170a-146">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="9170a-146">-TargetSlot</span></span>
<span data-ttu-id="9170a-147">Namnet på den nya Azure Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="9170a-147">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="9170a-148">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="9170a-148">-UseDisasterRecovery</span></span>
<span data-ttu-id="9170a-149">Använd det här alternativet om du vill återställa en borttagen app från en enhet som är offline.</span><span class="sxs-lookup"><span data-stu-id="9170a-149">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="9170a-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9170a-150">-Confirm</span></span>
<span data-ttu-id="9170a-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9170a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9170a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9170a-152">-WhatIf</span></span>
<span data-ttu-id="9170a-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9170a-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9170a-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9170a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9170a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9170a-155">CommonParameters</span></span>
<span data-ttu-id="9170a-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9170a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9170a-157">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9170a-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9170a-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9170a-158">INPUTS</span></span>

### <span data-ttu-id="9170a-159">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="9170a-159">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="9170a-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9170a-160">OUTPUTS</span></span>

### <span data-ttu-id="9170a-161">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9170a-161">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9170a-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9170a-162">NOTES</span></span>

## <span data-ttu-id="9170a-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9170a-163">RELATED LINKS</span></span>

[<span data-ttu-id="9170a-164">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="9170a-164">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)