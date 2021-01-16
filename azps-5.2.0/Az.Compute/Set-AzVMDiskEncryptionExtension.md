---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 1c69d79e148eae92307855ecfe308f5208a2f455
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398744"
---
# <span data-ttu-id="0a6a8-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0a6a8-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="0a6a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6a8-103">Aktiverar kryptering på en virtuell dator med IaaS i Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="0a6a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a6a8-104">SYNTAX</span></span>

### <span data-ttu-id="0a6a8-105">SinglePassParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0a6a8-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a6a8-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a6a8-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a6a8-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a6a8-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a6a8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a6a8-108">DESCRIPTION</span></span>
<span data-ttu-id="0a6a8-109">Cmdleten **set-AzVMDiskEncryptionExtension** aktiverar kryptering på en infrastruktur som körs som en tjänst (IaaS) virtuell dator i Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="0a6a8-110">Den aktiverar kryptering genom att installera disk krypterings tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="0a6a8-111">Denna cmdlet kräver att användarna kan bekräftas genom att starta om datorn.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="0a6a8-112">Vi rekommenderar att du sparar ditt arbete på den virtuella datorn innan du kör denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="0a6a8-113">Linux: parametern **VolumeType** är obligatorisk när du krypterar virtuella Linux-datorer och måste vara inställd på ett värde ("OS", "data" eller "all") som stöds av Linux-distributionen.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="0a6a8-114">Windows: parametern **VolumeType** kan utelämnas, vilket innebär att operationen är standardvärdet för alla; Om parametern VolumeType finns för en virtuell Windows-dator måste den vara inställd på antingen all eller OS.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="0a6a8-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a6a8-115">EXAMPLES</span></span>

### <span data-ttu-id="0a6a8-116">Exempel 1: Aktivera kryptering</span><span class="sxs-lookup"><span data-stu-id="0a6a8-116">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="0a6a8-117">Det här exemplet aktiverar kryptering på en virtuell dator utan att ange autentiseringsuppgifter för annonser.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="0a6a8-118">Exempel 2: Aktivera kryptering med inlednings ingång</span><span class="sxs-lookup"><span data-stu-id="0a6a8-118">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzVmDiskEncryptionExtension
```

<span data-ttu-id="0a6a8-119">I det här exemplet skickas parametrar med pipeline-inmatning för att aktivera kryptering på en virtuell dator utan att ange autentiseringsuppgifter för annonser.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="0a6a8-120">Exempel 3: Aktivera kryptering med Azure AD-klient-ID och klient hemlighet</span><span class="sxs-lookup"><span data-stu-id="0a6a8-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="0a6a8-121">I det här exemplet används Azure AD-klient-ID och klient hemlighet för att aktivera kryptering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="0a6a8-122">Exempel 4: Aktivera kryptering med Azure AD-klient-ID och klient certifierings-tumavtryck</span><span class="sxs-lookup"><span data-stu-id="0a6a8-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="0a6a8-123">I det här exemplet används Azure AD-klient-ID och klient certifierings thumbprints för att aktivera kryptering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="0a6a8-124">Exempel 5: Aktivera kryptering med Azure AD Client-ID, klient hemlighet och wrap disk krypterings nyckel med nyckel krypterings nyckel</span><span class="sxs-lookup"><span data-stu-id="0a6a8-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="0a6a8-125">I det här exemplet används Azure AD-klient-ID och klient hemlighet för att aktivera kryptering på en virtuell dator och vid inskrivning av disk krypterings nyckel med en nyckel krypterings nyckel.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="0a6a8-126">Exempel 6: Aktivera kryptering med Azure AD-klient-ID, klient certifikat-tumavtryck och encryptionKey med hjälp av Key Encryption Key</span><span class="sxs-lookup"><span data-stu-id="0a6a8-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid
$VolumeType = "All"

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="0a6a8-127">I det här exemplet används ett Azure AD-klient-ID och ett tumavtryck för klient certifikat för att aktivera kryptering på en virtuell dator och för att kapsla in disk krypterings knappen med en krypterings nycklar.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="0a6a8-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a6a8-128">PARAMETERS</span></span>

### <span data-ttu-id="0a6a8-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="0a6a8-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="0a6a8-130">Anger tumavtrycket för det AzureActive-katalog (Azure AD)-klient certifikat som har **behörighet att skriva** hemligheter till ett par.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="0a6a8-131">Som förutsättning måste Azure AD client-certifikatet distribueras till den virtuella datorns `my` certifikat arkiv.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="0a6a8-132">Add-AzVMSecret cmdlet kan användas för att distribuera ett certifikat till en virtuell dator i Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="0a6a8-133">Mer information finns i hjälp för cmdleten **Add-AzVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="0a6a8-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="0a6a8-134">Certifikatet måste först distribueras till den virtuella datorn lokal dator mitt certifikat arkiv.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="0a6a8-135">-AadClientID</span></span>
<span data-ttu-id="0a6a8-136">Anger klient-ID för Azure AD-programmet som har **behörighet att skriva** hemligheter till ett par.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="0a6a8-137">-AadClientSecret</span></span>
<span data-ttu-id="0a6a8-138">Anger klient hemlighet för Azure AD-programmet som har behörighet att skriva hemligheter till ett nyckel **valv**.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6a8-139">-DefaultProfile</span></span>
<span data-ttu-id="0a6a8-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a6a8-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0a6a8-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0a6a8-142">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0a6a8-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="0a6a8-144">Anger resurs-ID för det nyckel **valv** där krypterings nycklarna för den virtuella datorn ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="0a6a8-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="0a6a8-146">Anger den URL till nyckel **valvet** som den virtuella datorns krypterings nycklar ska laddas upp till.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="0a6a8-147">-EncryptFormatAll</span></span>
<span data-ttu-id="0a6a8-148">Encrypt-Format alla data enheter som inte redan är krypterade</span><span class="sxs-lookup"><span data-stu-id="0a6a8-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="0a6a8-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="0a6a8-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="0a6a8-150">Tillägget utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-150">The extension publisher name.</span></span> <span data-ttu-id="0a6a8-151">Ange endast den här parametern om du vill åsidosätta standardvärdet för "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="0a6a8-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="0a6a8-152">-ExtensionType</span></span>
<span data-ttu-id="0a6a8-153">Fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-153">The extension type.</span></span> <span data-ttu-id="0a6a8-154">Ange den här parametern om du vill åsidosätta standardvärdet "AzureDiskEncryption" för Windows-VMs och "AzureDiskEncryptionForLinux" för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-155">-Force</span><span class="sxs-lookup"><span data-stu-id="0a6a8-155">-Force</span></span>
<span data-ttu-id="0a6a8-156">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a6a8-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0a6a8-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="0a6a8-158">Anger den algoritm som används för att radbryta och packa upp den virtuella datorns krypterings nycklar.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="0a6a8-159">Standardvärdet är RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-159">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="0a6a8-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="0a6a8-161">Anger URL-adressen till den Key Encryption Key som används för att radbryta och packa upp den virtuella dator krypterings knappen.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="0a6a8-162">Det måste vara den fullständiga versionen av URL: en.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-162">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0a6a8-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="0a6a8-164">Anger resurs-ID för det nyckelord som innehåller en krypterings **nycklar som används** för att radbryta och avbryta den virtuella dator krypterings knappen.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="0a6a8-165">Det måste vara en fullständig version av URL.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-165">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-166">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a6a8-166">-Name</span></span>
<span data-ttu-id="0a6a8-167">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="0a6a8-168">Om parametern *Name* utelämnas får det installerade tillägget namnet AzureDiskEncryption på Windows Virtual Machines och AzureDiskEncryptionForLinux på virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-169">-Lösen fras</span><span class="sxs-lookup"><span data-stu-id="0a6a8-169">-Passphrase</span></span>
<span data-ttu-id="0a6a8-170">Anger den lösen fras som endast används för att kryptera virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="0a6a8-171">Den här parametern används inte för virtuella datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6a8-172">-ResourceGroupName</span></span>
<span data-ttu-id="0a6a8-173">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0a6a8-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="0a6a8-174">-SequenceVersion</span></span>
<span data-ttu-id="0a6a8-175">Anger sekvensnumret för krypterings åtgärderna för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="0a6a8-176">Detta är unikt för varje krypterings åtgärd som utförs på samma virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="0a6a8-177">Get-AzVMExtension cmdlet kan användas för att hämta föregående serie nummer som användes.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="0a6a8-178">-SkipVmBackup</span></span>
<span data-ttu-id="0a6a8-179">Hoppa över skapande av säkerhets kopiering för Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="0a6a8-179">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0a6a8-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="0a6a8-181">Anger krypterings tillägget.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-181">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="0a6a8-182">-VMName</span></span>
<span data-ttu-id="0a6a8-183">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-183">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-184">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="0a6a8-184">-VolumeType</span></span>
<span data-ttu-id="0a6a8-185">Anger den typ av volym för virtuell dator som du vill utföra krypteringen på: OS, data eller alla.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="0a6a8-186">Linux: parametern **VolumeType** är obligatorisk när du krypterar virtuella Linux-datorer och måste vara inställd på ett värde ("OS", "data" eller "all") som stöds av Linux-distributionen.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="0a6a8-187">Windows: parametern **VolumeType** kan utelämnas, vilket innebär att operationen är standardvärdet för alla; Om parametern VolumeType finns för en virtuell Windows-dator måste den vara inställd på antingen all eller OS.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-188">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a6a8-188">-Confirm</span></span>
<span data-ttu-id="0a6a8-189">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-189">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a6a8-190">-WhatIf</span></span>
<span data-ttu-id="0a6a8-191">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a6a8-192">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-192">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6a8-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6a8-193">CommonParameters</span></span>
<span data-ttu-id="0a6a8-194">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6a8-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6a8-195">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a6a8-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6a8-196">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a6a8-196">INPUTS</span></span>

### <span data-ttu-id="0a6a8-197">System. String</span><span class="sxs-lookup"><span data-stu-id="0a6a8-197">System.String</span></span>

### <span data-ttu-id="0a6a8-198">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0a6a8-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0a6a8-199">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a6a8-199">OUTPUTS</span></span>

### <span data-ttu-id="0a6a8-200">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0a6a8-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0a6a8-201">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a6a8-201">NOTES</span></span>

## <span data-ttu-id="0a6a8-202">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a6a8-202">RELATED LINKS</span></span>

[<span data-ttu-id="0a6a8-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="0a6a8-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="0a6a8-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="0a6a8-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="0a6a8-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0a6a8-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


