---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 998c4f05e8b6a03749a4872e3f4b069e29ef634d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319500"
---
# <span data-ttu-id="5ed8c-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="5ed8c-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="5ed8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ed8c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed8c-103">Ta bort en mall för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="5ed8c-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="5ed8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ed8c-104">SYNTAX</span></span>

### <span data-ttu-id="5ed8c-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="5ed8c-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5ed8c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ed8c-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ed8c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ed8c-107">DESCRIPTION</span></span>
<span data-ttu-id="5ed8c-108">Ta bort en mall för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="5ed8c-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="5ed8c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ed8c-109">EXAMPLES</span></span>

### <span data-ttu-id="5ed8c-110">Exempel 1: ta bort en bildmall</span><span class="sxs-lookup"><span data-stu-id="5ed8c-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="5ed8c-111">Det här kommandot tar bort en bildmall.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-111">This command removes a image template.</span></span>

### <span data-ttu-id="5ed8c-112">Exempel 2: ta bort en bildmall</span><span class="sxs-lookup"><span data-stu-id="5ed8c-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="5ed8c-113">Det här kommandot tar bort en bildmall.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-113">This command removes a image template.</span></span>

## <span data-ttu-id="5ed8c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ed8c-114">PARAMETERS</span></span>

### <span data-ttu-id="5ed8c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ed8c-115">-AsJob</span></span>
<span data-ttu-id="5ed8c-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="5ed8c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5ed8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed8c-117">-DefaultProfile</span></span>
<span data-ttu-id="5ed8c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ed8c-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="5ed8c-119">-ImageTemplateName</span></span>
<span data-ttu-id="5ed8c-120">Namnet på bild mal len</span><span class="sxs-lookup"><span data-stu-id="5ed8c-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed8c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ed8c-121">-InputObject</span></span>
<span data-ttu-id="5ed8c-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed8c-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5ed8c-123">-NoWait</span></span>
<span data-ttu-id="5ed8c-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="5ed8c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5ed8c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ed8c-125">-PassThru</span></span>
<span data-ttu-id="5ed8c-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="5ed8c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5ed8c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed8c-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ed8c-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed8c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ed8c-129">-SubscriptionId</span></span>
<span data-ttu-id="5ed8c-130">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ed8c-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed8c-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ed8c-132">-Confirm</span></span>
<span data-ttu-id="5ed8c-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ed8c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ed8c-134">-WhatIf</span></span>
<span data-ttu-id="5ed8c-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ed8c-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ed8c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed8c-137">CommonParameters</span></span>
<span data-ttu-id="5ed8c-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed8c-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ed8c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed8c-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ed8c-140">INPUTS</span></span>

### <span data-ttu-id="5ed8c-141">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="5ed8c-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="5ed8c-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ed8c-142">OUTPUTS</span></span>

### <span data-ttu-id="5ed8c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ed8c-143">System.Boolean</span></span>

## <span data-ttu-id="5ed8c-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ed8c-144">NOTES</span></span>

<span data-ttu-id="5ed8c-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5ed8c-145">ALIASES</span></span>

<span data-ttu-id="5ed8c-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5ed8c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ed8c-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ed8c-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ed8c-149">INPUTOBJECT <IImageBuilderIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5ed8c-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ed8c-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5ed8c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ed8c-151">`[ImageTemplateName <String>]`: Namnet på bild mal len</span><span class="sxs-lookup"><span data-stu-id="5ed8c-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="5ed8c-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5ed8c-153">`[RunOutputName <String>]`: Namnet på Kör-resultatet</span><span class="sxs-lookup"><span data-stu-id="5ed8c-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="5ed8c-154">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5ed8c-155">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5ed8c-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ed8c-156">RELATED LINKS</span></span>

