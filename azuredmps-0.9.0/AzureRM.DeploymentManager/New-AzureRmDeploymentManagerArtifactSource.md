---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: a6e69693d10adcb051ec8b33e35070f5c6656481
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571528"
---
# <span data-ttu-id="36e37-101">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="36e37-101">New-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="36e37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36e37-102">SYNOPSIS</span></span>
<span data-ttu-id="36e37-103">Skapar en artefakt källa.</span><span class="sxs-lookup"><span data-stu-id="36e37-103">Creates an artifact source.</span></span>

## <span data-ttu-id="36e37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36e37-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36e37-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36e37-105">DESCRIPTION</span></span>
<span data-ttu-id="36e37-106">Cmdleten **New-AzureRmDeploymentManagerArtifactSource** skapar en artefakt källa.</span><span class="sxs-lookup"><span data-stu-id="36e37-106">The **New-AzureRmDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="36e37-107">Ange *namn* , *ResourceGroupName* och obligatoriska egenskaper.</span><span class="sxs-lookup"><span data-stu-id="36e37-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="36e37-108">Du kan ändra det objekt som returneras lokalt och sedan tillämpa ändringarna på artefakt källan med hjälp av Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36e37-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="36e37-109">Cmdleten returnerar ett ArtifactSource-objekt som har en ResourceId som kan refereras till i New-AzureRmDeloymentManagerServiceTopology-cmdleten så att artefakter som behövs för en ServiceUnit-resurs, mall-och mallparametrar kan refereras från den här platsen.</span><span class="sxs-lookup"><span data-stu-id="36e37-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzureRmDeloymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="36e37-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36e37-110">EXAMPLES</span></span>

### <span data-ttu-id="36e37-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="36e37-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="36e37-112">Skapar en artefakt källa i ContosoResourceGroup med namnet ContosoArtifactSource med central oss som resursens plats.</span><span class="sxs-lookup"><span data-stu-id="36e37-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="36e37-113">Egenskapen SasUri tillhandahåller en Azure Storage SAS URI till lagrings behållaren där artefakterna lagras.</span><span class="sxs-lookup"><span data-stu-id="36e37-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="36e37-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36e37-114">PARAMETERS</span></span>

### <span data-ttu-id="36e37-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="36e37-115">-ArtifactRoot</span></span>
<span data-ttu-id="36e37-116">Valfri katalog förskjutning under lagrings behållaren för artefakterna.</span><span class="sxs-lookup"><span data-stu-id="36e37-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="36e37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e37-117">-DefaultProfile</span></span>
<span data-ttu-id="36e37-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36e37-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e37-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="36e37-119">-Location</span></span>
<span data-ttu-id="36e37-120">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="36e37-120">The location of the resource.</span></span>

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

### <span data-ttu-id="36e37-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="36e37-121">-Name</span></span>
<span data-ttu-id="36e37-122">Namnet på artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="36e37-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="36e37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e37-123">-ResourceGroupName</span></span>
<span data-ttu-id="36e37-124">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="36e37-124">The resource group.</span></span>

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

### <span data-ttu-id="36e37-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="36e37-125">-SasUri</span></span>
<span data-ttu-id="36e37-126">SAS URI till den Azure Storage-behållare där artefakterna lagras.</span><span class="sxs-lookup"><span data-stu-id="36e37-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="36e37-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="36e37-127">-Tag</span></span>
<span data-ttu-id="36e37-128">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="36e37-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="36e37-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36e37-129">-Confirm</span></span>
<span data-ttu-id="36e37-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36e37-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e37-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e37-131">-WhatIf</span></span>
<span data-ttu-id="36e37-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="36e37-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36e37-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="36e37-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e37-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e37-134">CommonParameters</span></span>
<span data-ttu-id="36e37-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e37-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e37-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36e37-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e37-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36e37-137">INPUTS</span></span>

### <span data-ttu-id="36e37-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="36e37-138">None</span></span>

## <span data-ttu-id="36e37-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36e37-139">OUTPUTS</span></span>

### <span data-ttu-id="36e37-140">Microsoft. Azure. commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="36e37-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="36e37-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36e37-141">NOTES</span></span>

## <span data-ttu-id="36e37-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36e37-142">RELATED LINKS</span></span>

[<span data-ttu-id="36e37-143">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="36e37-143">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="36e37-144">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="36e37-144">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="36e37-145">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="36e37-145">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)