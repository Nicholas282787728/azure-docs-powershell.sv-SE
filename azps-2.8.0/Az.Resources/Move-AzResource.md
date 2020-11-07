---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: d885c4084390a46104267d7d39cb9e4f8a7a0924
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "93931602"
---
# <span data-ttu-id="f4a2e-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="f4a2e-101">Move-AzResource</span></span>

## <span data-ttu-id="f4a2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a2e-103">Flyttar en resurs till en annan resurs grupp eller prenumeration.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="f4a2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4a2e-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a2e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4a2e-105">DESCRIPTION</span></span>
<span data-ttu-id="f4a2e-106">Cmdleten **Move-AzResource** flyttar befintliga resurser till en annan resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="f4a2e-107">Resurs gruppen kan vara i ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="f4a2e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4a2e-108">EXAMPLES</span></span>

### <span data-ttu-id="f4a2e-109">Exempel 1: flytta en resurs till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="f4a2e-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="f4a2e-110">Det första kommandot får en resurs som heter ContosoStorageAccount med hjälp av Get-AzResource cmdlet och lagrar sedan resursen i $Resource-variabeln.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="f4a2e-111">Det andra kommandot flyttar resursen till resurs gruppen med namnet ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="f4a2e-112">Kommandot identifierar den resurs som ska flyttas genom att använda egenskapen **ResourceID** för $Resource.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="f4a2e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4a2e-113">PARAMETERS</span></span>

### <span data-ttu-id="f4a2e-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f4a2e-114">-ApiVersion</span></span>
<span data-ttu-id="f4a2e-115">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f4a2e-116">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f4a2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a2e-117">-DefaultProfile</span></span>
<span data-ttu-id="f4a2e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f4a2e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4a2e-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a2e-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="f4a2e-120">Anger namnet på den resurs grupp där cmdleten flyttas till resurserna.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="f4a2e-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4a2e-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="f4a2e-122">Anger ID för den prenumeration som den här cmdleten flyttar resurser till.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="f4a2e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f4a2e-123">-Force</span></span>
<span data-ttu-id="f4a2e-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4a2e-125">-För</span><span class="sxs-lookup"><span data-stu-id="f4a2e-125">-Pre</span></span>
<span data-ttu-id="f4a2e-126">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f4a2e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4a2e-127">-ResourceId</span></span>
<span data-ttu-id="f4a2e-128">Anger en matris med ID: n för de resurser som den här cmdleten flyttar.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="f4a2e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4a2e-129">-Confirm</span></span>
<span data-ttu-id="f4a2e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a2e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a2e-131">-WhatIf</span></span>
<span data-ttu-id="f4a2e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a2e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a2e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a2e-134">CommonParameters</span></span>
<span data-ttu-id="f4a2e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a2e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a2e-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4a2e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a2e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4a2e-137">INPUTS</span></span>

### <span data-ttu-id="f4a2e-138">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4a2e-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f4a2e-139">System. string []</span><span class="sxs-lookup"><span data-stu-id="f4a2e-139">System.String[]</span></span>

## <span data-ttu-id="f4a2e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4a2e-140">OUTPUTS</span></span>

### <span data-ttu-id="f4a2e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4a2e-141">System.Boolean</span></span>

## <span data-ttu-id="f4a2e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4a2e-142">NOTES</span></span>

## <span data-ttu-id="f4a2e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4a2e-143">RELATED LINKS</span></span>

[<span data-ttu-id="f4a2e-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f4a2e-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="f4a2e-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="f4a2e-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="f4a2e-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="f4a2e-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="f4a2e-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="f4a2e-147">Set-AzResource</span></span>](./Set-AzResource.md)


