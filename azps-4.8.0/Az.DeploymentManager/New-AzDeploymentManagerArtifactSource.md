---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: dcd8d4164d091564aef3d3802430ab499eac38ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260535"
---
# <span data-ttu-id="d1a3e-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d1a3e-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="d1a3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a3e-103">Skapar en artefakt källa.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-103">Creates an artifact source.</span></span>

## <span data-ttu-id="d1a3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1a3e-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1a3e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1a3e-105">DESCRIPTION</span></span>
<span data-ttu-id="d1a3e-106">Cmdleten **New-AzDeploymentManagerArtifactSource** skapar en artefakt källa.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="d1a3e-107">Ange *namn* , *ResourceGroupName* och obligatoriska egenskaper.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="d1a3e-108">Du kan ändra det objekt som returneras lokalt och sedan tillämpa ändringarna på artefakt källan med hjälp av Set-AzDeploymentManagerArtifactSource cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="d1a3e-109">Cmdleten returnerar ett ArtifactSource-objekt som har en ResourceId som kan refereras till i New-AzDeploymentManagerServiceTopology-cmdleten så att artefakter som behövs för en ServiceUnit-resurs, mall-och mallparametrar kan refereras från den här platsen.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="d1a3e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1a3e-110">EXAMPLES</span></span>

### <span data-ttu-id="d1a3e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d1a3e-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="d1a3e-112">Skapar en artefakt källa i ContosoResourceGroup med namnet ContosoArtifactSource med central oss som resursens plats.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="d1a3e-113">Egenskapen SasUri tillhandahåller en Azure Storage SAS URI till lagrings behållaren där artefakterna lagras.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="d1a3e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1a3e-114">PARAMETERS</span></span>

### <span data-ttu-id="d1a3e-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="d1a3e-115">-ArtifactRoot</span></span>
<span data-ttu-id="d1a3e-116">Valfri katalog förskjutning under lagrings behållaren för artefakterna.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="d1a3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a3e-117">-DefaultProfile</span></span>
<span data-ttu-id="d1a3e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1a3e-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="d1a3e-119">-Location</span></span>
<span data-ttu-id="d1a3e-120">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-120">The location of the resource.</span></span>

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

### <span data-ttu-id="d1a3e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1a3e-121">-Name</span></span>
<span data-ttu-id="d1a3e-122">Namnet på artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="d1a3e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a3e-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1a3e-124">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-124">The resource group.</span></span>

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

### <span data-ttu-id="d1a3e-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="d1a3e-125">-SasUri</span></span>
<span data-ttu-id="d1a3e-126">SAS URI till den Azure Storage-behållare där artefakterna lagras.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="d1a3e-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d1a3e-127">-Tag</span></span>
<span data-ttu-id="d1a3e-128">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="d1a3e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1a3e-129">-Confirm</span></span>
<span data-ttu-id="d1a3e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a3e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1a3e-131">-WhatIf</span></span>
<span data-ttu-id="d1a3e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1a3e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1a3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a3e-134">CommonParameters</span></span>
<span data-ttu-id="d1a3e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a3e-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1a3e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a3e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1a3e-137">INPUTS</span></span>

### <span data-ttu-id="d1a3e-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="d1a3e-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d1a3e-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1a3e-139">OUTPUTS</span></span>

### <span data-ttu-id="d1a3e-140">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d1a3e-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="d1a3e-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1a3e-141">NOTES</span></span>

## <span data-ttu-id="d1a3e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1a3e-142">RELATED LINKS</span></span>
