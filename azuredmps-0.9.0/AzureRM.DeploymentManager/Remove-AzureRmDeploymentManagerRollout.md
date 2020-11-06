---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: f329468dce9c520eb647bb0d927ba91de64a5c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571427"
---
# <span data-ttu-id="af9a5-101">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="af9a5-101">Remove-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="af9a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="af9a5-103">Tar bort en installation.</span><span class="sxs-lookup"><span data-stu-id="af9a5-103">Deletes a rollout.</span></span>

## <span data-ttu-id="af9a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af9a5-104">SYNTAX</span></span>

### <span data-ttu-id="af9a5-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="af9a5-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9a5-106">ID</span><span class="sxs-lookup"><span data-stu-id="af9a5-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9a5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="af9a5-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af9a5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af9a5-108">DESCRIPTION</span></span>
<span data-ttu-id="af9a5-109">Cmdleten **Remove-AzureRmDeploymentManagerRollout** tar bort en installation i ett Terminal-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="af9a5-109">The **Remove-AzureRmDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="af9a5-110">Ange utgivningen med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="af9a5-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="af9a5-111">Du kan också ange ett installations objekt eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="af9a5-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="af9a5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af9a5-112">EXAMPLES</span></span>

### <span data-ttu-id="af9a5-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="af9a5-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="af9a5-114">Det här kommandot tar bort en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="af9a5-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="af9a5-115">Exempel 2: ta bort en lansering med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="af9a5-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="af9a5-116">Det här kommandot tar bort en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="af9a5-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="af9a5-117">Exempel 3: ta bort en lansering med hjälp av installations objekt.</span><span class="sxs-lookup"><span data-stu-id="af9a5-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="af9a5-118">Det här kommandot tar bort en installation vars namn och ResourceGroup matchar $rolloutObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="af9a5-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="af9a5-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af9a5-119">PARAMETERS</span></span>

### <span data-ttu-id="af9a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9a5-120">-DefaultProfile</span></span>
<span data-ttu-id="af9a5-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af9a5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9a5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="af9a5-122">-Force</span></span>
<span data-ttu-id="af9a5-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="af9a5-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="af9a5-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="af9a5-124">-Name</span></span>
<span data-ttu-id="af9a5-125">Namnet på installationen.</span><span class="sxs-lookup"><span data-stu-id="af9a5-125">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af9a5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af9a5-126">-PassThru</span></span>
<span data-ttu-id="af9a5-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="af9a5-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="af9a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="af9a5-129">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="af9a5-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af9a5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af9a5-130">-ResourceId</span></span>
<span data-ttu-id="af9a5-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="af9a5-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af9a5-132">-Lansering</span><span class="sxs-lookup"><span data-stu-id="af9a5-132">-Rollout</span></span>
<span data-ttu-id="af9a5-133">Resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="af9a5-133">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af9a5-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af9a5-134">-Confirm</span></span>
<span data-ttu-id="af9a5-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af9a5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af9a5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9a5-136">-WhatIf</span></span>
<span data-ttu-id="af9a5-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af9a5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af9a5-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af9a5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af9a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9a5-139">CommonParameters</span></span>
<span data-ttu-id="af9a5-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9a5-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af9a5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9a5-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af9a5-142">INPUTS</span></span>

### <span data-ttu-id="af9a5-143">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="af9a5-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="af9a5-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af9a5-144">OUTPUTS</span></span>

### <span data-ttu-id="af9a5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af9a5-145">System.Boolean</span></span>

## <span data-ttu-id="af9a5-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af9a5-146">NOTES</span></span>

## <span data-ttu-id="af9a5-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af9a5-147">RELATED LINKS</span></span>

[<span data-ttu-id="af9a5-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="af9a5-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="af9a5-149">Stopp-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="af9a5-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="af9a5-150">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="af9a5-150">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)