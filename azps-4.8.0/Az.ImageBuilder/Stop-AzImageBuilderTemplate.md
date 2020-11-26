---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260480"
---
# <span data-ttu-id="f3672-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="f3672-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="f3672-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3672-102">SYNOPSIS</span></span>
<span data-ttu-id="f3672-103">Avbryta den långa bild versionen som baseras på bild mal len</span><span class="sxs-lookup"><span data-stu-id="f3672-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="f3672-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3672-104">SYNTAX</span></span>

### <span data-ttu-id="f3672-105">Avbryt (standard)</span><span class="sxs-lookup"><span data-stu-id="f3672-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f3672-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f3672-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3672-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3672-107">DESCRIPTION</span></span>
<span data-ttu-id="f3672-108">Avbryta den långa bild versionen som baseras på bild mal len</span><span class="sxs-lookup"><span data-stu-id="f3672-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="f3672-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3672-109">EXAMPLES</span></span>

### <span data-ttu-id="f3672-110">Exempel 1: stoppa skapandet av bildmallar</span><span class="sxs-lookup"><span data-stu-id="f3672-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="f3672-111">Med det här kommandot stoppas bildmallar.</span><span class="sxs-lookup"><span data-stu-id="f3672-111">This command stops image template creation.</span></span>

### <span data-ttu-id="f3672-112">Exempel 2: stoppa skapandet av bildmallar</span><span class="sxs-lookup"><span data-stu-id="f3672-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="f3672-113">Med det här kommandot stoppas bildmallar.</span><span class="sxs-lookup"><span data-stu-id="f3672-113">This command stops image template creation.</span></span>

## <span data-ttu-id="f3672-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3672-114">PARAMETERS</span></span>

### <span data-ttu-id="f3672-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3672-115">-AsJob</span></span>
<span data-ttu-id="f3672-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="f3672-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f3672-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3672-117">-DefaultProfile</span></span>
<span data-ttu-id="f3672-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3672-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3672-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="f3672-119">-ImageTemplateName</span></span>
<span data-ttu-id="f3672-120">Namnet på bild mal len</span><span class="sxs-lookup"><span data-stu-id="f3672-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3672-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3672-121">-InputObject</span></span>
<span data-ttu-id="f3672-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f3672-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: CancelViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3672-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f3672-123">-NoWait</span></span>
<span data-ttu-id="f3672-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="f3672-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f3672-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3672-125">-PassThru</span></span>
<span data-ttu-id="f3672-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="f3672-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f3672-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3672-127">-ResourceGroupName</span></span>
<span data-ttu-id="f3672-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f3672-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3672-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3672-129">-SubscriptionId</span></span>
<span data-ttu-id="f3672-130">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f3672-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f3672-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f3672-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3672-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3672-132">-Confirm</span></span>
<span data-ttu-id="f3672-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3672-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3672-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3672-134">-WhatIf</span></span>
<span data-ttu-id="f3672-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3672-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3672-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3672-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3672-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3672-137">CommonParameters</span></span>
<span data-ttu-id="f3672-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3672-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3672-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3672-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3672-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3672-140">INPUTS</span></span>

### <span data-ttu-id="f3672-141">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="f3672-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="f3672-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3672-142">OUTPUTS</span></span>

### <span data-ttu-id="f3672-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3672-143">System.Boolean</span></span>

## <span data-ttu-id="f3672-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3672-144">NOTES</span></span>

<span data-ttu-id="f3672-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f3672-145">ALIASES</span></span>

<span data-ttu-id="f3672-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f3672-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f3672-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f3672-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3672-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f3672-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f3672-149">INPUTOBJECT <IImageBuilderIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f3672-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f3672-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f3672-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f3672-151">`[ImageTemplateName <String>]`: Namnet på bild mal len</span><span class="sxs-lookup"><span data-stu-id="f3672-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="f3672-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f3672-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f3672-153">`[RunOutputName <String>]`: Namnet på Kör-resultatet</span><span class="sxs-lookup"><span data-stu-id="f3672-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="f3672-154">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f3672-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f3672-155">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f3672-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f3672-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3672-156">RELATED LINKS</span></span>
