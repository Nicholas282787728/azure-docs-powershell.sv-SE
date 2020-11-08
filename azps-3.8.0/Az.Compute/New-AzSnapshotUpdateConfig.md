---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089171"
---
# <span data-ttu-id="07c12-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="07c12-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="07c12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07c12-102">SYNOPSIS</span></span>
<span data-ttu-id="07c12-103">Skapar ett konfigurerbart uppdaterings objekt för ögonblicks bilder.</span><span class="sxs-lookup"><span data-stu-id="07c12-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="07c12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07c12-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07c12-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07c12-105">DESCRIPTION</span></span>
<span data-ttu-id="07c12-106">Cmdleten **New-AzSnapshotUpdateConfig** skapar ett konfigurerbart uppdaterings objekt för ögonblicks bilder.</span><span class="sxs-lookup"><span data-stu-id="07c12-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="07c12-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07c12-107">EXAMPLES</span></span>

### <span data-ttu-id="07c12-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="07c12-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="07c12-109">Det första kommandot skapar ett lokalt, tomt ögonblicks bilds uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="07c12-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="07c12-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="07c12-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="07c12-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för objektet ögonblicks bild uppdatering.</span><span class="sxs-lookup"><span data-stu-id="07c12-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="07c12-112">Med det senaste kommandot tas ögonblicks bilden uppdatera objekt och en befintlig ögonblicks bild med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="07c12-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="07c12-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="07c12-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="07c12-114">Det här kommandot uppdaterar en befintlig ögonblicks bild med namnet ' Snapshot01 ' i resurs gruppen ' ResourceGroup01 ' till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="07c12-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="07c12-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07c12-115">PARAMETERS</span></span>

### <span data-ttu-id="07c12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c12-116">-DefaultProfile</span></span>
<span data-ttu-id="07c12-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07c12-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07c12-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="07c12-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="07c12-119">Anger disk krypterings nyckelvärdet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="07c12-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="07c12-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="07c12-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="07c12-121">Anger resurs-ID för den disk krypterings uppsättning som ska användas för att aktivera kryptering på rest.</span><span class="sxs-lookup"><span data-stu-id="07c12-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="07c12-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="07c12-122">-DiskSizeGB</span></span>
<span data-ttu-id="07c12-123">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="07c12-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="07c12-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="07c12-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="07c12-125">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="07c12-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="07c12-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="07c12-126">-EncryptionType</span></span>
<span data-ttu-id="07c12-127">Den typ av nycklar som används för att kryptera diskens data.</span><span class="sxs-lookup"><span data-stu-id="07c12-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="07c12-128">Tillgängliga värden är: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="07c12-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="07c12-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="07c12-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="07c12-130">Anger Key Encryption Key för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="07c12-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="07c12-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="07c12-131">-OsType</span></span>
<span data-ttu-id="07c12-132">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="07c12-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="07c12-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="07c12-133">-SkuName</span></span>
<span data-ttu-id="07c12-134">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="07c12-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="07c12-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="07c12-135">-Tag</span></span>
<span data-ttu-id="07c12-136">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="07c12-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="07c12-137">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="07c12-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="07c12-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="07c12-138">-Confirm</span></span>
<span data-ttu-id="07c12-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="07c12-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07c12-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07c12-140">-WhatIf</span></span>
<span data-ttu-id="07c12-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="07c12-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07c12-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="07c12-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07c12-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c12-143">CommonParameters</span></span>
<span data-ttu-id="07c12-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c12-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c12-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07c12-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c12-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07c12-146">INPUTS</span></span>

### <span data-ttu-id="07c12-147">System. String</span><span class="sxs-lookup"><span data-stu-id="07c12-147">System.String</span></span>

### <span data-ttu-id="07c12-148">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="07c12-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="07c12-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="07c12-149">System.Int32</span></span>

### <span data-ttu-id="07c12-150">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="07c12-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="07c12-151">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="07c12-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="07c12-152">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="07c12-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="07c12-153">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="07c12-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="07c12-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07c12-154">OUTPUTS</span></span>

### <span data-ttu-id="07c12-155">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="07c12-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="07c12-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07c12-156">NOTES</span></span>

## <span data-ttu-id="07c12-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07c12-157">RELATED LINKS</span></span>