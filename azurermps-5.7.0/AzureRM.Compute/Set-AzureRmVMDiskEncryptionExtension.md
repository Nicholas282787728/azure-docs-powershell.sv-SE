---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: ed18e7de10df5762309f3bcd4ddf6dcee7ee1b94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755980"
---
# <span data-ttu-id="fcd6d-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="fcd6d-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="fcd6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fcd6d-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd6d-103">Aktiverar kryptering på en virtuell dator med IaaS i Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcd6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fcd6d-104">SYNTAX</span></span>

### <span data-ttu-id="fcd6d-105">AAD-parametrar för klient hemlighet (standard)</span><span class="sxs-lookup"><span data-stu-id="fcd6d-105">AAD Client Secret Parameters (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcd6d-106">AAD-parametrar för klient certifikat</span><span class="sxs-lookup"><span data-stu-id="fcd6d-106">AAD Client Cert Parameters</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcd6d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fcd6d-107">DESCRIPTION</span></span>
<span data-ttu-id="fcd6d-108">Cmdleten **set-AzureRmVMDiskEncryptionExtension** aktiverar kryptering på en infrastruktur som körs som en tjänst (IaaS) virtuell dator i Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="fcd6d-109">Denna cmdlet aktiverar kryptering genom att installera disk krypterings tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="fcd6d-110">Om ingen *namn* parameter anges installeras ett tillägg med standard namnet AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="fcd6d-111">Denna cmdlet kräver att användarna kan bekräftas genom att starta om datorn.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="fcd6d-112">Vi rekommenderar att du sparar ditt arbete på den virtuella datorn innan du kör denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="fcd6d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fcd6d-113">EXAMPLES</span></span>

### <span data-ttu-id="fcd6d-114">Exempel 1: Aktivera kryptering med Azure AD-klient-ID och klient hemlighet</span><span class="sxs-lookup"><span data-stu-id="fcd6d-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="fcd6d-115">Det här exemplet aktiverar kryptering med Azure AD-klient-ID och klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="fcd6d-116">Exempel 2: Aktivera kryptering med Azure AD-klient-ID och klient certifierings-tumavtryck</span><span class="sxs-lookup"><span data-stu-id="fcd6d-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="fcd6d-117">Det här exemplet aktiverar kryptering med Azure AD-klient-ID och klient certifierings thumbprints.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="fcd6d-118">Exempel 3: Aktivera kryptering med Azure AD Client-ID, klient hemlighet och wrap disk krypterings nyckel med nyckel krypterings nyckel</span><span class="sxs-lookup"><span data-stu-id="fcd6d-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="fcd6d-119">I det här exemplet aktive ras kryptering med Azure AD Client-ID, klient hemlighet och wrap disk krypterings nyckel med nyckel krypterings nyckel.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="fcd6d-120">Exempel 4: Aktivera kryptering med Azure AD-klient-ID, klient certifikat-tumavtryck och encryptionKey med hjälp av Key Encryption Key</span><span class="sxs-lookup"><span data-stu-id="fcd6d-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="fcd6d-121">Det här exemplet aktiverar kryptering med Azure AD-klient-ID, klient certifikat-tumavtryck och wrap disk krypterings nycklar med hjälp av Key Encryption Key.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="fcd6d-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fcd6d-122">PARAMETERS</span></span>

### <span data-ttu-id="fcd6d-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="fcd6d-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="fcd6d-124">Anger tumavtrycket för det AzureActive-katalog (Azure AD)-klient certifikat som har **behörighet att skriva** hemligheter till ett par.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="fcd6d-125">Som förutsättning måste Azure AD client-certifikatet distribueras till den virtuella datorns `my` certifikat arkiv.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="fcd6d-126">Add-AzureRmVMSecret cmdlet kan användas för att distribuera ett certifikat till en virtuell dator i Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="fcd6d-127">Mer information finns i hjälp för cmdleten **Add-AzureRmVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="fcd6d-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="fcd6d-128">Certifikatet måste först distribueras till den virtuella datorn lokal dator mitt certifikat arkiv.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AAD Client Cert Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="fcd6d-129">-AadClientID</span></span>
<span data-ttu-id="fcd6d-130">Anger klient-ID för Azure AD-programmet som har **behörighet att skriva** hemligheter till ett par.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="fcd6d-131">-AadClientSecret</span></span>
<span data-ttu-id="fcd6d-132">Anger klient hemlighet för Azure AD-programmet som har behörighet att skriva hemligheter till ett nyckel **valv**.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AAD Client Secret Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-133">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fcd6d-133">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fcd6d-134">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-134">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-135">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="fcd6d-135">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="fcd6d-136">Anger resurs-ID för det nyckel **valv** där krypterings nycklarna för den virtuella datorn ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-136">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-137">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="fcd6d-137">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="fcd6d-138">Anger den URL till nyckel **valvet** som den virtuella datorns krypterings nycklar ska laddas upp till.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-138">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-139">-Force</span><span class="sxs-lookup"><span data-stu-id="fcd6d-139">-Force</span></span>
<span data-ttu-id="fcd6d-140">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-140">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-141">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="fcd6d-141">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="fcd6d-142">Anger den algoritm som används för att radbryta och packa upp den virtuella datorns krypterings nycklar.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-142">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="fcd6d-143">Standardvärdet är RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-143">The default value is RSA-OAEP.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-144">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="fcd6d-144">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="fcd6d-145">Anger URL-adressen till den Key Encryption Key som används för att radbryta och packa upp den virtuella dator krypterings knappen.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-145">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="fcd6d-146">Det måste vara den fullständiga versionen av URL: en.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-146">This must be the full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-147">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="fcd6d-147">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="fcd6d-148">Anger resurs-ID för det nyckelord som innehåller en krypterings **nycklar som används** för att radbryta och avbryta den virtuella dator krypterings knappen.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-148">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="fcd6d-149">Det måste vara en fullständig version av URL.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-149">This must be a full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="fcd6d-150">-Name</span></span>
<span data-ttu-id="fcd6d-151">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-151">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="fcd6d-152">Standardvärdet är AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-152">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-153">-Lösen fras</span><span class="sxs-lookup"><span data-stu-id="fcd6d-153">-Passphrase</span></span>
<span data-ttu-id="fcd6d-154">Anger den lösen fras som endast används för att kryptera virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-154">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="fcd6d-155">Den här parametern används inte för virtuella datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-155">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcd6d-156">-ResourceGroupName</span></span>
<span data-ttu-id="fcd6d-157">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-157">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fcd6d-158">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="fcd6d-158">-SequenceVersion</span></span>
<span data-ttu-id="fcd6d-159">Anger sekvensnumret för krypterings åtgärderna för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-159">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="fcd6d-160">Detta är unikt för varje krypterings åtgärd som utförs på samma virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-160">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="fcd6d-161">Get-AzureRmVMExtension cmdlet kan användas för att hämta föregående serie nummer som användes.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-161">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-162">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="fcd6d-162">-SkipVmBackup</span></span>
<span data-ttu-id="fcd6d-163">Hoppa över skapande av säkerhets kopiering för Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="fcd6d-163">Skip backup creation for Linux VMs</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fcd6d-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="fcd6d-165">Anger krypterings tillägget.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-165">Specifies the version of the encryption extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="fcd6d-166">-VMName</span></span>
<span data-ttu-id="fcd6d-167">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-167">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-168">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="fcd6d-168">-VolumeType</span></span>
<span data-ttu-id="fcd6d-169">Anger vilken typ av virtuell dator volym som ska utföra krypterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-169">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="fcd6d-170">Tillåtna värden för virtuella datorer som kör operativ systemet Windows är följande: alla, OS och data.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-170">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="fcd6d-171">De tillåtna värdena för virtuella Linux-datorer är följande: endast data.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-171">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-172">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fcd6d-172">-Confirm</span></span>
<span data-ttu-id="fcd6d-173">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-173">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcd6d-174">-WhatIf</span></span>
<span data-ttu-id="fcd6d-175">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-175">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fcd6d-176">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-176">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd6d-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd6d-177">CommonParameters</span></span>
<span data-ttu-id="fcd6d-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd6d-179">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcd6d-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd6d-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fcd6d-180">INPUTS</span></span>

### <span data-ttu-id="fcd6d-181">Ingen</span><span class="sxs-lookup"><span data-stu-id="fcd6d-181">None</span></span>
<span data-ttu-id="fcd6d-182">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="fcd6d-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fcd6d-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fcd6d-183">OUTPUTS</span></span>

## <span data-ttu-id="fcd6d-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fcd6d-184">NOTES</span></span>

## <span data-ttu-id="fcd6d-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fcd6d-185">RELATED LINKS</span></span>

[<span data-ttu-id="fcd6d-186">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="fcd6d-186">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="fcd6d-187">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="fcd6d-187">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="fcd6d-188">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="fcd6d-188">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


