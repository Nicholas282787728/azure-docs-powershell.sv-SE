---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261355"
---
# <span data-ttu-id="5118f-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="5118f-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="5118f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5118f-102">SYNOPSIS</span></span>
<span data-ttu-id="5118f-103">Skapa en ny Azure DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="5118f-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="5118f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5118f-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5118f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5118f-105">DESCRIPTION</span></span>
<span data-ttu-id="5118f-106">Skapa en ny Azure DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="5118f-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="5118f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5118f-107">EXAMPLES</span></span>

### <span data-ttu-id="5118f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5118f-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="5118f-109">Skapa en DevSpaces-styrenhet i resourcegroup devSpaceResourceGroup med ett namn devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="5118f-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="5118f-110">Använd klustrets kluster som mål för denna styrenhet.</span><span class="sxs-lookup"><span data-stu-id="5118f-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="5118f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5118f-111">PARAMETERS</span></span>

### <span data-ttu-id="5118f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5118f-112">-AsJob</span></span>
<span data-ttu-id="5118f-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5118f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5118f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5118f-114">-DefaultProfile</span></span>
<span data-ttu-id="5118f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5118f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5118f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5118f-116">-Name</span></span>
<span data-ttu-id="5118f-117">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="5118f-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="5118f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5118f-118">-ResourceGroupName</span></span>
<span data-ttu-id="5118f-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5118f-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="5118f-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5118f-120">-Tag</span></span>
<span data-ttu-id="5118f-121">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="5118f-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="5118f-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="5118f-122">-TargetClusterName</span></span>
<span data-ttu-id="5118f-123">Mål kluster namn.</span><span class="sxs-lookup"><span data-stu-id="5118f-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="5118f-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5118f-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="5118f-125">Mål resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5118f-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="5118f-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5118f-126">-Confirm</span></span>
<span data-ttu-id="5118f-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5118f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5118f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5118f-128">-WhatIf</span></span>
<span data-ttu-id="5118f-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5118f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5118f-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5118f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5118f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5118f-131">CommonParameters</span></span>
<span data-ttu-id="5118f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5118f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5118f-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5118f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5118f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5118f-134">INPUTS</span></span>

### <span data-ttu-id="5118f-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="5118f-135">None</span></span>

## <span data-ttu-id="5118f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5118f-136">OUTPUTS</span></span>

### <span data-ttu-id="5118f-137">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="5118f-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="5118f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5118f-138">NOTES</span></span>

## <span data-ttu-id="5118f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5118f-139">RELATED LINKS</span></span>
