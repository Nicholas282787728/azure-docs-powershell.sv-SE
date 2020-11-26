---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: c504a839b47fc36863e207f74d9b309309a31fbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258670"
---
# <span data-ttu-id="3813e-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3813e-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="3813e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3813e-102">SYNOPSIS</span></span>
<span data-ttu-id="3813e-103">Tar bort en resurs grupps distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="3813e-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="3813e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3813e-104">SYNTAX</span></span>

### <span data-ttu-id="3813e-105">RemoveByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="3813e-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3813e-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="3813e-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3813e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3813e-107">DESCRIPTION</span></span>

<span data-ttu-id="3813e-108">Cmdleten **Remove-AzResourceGroupDeployment** tar bort en Azure Resource Group-distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="3813e-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="3813e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3813e-109">EXAMPLES</span></span>

### <span data-ttu-id="3813e-110">Exempel 1: tar bort en resurs grupps distribution med ResourceId</span><span class="sxs-lookup"><span data-stu-id="3813e-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="3813e-111">Det här kommandot tar bort en resurs grupps distribution med det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="3813e-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="3813e-112">Lyckade borttagningar returnerar true.</span><span class="sxs-lookup"><span data-stu-id="3813e-112">Successful removal returns true.</span></span>

### <span data-ttu-id="3813e-113">Exempel 2: tar bort en distribution av resurs grupper med ResourceGroupName och ResourceName</span><span class="sxs-lookup"><span data-stu-id="3813e-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="3813e-114">Det här kommandot tar bort en distribution av resurs grupper med angiven ResourceGroupName och ResourceName.</span><span class="sxs-lookup"><span data-stu-id="3813e-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="3813e-115">Lyckade borttagningar returnerar true.</span><span class="sxs-lookup"><span data-stu-id="3813e-115">Successful removal returns true.</span></span>

## <span data-ttu-id="3813e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3813e-116">PARAMETERS</span></span>

### <span data-ttu-id="3813e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3813e-117">-ApiVersion</span></span>
<span data-ttu-id="3813e-118">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="3813e-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3813e-119">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="3813e-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="3813e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3813e-120">-DefaultProfile</span></span>
<span data-ttu-id="3813e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3813e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3813e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="3813e-122">-Id</span></span>
<span data-ttu-id="3813e-123">Anger ID för den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3813e-123">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="3813e-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3813e-124">-Name</span></span>
<span data-ttu-id="3813e-125">Anger namnet på den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3813e-125">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="3813e-126">-För</span><span class="sxs-lookup"><span data-stu-id="3813e-126">-Pre</span></span>
<span data-ttu-id="3813e-127">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3813e-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3813e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3813e-128">-ResourceGroupName</span></span>
<span data-ttu-id="3813e-129">Anger namnet på resurs gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3813e-129">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="3813e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3813e-130">-Confirm</span></span>
<span data-ttu-id="3813e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3813e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3813e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3813e-132">-WhatIf</span></span>
<span data-ttu-id="3813e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3813e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3813e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3813e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3813e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3813e-135">CommonParameters</span></span>
<span data-ttu-id="3813e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3813e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3813e-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3813e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3813e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3813e-138">INPUTS</span></span>

### <span data-ttu-id="3813e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3813e-139">System.String</span></span>

## <span data-ttu-id="3813e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3813e-140">OUTPUTS</span></span>

### <span data-ttu-id="3813e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3813e-141">System.Boolean</span></span>

## <span data-ttu-id="3813e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3813e-142">NOTES</span></span>

## <span data-ttu-id="3813e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3813e-143">RELATED LINKS</span></span>

[<span data-ttu-id="3813e-144">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3813e-144">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="3813e-145">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3813e-145">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="3813e-146">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3813e-146">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="3813e-147">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3813e-147">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)

