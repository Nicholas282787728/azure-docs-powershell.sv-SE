---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7b04fc95af1ee340e87fa5ed46cbba9f1956d9e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571432"
---
# <span data-ttu-id="c0288-101">New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="c0288-101">New-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="c0288-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0288-102">SYNOPSIS</span></span>
<span data-ttu-id="c0288-103">Skapar ett nytt distributions steg.</span><span class="sxs-lookup"><span data-stu-id="c0288-103">Creates a new deployment step.</span></span>

## <span data-ttu-id="c0288-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0288-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -Duration <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0288-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0288-105">DESCRIPTION</span></span>
<span data-ttu-id="c0288-106">Cmdleten **New-AzureRmDeploymentManagerStep** skapar ett distributions steg som kan hänvisas till i installations processen.</span><span class="sxs-lookup"><span data-stu-id="c0288-106">The **New-AzureRmDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="c0288-107">Ange *namn* , *ResourceGroupName* och obligatoriska egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c0288-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="c0288-108">Du kan ändra det objekt som returneras lokalt och sedan tillämpa ändringarna på steget genom att använda Set-AzureRmDeploymentManagerStep cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0288-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="c0288-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0288-109">EXAMPLES</span></span>

### <span data-ttu-id="c0288-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0288-110">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="c0288-111">Skapar ett steg i ContosoResourceGroup med namnet ContosoService1WaitStep med central till-resursen.</span><span class="sxs-lookup"><span data-stu-id="c0288-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="c0288-112">Egenskapen varaktighet anger hur länge installationen ska vänta innan nästa steg körs.</span><span class="sxs-lookup"><span data-stu-id="c0288-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="c0288-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0288-113">PARAMETERS</span></span>

### <span data-ttu-id="c0288-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0288-114">-DefaultProfile</span></span>
<span data-ttu-id="c0288-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0288-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0288-116">-Varaktighet</span><span class="sxs-lookup"><span data-stu-id="c0288-116">-Duration</span></span>
<span data-ttu-id="c0288-117">Varaktigheten för att vänta i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="c0288-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="c0288-118">T. ex.: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="c0288-118">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="c0288-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="c0288-119">-Location</span></span>
<span data-ttu-id="c0288-120">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="c0288-120">The location of the resource.</span></span>

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

### <span data-ttu-id="c0288-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0288-121">-Name</span></span>
<span data-ttu-id="c0288-122">Namnet på steget.</span><span class="sxs-lookup"><span data-stu-id="c0288-122">The name of the step.</span></span>

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

### <span data-ttu-id="c0288-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0288-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0288-124">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c0288-124">The resource group.</span></span>

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

### <span data-ttu-id="c0288-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c0288-125">-Tag</span></span>
<span data-ttu-id="c0288-126">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="c0288-126">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0288-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0288-127">-Confirm</span></span>
<span data-ttu-id="c0288-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0288-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0288-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0288-129">-WhatIf</span></span>
<span data-ttu-id="c0288-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0288-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0288-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0288-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0288-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0288-132">CommonParameters</span></span>
<span data-ttu-id="c0288-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0288-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c0288-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0288-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0288-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0288-135">INPUTS</span></span>

### <span data-ttu-id="c0288-136">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="c0288-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c0288-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0288-137">OUTPUTS</span></span>

### <span data-ttu-id="c0288-138">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="c0288-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="c0288-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0288-139">NOTES</span></span>

## <span data-ttu-id="c0288-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0288-140">RELATED LINKS</span></span>
