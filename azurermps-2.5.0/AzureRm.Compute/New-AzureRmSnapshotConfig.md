---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
ms.openlocfilehash: a18eb8513e419d174efac9179cb65fe175d12dd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931037"
---
# <span data-ttu-id="42dff-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="42dff-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="42dff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42dff-102">SYNOPSIS</span></span>
<span data-ttu-id="42dff-103">Skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="42dff-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42dff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42dff-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42dff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42dff-105">DESCRIPTION</span></span>
<span data-ttu-id="42dff-106">**New-AzureRmSnapshotConfig-** cmdleten skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="42dff-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="42dff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42dff-107">EXAMPLES</span></span>

### <span data-ttu-id="42dff-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="42dff-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="42dff-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="42dff-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="42dff-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="42dff-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="42dff-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="42dff-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="42dff-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="42dff-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="42dff-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42dff-113">PARAMETERS</span></span>

### <span data-ttu-id="42dff-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="42dff-114">-CreateOption</span></span>
<span data-ttu-id="42dff-115">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="42dff-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dff-116">-DefaultProfile</span></span>
<span data-ttu-id="42dff-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42dff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42dff-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="42dff-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="42dff-119">Anger disk krypterings nyckelvärdet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="42dff-119">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="42dff-120">-DiskSizeGB</span></span>
<span data-ttu-id="42dff-121">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="42dff-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="42dff-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="42dff-123">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="42dff-123">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="42dff-124">-ImageReference</span></span>
<span data-ttu-id="42dff-125">Anger bild referensen för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="42dff-125">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="42dff-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="42dff-127">Anger Key Encryption Key för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="42dff-127">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="42dff-128">-Location</span></span>
<span data-ttu-id="42dff-129">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="42dff-129">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="42dff-130">-OsType</span></span>
<span data-ttu-id="42dff-131">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="42dff-131">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="42dff-132">-SkuName</span></span>
<span data-ttu-id="42dff-133">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="42dff-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="42dff-134">-SourceResourceId</span></span>
<span data-ttu-id="42dff-135">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="42dff-135">Specifies the source resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="42dff-136">-SourceUri</span></span>
<span data-ttu-id="42dff-137">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="42dff-137">Specifies the source Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="42dff-138">-StorageAccountId</span></span>
<span data-ttu-id="42dff-139">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="42dff-139">Specifies the storage account ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="42dff-140">-Tag</span></span>
<span data-ttu-id="42dff-141">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="42dff-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42dff-142">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="42dff-142">For example:</span></span>

<span data-ttu-id="42dff-143">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="42dff-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dff-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42dff-144">-Confirm</span></span>
<span data-ttu-id="42dff-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42dff-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42dff-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42dff-146">-WhatIf</span></span>
<span data-ttu-id="42dff-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42dff-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42dff-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42dff-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42dff-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dff-149">CommonParameters</span></span>
<span data-ttu-id="42dff-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42dff-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42dff-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42dff-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dff-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42dff-152">INPUTS</span></span>

### <span data-ttu-id="42dff-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="42dff-153">None</span></span>
<span data-ttu-id="42dff-154">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="42dff-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42dff-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42dff-155">OUTPUTS</span></span>

### <span data-ttu-id="42dff-156">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="42dff-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="42dff-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42dff-157">NOTES</span></span>

## <span data-ttu-id="42dff-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42dff-158">RELATED LINKS</span></span>

