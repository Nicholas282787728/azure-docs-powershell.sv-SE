---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: c1f6dea6c4fb103107a052d64a82ad81eafdb8c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585307"
---
# <span data-ttu-id="e1afc-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e1afc-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="e1afc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1afc-102">SYNOPSIS</span></span>
<span data-ttu-id="e1afc-103">I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="e1afc-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="e1afc-104">Den kan använda en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="e1afc-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="e1afc-105">Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="e1afc-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1afc-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1afc-106">SYNTAX</span></span>

### <span data-ttu-id="e1afc-107">ByDefaultArmTemplate (standard)</span><span class="sxs-lookup"><span data-stu-id="e1afc-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1afc-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="e1afc-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1afc-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="e1afc-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1afc-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="e1afc-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1afc-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1afc-111">DESCRIPTION</span></span>
<span data-ttu-id="e1afc-112">Med det **nya AzureRmServiceFabricCluster-** kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="e1afc-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="e1afc-113">Den mall som används kan vara en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="e1afc-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="e1afc-114">Du kan välja att ange en mapp för att exportera de självsignerade certifikaten eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="e1afc-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="e1afc-115">Om du anger en anpassad mall och en parameter fil behöver du inte ange certifikat informationen i parameter filen så fyller systemet i dessa parametrar.</span><span class="sxs-lookup"><span data-stu-id="e1afc-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="e1afc-116">De fyra alternativen är detaljerade nedan.</span><span class="sxs-lookup"><span data-stu-id="e1afc-116">The four options are detailed below.</span></span> <span data-ttu-id="e1afc-117">Rulla nedåt för att få förklaringar till alla parametrar.</span><span class="sxs-lookup"><span data-stu-id="e1afc-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="e1afc-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1afc-118">EXAMPLES</span></span>

### <span data-ttu-id="e1afc-119">Exempel 1: Ange bara kluster storleken, certifikatets ämnes namn och operativ systemet för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="e1afc-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "create cluster in " $clusterloc "subject name for cert " $subname "and output the cert into " $pfxfolder

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pwd -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -OS WindowsServer2016Datacenter
```

<span data-ttu-id="e1afc-120">Det här kommandot anger endast kluster storleken, certifikatets ämnes namn och operativ systemet för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="e1afc-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="e1afc-121">Exempel 2: Ange en befintlig certifikat resurs i ett nyckelord och en anpassad mall för att distribuera ett kluster</span><span class="sxs-lookup"><span data-stu-id="e1afc-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secertId
```

<span data-ttu-id="e1afc-122">Det här kommandot anger en befintlig certifikat resurs i ett nyckelord och en anpassad mall för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="e1afc-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="e1afc-123">Exempel 3: skapa ett nytt kluster med en anpassad mall.</span><span class="sxs-lookup"><span data-stu-id="e1afc-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="e1afc-124">Ange det olika RG namnet på Key-valvet och låt systemet Ladda upp certifikatet till det</span><span class="sxs-lookup"><span data-stu-id="e1afc-124">Specify the different RG name for the key vault and have the system upload the certificate to it</span></span>
```
$pwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/55ec7c4dc61a462bbc645ffc9b4b225f"
$thumprint="C2D7E11DD35153A702A51D10A424A3014B9B6E8B"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="e1afc-125">Det här kommandot skapar ett nytt kluster med en anpassad mall.</span><span class="sxs-lookup"><span data-stu-id="e1afc-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="e1afc-126">Ange ett annat RG namn för Key Vault och låt systemet Ladda upp certifikatet till det.</span><span class="sxs-lookup"><span data-stu-id="e1afc-126">Specify the different RG name for the key vault and have the system upload the certificate to it.</span></span>

### <span data-ttu-id="e1afc-127">Exempel 4: skaffa ett eget certifikat och en anpassad mall och skapa ett nytt kluster</span><span class="sxs-lookup"><span data-stu-id="e1afc-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$certPwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateSourceFile $pfxsourcefile -CertificatePassword $certpwd -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="e1afc-128">Med det här kommandot kan du föra in ett eget certifikat och en anpassad mall och skapa ett nytt kluster.</span><span class="sxs-lookup"><span data-stu-id="e1afc-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="e1afc-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1afc-129">PARAMETERS</span></span>

### <span data-ttu-id="e1afc-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e1afc-130">-CertificateFile</span></span>
<span data-ttu-id="e1afc-131">Den befintliga certifikats fil Sök vägen för det primära kluster certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e1afc-131">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="e1afc-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="e1afc-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="e1afc-133">Mappen för den nya certifikat filen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e1afc-133">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="e1afc-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e1afc-134">-CertificatePassword</span></span>
<span data-ttu-id="e1afc-135">Lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="e1afc-135">The password of the certificate file.</span></span>

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

### <span data-ttu-id="e1afc-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="e1afc-136">-CertificateSubjectName</span></span>
<span data-ttu-id="e1afc-137">Ämnes namnet för det certifikat som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e1afc-137">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="e1afc-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="e1afc-138">-ClusterSize</span></span>
<span data-ttu-id="e1afc-139">Antalet noder i klustret.</span><span class="sxs-lookup"><span data-stu-id="e1afc-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="e1afc-140">Standardvärden är 5 noder.</span><span class="sxs-lookup"><span data-stu-id="e1afc-140">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="e1afc-141">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="e1afc-141">-KeyVaultName</span></span>
<span data-ttu-id="e1afc-142">Namn på Azure Key valv.</span><span class="sxs-lookup"><span data-stu-id="e1afc-142">Azure key vault name.</span></span> <span data-ttu-id="e1afc-143">Om inget anges blir det standard namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e1afc-143">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="e1afc-144">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1afc-144">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="e1afc-145">Namnet på Azure Key valv-resursen.</span><span class="sxs-lookup"><span data-stu-id="e1afc-145">Azure key vault resource group name.</span></span> <span data-ttu-id="e1afc-146">Om det inte anges blir det standard namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e1afc-146">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="e1afc-147">-Plats</span><span class="sxs-lookup"><span data-stu-id="e1afc-147">-Location</span></span>
<span data-ttu-id="e1afc-148">Resurs gruppens plats.</span><span class="sxs-lookup"><span data-stu-id="e1afc-148">The resource group location.</span></span>

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

### <span data-ttu-id="e1afc-149">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1afc-149">-Name</span></span>
<span data-ttu-id="e1afc-150">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="e1afc-150">Specify the name of the cluster.</span></span> <span data-ttu-id="e1afc-151">Om det inte anges kommer det att vara samma som resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e1afc-151">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="e1afc-152">-OS</span><span class="sxs-lookup"><span data-stu-id="e1afc-152">-OS</span></span>
<span data-ttu-id="e1afc-153">Operativ systemet för de virtuella datorer som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="e1afc-153">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="e1afc-154">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="e1afc-154">-ParameterFile</span></span>
<span data-ttu-id="e1afc-155">Sökvägen till mallnamnet.</span><span class="sxs-lookup"><span data-stu-id="e1afc-155">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="e1afc-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1afc-156">-ResourceGroupName</span></span>
<span data-ttu-id="e1afc-157">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e1afc-157">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e1afc-158">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="e1afc-158">-SecondaryCertificateFile</span></span>
<span data-ttu-id="e1afc-159">Den befintliga certifikats fil Sök vägen för det sekundära kluster certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e1afc-159">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="e1afc-160">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e1afc-160">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="e1afc-161">Lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="e1afc-161">The password of the certificate file.</span></span>

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

### <span data-ttu-id="e1afc-162">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="e1afc-162">-SecretIdentifier</span></span>
<span data-ttu-id="e1afc-163">Den hemliga URL-adressen för Azure Key-valvet, till exempel: ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="e1afc-163">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="e1afc-164">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e1afc-164">-TemplateFile</span></span>
<span data-ttu-id="e1afc-165">Sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="e1afc-165">The path to the template file.</span></span>

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

### <span data-ttu-id="e1afc-166">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="e1afc-166">-VmPassword</span></span>
<span data-ttu-id="e1afc-167">Lösen ordet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e1afc-167">The password of the Vm.</span></span>

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

### <span data-ttu-id="e1afc-168">-VmSku</span><span class="sxs-lookup"><span data-stu-id="e1afc-168">-VmSku</span></span>
<span data-ttu-id="e1afc-169">VM-SKU.</span><span class="sxs-lookup"><span data-stu-id="e1afc-169">The Vm Sku.</span></span>

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

### <span data-ttu-id="e1afc-170">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="e1afc-170">-VmUserName</span></span>
<span data-ttu-id="e1afc-171">Användar namnet för loggning till VM.</span><span class="sxs-lookup"><span data-stu-id="e1afc-171">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="e1afc-172">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1afc-172">-Confirm</span></span>
<span data-ttu-id="e1afc-173">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1afc-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1afc-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1afc-174">-WhatIf</span></span>
<span data-ttu-id="e1afc-175">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1afc-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1afc-176">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1afc-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1afc-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1afc-177">-DefaultProfile</span></span>
<span data-ttu-id="e1afc-178">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1afc-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1afc-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1afc-179">CommonParameters</span></span>
<span data-ttu-id="e1afc-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1afc-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1afc-181">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1afc-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1afc-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1afc-182">INPUTS</span></span>

### <span data-ttu-id="e1afc-183">System. String</span><span class="sxs-lookup"><span data-stu-id="e1afc-183">System.String</span></span>
<span data-ttu-id="e1afc-184">System. Security. SecureString system. Int32 Microsoft. Azure. commands. ServiceFabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e1afc-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="e1afc-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1afc-185">OUTPUTS</span></span>

### <span data-ttu-id="e1afc-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="e1afc-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="e1afc-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1afc-187">NOTES</span></span>

## <span data-ttu-id="e1afc-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1afc-188">RELATED LINKS</span></span>

