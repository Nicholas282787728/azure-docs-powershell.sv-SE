---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 0c3fe2ffc9e5ce74c991e182ef1112629f05b88a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919927"
---
# <span data-ttu-id="7abd6-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="7abd6-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="7abd6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7abd6-102">SYNOPSIS</span></span>
<span data-ttu-id="7abd6-103">I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="7abd6-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="7abd6-104">Den kan använda en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="7abd6-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="7abd6-105">Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="7abd6-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

## <span data-ttu-id="7abd6-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7abd6-106">SYNTAX</span></span>

### <span data-ttu-id="7abd6-107">ByDefaultArmTemplate (standard)</span><span class="sxs-lookup"><span data-stu-id="7abd6-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7abd6-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="7abd6-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7abd6-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="7abd6-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7abd6-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="7abd6-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7abd6-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7abd6-111">DESCRIPTION</span></span>
<span data-ttu-id="7abd6-112">Med det **nya AzServiceFabricCluster-** kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="7abd6-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="7abd6-113">Den mall som används kan vara en standardmall eller en anpassad mall som du anger.</span><span class="sxs-lookup"><span data-stu-id="7abd6-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="7abd6-114">Du kan välja att ange en mapp för att exportera de självsignerade certifikaten eller hämta dem senare från huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="7abd6-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="7abd6-115">Om du anger en anpassad mall och en parameter fil behöver du inte ange certifikat informationen i parameter filen så fyller systemet i dessa parametrar.</span><span class="sxs-lookup"><span data-stu-id="7abd6-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="7abd6-116">De fyra alternativen är detaljerade nedan.</span><span class="sxs-lookup"><span data-stu-id="7abd6-116">The four options are detailed below.</span></span> <span data-ttu-id="7abd6-117">Rulla nedåt för att få förklaringar till alla parametrar.</span><span class="sxs-lookup"><span data-stu-id="7abd6-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="7abd6-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7abd6-118">EXAMPLES</span></span>

### <span data-ttu-id="7abd6-119">Exempel 1: Ange bara kluster storleken, certifikatets ämnes namn och operativ systemet för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="7abd6-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="c:\certs"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 5 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="7abd6-120">Det här kommandot anger endast kluster storleken, certifikatets ämnes namn och operativ systemet för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="7abd6-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="7abd6-121">Exempel 2: Ange en befintlig certifikat resurs i ett nyckelord och en anpassad mall för att distribuera ett kluster</span><span class="sxs-lookup"><span data-stu-id="7abd6-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="7abd6-122">Det här kommandot anger en befintlig certifikat resurs i ett nyckelord och en anpassad mall för att distribuera ett kluster.</span><span class="sxs-lookup"><span data-stu-id="7abd6-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="7abd6-123">Exempel 3: skapa ett nytt kluster med en anpassad mall.</span><span class="sxs-lookup"><span data-stu-id="7abd6-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="7abd6-124">Ange ett annat resurs grupp namn för Key Vault och låta systemet överföra ett nytt certifikat till det</span><span class="sxs-lookup"><span data-stu-id="7abd6-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
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

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResourceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="7abd6-125">Det här kommandot skapar ett nytt kluster med en anpassad mall.</span><span class="sxs-lookup"><span data-stu-id="7abd6-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="7abd6-126">Ange ett annat resurs grupp namn för Key Vault och låta systemet överföra ett nytt certifikat till det</span><span class="sxs-lookup"><span data-stu-id="7abd6-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="7abd6-127">Exempel 4: skaffa ett eget certifikat och en anpassad mall och skapa ett nytt kluster</span><span class="sxs-lookup"><span data-stu-id="7abd6-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResourceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="7abd6-128">Med det här kommandot kan du föra in ett eget certifikat och en anpassad mall och skapa ett nytt kluster.</span><span class="sxs-lookup"><span data-stu-id="7abd6-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="7abd6-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7abd6-129">PARAMETERS</span></span>

### <span data-ttu-id="7abd6-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="7abd6-130">-CertificateCommonName</span></span>
<span data-ttu-id="7abd6-131">Certifikatets nätverks namn</span><span class="sxs-lookup"><span data-stu-id="7abd6-131">Certificate common name</span></span>

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

### <span data-ttu-id="7abd6-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7abd6-132">-CertificateFile</span></span>
<span data-ttu-id="7abd6-133">Befintlig sökväg till certifikat filen för det primära kluster certifikatet</span><span class="sxs-lookup"><span data-stu-id="7abd6-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="7abd6-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="7abd6-134">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="7abd6-135">Certifikat utfärdarens tumavtryck, avgränsade med kommatecken om fler än en</span><span class="sxs-lookup"><span data-stu-id="7abd6-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="7abd6-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="7abd6-136">-CertificateOutputFolder</span></span>
<span data-ttu-id="7abd6-137">Mappen för den nya certifikat filen som ska skapas</span><span class="sxs-lookup"><span data-stu-id="7abd6-137">The folder of the new certificate file to be created</span></span>

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

### <span data-ttu-id="7abd6-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7abd6-138">-CertificatePassword</span></span>
<span data-ttu-id="7abd6-139">Lösen ordet för certifikat filen</span><span class="sxs-lookup"><span data-stu-id="7abd6-139">The password of the certificate file</span></span>

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

### <span data-ttu-id="7abd6-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="7abd6-140">-CertificateSubjectName</span></span>
<span data-ttu-id="7abd6-141">Ämnes namnet för det certifikat som ska skapas</span><span class="sxs-lookup"><span data-stu-id="7abd6-141">The subject name of the certificate to be created</span></span>

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

### <span data-ttu-id="7abd6-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="7abd6-142">-ClusterSize</span></span>
<span data-ttu-id="7abd6-143">Antalet noder i klustret.</span><span class="sxs-lookup"><span data-stu-id="7abd6-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="7abd6-144">Standardvärden är 5</span><span class="sxs-lookup"><span data-stu-id="7abd6-144">Default are 5 nodes</span></span>

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

### <span data-ttu-id="7abd6-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abd6-145">-DefaultProfile</span></span>
<span data-ttu-id="7abd6-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7abd6-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7abd6-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="7abd6-147">-KeyVaultName</span></span>
<span data-ttu-id="7abd6-148">Namn på Azure-valv om det inte anges blir det standard namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="7abd6-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="7abd6-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7abd6-149">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="7abd6-150">Resurs grupp namn för Azure-valv om det inte anges blir det standard för resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7abd6-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="7abd6-151">-Plats</span><span class="sxs-lookup"><span data-stu-id="7abd6-151">-Location</span></span>
<span data-ttu-id="7abd6-152">Resurs gruppens plats</span><span class="sxs-lookup"><span data-stu-id="7abd6-152">The resource group location</span></span>

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

### <span data-ttu-id="7abd6-153">-Namn</span><span class="sxs-lookup"><span data-stu-id="7abd6-153">-Name</span></span>
<span data-ttu-id="7abd6-154">Ange namnet på klustret, om det inte anges kommer det att vara samma som resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="7abd6-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

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

### <span data-ttu-id="7abd6-155">-OS</span><span class="sxs-lookup"><span data-stu-id="7abd6-155">-OS</span></span>
<span data-ttu-id="7abd6-156">Operativ systemet för de virtuella datorer som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="7abd6-156">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="7abd6-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="7abd6-157">-ParameterFile</span></span>
<span data-ttu-id="7abd6-158">Sökvägen till mallnamnet.</span><span class="sxs-lookup"><span data-stu-id="7abd6-158">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="7abd6-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7abd6-159">-ResourceGroupName</span></span>
<span data-ttu-id="7abd6-160">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7abd6-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7abd6-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="7abd6-161">-SecondaryCertificateFile</span></span>
<span data-ttu-id="7abd6-162">Befintlig sökväg till certifikat filen för det sekundära kluster certifikatet</span><span class="sxs-lookup"><span data-stu-id="7abd6-162">The existing certificate file path for the secondary cluster certificate</span></span>

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

### <span data-ttu-id="7abd6-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7abd6-163">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="7abd6-164">Lösen ordet för certifikat filen</span><span class="sxs-lookup"><span data-stu-id="7abd6-164">The password of the certificate file</span></span>

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

### <span data-ttu-id="7abd6-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="7abd6-165">-SecretIdentifier</span></span>
<span data-ttu-id="7abd6-166">Den befintliga hemliga URL-adressen för Azure Key Vault, till exempel " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="7abd6-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="7abd6-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="7abd6-167">-TemplateFile</span></span>
<span data-ttu-id="7abd6-168">Sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="7abd6-168">The path to the template file.</span></span>

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

### <span data-ttu-id="7abd6-169">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="7abd6-169">-VmPassword</span></span>
<span data-ttu-id="7abd6-170">Lösen ordet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7abd6-170">The password of the Vm.</span></span>

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

### <span data-ttu-id="7abd6-171">-VmSku</span><span class="sxs-lookup"><span data-stu-id="7abd6-171">-VmSku</span></span>
<span data-ttu-id="7abd6-172">VM-SKU</span><span class="sxs-lookup"><span data-stu-id="7abd6-172">The Vm Sku</span></span>

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

### <span data-ttu-id="7abd6-173">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="7abd6-173">-VmUserName</span></span>
<span data-ttu-id="7abd6-174">Användar namn för loggning till VM</span><span class="sxs-lookup"><span data-stu-id="7abd6-174">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="7abd6-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7abd6-175">-Confirm</span></span>
<span data-ttu-id="7abd6-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7abd6-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7abd6-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7abd6-177">-WhatIf</span></span>
<span data-ttu-id="7abd6-178">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7abd6-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7abd6-179">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7abd6-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7abd6-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abd6-180">CommonParameters</span></span>
<span data-ttu-id="7abd6-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7abd6-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abd6-182">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7abd6-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abd6-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7abd6-183">INPUTS</span></span>

### <span data-ttu-id="7abd6-184">System. String</span><span class="sxs-lookup"><span data-stu-id="7abd6-184">System.String</span></span>

### <span data-ttu-id="7abd6-185">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="7abd6-185">System.Security.SecureString</span></span>

### <span data-ttu-id="7abd6-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7abd6-186">System.Int32</span></span>

### <span data-ttu-id="7abd6-187">Microsoft. Azure. commands. ServiceFabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7abd6-187">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="7abd6-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7abd6-188">OUTPUTS</span></span>

### <span data-ttu-id="7abd6-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="7abd6-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="7abd6-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7abd6-190">NOTES</span></span>

## <span data-ttu-id="7abd6-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7abd6-191">RELATED LINKS</span></span>
