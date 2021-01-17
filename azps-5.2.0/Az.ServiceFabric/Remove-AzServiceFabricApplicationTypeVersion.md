---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403528"
---
# <span data-ttu-id="31503-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="31503-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="31503-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31503-102">SYNOPSIS</span></span>
<span data-ttu-id="31503-103">Ta bort Service Fabric en program typ version från klustret.</span><span class="sxs-lookup"><span data-stu-id="31503-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="31503-104">Det går endast att använda program typer som distribueras av ARM.</span><span class="sxs-lookup"><span data-stu-id="31503-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="31503-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31503-105">SYNTAX</span></span>

### <span data-ttu-id="31503-106">ByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="31503-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31503-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="31503-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31503-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="31503-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31503-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31503-109">DESCRIPTION</span></span>
<span data-ttu-id="31503-110">Denna cmdlet tar bort tjänstens infrastruktur program typ version från klustret.</span><span class="sxs-lookup"><span data-stu-id="31503-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="31503-111">Alla program under den här resursen måste tas bort innan du kör det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="31503-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="31503-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31503-112">EXAMPLES</span></span>

### <span data-ttu-id="31503-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="31503-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="31503-114">I det här exemplet tas versionen "v1" bort under typen "testAppType".</span><span class="sxs-lookup"><span data-stu-id="31503-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="31503-115">Det finns några program under den här resursen kommandot kommer att utlösa ett undantag.</span><span class="sxs-lookup"><span data-stu-id="31503-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="31503-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31503-116">PARAMETERS</span></span>

### <span data-ttu-id="31503-117">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="31503-117">-ClusterName</span></span>
<span data-ttu-id="31503-118">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="31503-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="31503-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31503-119">-DefaultProfile</span></span>
<span data-ttu-id="31503-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31503-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31503-121">-Force</span><span class="sxs-lookup"><span data-stu-id="31503-121">-Force</span></span>
<span data-ttu-id="31503-122">Ta bort utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="31503-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="31503-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31503-123">-InputObject</span></span>
<span data-ttu-id="31503-124">Versions resursen för program typ.</span><span class="sxs-lookup"><span data-stu-id="31503-124">The application type version resource.</span></span>

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

### <span data-ttu-id="31503-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="31503-125">-Name</span></span>
<span data-ttu-id="31503-126">Ange namnet på program typen.</span><span class="sxs-lookup"><span data-stu-id="31503-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="31503-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31503-127">-PassThru</span></span>
<span data-ttu-id="31503-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="31503-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="31503-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31503-129">-ResourceGroupName</span></span>
<span data-ttu-id="31503-130">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="31503-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="31503-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31503-131">-ResourceId</span></span>
<span data-ttu-id="31503-132">Arm-ResourceId för program typ version.</span><span class="sxs-lookup"><span data-stu-id="31503-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="31503-133">-Version</span><span class="sxs-lookup"><span data-stu-id="31503-133">-Version</span></span>
<span data-ttu-id="31503-134">Ange program typ version.</span><span class="sxs-lookup"><span data-stu-id="31503-134">Specify the application type version.</span></span>

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

### <span data-ttu-id="31503-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="31503-135">-Confirm</span></span>
<span data-ttu-id="31503-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="31503-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31503-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31503-137">-WhatIf</span></span>
<span data-ttu-id="31503-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="31503-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31503-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="31503-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31503-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31503-140">CommonParameters</span></span>
<span data-ttu-id="31503-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31503-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31503-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31503-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31503-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31503-143">INPUTS</span></span>

### <span data-ttu-id="31503-144">System. String</span><span class="sxs-lookup"><span data-stu-id="31503-144">System.String</span></span>

### <span data-ttu-id="31503-145">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="31503-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="31503-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31503-146">OUTPUTS</span></span>

### <span data-ttu-id="31503-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31503-147">System.Boolean</span></span>

## <span data-ttu-id="31503-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31503-148">NOTES</span></span>

## <span data-ttu-id="31503-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31503-149">RELATED LINKS</span></span>
