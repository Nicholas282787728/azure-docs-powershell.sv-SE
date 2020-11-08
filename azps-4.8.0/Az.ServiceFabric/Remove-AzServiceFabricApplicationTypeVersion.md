---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 498dec77dfc2f4ede8ae81aa70b10acfe2ad2954
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103499"
---
# <span data-ttu-id="1c317-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1c317-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="1c317-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c317-102">SYNOPSIS</span></span>
<span data-ttu-id="1c317-103">Ta bort Service Fabric en program typ version från klustret.</span><span class="sxs-lookup"><span data-stu-id="1c317-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="1c317-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c317-104">SYNTAX</span></span>

### <span data-ttu-id="1c317-105">ByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="1c317-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c317-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c317-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c317-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1c317-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c317-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c317-108">DESCRIPTION</span></span>
<span data-ttu-id="1c317-109">Denna cmdlet tar bort tjänstens infrastruktur program typ version från klustret.</span><span class="sxs-lookup"><span data-stu-id="1c317-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="1c317-110">Alla program under den här resursen måste tas bort innan du kör det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="1c317-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="1c317-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c317-111">EXAMPLES</span></span>

### <span data-ttu-id="1c317-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1c317-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="1c317-113">I det här exemplet tas versionen "v1" bort under typen "testAppType".</span><span class="sxs-lookup"><span data-stu-id="1c317-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="1c317-114">Det finns några program under den här resursen kommandot kommer att utlösa ett undantag.</span><span class="sxs-lookup"><span data-stu-id="1c317-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="1c317-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c317-115">PARAMETERS</span></span>

### <span data-ttu-id="1c317-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="1c317-116">-ClusterName</span></span>
<span data-ttu-id="1c317-117">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="1c317-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c317-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c317-118">-DefaultProfile</span></span>
<span data-ttu-id="1c317-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c317-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c317-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1c317-120">-Force</span></span>
<span data-ttu-id="1c317-121">Ta bort utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="1c317-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="1c317-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c317-122">-InputObject</span></span>
<span data-ttu-id="1c317-123">Versions resursen för program typ.</span><span class="sxs-lookup"><span data-stu-id="1c317-123">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c317-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c317-124">-Name</span></span>
<span data-ttu-id="1c317-125">Ange namnet på program typen.</span><span class="sxs-lookup"><span data-stu-id="1c317-125">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c317-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c317-126">-PassThru</span></span>
<span data-ttu-id="1c317-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1c317-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1c317-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c317-128">-ResourceGroupName</span></span>
<span data-ttu-id="1c317-129">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1c317-129">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c317-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c317-130">-ResourceId</span></span>
<span data-ttu-id="1c317-131">Arm-ResourceId för program typ version.</span><span class="sxs-lookup"><span data-stu-id="1c317-131">Arm ResourceId of the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c317-132">-Version</span><span class="sxs-lookup"><span data-stu-id="1c317-132">-Version</span></span>
<span data-ttu-id="1c317-133">Ange program typ version.</span><span class="sxs-lookup"><span data-stu-id="1c317-133">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c317-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c317-134">-Confirm</span></span>
<span data-ttu-id="1c317-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c317-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c317-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c317-136">-WhatIf</span></span>
<span data-ttu-id="1c317-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c317-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c317-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c317-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c317-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c317-139">CommonParameters</span></span>
<span data-ttu-id="1c317-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c317-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c317-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c317-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c317-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c317-142">INPUTS</span></span>

### <span data-ttu-id="1c317-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1c317-143">System.String</span></span>

### <span data-ttu-id="1c317-144">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1c317-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="1c317-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c317-145">OUTPUTS</span></span>

### <span data-ttu-id="1c317-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c317-146">System.Boolean</span></span>

## <span data-ttu-id="1c317-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c317-147">NOTES</span></span>

## <span data-ttu-id="1c317-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c317-148">RELATED LINKS</span></span>
