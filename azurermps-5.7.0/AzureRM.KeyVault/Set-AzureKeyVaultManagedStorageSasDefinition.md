---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 5a4c1effd1cbda4399e06f3b6db606cff87d8955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757937"
---
# <span data-ttu-id="02b9d-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="02b9d-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="02b9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="02b9d-103">Ställer in en säkerhets beskrivning för en delad åtkomst (SAS) med ett huvud valv för ett visst offentligt hanterat Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="02b9d-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02b9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02b9d-104">SYNTAX</span></span>

### <span data-ttu-id="02b9d-105">RawSas (standard)</span><span class="sxs-lookup"><span data-stu-id="02b9d-105">RawSas (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-106">AdhocAccountSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-107">AdhocServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-108">AdhocServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02b9d-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-109">AdhocServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-110">AdhocServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-111">AdhocServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-112">AdhocServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02b9d-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b9d-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="02b9d-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02b9d-119">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02b9d-119">DESCRIPTION</span></span>
<span data-ttu-id="02b9d-120">Ställer in en säkerhets beskrivning för en signatur (SAS) med ett angivet Azure Storage-konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="02b9d-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="02b9d-121">Detta anger också en hemlighet som kan användas för att hämta SAS-token per denna SAS-definition.</span><span class="sxs-lookup"><span data-stu-id="02b9d-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="02b9d-122">SAS-token genereras med de här parametrarna och den aktiva nyckeln för det hanterade Azure Storage-kontot för Key valv.</span><span class="sxs-lookup"><span data-stu-id="02b9d-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="02b9d-123">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02b9d-123">EXAMPLES</span></span>

### <span data-ttu-id="02b9d-124">Exempel 1: Ange en ad hoc-huvudassociation för BLOB</span><span class="sxs-lookup"><span data-stu-id="02b9d-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="02b9d-125">Ställer in en ad hoc service BLOB SAS-definitionen ' SAS1 ' med Key valv Managed Storage-kontot ' datorkonto1 ' i valvet ' vault1 '.</span><span class="sxs-lookup"><span data-stu-id="02b9d-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="02b9d-126">Exempel 2: Ange en ad hoc-huvuddefinition</span><span class="sxs-lookup"><span data-stu-id="02b9d-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="02b9d-127">Ställer in en ad hoc BLOB SAS-definitionen ' SAS1 ' med Key valv Managed Storage-kontot ' datorkonto1 ' i valvet ' vault1 '.</span><span class="sxs-lookup"><span data-stu-id="02b9d-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="02b9d-128">Exempel 3: Ange en SAS-definition med en hash</span><span class="sxs-lookup"><span data-stu-id="02b9d-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="02b9d-129">Ställer in en ad hoc BLOB SAS-definitionen ' SAS1 ' med Key valv Managed Storage-kontot ' datorkonto1 ' i valvet ' vault1 ' med en hash.</span><span class="sxs-lookup"><span data-stu-id="02b9d-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="02b9d-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02b9d-130">PARAMETERS</span></span>

### <span data-ttu-id="02b9d-131">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02b9d-131">-AccountName</span></span>
<span data-ttu-id="02b9d-132">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="02b9d-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="02b9d-133">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="02b9d-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="02b9d-134">-ApiVersion</span></span>
<span data-ttu-id="02b9d-135">Anger den lagrings tjänst version som ska användas för att utföra begäran som gjorts med hjälp av kontots SAS URI.</span><span class="sxs-lookup"><span data-stu-id="02b9d-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-136">-BLOB</span><span class="sxs-lookup"><span data-stu-id="02b9d-136">-Blob</span></span>
<span data-ttu-id="02b9d-137">BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="02b9d-137">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-138">-Container</span><span class="sxs-lookup"><span data-stu-id="02b9d-138">-Container</span></span>
<span data-ttu-id="02b9d-139">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="02b9d-139">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b9d-140">-DefaultProfile</span></span>
<span data-ttu-id="02b9d-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="02b9d-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02b9d-142">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="02b9d-142">-Disable</span></span>
<span data-ttu-id="02b9d-143">Inaktiverar användning av SAS-definition för generering av SAS-token.</span><span class="sxs-lookup"><span data-stu-id="02b9d-143">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="02b9d-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="02b9d-144">-EndPartitionKey</span></span>
<span data-ttu-id="02b9d-145">Avsluta partitionsnyckel</span><span class="sxs-lookup"><span data-stu-id="02b9d-145">End Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="02b9d-146">-EndRowKey</span></span>
<span data-ttu-id="02b9d-147">Slut rad</span><span class="sxs-lookup"><span data-stu-id="02b9d-147">End Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-148">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="02b9d-148">-IPAddressOrRange</span></span>
<span data-ttu-id="02b9d-149">IP-adress eller IP Range ACL (Access Control List) för begäran som skulle godkännas av Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="02b9d-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="02b9d-150">-Name</span></span>
<span data-ttu-id="02b9d-151">Namn på lagrings-sa.</span><span class="sxs-lookup"><span data-stu-id="02b9d-151">Storage sas definition name.</span></span> <span data-ttu-id="02b9d-152">Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.</span><span class="sxs-lookup"><span data-stu-id="02b9d-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-153">-Parameter</span><span class="sxs-lookup"><span data-stu-id="02b9d-153">-Parameter</span></span>
<span data-ttu-id="02b9d-154">SAS-definitionsfiler som används för att skapa SAS-token.</span><span class="sxs-lookup"><span data-stu-id="02b9d-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: Hashtable
Parameter Sets: RawSas
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-155">-Path</span><span class="sxs-lookup"><span data-stu-id="02b9d-155">-Path</span></span>
<span data-ttu-id="02b9d-156">Sökväg till moln filen för att skapa SAS-token.</span><span class="sxs-lookup"><span data-stu-id="02b9d-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-157">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="02b9d-157">-Permission</span></span>
<span data-ttu-id="02b9d-158">Tillåtelse.</span><span class="sxs-lookup"><span data-stu-id="02b9d-158">Permission.</span></span> <span data-ttu-id="02b9d-159">Värden inkluderar "fråga", "Lägg till", "process"</span><span class="sxs-lookup"><span data-stu-id="02b9d-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases:
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-160">-Princip</span><span class="sxs-lookup"><span data-stu-id="02b9d-160">-Policy</span></span>
<span data-ttu-id="02b9d-161">Princip identifierare</span><span class="sxs-lookup"><span data-stu-id="02b9d-161">Policy Identifier</span></span>

```yaml
Type: String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-162">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="02b9d-162">-Protocol</span></span>
<span data-ttu-id="02b9d-163">Protokollet kan användas i begäran med SAS-token.</span><span class="sxs-lookup"><span data-stu-id="02b9d-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-164">-Kö</span><span class="sxs-lookup"><span data-stu-id="02b9d-164">-Queue</span></span>
<span data-ttu-id="02b9d-165">Könamn</span><span class="sxs-lookup"><span data-stu-id="02b9d-165">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-166">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="02b9d-166">-ResourceType</span></span>
<span data-ttu-id="02b9d-167">Resurs typer som den här SAS-token gäller för.</span><span class="sxs-lookup"><span data-stu-id="02b9d-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="02b9d-168">Värden inkluderar "service", "container", "objekt"</span><span class="sxs-lookup"><span data-stu-id="02b9d-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases:
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-169">-Service</span><span class="sxs-lookup"><span data-stu-id="02b9d-169">-Service</span></span>
<span data-ttu-id="02b9d-170">Tjänst typer som denna SAS-token gäller för.</span><span class="sxs-lookup"><span data-stu-id="02b9d-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="02b9d-171">Värden innehåller "BLOB", "fil", "kö", "Tabell"</span><span class="sxs-lookup"><span data-stu-id="02b9d-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases:
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-172">-Dela</span><span class="sxs-lookup"><span data-stu-id="02b9d-172">-Share</span></span>
<span data-ttu-id="02b9d-173">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="02b9d-173">Share Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="02b9d-174">-SharedAccessHeader</span></span>
<span data-ttu-id="02b9d-175">Anger frågeparametrarna för att åsidosätta svarshuvuden.</span><span class="sxs-lookup"><span data-stu-id="02b9d-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases:
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="02b9d-176">-StartPartitionKey</span></span>
<span data-ttu-id="02b9d-177">Starta partitionsnyckel</span><span class="sxs-lookup"><span data-stu-id="02b9d-177">Start Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="02b9d-178">-StartRowKey</span></span>
<span data-ttu-id="02b9d-179">Starta rad-tangenten</span><span class="sxs-lookup"><span data-stu-id="02b9d-179">Start Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-180">-Tabell</span><span class="sxs-lookup"><span data-stu-id="02b9d-180">-Table</span></span>
<span data-ttu-id="02b9d-181">Tabell namn</span><span class="sxs-lookup"><span data-stu-id="02b9d-181">Table Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-182">-Tagg</span><span class="sxs-lookup"><span data-stu-id="02b9d-182">-Tag</span></span>
<span data-ttu-id="02b9d-183">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="02b9d-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="02b9d-184">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="02b9d-184">For example:</span></span>

<span data-ttu-id="02b9d-185">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="02b9d-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="02b9d-186">-TargetStorageVersion</span></span>
<span data-ttu-id="02b9d-187">Anger den signerade lagrings tjänst version som ska användas för att autentisera förfrågningar som görs med SAS-token.</span><span class="sxs-lookup"><span data-stu-id="02b9d-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="02b9d-188">-ValidityPeriod</span></span>
<span data-ttu-id="02b9d-189">Giltighets tids period som används för att ange förfallo tiden för SAS-token från den tid då den genereras</span><span class="sxs-lookup"><span data-stu-id="02b9d-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: TimeSpan
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b9d-190">-VaultName</span><span class="sxs-lookup"><span data-stu-id="02b9d-190">-VaultName</span></span>
<span data-ttu-id="02b9d-191">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="02b9d-191">Vault name.</span></span>
<span data-ttu-id="02b9d-192">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="02b9d-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="02b9d-193">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02b9d-193">-Confirm</span></span>
<span data-ttu-id="02b9d-194">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02b9d-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02b9d-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02b9d-195">-WhatIf</span></span>
<span data-ttu-id="02b9d-196">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02b9d-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02b9d-197">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02b9d-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02b9d-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b9d-198">CommonParameters</span></span>
<span data-ttu-id="02b9d-199">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02b9d-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b9d-200">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02b9d-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b9d-201">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02b9d-201">INPUTS</span></span>

### <span data-ttu-id="02b9d-202">Ingen</span><span class="sxs-lookup"><span data-stu-id="02b9d-202">None</span></span>
<span data-ttu-id="02b9d-203">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="02b9d-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02b9d-204">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02b9d-204">OUTPUTS</span></span>

### <span data-ttu-id="02b9d-205">Microsoft. Azure. commands. valv. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="02b9d-205">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="02b9d-206">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02b9d-206">NOTES</span></span>

## <span data-ttu-id="02b9d-207">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02b9d-207">RELATED LINKS</span></span>

[<span data-ttu-id="02b9d-208">Azureâ € ofta ‹ RM. â € ofta ‹ keyâ € ofta ‹ valv</span><span class="sxs-lookup"><span data-stu-id="02b9d-208">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)
