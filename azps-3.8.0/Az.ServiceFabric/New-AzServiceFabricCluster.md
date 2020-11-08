---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 5c28bf3e3bb6269ff9adc3b879d58d01e15e493f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089450"
---
# <span data-ttu-id="a95f2-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a95f2-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="a95f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a95f2-102">SYNOPSIS</span></span>

<span data-ttu-id="a95f2-103">I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="a95f2-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="a95f2-104">Den kan använda en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="a95f2-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="a95f2-105">Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="a95f2-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="a95f2-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a95f2-106">SYNTAX</span></span>

### <span data-ttu-id="a95f2-107">ByDefaultArmTemplate (standard)</span><span class="sxs-lookup"><span data-stu-id="a95f2-107">ByDefaultArmTemplate (Default)</span></span>

```powershell
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a95f2-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="a95f2-108">ByExistingKeyVault</span></span>

```powershell
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a95f2-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a95f2-109">ByNewPfxAndVaultName</span></span>

```powershell
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a95f2-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a95f2-110">ByExistingPfxAndVaultName</span></span>

```powershell
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a95f2-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a95f2-111">DESCRIPTION</span></span>

<span data-ttu-id="a95f2-112">Med det **nya AzServiceFabricCluster-** kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="a95f2-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="a95f2-113">Den mall som används kan vara en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="a95f2-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="a95f2-114">Du kan välja att ange en mapp för att exportera de självsignerade certifikaten eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="a95f2-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="a95f2-115">Om du anger en anpassad mall och en parameter fil behöver du inte ange certifikat informationen i parameter filen så fyller systemet i dessa parametrar.</span><span class="sxs-lookup"><span data-stu-id="a95f2-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="a95f2-116">De fyra alternativen är detaljerade nedan.</span><span class="sxs-lookup"><span data-stu-id="a95f2-116">The four options are detailed below.</span></span> <span data-ttu-id="a95f2-117">Rulla nedåt för att få förklaringar till alla parametrar.</span><span class="sxs-lookup"><span data-stu-id="a95f2-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="a95f2-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a95f2-118">EXAMPLES</span></span>

### <span data-ttu-id="a95f2-119">Exempel 1: Ange endast kluster storleken, certifikatets ämnes namn och operativ systemet för att distribuera ett kluster</span><span class="sxs-lookup"><span data-stu-id="a95f2-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="a95f2-120">Det här kommandot anger endast kluster storleken, certifikatets ämnes namn och operativ systemet för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="a95f2-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="a95f2-121">Exempel 2: Ange en befintlig certifikat resurs i ett nyckelord och en anpassad mall för att distribuera ett kluster</span><span class="sxs-lookup"><span data-stu-id="a95f2-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="a95f2-122">Det här kommandot anger en befintlig certifikat resurs i ett nyckelord och en anpassad mall för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="a95f2-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="a95f2-123">Exempel 3: skapa ett nytt kluster med en anpassad mall.</span><span class="sxs-lookup"><span data-stu-id="a95f2-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="a95f2-124">Ange ett annat resurs grupp namn för Key Vault och låta systemet överföra ett nytt certifikat till det</span><span class="sxs-lookup"><span data-stu-id="a95f2-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

<span data-ttu-id="a95f2-125">Det här kommandot skapar ett nytt kluster med en anpassad mall.</span><span class="sxs-lookup"><span data-stu-id="a95f2-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="a95f2-126">Ange ett annat resurs grupp namn för Key Vault och låta systemet överföra ett nytt certifikat till det</span><span class="sxs-lookup"><span data-stu-id="a95f2-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="a95f2-127">Exempel 4: skaffa ett eget certifikat och en anpassad mall och skapa ett nytt kluster</span><span class="sxs-lookup"><span data-stu-id="a95f2-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

<span data-ttu-id="a95f2-128">Med det här kommandot kan du föra in ett eget certifikat och en anpassad mall och skapa ett nytt kluster.</span><span class="sxs-lookup"><span data-stu-id="a95f2-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="a95f2-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a95f2-129">PARAMETERS</span></span>

### <span data-ttu-id="a95f2-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="a95f2-130">-CertificateCommonName</span></span>

<span data-ttu-id="a95f2-131">Certifikatets nätverks namn</span><span class="sxs-lookup"><span data-stu-id="a95f2-131">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a95f2-132">-CertificateFile</span></span>

<span data-ttu-id="a95f2-133">Befintlig sökväg till certifikat filen för det primära kluster certifikatet</span><span class="sxs-lookup"><span data-stu-id="a95f2-133">The existing certificate file path for the primary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a95f2-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="a95f2-135">Certifikat utfärdarens tumavtryck, avgränsade med kommatecken om fler än en</span><span class="sxs-lookup"><span data-stu-id="a95f2-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="a95f2-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="a95f2-137">Mappen för den nya certifikat filen som ska skapas</span><span class="sxs-lookup"><span data-stu-id="a95f2-137">The folder of the new certificate file to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a95f2-138">-CertificatePassword</span></span>

<span data-ttu-id="a95f2-139">Lösen ordet för certifikat filen</span><span class="sxs-lookup"><span data-stu-id="a95f2-139">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="a95f2-140">-CertificateSubjectName</span></span>

<span data-ttu-id="a95f2-141">Ämnes namnet för det certifikat som ska skapas</span><span class="sxs-lookup"><span data-stu-id="a95f2-141">The subject name of the certificate to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="a95f2-142">-ClusterSize</span></span>

<span data-ttu-id="a95f2-143">Antalet noder i klustret.</span><span class="sxs-lookup"><span data-stu-id="a95f2-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="a95f2-144">Standardvärden är 5</span><span class="sxs-lookup"><span data-stu-id="a95f2-144">Default are 5 nodes</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95f2-145">-DefaultProfile</span></span>

<span data-ttu-id="a95f2-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a95f2-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a95f2-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="a95f2-147">-KeyVaultName</span></span>

<span data-ttu-id="a95f2-148">Namn på Azure-valv om det inte anges blir det standard namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="a95f2-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95f2-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="a95f2-150">Resurs grupp namn för Azure-valv om det inte anges blir det standard för resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a95f2-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-151">-Plats</span><span class="sxs-lookup"><span data-stu-id="a95f2-151">-Location</span></span>

<span data-ttu-id="a95f2-152">Resurs gruppens plats</span><span class="sxs-lookup"><span data-stu-id="a95f2-152">The resource group location</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-153">-Namn</span><span class="sxs-lookup"><span data-stu-id="a95f2-153">-Name</span></span>

<span data-ttu-id="a95f2-154">Ange namnet på klustret, om det inte anges kommer det att vara samma som resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="a95f2-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-155">-OS</span><span class="sxs-lookup"><span data-stu-id="a95f2-155">-OS</span></span>

<span data-ttu-id="a95f2-156">Operativ systemet för de virtuella datorer som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="a95f2-156">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="a95f2-157">-ParameterFile</span></span>

<span data-ttu-id="a95f2-158">Sökvägen till mallnamnet.</span><span class="sxs-lookup"><span data-stu-id="a95f2-158">The path to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95f2-159">-ResourceGroupName</span></span>

<span data-ttu-id="a95f2-160">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a95f2-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a95f2-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="a95f2-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="a95f2-162">Befintlig sökväg till certifikat filen för det sekundära kluster certifikatet</span><span class="sxs-lookup"><span data-stu-id="a95f2-162">The existing certificate file path for the secondary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a95f2-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="a95f2-164">Lösen ordet för certifikat filen</span><span class="sxs-lookup"><span data-stu-id="a95f2-164">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="a95f2-165">-SecretIdentifier</span></span>

<span data-ttu-id="a95f2-166">Den befintliga hemliga URL-adressen för Azure Key Vault, till exempel " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="a95f2-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a95f2-167">-TemplateFile</span></span>

<span data-ttu-id="a95f2-168">Sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="a95f2-168">The path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-169">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="a95f2-169">-VmPassword</span></span>

<span data-ttu-id="a95f2-170">Lösen ordet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a95f2-170">The password of the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-171">-VmSku</span><span class="sxs-lookup"><span data-stu-id="a95f2-171">-VmSku</span></span>

<span data-ttu-id="a95f2-172">VM-SKU</span><span class="sxs-lookup"><span data-stu-id="a95f2-172">The Vm Sku</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-173">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="a95f2-173">-VmUserName</span></span>

<span data-ttu-id="a95f2-174">Användar namn för loggning till VM</span><span class="sxs-lookup"><span data-stu-id="a95f2-174">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f2-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a95f2-175">-Confirm</span></span>

<span data-ttu-id="a95f2-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a95f2-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a95f2-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a95f2-177">-WhatIf</span></span>

<span data-ttu-id="a95f2-178">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a95f2-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a95f2-179">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a95f2-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a95f2-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95f2-180">CommonParameters</span></span>

<span data-ttu-id="a95f2-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a95f2-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95f2-182">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a95f2-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95f2-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a95f2-183">INPUTS</span></span>

### <span data-ttu-id="a95f2-184">System. String</span><span class="sxs-lookup"><span data-stu-id="a95f2-184">System.String</span></span>

### <span data-ttu-id="a95f2-185">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a95f2-185">System.Security.SecureString</span></span>

### <span data-ttu-id="a95f2-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a95f2-186">System.Int32</span></span>

### <span data-ttu-id="a95f2-187">Microsoft. Azure. commands. ServiceFabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a95f2-187">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="a95f2-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a95f2-188">OUTPUTS</span></span>

### <span data-ttu-id="a95f2-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="a95f2-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="a95f2-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a95f2-190">NOTES</span></span>

## <span data-ttu-id="a95f2-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a95f2-191">RELATED LINKS</span></span>