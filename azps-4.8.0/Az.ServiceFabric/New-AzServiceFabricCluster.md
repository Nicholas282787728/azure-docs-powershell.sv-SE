---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 9e5ba2d2ee228da30a887c0c7b318dd9d270d763
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103505"
---
# <span data-ttu-id="c6bdc-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c6bdc-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="c6bdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6bdc-102">SYNOPSIS</span></span>

<span data-ttu-id="c6bdc-103">I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="c6bdc-104">Den kan använda en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="c6bdc-105">Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="c6bdc-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6bdc-106">SYNTAX</span></span>

### <span data-ttu-id="c6bdc-107">ByDefaultArmTemplate (standard)</span><span class="sxs-lookup"><span data-stu-id="c6bdc-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6bdc-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="c6bdc-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6bdc-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c6bdc-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6bdc-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="c6bdc-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6bdc-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6bdc-111">DESCRIPTION</span></span>

<span data-ttu-id="c6bdc-112">Med det **nya AzServiceFabricCluster-** kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="c6bdc-113">Den mall som används kan vara en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="c6bdc-114">Du kan välja att ange en mapp för att exportera de självsignerade certifikaten eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="c6bdc-115">Om du anger en anpassad mall och en parameter fil behöver du inte ange certifikat informationen i parameter filen så fyller systemet i dessa parametrar.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="c6bdc-116">De fyra alternativen är detaljerade nedan.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-116">The four options are detailed below.</span></span> <span data-ttu-id="c6bdc-117">Rulla nedåt för att få förklaringar till alla parametrar.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="c6bdc-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6bdc-118">EXAMPLES</span></span>

### <span data-ttu-id="c6bdc-119">Exempel 1: Ange endast kluster storleken, certifikatets ämnes namn och operativ systemet för att distribuera ett kluster</span><span class="sxs-lookup"><span data-stu-id="c6bdc-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="c6bdc-120">Det här kommandot anger endast kluster storleken, certifikatets ämnes namn och operativ systemet för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="c6bdc-121">Exempel 2: Ange en befintlig certifikat resurs i ett nyckelord och en anpassad mall för att distribuera ett kluster</span><span class="sxs-lookup"><span data-stu-id="c6bdc-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="c6bdc-122">Det här kommandot anger en befintlig certifikat resurs i ett nyckelord och en anpassad mall för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="c6bdc-123">Exempel 3: skapa ett nytt kluster med en anpassad mall.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="c6bdc-124">Ange ett annat resurs grupp namn för Key Vault och låta systemet överföra ett nytt certifikat till det</span><span class="sxs-lookup"><span data-stu-id="c6bdc-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

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

<span data-ttu-id="c6bdc-125">Det här kommandot skapar ett nytt kluster med en anpassad mall.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="c6bdc-126">Ange ett annat resurs grupp namn för Key Vault och låta systemet överföra ett nytt certifikat till det</span><span class="sxs-lookup"><span data-stu-id="c6bdc-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="c6bdc-127">Exempel 4: skaffa ett eget certifikat och en anpassad mall och skapa ett nytt kluster</span><span class="sxs-lookup"><span data-stu-id="c6bdc-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

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

<span data-ttu-id="c6bdc-128">Med det här kommandot kan du föra in ett eget certifikat och en anpassad mall och skapa ett nytt kluster.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="c6bdc-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6bdc-129">PARAMETERS</span></span>

### <span data-ttu-id="c6bdc-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="c6bdc-130">-CertificateCommonName</span></span>

<span data-ttu-id="c6bdc-131">Certifikatets nätverks namn</span><span class="sxs-lookup"><span data-stu-id="c6bdc-131">Certificate common name</span></span>

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

### <span data-ttu-id="c6bdc-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c6bdc-132">-CertificateFile</span></span>

<span data-ttu-id="c6bdc-133">Befintlig sökväg till certifikat filen för det primära kluster certifikatet</span><span class="sxs-lookup"><span data-stu-id="c6bdc-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="c6bdc-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="c6bdc-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="c6bdc-135">Certifikat utfärdarens tumavtryck, avgränsade med kommatecken om fler än en</span><span class="sxs-lookup"><span data-stu-id="c6bdc-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="c6bdc-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="c6bdc-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="c6bdc-137">Mappen för den nya certifikat filen som ska skapas</span><span class="sxs-lookup"><span data-stu-id="c6bdc-137">The folder of the new certificate file to be created</span></span>

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

### <span data-ttu-id="c6bdc-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c6bdc-138">-CertificatePassword</span></span>

<span data-ttu-id="c6bdc-139">Lösen ordet för certifikat filen</span><span class="sxs-lookup"><span data-stu-id="c6bdc-139">The password of the certificate file</span></span>

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

### <span data-ttu-id="c6bdc-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="c6bdc-140">-CertificateSubjectName</span></span>

<span data-ttu-id="c6bdc-141">Ämnes namnet för det certifikat som ska skapas</span><span class="sxs-lookup"><span data-stu-id="c6bdc-141">The subject name of the certificate to be created</span></span>

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

### <span data-ttu-id="c6bdc-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="c6bdc-142">-ClusterSize</span></span>

<span data-ttu-id="c6bdc-143">Antalet noder i klustret.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="c6bdc-144">Standardvärden är 5</span><span class="sxs-lookup"><span data-stu-id="c6bdc-144">Default are 5 nodes</span></span>

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

### <span data-ttu-id="c6bdc-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6bdc-145">-DefaultProfile</span></span>

<span data-ttu-id="c6bdc-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6bdc-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="c6bdc-147">-KeyVaultName</span></span>

<span data-ttu-id="c6bdc-148">Namn på Azure-valv om det inte anges blir det standard namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c6bdc-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="c6bdc-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6bdc-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="c6bdc-150">Resurs grupp namn för Azure-valv om det inte anges blir det standard för resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c6bdc-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="c6bdc-151">-Plats</span><span class="sxs-lookup"><span data-stu-id="c6bdc-151">-Location</span></span>

<span data-ttu-id="c6bdc-152">Resurs gruppens plats</span><span class="sxs-lookup"><span data-stu-id="c6bdc-152">The resource group location</span></span>

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

### <span data-ttu-id="c6bdc-153">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6bdc-153">-Name</span></span>

<span data-ttu-id="c6bdc-154">Ange namnet på klustret, om det inte anges kommer det att vara samma som resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="c6bdc-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

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

### <span data-ttu-id="c6bdc-155">-OS</span><span class="sxs-lookup"><span data-stu-id="c6bdc-155">-OS</span></span>

<span data-ttu-id="c6bdc-156">Operativ systemet för de virtuella datorer som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-156">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="c6bdc-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="c6bdc-157">-ParameterFile</span></span>

<span data-ttu-id="c6bdc-158">Sökvägen till mallnamnet.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-158">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="c6bdc-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6bdc-159">-ResourceGroupName</span></span>

<span data-ttu-id="c6bdc-160">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c6bdc-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="c6bdc-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="c6bdc-162">Befintlig sökväg till certifikat filen för det sekundära kluster certifikatet</span><span class="sxs-lookup"><span data-stu-id="c6bdc-162">The existing certificate file path for the secondary cluster certificate</span></span>

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

### <span data-ttu-id="c6bdc-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c6bdc-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="c6bdc-164">Lösen ordet för certifikat filen</span><span class="sxs-lookup"><span data-stu-id="c6bdc-164">The password of the certificate file</span></span>

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

### <span data-ttu-id="c6bdc-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="c6bdc-165">-SecretIdentifier</span></span>

<span data-ttu-id="c6bdc-166">Den befintliga hemliga URL-adressen för Azure Key Vault, till exempel " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="c6bdc-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="c6bdc-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c6bdc-167">-TemplateFile</span></span>

<span data-ttu-id="c6bdc-168">Sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-168">The path to the template file.</span></span>

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

### <span data-ttu-id="c6bdc-169">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="c6bdc-169">-Thumbprint</span></span>
<span data-ttu-id="c6bdc-170">Tumavtrycket för certifikatet correspoinding till SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="c6bdc-171">Använd det här alternativet om certifikatet inte är hanterat eftersom nyckel valvet bara har certifikatet lagrat som hemligt och cmdleten inte kan hämta tumavtrycket.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6bdc-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="c6bdc-172">-VmPassword</span></span>

<span data-ttu-id="c6bdc-173">Lösen ordet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-173">The password of the Vm.</span></span>

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

### <span data-ttu-id="c6bdc-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="c6bdc-174">-VmSku</span></span>

<span data-ttu-id="c6bdc-175">VM-SKU</span><span class="sxs-lookup"><span data-stu-id="c6bdc-175">The Vm Sku</span></span>

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

### <span data-ttu-id="c6bdc-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="c6bdc-176">-VmUserName</span></span>

<span data-ttu-id="c6bdc-177">Användar namn för loggning till VM</span><span class="sxs-lookup"><span data-stu-id="c6bdc-177">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="c6bdc-178">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c6bdc-178">-Confirm</span></span>

<span data-ttu-id="c6bdc-179">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6bdc-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6bdc-180">-WhatIf</span></span>

<span data-ttu-id="c6bdc-181">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6bdc-182">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6bdc-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6bdc-183">CommonParameters</span></span>
<span data-ttu-id="c6bdc-184">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6bdc-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6bdc-185">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6bdc-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6bdc-186">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6bdc-186">INPUTS</span></span>

### <span data-ttu-id="c6bdc-187">System. String</span><span class="sxs-lookup"><span data-stu-id="c6bdc-187">System.String</span></span>

### <span data-ttu-id="c6bdc-188">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c6bdc-188">System.Security.SecureString</span></span>

### <span data-ttu-id="c6bdc-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c6bdc-189">System.Int32</span></span>

### <span data-ttu-id="c6bdc-190">Microsoft. Azure. commands. ServiceFabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c6bdc-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="c6bdc-191">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6bdc-191">OUTPUTS</span></span>

### <span data-ttu-id="c6bdc-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="c6bdc-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="c6bdc-193">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6bdc-193">NOTES</span></span>

## <span data-ttu-id="c6bdc-194">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6bdc-194">RELATED LINKS</span></span>
