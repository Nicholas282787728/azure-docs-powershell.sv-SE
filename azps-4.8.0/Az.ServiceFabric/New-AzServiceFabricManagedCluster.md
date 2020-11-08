---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259878"
---
# <span data-ttu-id="d8101-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d8101-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="d8101-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8101-102">SYNOPSIS</span></span>
<span data-ttu-id="d8101-103">Skapa ett nytt hanterat kluster.</span><span class="sxs-lookup"><span data-stu-id="d8101-103">Create new managed cluster.</span></span>

## <span data-ttu-id="d8101-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8101-104">SYNTAX</span></span>

### <span data-ttu-id="d8101-105">ClientCertByTp (standard)</span><span class="sxs-lookup"><span data-stu-id="d8101-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8101-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="d8101-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8101-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8101-107">DESCRIPTION</span></span>
<span data-ttu-id="d8101-108">Denna cmdlet skapar en hanterad kluster resurs utan nodtyper.</span><span class="sxs-lookup"><span data-stu-id="d8101-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="d8101-109">Om du vill starta klustret måste du lägga till en primär nodtyp med den [nya-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span><span class="sxs-lookup"><span data-stu-id="d8101-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="d8101-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8101-110">EXAMPLES</span></span>

### <span data-ttu-id="d8101-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d8101-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="d8101-112">Det här kommandot skapar en kluster resurs med standard-Basic-SKU.</span><span class="sxs-lookup"><span data-stu-id="d8101-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="d8101-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d8101-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="d8101-114">Det här kommandot skapar en kluster resurs i centraluseuap med ett första administratörs klient certifikat och standard-SKU.</span><span class="sxs-lookup"><span data-stu-id="d8101-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="d8101-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8101-115">PARAMETERS</span></span>

### <span data-ttu-id="d8101-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="d8101-116">-AdminPassword</span></span>
<span data-ttu-id="d8101-117">Administratörs lösen ord som används för de virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="d8101-117">Admin password used for the virtual machines.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="d8101-118">-AdminUserName</span></span>
<span data-ttu-id="d8101-119">Administratörs lösen ord som används för de virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="d8101-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="d8101-120">Standard: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="d8101-120">Default: vmadmin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "vmadmin"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8101-121">-AsJob</span></span>
<span data-ttu-id="d8101-122">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="d8101-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d8101-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="d8101-123">-ClientCertCommonName</span></span>
<span data-ttu-id="d8101-124">Klient certifikatets nätverks namn.</span><span class="sxs-lookup"><span data-stu-id="d8101-124">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="d8101-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="d8101-126">Används för att ange om klient certifikatet har administratörs nivå.</span><span class="sxs-lookup"><span data-stu-id="d8101-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="d8101-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="d8101-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="d8101-128">Lista över utgivare thumbprints för klient certifikatet.</span><span class="sxs-lookup"><span data-stu-id="d8101-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="d8101-129">Används bara i kombination med ClientCertCommonName.</span><span class="sxs-lookup"><span data-stu-id="d8101-129">Only use in combination with ClientCertCommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="d8101-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="d8101-131">Tumavtryck för klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="d8101-131">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="d8101-132">-ClientConnectionPort</span></span>
<span data-ttu-id="d8101-133">Port som används för klient anslutningar till klustret.</span><span class="sxs-lookup"><span data-stu-id="d8101-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="d8101-134">Standard: 19000.</span><span class="sxs-lookup"><span data-stu-id="d8101-134">Default: 19000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="d8101-135">-CodeVersion</span></span>
<span data-ttu-id="d8101-136">Kluster tjänstens Fabric-kod version.</span><span class="sxs-lookup"><span data-stu-id="d8101-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="d8101-137">Använd endast om uppgraderings läget är manuell.</span><span class="sxs-lookup"><span data-stu-id="d8101-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="d8101-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8101-138">-DefaultProfile</span></span>
<span data-ttu-id="d8101-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8101-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8101-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="d8101-140">-DnsName</span></span>
<span data-ttu-id="d8101-141">Klustrets DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="d8101-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="d8101-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="d8101-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="d8101-143">Port som används för HTTP-anslutningar till klustret.</span><span class="sxs-lookup"><span data-stu-id="d8101-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="d8101-144">Standard: 19080.</span><span class="sxs-lookup"><span data-stu-id="d8101-144">Default: 19080.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19080
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-145">-Plats</span><span class="sxs-lookup"><span data-stu-id="d8101-145">-Location</span></span>
<span data-ttu-id="d8101-146">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="d8101-146">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8101-147">-Name</span></span>
<span data-ttu-id="d8101-148">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="d8101-148">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8101-149">-ResourceGroupName</span></span>
<span data-ttu-id="d8101-150">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8101-150">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="d8101-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="d8101-152">Slut punkt som används av omvänd proxy.</span><span class="sxs-lookup"><span data-stu-id="d8101-152">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="d8101-153">-Sku</span></span>
<span data-ttu-id="d8101-154">I klusterets SKU är alternativen grundläggande: det får minst tre startnoder och tillåter bara en nodtyp och standard: det får minst fem startnoder och tillåter flera nodtyper.</span><span class="sxs-lookup"><span data-stu-id="d8101-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ManagedClusterSku
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: Basic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="d8101-155">-UpgradeMode</span></span>
<span data-ttu-id="d8101-156">Kluster tjänst Fabric Code version uppgraderings läge.</span><span class="sxs-lookup"><span data-stu-id="d8101-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="d8101-157">Automatisk eller manuell.</span><span class="sxs-lookup"><span data-stu-id="d8101-157">Automatic or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8101-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="d8101-158">-UseTestExtension</span></span>
<span data-ttu-id="d8101-159">Om du anger att klustret ska ställas in med service test VMSS tillägget.</span><span class="sxs-lookup"><span data-stu-id="d8101-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="d8101-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8101-160">-Confirm</span></span>
<span data-ttu-id="d8101-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8101-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8101-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8101-162">-WhatIf</span></span>
<span data-ttu-id="d8101-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8101-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8101-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8101-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8101-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8101-165">CommonParameters</span></span>
<span data-ttu-id="d8101-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8101-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8101-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8101-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8101-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8101-168">INPUTS</span></span>

### <span data-ttu-id="d8101-169">System. String</span><span class="sxs-lookup"><span data-stu-id="d8101-169">System.String</span></span>

## <span data-ttu-id="d8101-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8101-170">OUTPUTS</span></span>

### <span data-ttu-id="d8101-171">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d8101-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="d8101-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8101-172">NOTES</span></span>

## <span data-ttu-id="d8101-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8101-173">RELATED LINKS</span></span>

[<span data-ttu-id="d8101-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d8101-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)