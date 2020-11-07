---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/new-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/New-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/New-AzureRmDevSpacesController.md
ms.openlocfilehash: 13fea6a0f7c7fda06e171538c92fe52db969fe36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756180"
---
# <span data-ttu-id="b629d-101">New-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="b629d-101">New-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="b629d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b629d-102">SYNOPSIS</span></span>
<span data-ttu-id="b629d-103">Skapa en ny Azure DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="b629d-103">Create a new Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b629d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b629d-104">SYNTAX</span></span>

```
New-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-TargetResourceGroupName] <String> [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b629d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b629d-105">DESCRIPTION</span></span>
<span data-ttu-id="b629d-106">Skapa en ny Azure DevSpaces-styrenhet.</span><span class="sxs-lookup"><span data-stu-id="b629d-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="b629d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b629d-107">EXAMPLES</span></span>

### <span data-ttu-id="b629d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b629d-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="b629d-109">Crreate en DevSpaces-styrenhet i resourcegroup devSpaceResourceGroup med ett namn devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="b629d-109">Crreate a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="b629d-110">Använd klustrets kluster som mål för denna styrenhet.</span><span class="sxs-lookup"><span data-stu-id="b629d-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="b629d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b629d-111">PARAMETERS</span></span>

### <span data-ttu-id="b629d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b629d-112">-AsJob</span></span>
<span data-ttu-id="b629d-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b629d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b629d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b629d-114">-DefaultProfile</span></span>
<span data-ttu-id="b629d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b629d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b629d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b629d-116">-Name</span></span>
<span data-ttu-id="b629d-117">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="b629d-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="b629d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b629d-118">-ResourceGroupName</span></span>
<span data-ttu-id="b629d-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b629d-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="b629d-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b629d-120">-Tag</span></span>
<span data-ttu-id="b629d-121">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="b629d-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b629d-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="b629d-122">-TargetClusterName</span></span>
<span data-ttu-id="b629d-123">Mål kluster namn.</span><span class="sxs-lookup"><span data-stu-id="b629d-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="b629d-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b629d-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="b629d-125">Mål resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b629d-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="b629d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b629d-126">-Confirm</span></span>
<span data-ttu-id="b629d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b629d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b629d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b629d-128">-WhatIf</span></span>
<span data-ttu-id="b629d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b629d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b629d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b629d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b629d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b629d-131">CommonParameters</span></span>
<span data-ttu-id="b629d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b629d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b629d-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b629d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b629d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b629d-134">INPUTS</span></span>

### <span data-ttu-id="b629d-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="b629d-135">None</span></span>

## <span data-ttu-id="b629d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b629d-136">OUTPUTS</span></span>

### <span data-ttu-id="b629d-137">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="b629d-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="b629d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b629d-138">NOTES</span></span>

## <span data-ttu-id="b629d-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b629d-139">RELATED LINKS</span></span>
