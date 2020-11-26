---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269088"
---
# <span data-ttu-id="bde52-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="bde52-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="bde52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bde52-102">SYNOPSIS</span></span>
<span data-ttu-id="bde52-103">Ta bort virtuellt dator tillägg från nodtyp.</span><span class="sxs-lookup"><span data-stu-id="bde52-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="bde52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bde52-104">SYNTAX</span></span>

### <span data-ttu-id="bde52-105">ByObj (standard)</span><span class="sxs-lookup"><span data-stu-id="bde52-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bde52-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bde52-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bde52-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bde52-107">DESCRIPTION</span></span>
<span data-ttu-id="bde52-108">Ta bort virtuellt dator tillägg från nodtypen efter namn.</span><span class="sxs-lookup"><span data-stu-id="bde52-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="bde52-109">Använd [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) och titta på egenskapen VmExtensions för att se det aktuella tillägget för nodtypen.</span><span class="sxs-lookup"><span data-stu-id="bde52-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="bde52-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bde52-110">EXAMPLES</span></span>

### <span data-ttu-id="bde52-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bde52-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="bde52-112">Ta bort tillägget från nodtyp efter namn.</span><span class="sxs-lookup"><span data-stu-id="bde52-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="bde52-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bde52-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="bde52-114">Ta bort tillägget från nodtyp med namn, med rör dragning.</span><span class="sxs-lookup"><span data-stu-id="bde52-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="bde52-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bde52-115">PARAMETERS</span></span>

### <span data-ttu-id="bde52-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bde52-116">-AsJob</span></span>
<span data-ttu-id="bde52-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="bde52-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bde52-118">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="bde52-118">-ClusterName</span></span>
<span data-ttu-id="bde52-119">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="bde52-119">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bde52-120">-DefaultProfile</span></span>
<span data-ttu-id="bde52-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bde52-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bde52-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bde52-122">-InputObject</span></span>
<span data-ttu-id="bde52-123">Resurs för nodtyp</span><span class="sxs-lookup"><span data-stu-id="bde52-123">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="bde52-124">-Name</span></span>
<span data-ttu-id="bde52-125">namn på tillägg.</span><span class="sxs-lookup"><span data-stu-id="bde52-125">extension name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="bde52-126">-NodeTypeName</span></span>
<span data-ttu-id="bde52-127">Ange namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="bde52-127">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bde52-128">-PassThru</span></span>
<span data-ttu-id="bde52-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bde52-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="bde52-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bde52-130">-ResourceGroupName</span></span>
<span data-ttu-id="bde52-131">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bde52-131">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde52-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bde52-132">-Confirm</span></span>
<span data-ttu-id="bde52-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bde52-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bde52-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bde52-134">-WhatIf</span></span>
<span data-ttu-id="bde52-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bde52-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bde52-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bde52-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bde52-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde52-137">CommonParameters</span></span>
<span data-ttu-id="bde52-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bde52-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde52-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bde52-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde52-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bde52-140">INPUTS</span></span>

### <span data-ttu-id="bde52-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bde52-141">System.String</span></span>

## <span data-ttu-id="bde52-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bde52-142">OUTPUTS</span></span>

### <span data-ttu-id="bde52-143">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="bde52-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="bde52-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bde52-144">NOTES</span></span>

## <span data-ttu-id="bde52-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bde52-145">RELATED LINKS</span></span>