---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525452"
---
# <span data-ttu-id="af8d8-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="af8d8-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="af8d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="af8d8-103">Lägg till certifikatets namn eller tumavtryck i klustret.</span><span class="sxs-lookup"><span data-stu-id="af8d8-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="af8d8-104">Detta registrerar certifikatet igen i klustret för klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="af8d8-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="af8d8-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af8d8-105">SYNTAX</span></span>

### <span data-ttu-id="af8d8-106">ClientCertByTpByObj (standard)</span><span class="sxs-lookup"><span data-stu-id="af8d8-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af8d8-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="af8d8-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af8d8-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="af8d8-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af8d8-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="af8d8-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af8d8-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af8d8-110">DESCRIPTION</span></span>
<span data-ttu-id="af8d8-111">Lägg till certifikatets namn eller tumavtryck i klustret.</span><span class="sxs-lookup"><span data-stu-id="af8d8-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="af8d8-112">Detta registrerar certifikatet igen i klustret för klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="af8d8-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="af8d8-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af8d8-113">EXAMPLES</span></span>

### <span data-ttu-id="af8d8-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="af8d8-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="af8d8-115">Det här kommandot lägger till certifikatet med tumavtrycket ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' i klustret, så klienten kan använda certifikatet som administratör för att kommunicera med klustret.</span><span class="sxs-lookup"><span data-stu-id="af8d8-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="af8d8-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="af8d8-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="af8d8-117">Det här kommandot lägger till ett skrivskyddat klient certifikat med det vanliga namnet ' Contoso.com ' och 2 utfärdare.</span><span class="sxs-lookup"><span data-stu-id="af8d8-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="af8d8-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="af8d8-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="af8d8-119">Det här kommandot lägger till ett skrivskyddat klient certifikat med det vanliga namnet ' Contoso.com ' och 2 emittenter med rör.</span><span class="sxs-lookup"><span data-stu-id="af8d8-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="af8d8-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af8d8-120">PARAMETERS</span></span>

### <span data-ttu-id="af8d8-121">-Admin</span><span class="sxs-lookup"><span data-stu-id="af8d8-121">-Admin</span></span>
<span data-ttu-id="af8d8-122">Används för att ange om klient certifikatet har administratörs nivå.</span><span class="sxs-lookup"><span data-stu-id="af8d8-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="af8d8-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af8d8-123">-AsJob</span></span>
<span data-ttu-id="af8d8-124">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="af8d8-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="af8d8-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="af8d8-125">-CommonName</span></span>
<span data-ttu-id="af8d8-126">Klient certifikatets nätverks namn.</span><span class="sxs-lookup"><span data-stu-id="af8d8-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="af8d8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af8d8-127">-DefaultProfile</span></span>
<span data-ttu-id="af8d8-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af8d8-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af8d8-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af8d8-129">-InputObject</span></span>
<span data-ttu-id="af8d8-130">Hanterad kluster resurs</span><span class="sxs-lookup"><span data-stu-id="af8d8-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="af8d8-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="af8d8-131">-IssuerThumbprint</span></span>
<span data-ttu-id="af8d8-132">Lista över utgivare thumbprints för klient certifikatet.</span><span class="sxs-lookup"><span data-stu-id="af8d8-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="af8d8-133">Används bara i kombination med CommonName.</span><span class="sxs-lookup"><span data-stu-id="af8d8-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8d8-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="af8d8-134">-Name</span></span>
<span data-ttu-id="af8d8-135">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="af8d8-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8d8-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af8d8-136">-ResourceGroupName</span></span>
<span data-ttu-id="af8d8-137">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="af8d8-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8d8-138">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="af8d8-138">-Thumbprint</span></span>
<span data-ttu-id="af8d8-139">Tumavtryck för klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="af8d8-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8d8-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af8d8-140">-Confirm</span></span>
<span data-ttu-id="af8d8-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af8d8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af8d8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af8d8-142">-WhatIf</span></span>
<span data-ttu-id="af8d8-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af8d8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af8d8-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af8d8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af8d8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af8d8-145">CommonParameters</span></span>
<span data-ttu-id="af8d8-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af8d8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af8d8-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af8d8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af8d8-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af8d8-148">INPUTS</span></span>

### <span data-ttu-id="af8d8-149">System. String</span><span class="sxs-lookup"><span data-stu-id="af8d8-149">System.String</span></span>

## <span data-ttu-id="af8d8-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af8d8-150">OUTPUTS</span></span>

### <span data-ttu-id="af8d8-151">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="af8d8-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="af8d8-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af8d8-152">NOTES</span></span>

## <span data-ttu-id="af8d8-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af8d8-153">RELATED LINKS</span></span>
