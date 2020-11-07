---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4a40b3fd0045a48d6a69c76970b3835ef2d685c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756559"
---
# <span data-ttu-id="0f8dd-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0f8dd-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="0f8dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f8dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0f8dd-103">Flyttar en resurs till en annan resurs grupp eller prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f8dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f8dd-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f8dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f8dd-105">DESCRIPTION</span></span>
<span data-ttu-id="0f8dd-106">Cmdleten **Move-AzureRmResource** flyttar befintliga resurser till en annan resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="0f8dd-107">Resurs gruppen kan vara i ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="0f8dd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f8dd-108">EXAMPLES</span></span>

### <span data-ttu-id="0f8dd-109">Exempel 1: flytta en resurs till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="0f8dd-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="0f8dd-110">Det första kommandot får en resurs som heter ContosoStorageAccount med hjälp av Get-AzureRmResource cmdlet och lagrar sedan resursen i $Resource-variabeln.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="0f8dd-111">Det andra kommandot flyttar resursen till resurs gruppen med namnet ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="0f8dd-112">Kommandot identifierar den resurs som ska flyttas genom att använda egenskapen **ResourceID** för $Resource.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="0f8dd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f8dd-113">PARAMETERS</span></span>

### <span data-ttu-id="0f8dd-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0f8dd-114">-ApiVersion</span></span>
<span data-ttu-id="0f8dd-115">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0f8dd-116">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0f8dd-117">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f8dd-117">-DestinationResourceGroupName</span></span>
<span data-ttu-id="0f8dd-118">Anger namnet på den resurs grupp där cmdleten flyttas till resurserna.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-118">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="0f8dd-119">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f8dd-119">-DestinationSubscriptionId</span></span>
<span data-ttu-id="0f8dd-120">Anger ID för den prenumeration som den här cmdleten flyttar resurser till.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-120">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="0f8dd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0f8dd-121">-Force</span></span>
<span data-ttu-id="0f8dd-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f8dd-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0f8dd-123">-InformationAction</span></span>
<span data-ttu-id="0f8dd-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0f8dd-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0f8dd-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f8dd-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="0f8dd-126">Continue</span></span>
- <span data-ttu-id="0f8dd-127">Över</span><span class="sxs-lookup"><span data-stu-id="0f8dd-127">Ignore</span></span>
- <span data-ttu-id="0f8dd-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="0f8dd-128">Inquire</span></span>
- <span data-ttu-id="0f8dd-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0f8dd-129">SilentlyContinue</span></span>
- <span data-ttu-id="0f8dd-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="0f8dd-130">Stop</span></span>
- <span data-ttu-id="0f8dd-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="0f8dd-131">Suspend</span></span>

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

### <span data-ttu-id="0f8dd-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0f8dd-132">-InformationVariable</span></span>
<span data-ttu-id="0f8dd-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0f8dd-134">-För</span><span class="sxs-lookup"><span data-stu-id="0f8dd-134">-Pre</span></span>
<span data-ttu-id="0f8dd-135">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0f8dd-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f8dd-136">-ResourceId</span></span>
<span data-ttu-id="0f8dd-137">Anger en matris med ID: n för de resurser som den här cmdleten flyttar.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-137">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="0f8dd-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f8dd-138">-Confirm</span></span>
<span data-ttu-id="0f8dd-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f8dd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f8dd-140">-WhatIf</span></span>
<span data-ttu-id="0f8dd-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f8dd-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f8dd-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8dd-143">-DefaultProfile</span></span>
<span data-ttu-id="0f8dd-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f8dd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8dd-145">CommonParameters</span></span>
<span data-ttu-id="0f8dd-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f8dd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8dd-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f8dd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8dd-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f8dd-148">INPUTS</span></span>

### <span data-ttu-id="0f8dd-149">String []</span><span class="sxs-lookup"><span data-stu-id="0f8dd-149">String[]</span></span>
<span data-ttu-id="0f8dd-150">Parametern ' ResourceId ' godkänner värdet för typen ' string [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0f8dd-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="0f8dd-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f8dd-151">OUTPUTS</span></span>

### <span data-ttu-id="0f8dd-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f8dd-152">System.Boolean</span></span>

## <span data-ttu-id="0f8dd-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f8dd-153">NOTES</span></span>

## <span data-ttu-id="0f8dd-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f8dd-154">RELATED LINKS</span></span>

[<span data-ttu-id="0f8dd-155">Sök-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0f8dd-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="0f8dd-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0f8dd-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="0f8dd-157">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0f8dd-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="0f8dd-158">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0f8dd-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="0f8dd-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0f8dd-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


