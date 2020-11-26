---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273059"
---
# <span data-ttu-id="5c6ab-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5c6ab-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="5c6ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="5c6ab-103">Tar bort en resurs grupps distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="5c6ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c6ab-104">SYNTAX</span></span>

### <span data-ttu-id="5c6ab-105">RemoveByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="5c6ab-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c6ab-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="5c6ab-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c6ab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c6ab-107">DESCRIPTION</span></span>

<span data-ttu-id="5c6ab-108">Cmdleten **Remove-AzResourceGroupDeployment** tar bort en Azure Resource Group-distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="5c6ab-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c6ab-109">EXAMPLES</span></span>

### <span data-ttu-id="5c6ab-110">Exempel 1: tar bort en resurs grupps distribution med ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c6ab-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="5c6ab-111">Det här kommandot tar bort en resurs grupps distribution med det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="5c6ab-112">Lyckade borttagningar returnerar true.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-112">Successful removal returns true.</span></span>

### <span data-ttu-id="5c6ab-113">Exempel 2: tar bort en distribution av resurs grupper med ResourceGroupName och ResourceName</span><span class="sxs-lookup"><span data-stu-id="5c6ab-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="5c6ab-114">Det här kommandot tar bort en distribution av resurs grupper med angiven ResourceGroupName och ResourceName.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="5c6ab-115">Lyckade borttagningar returnerar true.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-115">Successful removal returns true.</span></span>

## <span data-ttu-id="5c6ab-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c6ab-116">PARAMETERS</span></span>

### <span data-ttu-id="5c6ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c6ab-117">-DefaultProfile</span></span>
<span data-ttu-id="5c6ab-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5c6ab-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c6ab-119">-ID</span><span class="sxs-lookup"><span data-stu-id="5c6ab-119">-Id</span></span>
<span data-ttu-id="5c6ab-120">Anger ID för den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-120">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c6ab-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c6ab-121">-Name</span></span>
<span data-ttu-id="5c6ab-122">Anger namnet på den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-122">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c6ab-123">-För</span><span class="sxs-lookup"><span data-stu-id="5c6ab-123">-Pre</span></span>
<span data-ttu-id="5c6ab-124">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5c6ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c6ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c6ab-126">Anger namnet på resurs gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-126">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c6ab-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c6ab-127">-Confirm</span></span>
<span data-ttu-id="5c6ab-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c6ab-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c6ab-129">-WhatIf</span></span>
<span data-ttu-id="5c6ab-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c6ab-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c6ab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c6ab-132">CommonParameters</span></span>
<span data-ttu-id="5c6ab-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c6ab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c6ab-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c6ab-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c6ab-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c6ab-135">INPUTS</span></span>

### <span data-ttu-id="5c6ab-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5c6ab-136">System.String</span></span>

## <span data-ttu-id="5c6ab-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c6ab-137">OUTPUTS</span></span>

### <span data-ttu-id="5c6ab-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c6ab-138">System.Boolean</span></span>

## <span data-ttu-id="5c6ab-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c6ab-139">NOTES</span></span>

## <span data-ttu-id="5c6ab-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c6ab-140">RELATED LINKS</span></span>

[<span data-ttu-id="5c6ab-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5c6ab-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="5c6ab-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5c6ab-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="5c6ab-143">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5c6ab-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="5c6ab-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5c6ab-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)

