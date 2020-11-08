---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092084"
---
# <span data-ttu-id="24e12-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="24e12-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="24e12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24e12-102">SYNOPSIS</span></span>
<span data-ttu-id="24e12-103">Skapa en ny Azure DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="24e12-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="24e12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24e12-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e12-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24e12-105">DESCRIPTION</span></span>
<span data-ttu-id="24e12-106">Skapa en ny Azure DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="24e12-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="24e12-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24e12-107">EXAMPLES</span></span>

### <span data-ttu-id="24e12-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="24e12-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="24e12-109">Skapa en DevSpaces-styrenhet i resourcegroup devSpaceResourceGroup med ett namn devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="24e12-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="24e12-110">Använd klustrets kluster som mål för denna styrenhet.</span><span class="sxs-lookup"><span data-stu-id="24e12-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="24e12-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24e12-111">PARAMETERS</span></span>

### <span data-ttu-id="24e12-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24e12-112">-AsJob</span></span>
<span data-ttu-id="24e12-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="24e12-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24e12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e12-114">-DefaultProfile</span></span>
<span data-ttu-id="24e12-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24e12-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24e12-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="24e12-116">-Name</span></span>
<span data-ttu-id="24e12-117">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="24e12-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e12-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e12-118">-ResourceGroupName</span></span>
<span data-ttu-id="24e12-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="24e12-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e12-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="24e12-120">-Tag</span></span>
<span data-ttu-id="24e12-121">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="24e12-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="24e12-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="24e12-122">-TargetClusterName</span></span>
<span data-ttu-id="24e12-123">Mål kluster namn.</span><span class="sxs-lookup"><span data-stu-id="24e12-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e12-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e12-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="24e12-125">Mål resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="24e12-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e12-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24e12-126">-Confirm</span></span>
<span data-ttu-id="24e12-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24e12-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e12-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e12-128">-WhatIf</span></span>
<span data-ttu-id="24e12-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24e12-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24e12-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24e12-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e12-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e12-131">CommonParameters</span></span>
<span data-ttu-id="24e12-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e12-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e12-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24e12-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e12-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24e12-134">INPUTS</span></span>

### <span data-ttu-id="24e12-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="24e12-135">None</span></span>

## <span data-ttu-id="24e12-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24e12-136">OUTPUTS</span></span>

### <span data-ttu-id="24e12-137">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="24e12-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="24e12-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24e12-138">NOTES</span></span>

## <span data-ttu-id="24e12-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24e12-139">RELATED LINKS</span></span>
