---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523638"
---
# <span data-ttu-id="9c358-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="9c358-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="9c358-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c358-102">SYNOPSIS</span></span>
<span data-ttu-id="9c358-103">Ta bort WAF policy</span><span class="sxs-lookup"><span data-stu-id="9c358-103">Remove WAF policy</span></span>

## <span data-ttu-id="9c358-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c358-104">SYNTAX</span></span>

### <span data-ttu-id="9c358-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9c358-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c358-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c358-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c358-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c358-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c358-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c358-108">DESCRIPTION</span></span>
<span data-ttu-id="9c358-109">Cmdleten **Remove-AzFrontDoorWafPolicy** tar bort en WAF-princip under den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="9c358-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="9c358-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c358-110">EXAMPLES</span></span>

### <span data-ttu-id="9c358-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9c358-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="9c358-112">Ta bort WAF policy $policyName i $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9c358-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="9c358-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9c358-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="9c358-114">Ta bort alla WAF-principer i $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9c358-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="9c358-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c358-115">PARAMETERS</span></span>

### <span data-ttu-id="9c358-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c358-116">-DefaultProfile</span></span>
<span data-ttu-id="9c358-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c358-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c358-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c358-118">-InputObject</span></span>
<span data-ttu-id="9c358-119">WAF princip objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9c358-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c358-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c358-120">-Name</span></span>
<span data-ttu-id="9c358-121">Namnet på den WAF-princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9c358-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c358-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c358-122">-PassThru</span></span>
<span data-ttu-id="9c358-123">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="9c358-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="9c358-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c358-124">-ResourceGroupName</span></span>
<span data-ttu-id="9c358-125">Resurs gruppen som WAF policy tillhör.</span><span class="sxs-lookup"><span data-stu-id="9c358-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c358-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c358-126">-ResourceId</span></span>
<span data-ttu-id="9c358-127">Resurs-ID för WAF princip som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="9c358-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c358-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9c358-128">-Confirm</span></span>
<span data-ttu-id="9c358-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9c358-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c358-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c358-130">-WhatIf</span></span>
<span data-ttu-id="9c358-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9c358-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c358-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9c358-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c358-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c358-133">CommonParameters</span></span>
<span data-ttu-id="9c358-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c358-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c358-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c358-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c358-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c358-136">INPUTS</span></span>

### <span data-ttu-id="9c358-137">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9c358-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="9c358-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9c358-138">System.String</span></span>

## <span data-ttu-id="9c358-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c358-139">OUTPUTS</span></span>

### <span data-ttu-id="9c358-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c358-140">System.Boolean</span></span>

## <span data-ttu-id="9c358-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c358-141">NOTES</span></span>

## <span data-ttu-id="9c358-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c358-142">RELATED LINKS</span></span>

<span data-ttu-id="9c358-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="9c358-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
