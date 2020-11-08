---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092129"
---
# <span data-ttu-id="f183e-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f183e-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f183e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f183e-102">SYNOPSIS</span></span>
<span data-ttu-id="f183e-103">Skapar ett steg.</span><span class="sxs-lookup"><span data-stu-id="f183e-103">Creates a step.</span></span>

## <span data-ttu-id="f183e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f183e-104">SYNTAX</span></span>

### <span data-ttu-id="f183e-105">Vänta (standard)</span><span class="sxs-lookup"><span data-stu-id="f183e-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f183e-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="f183e-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f183e-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="f183e-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f183e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f183e-108">DESCRIPTION</span></span>
<span data-ttu-id="f183e-109">Cmdleten **New-AzDeploymentManagerStep** skapar ett distributions steg som kan hänvisas till i installations processen.</span><span class="sxs-lookup"><span data-stu-id="f183e-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="f183e-110">Ange *namn* , *ResourceGroupName* och obligatoriska egenskaper.</span><span class="sxs-lookup"><span data-stu-id="f183e-110">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="f183e-111">Du kan ändra det objekt som returneras lokalt och sedan tillämpa ändringarna på steget genom att använda Set-AzDeploymentManagerStep cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f183e-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="f183e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f183e-112">EXAMPLES</span></span>

### <span data-ttu-id="f183e-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f183e-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="f183e-114">Skapar ett steg i ContosoResourceGroup med namnet ContosoService1WaitStep med central till-resursen.</span><span class="sxs-lookup"><span data-stu-id="f183e-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="f183e-115">Egenskapen varaktighet anger hur länge installationen ska vänta innan nästa steg körs.</span><span class="sxs-lookup"><span data-stu-id="f183e-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="f183e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f183e-116">PARAMETERS</span></span>

### <span data-ttu-id="f183e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f183e-117">-DefaultProfile</span></span>
<span data-ttu-id="f183e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f183e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f183e-119">-Varaktighet</span><span class="sxs-lookup"><span data-stu-id="f183e-119">-Duration</span></span>
<span data-ttu-id="f183e-120">Varaktigheten för att vänta i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="f183e-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="f183e-121">T. ex.: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="f183e-121">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: Wait
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="f183e-122">-HealthCheckProperties</span></span>
<span data-ttu-id="f183e-123">Egenskaper för hälso kontroll.</span><span class="sxs-lookup"><span data-stu-id="f183e-123">The health check properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSHealthCheckStepProperties
Parameter Sets: HealthCheckObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="f183e-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="f183e-125">Sökvägen till filen där egenskaper för hälso kontroll har definierats.</span><span class="sxs-lookup"><span data-stu-id="f183e-125">The path to the file where health check properties are defined.</span></span>

```yaml
Type: System.String
Parameter Sets: HealthCheckFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="f183e-126">-Location</span></span>
<span data-ttu-id="f183e-127">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="f183e-127">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="f183e-128">-Name</span></span>
<span data-ttu-id="f183e-129">Namnet på steget.</span><span class="sxs-lookup"><span data-stu-id="f183e-129">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f183e-130">-ResourceGroupName</span></span>
<span data-ttu-id="f183e-131">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f183e-131">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f183e-132">-Tag</span></span>
<span data-ttu-id="f183e-133">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="f183e-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f183e-134">-Confirm</span></span>
<span data-ttu-id="f183e-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f183e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f183e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f183e-136">-WhatIf</span></span>
<span data-ttu-id="f183e-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f183e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f183e-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f183e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f183e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f183e-139">CommonParameters</span></span>
<span data-ttu-id="f183e-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f183e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f183e-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f183e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f183e-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f183e-142">INPUTS</span></span>

### <span data-ttu-id="f183e-143">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f183e-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f183e-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f183e-144">OUTPUTS</span></span>

### <span data-ttu-id="f183e-145">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f183e-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f183e-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f183e-146">NOTES</span></span>

## <span data-ttu-id="f183e-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f183e-147">RELATED LINKS</span></span>
