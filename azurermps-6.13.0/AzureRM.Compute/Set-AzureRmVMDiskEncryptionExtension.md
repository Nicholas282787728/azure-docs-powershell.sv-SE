---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 3eb2c1c175f52f980ecd451bb7a9474984543f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577091"
---
# <span data-ttu-id="af9c7-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="af9c7-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="af9c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="af9c7-103">Aktiverar kryptering på en virtuell dator med IaaS i Azure.</span><span class="sxs-lookup"><span data-stu-id="af9c7-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af9c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af9c7-104">SYNTAX</span></span>

### <span data-ttu-id="af9c7-105">SinglePassParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="af9c7-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9c7-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="af9c7-106">AADClientSecretParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9c7-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="af9c7-107">AADClientCertParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af9c7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af9c7-108">DESCRIPTION</span></span>
<span data-ttu-id="af9c7-109">Cmdleten **set-AzureRmVMDiskEncryptionExtension** aktiverar kryptering på en infrastruktur som körs som en tjänst (IaaS) virtuell dator i Azure.</span><span class="sxs-lookup"><span data-stu-id="af9c7-109">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="af9c7-110">Denna cmdlet aktiverar kryptering genom att installera disk krypterings tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="af9c7-110">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="af9c7-111">Om ingen *namn* parameter anges installeras ett tillägg med standard namnet AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="af9c7-111">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="af9c7-112">Denna cmdlet kräver att användarna kan bekräftas genom att starta om datorn.</span><span class="sxs-lookup"><span data-stu-id="af9c7-112">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="af9c7-113">Vi rekommenderar att du sparar ditt arbete på den virtuella datorn innan du kör denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af9c7-113">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="af9c7-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af9c7-114">EXAMPLES</span></span>

### <span data-ttu-id="af9c7-115">Exempel 1: Aktivera kryptering</span><span class="sxs-lookup"><span data-stu-id="af9c7-115">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="af9c7-116">Det här exemplet visar hur du aktiverar kryptering utan att ange autentiseringsuppgifter för annonser.</span><span class="sxs-lookup"><span data-stu-id="af9c7-116">This example demonstrates enabling encryption without specifying AD credentials.</span></span>

### <span data-ttu-id="af9c7-117">Exempel 2: Aktivera kryptering med inlednings ingång</span><span class="sxs-lookup"><span data-stu-id="af9c7-117">Example 2: Enable encryption with pipelined input</span></span>
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

$params | Set-AzureRmVmDiskEncryptionExtension
```

<span data-ttu-id="af9c7-118">I det här exemplet visas hur du skickar parametrar genom att använda förflyttad inmatning för att aktivera kryptering utan att ange autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="af9c7-118">This example demonstrates sending parameters using pipelined input to enable encryption without specifying AD credentials.</span></span>

### <span data-ttu-id="af9c7-119">Exempel 3: Aktivera kryptering med Azure AD-klient-ID och klient hemlighet</span><span class="sxs-lookup"><span data-stu-id="af9c7-119">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="af9c7-120">Det här exemplet aktiverar kryptering med Azure AD-klient-ID och klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="af9c7-120">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="af9c7-121">Exempel 4: Aktivera kryptering med Azure AD-klient-ID och klient certifierings-tumavtryck</span><span class="sxs-lookup"><span data-stu-id="af9c7-121">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
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

<span data-ttu-id="af9c7-122">Det här exemplet aktiverar kryptering med Azure AD-klient-ID och klient certifierings thumbprints.</span><span class="sxs-lookup"><span data-stu-id="af9c7-122">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="af9c7-123">Exempel 5: Aktivera kryptering med Azure AD Client-ID, klient hemlighet och wrap disk krypterings nyckel med nyckel krypterings nyckel</span><span class="sxs-lookup"><span data-stu-id="af9c7-123">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="af9c7-124">I det här exemplet aktive ras kryptering med Azure AD Client-ID, klient hemlighet och wrap disk krypterings nyckel med nyckel krypterings nyckel.</span><span class="sxs-lookup"><span data-stu-id="af9c7-124">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="af9c7-125">Exempel 6: Aktivera kryptering med Azure AD-klient-ID, klient certifikat-tumavtryck och encryptionKey med hjälp av Key Encryption Key</span><span class="sxs-lookup"><span data-stu-id="af9c7-125">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
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
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="af9c7-126">Det här exemplet aktiverar kryptering med Azure AD-klient-ID, klient certifikat-tumavtryck och wrap disk krypterings nycklar med hjälp av Key Encryption Key.</span><span class="sxs-lookup"><span data-stu-id="af9c7-126">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="af9c7-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af9c7-127">PARAMETERS</span></span>

### <span data-ttu-id="af9c7-128">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="af9c7-128">-AadClientCertThumbprint</span></span>
<span data-ttu-id="af9c7-129">Anger tumavtrycket för det AzureActive-katalog (Azure AD)-klient certifikat som har **behörighet att skriva** hemligheter till ett par.</span><span class="sxs-lookup"><span data-stu-id="af9c7-129">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="af9c7-130">Som förutsättning måste Azure AD client-certifikatet distribueras till den virtuella datorns `my` certifikat arkiv.</span><span class="sxs-lookup"><span data-stu-id="af9c7-130">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="af9c7-131">Add-AzureRmVMSecret cmdlet kan användas för att distribuera ett certifikat till en virtuell dator i Azure.</span><span class="sxs-lookup"><span data-stu-id="af9c7-131">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="af9c7-132">Mer information finns i hjälp för cmdleten **Add-AzureRmVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="af9c7-132">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="af9c7-133">Certifikatet måste först distribueras till den virtuella datorn lokal dator mitt certifikat arkiv.</span><span class="sxs-lookup"><span data-stu-id="af9c7-133">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="af9c7-134">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="af9c7-134">-AadClientID</span></span>
<span data-ttu-id="af9c7-135">Anger klient-ID för Azure AD-programmet som har **behörighet att skriva** hemligheter till ett par.</span><span class="sxs-lookup"><span data-stu-id="af9c7-135">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="af9c7-136">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="af9c7-136">-AadClientSecret</span></span>
<span data-ttu-id="af9c7-137">Anger klient hemlighet för Azure AD-programmet som har behörighet att skriva hemligheter till ett nyckel **valv**.</span><span class="sxs-lookup"><span data-stu-id="af9c7-137">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="af9c7-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9c7-138">-DefaultProfile</span></span>
<span data-ttu-id="af9c7-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af9c7-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9c7-140">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="af9c7-140">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="af9c7-141">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="af9c7-141">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="af9c7-142">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="af9c7-142">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="af9c7-143">Anger resurs-ID för det nyckel **valv** där krypterings nycklarna för den virtuella datorn ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="af9c7-143">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="af9c7-144">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="af9c7-144">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="af9c7-145">Anger den URL till nyckel **valvet** som den virtuella datorns krypterings nycklar ska laddas upp till.</span><span class="sxs-lookup"><span data-stu-id="af9c7-145">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="af9c7-146">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="af9c7-146">-EncryptFormatAll</span></span>
<span data-ttu-id="af9c7-147">Encrypt-Format alla data enheter som inte redan är krypterade</span><span class="sxs-lookup"><span data-stu-id="af9c7-147">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="af9c7-148">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="af9c7-148">-ExtensionPublisherName</span></span>
<span data-ttu-id="af9c7-149">Tillägget utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="af9c7-149">The extension publisher name.</span></span> <span data-ttu-id="af9c7-150">Ange endast den här parametern om du vill åsidosätta standardvärdet för "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="af9c7-150">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="af9c7-151">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="af9c7-151">-ExtensionType</span></span>
<span data-ttu-id="af9c7-152">Fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="af9c7-152">The extension type.</span></span> <span data-ttu-id="af9c7-153">Ange den här parametern om du vill åsidosätta standardvärdet "AzureDiskEncryption" för Windows-VMs och "AzureDiskEncryptionForLinux" för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="af9c7-153">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="af9c7-154">-Force</span><span class="sxs-lookup"><span data-stu-id="af9c7-154">-Force</span></span>
<span data-ttu-id="af9c7-155">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="af9c7-155">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af9c7-156">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="af9c7-156">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="af9c7-157">Anger den algoritm som används för att radbryta och packa upp den virtuella datorns krypterings nycklar.</span><span class="sxs-lookup"><span data-stu-id="af9c7-157">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="af9c7-158">Standardvärdet är RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="af9c7-158">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="af9c7-159">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="af9c7-159">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="af9c7-160">Anger URL-adressen till den Key Encryption Key som används för att radbryta och packa upp den virtuella dator krypterings knappen.</span><span class="sxs-lookup"><span data-stu-id="af9c7-160">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="af9c7-161">Det måste vara den fullständiga versionen av URL: en.</span><span class="sxs-lookup"><span data-stu-id="af9c7-161">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="af9c7-162">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="af9c7-162">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="af9c7-163">Anger resurs-ID för det nyckelord som innehåller en krypterings **nycklar som används** för att radbryta och avbryta den virtuella dator krypterings knappen.</span><span class="sxs-lookup"><span data-stu-id="af9c7-163">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="af9c7-164">Det måste vara en fullständig version av URL.</span><span class="sxs-lookup"><span data-stu-id="af9c7-164">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="af9c7-165">-Namn</span><span class="sxs-lookup"><span data-stu-id="af9c7-165">-Name</span></span>
<span data-ttu-id="af9c7-166">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="af9c7-166">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="af9c7-167">Standardvärdet är AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="af9c7-167">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

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

### <span data-ttu-id="af9c7-168">-Lösen fras</span><span class="sxs-lookup"><span data-stu-id="af9c7-168">-Passphrase</span></span>
<span data-ttu-id="af9c7-169">Anger den lösen fras som endast används för att kryptera virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="af9c7-169">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="af9c7-170">Den här parametern används inte för virtuella datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="af9c7-170">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="af9c7-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9c7-171">-ResourceGroupName</span></span>
<span data-ttu-id="af9c7-172">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="af9c7-172">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="af9c7-173">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="af9c7-173">-SequenceVersion</span></span>
<span data-ttu-id="af9c7-174">Anger sekvensnumret för krypterings åtgärderna för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="af9c7-174">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="af9c7-175">Detta är unikt för varje krypterings åtgärd som utförs på samma virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="af9c7-175">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="af9c7-176">Get-AzureRmVMExtension cmdlet kan användas för att hämta föregående serie nummer som användes.</span><span class="sxs-lookup"><span data-stu-id="af9c7-176">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="af9c7-177">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="af9c7-177">-SkipVmBackup</span></span>
<span data-ttu-id="af9c7-178">Hoppa över skapande av säkerhets kopiering för Linux-datorer</span><span class="sxs-lookup"><span data-stu-id="af9c7-178">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="af9c7-179">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="af9c7-179">-TypeHandlerVersion</span></span>
<span data-ttu-id="af9c7-180">Anger krypterings tillägget.</span><span class="sxs-lookup"><span data-stu-id="af9c7-180">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="af9c7-181">-VMName</span><span class="sxs-lookup"><span data-stu-id="af9c7-181">-VMName</span></span>
<span data-ttu-id="af9c7-182">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="af9c7-182">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="af9c7-183">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="af9c7-183">-VolumeType</span></span>
<span data-ttu-id="af9c7-184">Anger vilken typ av virtuell dator volym som ska utföra krypterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="af9c7-184">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="af9c7-185">Tillåtna värden för virtuella datorer som kör operativ systemet Windows är följande: alla, OS och data.</span><span class="sxs-lookup"><span data-stu-id="af9c7-185">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="af9c7-186">De tillåtna värdena för virtuella dator datorer är följande: alla, operativ system och data när Linux distribueras.</span><span class="sxs-lookup"><span data-stu-id="af9c7-186">The allowed values for Linux virtual machines are as follows: All, OS, and Data when supported by the Linux distribution.</span></span>

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

### <span data-ttu-id="af9c7-187">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af9c7-187">-Confirm</span></span>
<span data-ttu-id="af9c7-188">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af9c7-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af9c7-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9c7-189">-WhatIf</span></span>
<span data-ttu-id="af9c7-190">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af9c7-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af9c7-191">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af9c7-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af9c7-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9c7-192">CommonParameters</span></span>
<span data-ttu-id="af9c7-193">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9c7-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9c7-194">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af9c7-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9c7-195">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af9c7-195">INPUTS</span></span>

### <span data-ttu-id="af9c7-196">System. String</span><span class="sxs-lookup"><span data-stu-id="af9c7-196">System.String</span></span>

### <span data-ttu-id="af9c7-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="af9c7-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="af9c7-198">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af9c7-198">OUTPUTS</span></span>

### <span data-ttu-id="af9c7-199">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="af9c7-199">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="af9c7-200">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af9c7-200">NOTES</span></span>

## <span data-ttu-id="af9c7-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af9c7-201">RELATED LINKS</span></span>

[<span data-ttu-id="af9c7-202">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="af9c7-202">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="af9c7-203">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="af9c7-203">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="af9c7-204">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="af9c7-204">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


