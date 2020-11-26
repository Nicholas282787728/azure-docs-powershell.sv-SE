---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261680"
---
# <span data-ttu-id="c41a7-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c41a7-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="c41a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c41a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c41a7-103">Remvoe klient certifikat via tumavtryck eller eget namn.</span><span class="sxs-lookup"><span data-stu-id="c41a7-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="c41a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c41a7-104">SYNTAX</span></span>

### <span data-ttu-id="c41a7-105">ClientCertByTpByObj (standard)</span><span class="sxs-lookup"><span data-stu-id="c41a7-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c41a7-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="c41a7-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c41a7-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="c41a7-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c41a7-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="c41a7-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c41a7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c41a7-109">DESCRIPTION</span></span>
<span data-ttu-id="c41a7-110">Remvoe klient certifikat via tumavtryck eller eget namn.</span><span class="sxs-lookup"><span data-stu-id="c41a7-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="c41a7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c41a7-111">EXAMPLES</span></span>

### <span data-ttu-id="c41a7-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c41a7-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="c41a7-113">Ta bort klient certifikat via eget namn.</span><span class="sxs-lookup"><span data-stu-id="c41a7-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="c41a7-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c41a7-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="c41a7-115">Ta bort klient certifikat via tumavtryck.</span><span class="sxs-lookup"><span data-stu-id="c41a7-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="c41a7-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c41a7-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="c41a7-117">Ta bort klient certifikat via tumavtryck med rör.</span><span class="sxs-lookup"><span data-stu-id="c41a7-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="c41a7-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c41a7-118">PARAMETERS</span></span>

### <span data-ttu-id="c41a7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c41a7-119">-AsJob</span></span>
<span data-ttu-id="c41a7-120">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="c41a7-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c41a7-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="c41a7-121">-CommonName</span></span>
<span data-ttu-id="c41a7-122">Klient certifikatets nätverks namn.</span><span class="sxs-lookup"><span data-stu-id="c41a7-122">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c41a7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c41a7-123">-DefaultProfile</span></span>
<span data-ttu-id="c41a7-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c41a7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c41a7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c41a7-125">-InputObject</span></span>
<span data-ttu-id="c41a7-126">Hanterad kluster resurs</span><span class="sxs-lookup"><span data-stu-id="c41a7-126">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c41a7-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="c41a7-127">-Name</span></span>
<span data-ttu-id="c41a7-128">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="c41a7-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41a7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c41a7-129">-PassThru</span></span>
<span data-ttu-id="c41a7-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c41a7-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c41a7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c41a7-131">-ResourceGroupName</span></span>
<span data-ttu-id="c41a7-132">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c41a7-132">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41a7-133">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="c41a7-133">-Thumbprint</span></span>
<span data-ttu-id="c41a7-134">Tumavtryck för klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="c41a7-134">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c41a7-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c41a7-135">-Confirm</span></span>
<span data-ttu-id="c41a7-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c41a7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c41a7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c41a7-137">-WhatIf</span></span>
<span data-ttu-id="c41a7-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c41a7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c41a7-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c41a7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c41a7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41a7-140">CommonParameters</span></span>
<span data-ttu-id="c41a7-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c41a7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41a7-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c41a7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41a7-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c41a7-143">INPUTS</span></span>

### <span data-ttu-id="c41a7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c41a7-144">System.String</span></span>

## <span data-ttu-id="c41a7-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c41a7-145">OUTPUTS</span></span>

### <span data-ttu-id="c41a7-146">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="c41a7-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="c41a7-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c41a7-147">NOTES</span></span>

## <span data-ttu-id="c41a7-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c41a7-148">RELATED LINKS</span></span>