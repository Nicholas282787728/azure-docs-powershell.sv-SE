---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 0429eebf0425a950bcf093d7659a2d87b3b661f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744349"
---
# <span data-ttu-id="d4658-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="d4658-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="d4658-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4658-102">SYNOPSIS</span></span>
<span data-ttu-id="d4658-103">Skapa en ny Azure DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="d4658-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="d4658-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4658-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4658-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4658-105">DESCRIPTION</span></span>
<span data-ttu-id="d4658-106">Skapa en ny Azure DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="d4658-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="d4658-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4658-107">EXAMPLES</span></span>

### <span data-ttu-id="d4658-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d4658-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="d4658-109">Skapa en DevSpaces-styrenhet i resourcegroup devSpaceResourceGroup med ett namn devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="d4658-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="d4658-110">Använd klustrets kluster som mål för denna styrenhet.</span><span class="sxs-lookup"><span data-stu-id="d4658-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="d4658-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4658-111">PARAMETERS</span></span>

### <span data-ttu-id="d4658-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4658-112">-AsJob</span></span>
<span data-ttu-id="d4658-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d4658-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4658-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4658-114">-DefaultProfile</span></span>
<span data-ttu-id="d4658-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4658-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4658-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4658-116">-Name</span></span>
<span data-ttu-id="d4658-117">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="d4658-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="d4658-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4658-118">-ResourceGroupName</span></span>
<span data-ttu-id="d4658-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d4658-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="d4658-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d4658-120">-Tag</span></span>
<span data-ttu-id="d4658-121">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="d4658-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="d4658-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="d4658-122">-TargetClusterName</span></span>
<span data-ttu-id="d4658-123">Mål kluster namn.</span><span class="sxs-lookup"><span data-stu-id="d4658-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="d4658-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4658-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="d4658-125">Mål resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d4658-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="d4658-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4658-126">-Confirm</span></span>
<span data-ttu-id="d4658-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4658-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4658-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4658-128">-WhatIf</span></span>
<span data-ttu-id="d4658-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4658-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4658-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4658-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4658-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4658-131">CommonParameters</span></span>
<span data-ttu-id="d4658-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4658-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4658-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4658-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4658-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4658-134">INPUTS</span></span>

### <span data-ttu-id="d4658-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="d4658-135">None</span></span>

## <span data-ttu-id="d4658-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4658-136">OUTPUTS</span></span>

### <span data-ttu-id="d4658-137">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="d4658-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="d4658-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4658-138">NOTES</span></span>

## <span data-ttu-id="d4658-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4658-139">RELATED LINKS</span></span>
