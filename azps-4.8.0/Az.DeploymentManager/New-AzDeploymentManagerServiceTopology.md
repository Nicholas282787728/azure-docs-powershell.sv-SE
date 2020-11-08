---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101038"
---
# <span data-ttu-id="1a066-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1a066-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="1a066-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a066-102">SYNOPSIS</span></span>
<span data-ttu-id="1a066-103">Skapar en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="1a066-103">Creates a service topology.</span></span>

## <span data-ttu-id="1a066-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a066-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a066-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a066-105">DESCRIPTION</span></span>
<span data-ttu-id="1a066-106">Cmdleten **New-AzDeploymentManagerServiceTopology** skapar en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="1a066-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="1a066-107">Du kan ändra det returnerade ServiceTopology-objektet lokalt och sedan tillämpa ändringarna på topologin med hjälp av Set-AzDeploymentManagerServiceTopology cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a066-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="1a066-108">Det returnerade objektet</span><span class="sxs-lookup"><span data-stu-id="1a066-108">The returned object</span></span> 

<span data-ttu-id="1a066-109">Det returnerade objektet har ett ResourceId-fält som kan refereras i en installations resurs för att indikera att tjänsterna som deklareras i denna tjänst topologi distribueras i installationen.</span><span class="sxs-lookup"><span data-stu-id="1a066-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="1a066-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a066-110">EXAMPLES</span></span>

### <span data-ttu-id="1a066-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1a066-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="1a066-112">Denna cmdlet skapar en ny tjänst sto pol Ogin i resurs gruppen ContosoResourceGroup med namnet ContosoServiceTopology och i plats centralt.</span><span class="sxs-lookup"><span data-stu-id="1a066-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="1a066-113">Resurs källan ResourceId visar att artefakter som krävs för definitioner av tjänst enheter i denna topologi måste läsas från den angivna artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="1a066-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="1a066-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1a066-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="1a066-115">Denna cmdlet skapar en ny tjänst sto pol Ogin i resurs gruppen ContosoResourceGroup med namnet ContosoServiceTopology och i plats centralt.</span><span class="sxs-lookup"><span data-stu-id="1a066-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="1a066-116">Frånvaron av en referens till en artefakt källa visar att artefakterna som behövs för definitioner av tjänst enheter i denna topologi skulle tillhandahållas som absoluta SAS URI: er i tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="1a066-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="1a066-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a066-117">PARAMETERS</span></span>

### <span data-ttu-id="1a066-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="1a066-118">-ArtifactSourceId</span></span>
<span data-ttu-id="1a066-119">ID för artefakt källan där artefakterna som utgör topologin lagras.</span><span class="sxs-lookup"><span data-stu-id="1a066-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="1a066-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a066-120">-DefaultProfile</span></span>
<span data-ttu-id="1a066-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a066-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a066-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="1a066-122">-Location</span></span>
<span data-ttu-id="1a066-123">Topologins plats.</span><span class="sxs-lookup"><span data-stu-id="1a066-123">The location of the topology.</span></span>

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

### <span data-ttu-id="1a066-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a066-124">-Name</span></span>
<span data-ttu-id="1a066-125">Namnet på topologin.</span><span class="sxs-lookup"><span data-stu-id="1a066-125">The name of the topology.</span></span>

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

### <span data-ttu-id="1a066-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a066-126">-ResourceGroupName</span></span>
<span data-ttu-id="1a066-127">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1a066-127">The resource group.</span></span>

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

### <span data-ttu-id="1a066-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1a066-128">-Tag</span></span>
<span data-ttu-id="1a066-129">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="1a066-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="1a066-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1a066-130">-Confirm</span></span>
<span data-ttu-id="1a066-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1a066-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a066-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a066-132">-WhatIf</span></span>
<span data-ttu-id="1a066-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1a066-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a066-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1a066-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a066-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a066-135">CommonParameters</span></span>
<span data-ttu-id="1a066-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a066-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a066-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a066-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a066-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a066-138">INPUTS</span></span>

### <span data-ttu-id="1a066-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1a066-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1a066-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a066-140">OUTPUTS</span></span>

### <span data-ttu-id="1a066-141">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="1a066-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="1a066-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a066-142">NOTES</span></span>

## <span data-ttu-id="1a066-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a066-143">RELATED LINKS</span></span>
