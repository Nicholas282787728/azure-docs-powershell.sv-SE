---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
ms.openlocfilehash: 8249bbb354d660f335316da503b0f19b6576fea6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929950"
---
# <span data-ttu-id="03d79-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="03d79-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="03d79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03d79-102">SYNOPSIS</span></span>
<span data-ttu-id="03d79-103">Skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="03d79-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03d79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03d79-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03d79-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03d79-105">DESCRIPTION</span></span>
<span data-ttu-id="03d79-106">Cmdleten **New-AzureRmDiskConfig** skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="03d79-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="03d79-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03d79-107">EXAMPLES</span></span>

### <span data-ttu-id="03d79-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="03d79-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="03d79-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="03d79-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="03d79-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="03d79-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="03d79-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="03d79-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="03d79-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="03d79-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="03d79-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03d79-113">PARAMETERS</span></span>

### <span data-ttu-id="03d79-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="03d79-114">-CreateOption</span></span>
<span data-ttu-id="03d79-115">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="03d79-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="03d79-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d79-116">-DefaultProfile</span></span>
<span data-ttu-id="03d79-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03d79-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03d79-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="03d79-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="03d79-119">Anger disk krypterings nyckelvärdet på en disk.</span><span class="sxs-lookup"><span data-stu-id="03d79-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="03d79-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="03d79-120">-DiskSizeGB</span></span>
<span data-ttu-id="03d79-121">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="03d79-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="03d79-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="03d79-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="03d79-123">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="03d79-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="03d79-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="03d79-124">-ImageReference</span></span>
<span data-ttu-id="03d79-125">Anger bild referensen på en disk.</span><span class="sxs-lookup"><span data-stu-id="03d79-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="03d79-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="03d79-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="03d79-127">Anger Key Encryption på en disk.</span><span class="sxs-lookup"><span data-stu-id="03d79-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="03d79-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="03d79-128">-Location</span></span>
<span data-ttu-id="03d79-129">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="03d79-129">Specifies a location.</span></span>

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

### <span data-ttu-id="03d79-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="03d79-130">-OsType</span></span>
<span data-ttu-id="03d79-131">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="03d79-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="03d79-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="03d79-132">-SkuName</span></span>
<span data-ttu-id="03d79-133">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="03d79-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="03d79-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="03d79-134">-SourceResourceId</span></span>
<span data-ttu-id="03d79-135">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="03d79-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="03d79-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="03d79-136">-SourceUri</span></span>
<span data-ttu-id="03d79-137">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="03d79-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="03d79-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="03d79-138">-StorageAccountId</span></span>
<span data-ttu-id="03d79-139">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="03d79-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="03d79-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="03d79-140">-Tag</span></span>
<span data-ttu-id="03d79-141">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="03d79-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="03d79-142">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="03d79-142">For example:</span></span>

<span data-ttu-id="03d79-143">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="03d79-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="03d79-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="03d79-144">-Zone</span></span>
<span data-ttu-id="03d79-145">Anger listan med logiska zoner för disk.</span><span class="sxs-lookup"><span data-stu-id="03d79-145">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03d79-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="03d79-146">-Confirm</span></span>
<span data-ttu-id="03d79-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03d79-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03d79-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03d79-148">-WhatIf</span></span>
<span data-ttu-id="03d79-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="03d79-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03d79-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="03d79-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03d79-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d79-151">CommonParameters</span></span>
<span data-ttu-id="03d79-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03d79-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d79-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03d79-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d79-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03d79-154">INPUTS</span></span>

### <span data-ttu-id="03d79-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="03d79-155">None</span></span>
<span data-ttu-id="03d79-156">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="03d79-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03d79-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03d79-157">OUTPUTS</span></span>

### <span data-ttu-id="03d79-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="03d79-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="03d79-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03d79-159">NOTES</span></span>

## <span data-ttu-id="03d79-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03d79-160">RELATED LINKS</span></span>

