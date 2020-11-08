---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: 9c267a01629922408f25669ab93aa9a20a01b02b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102366"
---
# <span data-ttu-id="7ec32-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7ec32-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="7ec32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ec32-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec32-103">Skapar ett konfigurerbart disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="7ec32-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="7ec32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ec32-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ec32-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ec32-105">DESCRIPTION</span></span>
<span data-ttu-id="7ec32-106">Cmdleten **New-AzDiskUpdateConfig** skapar ett konfigurerbart disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="7ec32-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="7ec32-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ec32-107">EXAMPLES</span></span>

### <span data-ttu-id="7ec32-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ec32-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="7ec32-109">Med det första kommandot skapas ett lokalt tomt disk uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="7ec32-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="7ec32-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="7ec32-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="7ec32-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="7ec32-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="7ec32-112">Det sista kommandot tar emot disk uppdaterings objekt och uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7ec32-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="7ec32-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7ec32-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="7ec32-114">Det här kommandot uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01" till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="7ec32-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="7ec32-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ec32-115">PARAMETERS</span></span>

### <span data-ttu-id="7ec32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec32-116">-DefaultProfile</span></span>
<span data-ttu-id="7ec32-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec32-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ec32-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="7ec32-118">-DiskAccessId</span></span>
<span data-ttu-id="7ec32-119">{{Fill DiskAccessId Description}}</span><span class="sxs-lookup"><span data-stu-id="7ec32-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="7ec32-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7ec32-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="7ec32-121">Anger disk krypterings nyckelvärdet på en disk.</span><span class="sxs-lookup"><span data-stu-id="7ec32-121">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="7ec32-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="7ec32-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="7ec32-123">Anger resurs-ID för den disk krypterings uppsättning som ska användas för att aktivera kryptering på rest.</span><span class="sxs-lookup"><span data-stu-id="7ec32-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="7ec32-124">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="7ec32-124">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="7ec32-125">Antalet IOPS som är tillåtna för denna disk; anges endast för UltraSSD-diskar.</span><span class="sxs-lookup"><span data-stu-id="7ec32-125">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="7ec32-126">En operation kan överföras mellan 4K och 256 000 byte.</span><span class="sxs-lookup"><span data-stu-id="7ec32-126">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec32-127">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="7ec32-127">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="7ec32-128">Bandbredd som tillåts för denna disk; anges endast för UltraSSD-diskar.</span><span class="sxs-lookup"><span data-stu-id="7ec32-128">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="7ec32-129">MBps betyder miljon tals byte per sekund-MB här använder ISO-notationen med 10.</span><span class="sxs-lookup"><span data-stu-id="7ec32-129">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec32-130">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7ec32-130">-DiskSizeGB</span></span>
<span data-ttu-id="7ec32-131">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="7ec32-131">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="7ec32-132">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="7ec32-132">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="7ec32-133">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="7ec32-133">Enable encryption settings.</span></span>

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

### <span data-ttu-id="7ec32-134">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="7ec32-134">-EncryptionType</span></span>
<span data-ttu-id="7ec32-135">Den typ av nycklar som används för att kryptera diskens data.</span><span class="sxs-lookup"><span data-stu-id="7ec32-135">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="7ec32-136">Tillgängliga värden är: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="7ec32-136">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="7ec32-137">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7ec32-137">-KeyEncryptionKey</span></span>
<span data-ttu-id="7ec32-138">Anger Key Encryption på en disk.</span><span class="sxs-lookup"><span data-stu-id="7ec32-138">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="7ec32-139">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7ec32-139">-NetworkAccessPolicy</span></span>
<span data-ttu-id="7ec32-140">{{Fill NetworkAccessPolicy Description}}</span><span class="sxs-lookup"><span data-stu-id="7ec32-140">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="7ec32-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="7ec32-141">-OsType</span></span>
<span data-ttu-id="7ec32-142">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="7ec32-142">Specifies the OS type.</span></span>

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

### <span data-ttu-id="7ec32-143">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7ec32-143">-SkuName</span></span>
<span data-ttu-id="7ec32-144">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="7ec32-144">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="7ec32-145">Tillgängliga värden är Standard_LRS, Premium_LRS, StandardSSD_LRS och UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="7ec32-145">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="7ec32-146">UltraSSD_LRS kan endast användas med ett tomt värde för CreateOption-parametern.</span><span class="sxs-lookup"><span data-stu-id="7ec32-146">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="7ec32-147">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7ec32-147">-Tag</span></span>
<span data-ttu-id="7ec32-148">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7ec32-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7ec32-149">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="7ec32-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec32-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ec32-150">-Confirm</span></span>
<span data-ttu-id="7ec32-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ec32-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ec32-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ec32-152">-WhatIf</span></span>
<span data-ttu-id="7ec32-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ec32-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ec32-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ec32-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ec32-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec32-155">CommonParameters</span></span>
<span data-ttu-id="7ec32-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ec32-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec32-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ec32-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec32-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ec32-158">INPUTS</span></span>

### <span data-ttu-id="7ec32-159">System. String</span><span class="sxs-lookup"><span data-stu-id="7ec32-159">System.String</span></span>

### <span data-ttu-id="7ec32-160">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7ec32-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7ec32-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7ec32-161">System.Int32</span></span>

### <span data-ttu-id="7ec32-162">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="7ec32-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7ec32-163">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7ec32-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7ec32-164">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="7ec32-164">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="7ec32-165">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="7ec32-165">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="7ec32-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ec32-166">OUTPUTS</span></span>

### <span data-ttu-id="7ec32-167">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="7ec32-167">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="7ec32-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ec32-168">NOTES</span></span>

## <span data-ttu-id="7ec32-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ec32-169">RELATED LINKS</span></span>
