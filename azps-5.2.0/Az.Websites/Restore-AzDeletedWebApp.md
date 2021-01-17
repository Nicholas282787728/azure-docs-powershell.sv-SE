---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389325"
---
# <span data-ttu-id="1486c-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1486c-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="1486c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1486c-102">SYNOPSIS</span></span>
<span data-ttu-id="1486c-103">Återställer en borttagen webbapp till en ny eller befintlig webbapp.</span><span class="sxs-lookup"><span data-stu-id="1486c-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="1486c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1486c-104">SYNTAX</span></span>

### <span data-ttu-id="1486c-105">FromDeletedResourceName (standard)</span><span class="sxs-lookup"><span data-stu-id="1486c-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1486c-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="1486c-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1486c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1486c-107">DESCRIPTION</span></span>
<span data-ttu-id="1486c-108">Cmdleten **restore-AzDeletedWebApp** återställer en borttagen webbapp.</span><span class="sxs-lookup"><span data-stu-id="1486c-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="1486c-109">Webb programmet som anges av TargetResourceGroupName, TargetName och TargetSlot kommer att skrivas över med innehållet och inställningarna för det borttagna webb programmet.</span><span class="sxs-lookup"><span data-stu-id="1486c-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="1486c-110">Om mål parametrarna inte anges fylls de automatiskt i med webb programmets resurs grupp, namn och plats.</span><span class="sxs-lookup"><span data-stu-id="1486c-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="1486c-111">Om mål webb programmet inte finns kommer det att skapas automatiskt i den app service-plan som anges av TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="1486c-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="1486c-112">Växeln RestoreContentOnly kan bara användas för att återställa de borttagna apparnas filer utan appinställningar.</span><span class="sxs-lookup"><span data-stu-id="1486c-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="1486c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1486c-113">EXAMPLES</span></span>

### <span data-ttu-id="1486c-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1486c-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="1486c-115">Återställer en borttagen app som heter ContosoApp som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="1486c-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="1486c-116">En ny app med samma namn och resurs grupp kommer att skapas i App Service-planen med namnet ContosoPlan och den borttagna appens filer och inställningar återställs.</span><span class="sxs-lookup"><span data-stu-id="1486c-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="1486c-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1486c-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="1486c-118">Återställer mellanlagrings platsen för en borttagen app som heter ContosoApp som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="1486c-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="1486c-119">Webb programmet som heter ContosoRestore som tillhör resurs gruppens standard-webeast skrivs över.</span><span class="sxs-lookup"><span data-stu-id="1486c-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="1486c-120">De borttagna webbappens inställningar återställs inte.</span><span class="sxs-lookup"><span data-stu-id="1486c-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="1486c-121">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="1486c-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="1486c-122">Om det finns två borttagna appar med samma namn (ContosoApp) kommer vi att få information om både webbplatserna och återställa appen med namnet ContosoRestore med appen av vårt val genom att ringa upp med ID.</span><span class="sxs-lookup"><span data-stu-id="1486c-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="1486c-123">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="1486c-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="1486c-124">Om det finns två borttagna appar med samma namn (ContosoApp) kommer vi att få information om både webbplatserna och återställa appen med namnet ContosoRestore med appen av vårt val genom att ringa upp med InputObject (Deletedsite) uppgifter</span><span class="sxs-lookup"><span data-stu-id="1486c-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="1486c-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1486c-125">PARAMETERS</span></span>

### <span data-ttu-id="1486c-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1486c-126">-AsJob</span></span>
<span data-ttu-id="1486c-127">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1486c-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1486c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1486c-128">-DefaultProfile</span></span>
<span data-ttu-id="1486c-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1486c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1486c-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="1486c-130">-DeletedId</span></span>
<span data-ttu-id="1486c-131">ID för den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1486c-131">The Id of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1486c-132">-Force</span><span class="sxs-lookup"><span data-stu-id="1486c-132">-Force</span></span>
<span data-ttu-id="1486c-133">Utför återställningen utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1486c-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1486c-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1486c-134">-InputObject</span></span>
<span data-ttu-id="1486c-135">Den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1486c-135">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1486c-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="1486c-136">-Location</span></span>
<span data-ttu-id="1486c-137">Platsen för den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1486c-137">The location of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1486c-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="1486c-138">-Name</span></span>
<span data-ttu-id="1486c-139">Namnet på den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1486c-139">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1486c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1486c-140">-ResourceGroupName</span></span>
<span data-ttu-id="1486c-141">Resurs gruppen för den borttagna Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1486c-141">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1486c-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="1486c-142">-RestoreContentOnly</span></span>
<span data-ttu-id="1486c-143">Återställ webbappens filer, men Återställ inte inställningarna.</span><span class="sxs-lookup"><span data-stu-id="1486c-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="1486c-144">-Plats</span><span class="sxs-lookup"><span data-stu-id="1486c-144">-Slot</span></span>
<span data-ttu-id="1486c-145">Den borttagna Azure Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="1486c-145">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="1486c-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="1486c-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="1486c-147">App Service-abonnemanget för den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1486c-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="1486c-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="1486c-148">-TargetName</span></span>
<span data-ttu-id="1486c-149">Namnet på den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1486c-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="1486c-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1486c-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="1486c-151">Resurs gruppen som innehåller den nya Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1486c-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="1486c-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="1486c-152">-TargetSlot</span></span>
<span data-ttu-id="1486c-153">Namnet på den nya Azure Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="1486c-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="1486c-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="1486c-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="1486c-155">Använd det här alternativet om du vill återställa en borttagen app från en enhet som är offline.</span><span class="sxs-lookup"><span data-stu-id="1486c-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="1486c-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1486c-156">-Confirm</span></span>
<span data-ttu-id="1486c-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1486c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1486c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1486c-158">-WhatIf</span></span>
<span data-ttu-id="1486c-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1486c-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1486c-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1486c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1486c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1486c-161">CommonParameters</span></span>
<span data-ttu-id="1486c-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1486c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1486c-163">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1486c-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1486c-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1486c-164">INPUTS</span></span>

### <span data-ttu-id="1486c-165">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1486c-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="1486c-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1486c-166">OUTPUTS</span></span>

### <span data-ttu-id="1486c-167">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1486c-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1486c-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1486c-168">NOTES</span></span>

## <span data-ttu-id="1486c-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1486c-169">RELATED LINKS</span></span>

[<span data-ttu-id="1486c-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1486c-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)