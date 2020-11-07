---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 2013f1722ee246db023f4d26d456eafffa8f40eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754221"
---
# <span data-ttu-id="14fe9-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="14fe9-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="14fe9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="14fe9-103">Skapar ett steg.</span><span class="sxs-lookup"><span data-stu-id="14fe9-103">Creates a step.</span></span>

## <span data-ttu-id="14fe9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14fe9-104">SYNTAX</span></span>

```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14fe9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14fe9-105">DESCRIPTION</span></span>
<span data-ttu-id="14fe9-106">Cmdleten **New-AzDeploymentManagerStep** skapar ett distributions steg som kan hänvisas till i installations processen.</span><span class="sxs-lookup"><span data-stu-id="14fe9-106">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="14fe9-107">Ange *namn* , *ResourceGroupName* och obligatoriska egenskaper.</span><span class="sxs-lookup"><span data-stu-id="14fe9-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="14fe9-108">Du kan ändra det objekt som returneras lokalt och sedan tillämpa ändringarna på steget genom att använda Set-AzDeploymentManagerStep cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14fe9-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="14fe9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14fe9-109">EXAMPLES</span></span>

### <span data-ttu-id="14fe9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="14fe9-110">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="14fe9-111">Skapar ett steg i ContosoResourceGroup med namnet ContosoService1WaitStep med central till-resursen.</span><span class="sxs-lookup"><span data-stu-id="14fe9-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="14fe9-112">Egenskapen varaktighet anger hur länge installationen ska vänta innan nästa steg körs.</span><span class="sxs-lookup"><span data-stu-id="14fe9-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="14fe9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14fe9-113">PARAMETERS</span></span>

### <span data-ttu-id="14fe9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14fe9-114">-DefaultProfile</span></span>
<span data-ttu-id="14fe9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14fe9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14fe9-116">-Varaktighet</span><span class="sxs-lookup"><span data-stu-id="14fe9-116">-Duration</span></span>
<span data-ttu-id="14fe9-117">Varaktigheten för att vänta i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="14fe9-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="14fe9-118">T. ex.: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="14fe9-118">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="14fe9-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="14fe9-119">-Location</span></span>
<span data-ttu-id="14fe9-120">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="14fe9-120">The location of the resource.</span></span>

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

### <span data-ttu-id="14fe9-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="14fe9-121">-Name</span></span>
<span data-ttu-id="14fe9-122">Namnet på steget.</span><span class="sxs-lookup"><span data-stu-id="14fe9-122">The name of the step.</span></span>

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

### <span data-ttu-id="14fe9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14fe9-123">-ResourceGroupName</span></span>
<span data-ttu-id="14fe9-124">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="14fe9-124">The resource group.</span></span>

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

### <span data-ttu-id="14fe9-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="14fe9-125">-Tag</span></span>
<span data-ttu-id="14fe9-126">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="14fe9-126">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="14fe9-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="14fe9-127">-Confirm</span></span>
<span data-ttu-id="14fe9-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14fe9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14fe9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14fe9-129">-WhatIf</span></span>
<span data-ttu-id="14fe9-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="14fe9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14fe9-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="14fe9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14fe9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14fe9-132">CommonParameters</span></span>
<span data-ttu-id="14fe9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14fe9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14fe9-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14fe9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14fe9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14fe9-135">INPUTS</span></span>

### <span data-ttu-id="14fe9-136">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="14fe9-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="14fe9-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14fe9-137">OUTPUTS</span></span>

### <span data-ttu-id="14fe9-138">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="14fe9-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="14fe9-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14fe9-139">NOTES</span></span>

## <span data-ttu-id="14fe9-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14fe9-140">RELATED LINKS</span></span>
