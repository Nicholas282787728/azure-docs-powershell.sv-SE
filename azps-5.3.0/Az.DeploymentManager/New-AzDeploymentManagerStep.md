---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522730"
---
# <span data-ttu-id="cbfc6-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="cbfc6-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="cbfc6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbfc6-102">SYNOPSIS</span></span>
<span data-ttu-id="cbfc6-103">Skapar ett steg.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-103">Creates a step.</span></span>

## <span data-ttu-id="cbfc6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbfc6-104">SYNTAX</span></span>

### <span data-ttu-id="cbfc6-105">Vänta (standard)</span><span class="sxs-lookup"><span data-stu-id="cbfc6-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbfc6-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="cbfc6-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbfc6-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="cbfc6-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbfc6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbfc6-108">DESCRIPTION</span></span>
<span data-ttu-id="cbfc6-109">Cmdleten **New-AzDeploymentManagerStep** skapar ett distributions steg som kan hänvisas till i installations processen.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="cbfc6-110">Ange *namn*, *ResourceGroupName* och obligatoriska egenskaper.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="cbfc6-111">Du kan ändra det objekt som returneras lokalt och sedan tillämpa ändringarna på steget genom att använda Set-AzDeploymentManagerStep cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="cbfc6-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbfc6-112">EXAMPLES</span></span>

### <span data-ttu-id="cbfc6-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cbfc6-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="cbfc6-114">Skapar ett steg i ContosoResourceGroup med namnet ContosoService1WaitStep med central till-resursen.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="cbfc6-115">Egenskapen varaktighet anger hur länge installationen ska vänta innan nästa steg körs.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="cbfc6-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbfc6-116">PARAMETERS</span></span>

### <span data-ttu-id="cbfc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbfc6-117">-DefaultProfile</span></span>
<span data-ttu-id="cbfc6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbfc6-119">-Varaktighet</span><span class="sxs-lookup"><span data-stu-id="cbfc6-119">-Duration</span></span>
<span data-ttu-id="cbfc6-120">Varaktigheten för att vänta i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="cbfc6-121">T. ex.: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="cbfc6-121">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="cbfc6-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="cbfc6-122">-HealthCheckProperties</span></span>
<span data-ttu-id="cbfc6-123">Egenskaper för hälso kontroll.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-123">The health check properties.</span></span>

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

### <span data-ttu-id="cbfc6-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="cbfc6-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="cbfc6-125">Sökvägen till filen där egenskaper för hälso kontroll har definierats.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-125">The path to the file where health check properties are defined.</span></span>

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

### <span data-ttu-id="cbfc6-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="cbfc6-126">-Location</span></span>
<span data-ttu-id="cbfc6-127">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-127">The location of the resource.</span></span>

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

### <span data-ttu-id="cbfc6-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbfc6-128">-Name</span></span>
<span data-ttu-id="cbfc6-129">Namnet på steget.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-129">The name of the step.</span></span>

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

### <span data-ttu-id="cbfc6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbfc6-130">-ResourceGroupName</span></span>
<span data-ttu-id="cbfc6-131">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-131">The resource group.</span></span>

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

### <span data-ttu-id="cbfc6-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cbfc6-132">-Tag</span></span>
<span data-ttu-id="cbfc6-133">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="cbfc6-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbfc6-134">-Confirm</span></span>
<span data-ttu-id="cbfc6-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbfc6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbfc6-136">-WhatIf</span></span>
<span data-ttu-id="cbfc6-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbfc6-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbfc6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbfc6-139">CommonParameters</span></span>
<span data-ttu-id="cbfc6-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbfc6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbfc6-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbfc6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbfc6-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbfc6-142">INPUTS</span></span>

### <span data-ttu-id="cbfc6-143">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="cbfc6-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cbfc6-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbfc6-144">OUTPUTS</span></span>

### <span data-ttu-id="cbfc6-145">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="cbfc6-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="cbfc6-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbfc6-146">NOTES</span></span>

## <span data-ttu-id="cbfc6-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbfc6-147">RELATED LINKS</span></span>
