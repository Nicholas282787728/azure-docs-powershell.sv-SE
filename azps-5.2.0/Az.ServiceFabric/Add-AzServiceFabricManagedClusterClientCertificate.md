---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403555"
---
# <span data-ttu-id="fb1a9-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="fb1a9-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="fb1a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb1a9-102">SYNOPSIS</span></span>
<span data-ttu-id="fb1a9-103">Lägg till certifikatets namn eller tumavtryck i klustret.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="fb1a9-104">Detta registrerar certifikatet igen i klustret för klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="fb1a9-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb1a9-105">SYNTAX</span></span>

### <span data-ttu-id="fb1a9-106">ClientCertByTpByObj (standard)</span><span class="sxs-lookup"><span data-stu-id="fb1a9-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb1a9-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="fb1a9-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb1a9-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="fb1a9-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb1a9-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="fb1a9-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb1a9-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb1a9-110">DESCRIPTION</span></span>
<span data-ttu-id="fb1a9-111">Lägg till certifikatets namn eller tumavtryck i klustret.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="fb1a9-112">Detta registrerar certifikatet igen i klustret för klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="fb1a9-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb1a9-113">EXAMPLES</span></span>

### <span data-ttu-id="fb1a9-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fb1a9-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="fb1a9-115">Det här kommandot lägger till certifikatet med tumavtrycket ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' i klustret, så klienten kan använda certifikatet som administratör för att kommunicera med klustret.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="fb1a9-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fb1a9-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="fb1a9-117">Det här kommandot lägger till ett skrivskyddat klient certifikat med det vanliga namnet ' Contoso.com ' och 2 utfärdare.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="fb1a9-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="fb1a9-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="fb1a9-119">Det här kommandot lägger till ett skrivskyddat klient certifikat med det vanliga namnet ' Contoso.com ' och 2 emittenter med rör.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="fb1a9-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb1a9-120">PARAMETERS</span></span>

### <span data-ttu-id="fb1a9-121">-Admin</span><span class="sxs-lookup"><span data-stu-id="fb1a9-121">-Admin</span></span>
<span data-ttu-id="fb1a9-122">Används för att ange om klient certifikatet har administratörs nivå.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="fb1a9-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb1a9-123">-AsJob</span></span>
<span data-ttu-id="fb1a9-124">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fb1a9-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="fb1a9-125">-CommonName</span></span>
<span data-ttu-id="fb1a9-126">Klient certifikatets nätverks namn.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="fb1a9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb1a9-127">-DefaultProfile</span></span>
<span data-ttu-id="fb1a9-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb1a9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb1a9-129">-InputObject</span></span>
<span data-ttu-id="fb1a9-130">Hanterad kluster resurs</span><span class="sxs-lookup"><span data-stu-id="fb1a9-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="fb1a9-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="fb1a9-131">-IssuerThumbprint</span></span>
<span data-ttu-id="fb1a9-132">Lista över utgivare thumbprints för klient certifikatet.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="fb1a9-133">Används bara i kombination med CommonName.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="fb1a9-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb1a9-134">-Name</span></span>
<span data-ttu-id="fb1a9-135">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fb1a9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb1a9-136">-ResourceGroupName</span></span>
<span data-ttu-id="fb1a9-137">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fb1a9-138">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="fb1a9-138">-Thumbprint</span></span>
<span data-ttu-id="fb1a9-139">Tumavtryck för klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="fb1a9-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb1a9-140">-Confirm</span></span>
<span data-ttu-id="fb1a9-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb1a9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb1a9-142">-WhatIf</span></span>
<span data-ttu-id="fb1a9-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb1a9-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb1a9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb1a9-145">CommonParameters</span></span>
<span data-ttu-id="fb1a9-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb1a9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb1a9-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb1a9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb1a9-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb1a9-148">INPUTS</span></span>

### <span data-ttu-id="fb1a9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="fb1a9-149">System.String</span></span>

## <span data-ttu-id="fb1a9-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb1a9-150">OUTPUTS</span></span>

### <span data-ttu-id="fb1a9-151">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="fb1a9-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="fb1a9-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb1a9-152">NOTES</span></span>

## <span data-ttu-id="fb1a9-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb1a9-153">RELATED LINKS</span></span>
