---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 5d9a48fbdc323ffdd232d6d961da6564fecc0dff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389046"
---
# <span data-ttu-id="37523-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="37523-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="37523-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37523-102">SYNOPSIS</span></span>
<span data-ttu-id="37523-103">Skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="37523-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="37523-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37523-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37523-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37523-105">DESCRIPTION</span></span>
<span data-ttu-id="37523-106">**New-AzSnapshotConfig-** cmdleten skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="37523-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="37523-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37523-107">EXAMPLES</span></span>

### <span data-ttu-id="37523-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="37523-108">Example 1</span></span>
```powershell
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="37523-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="37523-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="37523-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="37523-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="37523-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="37523-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="37523-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="37523-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="37523-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="37523-113">Example 2</span></span>

<span data-ttu-id="37523-114">Skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="37523-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="37523-115">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="37523-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="37523-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37523-116">PARAMETERS</span></span>

### <span data-ttu-id="37523-117">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="37523-117">-CreateOption</span></span>
<span data-ttu-id="37523-118">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="37523-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="37523-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37523-119">-DefaultProfile</span></span>
<span data-ttu-id="37523-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37523-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37523-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="37523-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="37523-122">Anger disk krypterings nyckelvärdet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="37523-122">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37523-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="37523-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="37523-124">Anger resurs-ID för den disk krypterings uppsättning som ska användas för att aktivera kryptering på rest.</span><span class="sxs-lookup"><span data-stu-id="37523-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="37523-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="37523-125">-DiskSizeGB</span></span>
<span data-ttu-id="37523-126">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="37523-126">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37523-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="37523-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="37523-128">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="37523-128">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37523-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="37523-129">-EncryptionType</span></span>
<span data-ttu-id="37523-130">Den typ av nycklar som används för att kryptera diskens data.</span><span class="sxs-lookup"><span data-stu-id="37523-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="37523-131">Tillgängliga värden är: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="37523-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="37523-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="37523-132">-DiskAccessId</span></span>
<span data-ttu-id="37523-133">Hämtar eller anger ARM-ID för DiskAccess-resursen för användning av privata slut punkter på.</span><span class="sxs-lookup"><span data-stu-id="37523-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="37523-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="37523-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="37523-135">Nätverks åtkomst princip definierar nätverks åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="37523-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="37523-136">Möjliga värden är: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="37523-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="37523-137">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="37523-137">-HyperVGeneration</span></span>
<span data-ttu-id="37523-138">Hypervisor-generering av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="37523-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="37523-139">Gäller endast för OS-diskar.</span><span class="sxs-lookup"><span data-stu-id="37523-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="37523-140">Tillåtna värden är v1 och v2.</span><span class="sxs-lookup"><span data-stu-id="37523-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="37523-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="37523-141">-ImageReference</span></span>
<span data-ttu-id="37523-142">Anger bild referensen för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="37523-142">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37523-143">-Inkrementellt</span><span class="sxs-lookup"><span data-stu-id="37523-143">-Incremental</span></span>
<span data-ttu-id="37523-144">Anger en stegvis ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="37523-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="37523-145">Inkrementella ögonblicks bilder på samma disk tar mindre plats än fullständiga stillbilder och kan omräknas.</span><span class="sxs-lookup"><span data-stu-id="37523-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37523-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="37523-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="37523-147">Anger Key Encryption Key för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="37523-147">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37523-148">-Plats</span><span class="sxs-lookup"><span data-stu-id="37523-148">-Location</span></span>
<span data-ttu-id="37523-149">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="37523-149">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37523-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="37523-150">-OsType</span></span>
<span data-ttu-id="37523-151">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="37523-151">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37523-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="37523-152">-SkuName</span></span>
<span data-ttu-id="37523-153">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="37523-153">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37523-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="37523-154">-SourceResourceId</span></span>
<span data-ttu-id="37523-155">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="37523-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="37523-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="37523-156">-SourceUri</span></span>
<span data-ttu-id="37523-157">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="37523-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="37523-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="37523-158">-StorageAccountId</span></span>
<span data-ttu-id="37523-159">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="37523-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="37523-160">-Tagg</span><span class="sxs-lookup"><span data-stu-id="37523-160">-Tag</span></span>
<span data-ttu-id="37523-161">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="37523-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="37523-162">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="37523-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37523-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37523-163">-Confirm</span></span>
<span data-ttu-id="37523-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37523-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37523-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37523-165">-WhatIf</span></span>
<span data-ttu-id="37523-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37523-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37523-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37523-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37523-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37523-168">CommonParameters</span></span>
<span data-ttu-id="37523-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37523-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37523-170">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37523-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37523-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37523-171">INPUTS</span></span>

### <span data-ttu-id="37523-172">System. String</span><span class="sxs-lookup"><span data-stu-id="37523-172">System.String</span></span>

### <span data-ttu-id="37523-173">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="37523-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="37523-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="37523-174">System.Int32</span></span>

### <span data-ttu-id="37523-175">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="37523-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="37523-176">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="37523-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="37523-177">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="37523-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="37523-178">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="37523-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="37523-179">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="37523-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="37523-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37523-180">OUTPUTS</span></span>

### <span data-ttu-id="37523-181">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="37523-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="37523-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37523-182">NOTES</span></span>

## <span data-ttu-id="37523-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37523-183">RELATED LINKS</span></span>
