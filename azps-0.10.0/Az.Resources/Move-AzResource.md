---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-Azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: fcee2d5575df49a8f93aa12874c8e658871ca078
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100603"
---
# <span data-ttu-id="62589-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="62589-101">Move-AzResource</span></span>

## <span data-ttu-id="62589-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62589-102">SYNOPSIS</span></span>
<span data-ttu-id="62589-103">Flyttar en resurs till en annan resurs grupp eller prenumeration.</span><span class="sxs-lookup"><span data-stu-id="62589-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="62589-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62589-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62589-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62589-105">DESCRIPTION</span></span>
<span data-ttu-id="62589-106">Cmdleten **Move-AzResource** flyttar befintliga resurser till en annan resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="62589-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="62589-107">Resurs gruppen kan vara i ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="62589-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="62589-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62589-108">EXAMPLES</span></span>

### <span data-ttu-id="62589-109">Exempel 1: flytta en resurs till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="62589-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="62589-110">Det första kommandot får en resurs som heter ContosoStorageAccount med hjälp av Get-AzResource cmdlet och lagrar sedan resursen i $Resource-variabeln.</span><span class="sxs-lookup"><span data-stu-id="62589-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="62589-111">Det andra kommandot flyttar resursen till resurs gruppen med namnet ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="62589-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="62589-112">Kommandot identifierar den resurs som ska flyttas genom att använda egenskapen **ResourceID** för $Resource.</span><span class="sxs-lookup"><span data-stu-id="62589-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="62589-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62589-113">PARAMETERS</span></span>

### <span data-ttu-id="62589-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="62589-114">-ApiVersion</span></span>
<span data-ttu-id="62589-115">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="62589-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="62589-116">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="62589-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="62589-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62589-117">-DefaultProfile</span></span>
<span data-ttu-id="62589-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="62589-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62589-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62589-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="62589-120">Anger namnet på den resurs grupp där cmdleten flyttas till resurserna.</span><span class="sxs-lookup"><span data-stu-id="62589-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62589-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62589-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="62589-122">Anger ID för den prenumeration som den här cmdleten flyttar resurser till.</span><span class="sxs-lookup"><span data-stu-id="62589-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62589-123">-Force</span><span class="sxs-lookup"><span data-stu-id="62589-123">-Force</span></span>
<span data-ttu-id="62589-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="62589-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62589-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="62589-125">-InformationAction</span></span>
<span data-ttu-id="62589-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="62589-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="62589-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="62589-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62589-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="62589-128">Continue</span></span>
- <span data-ttu-id="62589-129">Över</span><span class="sxs-lookup"><span data-stu-id="62589-129">Ignore</span></span>
- <span data-ttu-id="62589-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="62589-130">Inquire</span></span>
- <span data-ttu-id="62589-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="62589-131">SilentlyContinue</span></span>
- <span data-ttu-id="62589-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="62589-132">Stop</span></span>
- <span data-ttu-id="62589-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="62589-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62589-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="62589-134">-InformationVariable</span></span>
<span data-ttu-id="62589-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="62589-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62589-136">-För</span><span class="sxs-lookup"><span data-stu-id="62589-136">-Pre</span></span>
<span data-ttu-id="62589-137">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="62589-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="62589-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62589-138">-ResourceId</span></span>
<span data-ttu-id="62589-139">Anger en matris med ID: n för de resurser som den här cmdleten flyttar.</span><span class="sxs-lookup"><span data-stu-id="62589-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62589-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62589-140">-Confirm</span></span>
<span data-ttu-id="62589-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62589-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62589-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62589-142">-WhatIf</span></span>
<span data-ttu-id="62589-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62589-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62589-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62589-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62589-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62589-145">CommonParameters</span></span>
<span data-ttu-id="62589-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62589-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62589-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62589-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62589-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62589-148">INPUTS</span></span>

## <span data-ttu-id="62589-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62589-149">OUTPUTS</span></span>

## <span data-ttu-id="62589-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62589-150">NOTES</span></span>

## <span data-ttu-id="62589-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62589-151">RELATED LINKS</span></span>

[<span data-ttu-id="62589-152">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="62589-152">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="62589-153">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="62589-153">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="62589-154">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="62589-154">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="62589-155">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="62589-155">Set-AzResource</span></span>](./Set-AzResource.md)


