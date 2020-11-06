---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/new-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5da8d1f48a50cafc970278d59b99750f283a9414
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580972"
---
# <span data-ttu-id="ad1d0-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ad1d0-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="ad1d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad1d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1d0-103">I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="ad1d0-104">Den kan använda en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="ad1d0-105">Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad1d0-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad1d0-106">SYNTAX</span></span>

### <span data-ttu-id="ad1d0-107">ByDefaultArmTemplate (standard)</span><span class="sxs-lookup"><span data-stu-id="ad1d0-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad1d0-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="ad1d0-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-VmPassword <SecureString>] -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad1d0-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="ad1d0-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad1d0-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="ad1d0-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad1d0-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad1d0-111">DESCRIPTION</span></span>
<span data-ttu-id="ad1d0-112">Med det **nya AzureRmServiceFabricCluster-** kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="ad1d0-113">Den mall som används kan vara en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="ad1d0-114">Du kan välja att ange en mapp för att exportera de självsignerade certifikaten eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="ad1d0-115">Om du anger en anpassad mall och en parameter fil behöver du inte ange certifikat informationen i parameter filen så fyller systemet i dessa parametrar.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="ad1d0-116">De fyra alternativen är detaljerade nedan.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-116">The four options are detailed below.</span></span> <span data-ttu-id="ad1d0-117">Rulla nedåt för att få förklaringar till alla parametrar.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="ad1d0-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad1d0-118">EXAMPLES</span></span>

### <span data-ttu-id="ad1d0-119">Exempel 1: Ange bara kluster storleken, certifikatets ämnes namn och operativ systemet för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="ad1d0-120">Det här kommandot anger endast kluster storleken, certifikatets ämnes namn och operativ systemet för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="ad1d0-121">Exempel 2: Ange en befintlig certifikat resurs i ett nyckelord och en anpassad mall för att distribuera ett kluster</span><span class="sxs-lookup"><span data-stu-id="ad1d0-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="ad1d0-122">Det här kommandot anger en befintlig certifikat resurs i ett nyckelord och en anpassad mall för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="ad1d0-123">Exempel 3: skapa ett nytt kluster med en anpassad mall.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="ad1d0-124">Ange ett annat resurs grupp namn för Key Vault och låta systemet överföra ett nytt certifikat till det</span><span class="sxs-lookup"><span data-stu-id="ad1d0-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="ad1d0-125">Det här kommandot skapar ett nytt kluster med en anpassad mall.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="ad1d0-126">Ange ett annat resurs grupp namn för Key Vault och låta systemet överföra ett nytt certifikat till det</span><span class="sxs-lookup"><span data-stu-id="ad1d0-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="ad1d0-127">Exempel 4: skaffa ett eget certifikat och en anpassad mall och skapa ett nytt kluster</span><span class="sxs-lookup"><span data-stu-id="ad1d0-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="ad1d0-128">Med det här kommandot kan du föra in ett eget certifikat och en anpassad mall och skapa ett nytt kluster.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="ad1d0-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad1d0-129">PARAMETERS</span></span>

### <span data-ttu-id="ad1d0-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ad1d0-130">-CertificateFile</span></span>
<span data-ttu-id="ad1d0-131">Den befintliga certifikats fil Sök vägen för det primära kluster certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-131">The existing certificate file path for the primary cluster certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="ad1d0-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="ad1d0-133">Mappen för den nya certifikat filen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-133">The folder of the new certificate file to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ad1d0-134">-CertificatePassword</span></span>
<span data-ttu-id="ad1d0-135">Lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-135">The password of the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="ad1d0-136">-CertificateSubjectName</span></span>
<span data-ttu-id="ad1d0-137">Ämnes namnet för det certifikat som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-137">The subject name of the certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="ad1d0-138">-ClusterSize</span></span>
<span data-ttu-id="ad1d0-139">Antalet noder i klustret.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="ad1d0-140">Standardvärden är 5 noder.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-140">Default are 5 nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1d0-141">-DefaultProfile</span></span>
<span data-ttu-id="ad1d0-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-143">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="ad1d0-143">-KeyVaultName</span></span>
<span data-ttu-id="ad1d0-144">Namn på Azure Key valv.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-144">Azure key vault name.</span></span> <span data-ttu-id="ad1d0-145">Om inget anges blir det standard namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-145">If not given, it will be defaulted to the resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-146">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad1d0-146">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="ad1d0-147">Namnet på Azure Key valv-resursen.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-147">Azure key vault resource group name.</span></span> <span data-ttu-id="ad1d0-148">Om det inte anges blir det standard namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-148">If not given, it will be defaulted to resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-149">-Plats</span><span class="sxs-lookup"><span data-stu-id="ad1d0-149">-Location</span></span>
<span data-ttu-id="ad1d0-150">Resurs gruppens plats.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-150">The resource group location.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad1d0-151">-Name</span></span>
<span data-ttu-id="ad1d0-152">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-152">Specify the name of the cluster.</span></span> <span data-ttu-id="ad1d0-153">Om det inte anges kommer det att vara samma som resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-153">If not given, it will be same as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-154">-OS</span><span class="sxs-lookup"><span data-stu-id="ad1d0-154">-OS</span></span>
<span data-ttu-id="ad1d0-155">Operativ systemet för de virtuella datorer som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-155">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-156">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="ad1d0-156">-ParameterFile</span></span>
<span data-ttu-id="ad1d0-157">Sökvägen till mallnamnet.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-157">The path to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad1d0-158">-ResourceGroupName</span></span>
<span data-ttu-id="ad1d0-159">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-159">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-160">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="ad1d0-160">-SecondaryCertificateFile</span></span>
<span data-ttu-id="ad1d0-161">Den befintliga certifikats fil Sök vägen för det sekundära kluster certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-161">The existing certificate file path for the secondary cluster certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-162">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ad1d0-162">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="ad1d0-163">Lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-163">The password of the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-164">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="ad1d0-164">-SecretIdentifier</span></span>
<span data-ttu-id="ad1d0-165">Den hemliga URL-adressen för Azure Key-valvet, till exempel: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-165">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ad1d0-166">-TemplateFile</span></span>
<span data-ttu-id="ad1d0-167">Sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-167">The path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-168">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="ad1d0-168">-VmPassword</span></span>
<span data-ttu-id="ad1d0-169">Lösen ordet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-169">The password of the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-170">-VmSku</span><span class="sxs-lookup"><span data-stu-id="ad1d0-170">-VmSku</span></span>
<span data-ttu-id="ad1d0-171">VM-SKU.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-171">The Vm Sku.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-172">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="ad1d0-172">-VmUserName</span></span>
<span data-ttu-id="ad1d0-173">Användar namnet för loggning till VM.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-173">The user name for logging to Vm.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-174">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad1d0-174">-Confirm</span></span>
<span data-ttu-id="ad1d0-175">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad1d0-176">-WhatIf</span></span>
<span data-ttu-id="ad1d0-177">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-177">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad1d0-178">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1d0-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1d0-179">CommonParameters</span></span>
<span data-ttu-id="ad1d0-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad1d0-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1d0-181">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad1d0-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1d0-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad1d0-182">INPUTS</span></span>

### <span data-ttu-id="ad1d0-183">System. String</span><span class="sxs-lookup"><span data-stu-id="ad1d0-183">System.String</span></span>
<span data-ttu-id="ad1d0-184">System. Security. SecureString system. Int32 Microsoft. Azure. commands. ServiceFabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ad1d0-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="ad1d0-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad1d0-185">OUTPUTS</span></span>

### <span data-ttu-id="ad1d0-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="ad1d0-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="ad1d0-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad1d0-187">NOTES</span></span>

## <span data-ttu-id="ad1d0-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad1d0-188">RELATED LINKS</span></span>

