---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 1afd1631e398b5726a8e1002b6739fc7ac9b67a8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925062"
---
# <span data-ttu-id="de139-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="de139-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="de139-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de139-102">SYNOPSIS</span></span>
<span data-ttu-id="de139-103">Skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="de139-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="de139-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de139-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de139-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de139-105">DESCRIPTION</span></span>
<span data-ttu-id="de139-106">**New-AzSnapshotConfig-** cmdleten skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="de139-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="de139-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de139-107">EXAMPLES</span></span>

### <span data-ttu-id="de139-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="de139-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="de139-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="de139-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="de139-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="de139-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="de139-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="de139-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="de139-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="de139-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="de139-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de139-113">PARAMETERS</span></span>

### <span data-ttu-id="de139-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="de139-114">-CreateOption</span></span>
<span data-ttu-id="de139-115">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="de139-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="de139-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de139-116">-DefaultProfile</span></span>
<span data-ttu-id="de139-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de139-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de139-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="de139-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="de139-119">Anger disk krypterings nyckelvärdet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="de139-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="de139-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="de139-120">-DiskSizeGB</span></span>
<span data-ttu-id="de139-121">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="de139-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="de139-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="de139-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="de139-123">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="de139-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="de139-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="de139-124">-ImageReference</span></span>
<span data-ttu-id="de139-125">Anger bild referensen för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="de139-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="de139-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="de139-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="de139-127">Anger Key Encryption Key för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="de139-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="de139-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="de139-128">-Location</span></span>
<span data-ttu-id="de139-129">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="de139-129">Specifies a location.</span></span>

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

### <span data-ttu-id="de139-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="de139-130">-OsType</span></span>
<span data-ttu-id="de139-131">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="de139-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="de139-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="de139-132">-SkuName</span></span>
<span data-ttu-id="de139-133">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="de139-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="de139-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="de139-134">-SourceResourceId</span></span>
<span data-ttu-id="de139-135">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="de139-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="de139-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="de139-136">-SourceUri</span></span>
<span data-ttu-id="de139-137">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="de139-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="de139-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="de139-138">-StorageAccountId</span></span>
<span data-ttu-id="de139-139">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="de139-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="de139-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="de139-140">-Tag</span></span>
<span data-ttu-id="de139-141">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="de139-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="de139-142">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="de139-142">For example:</span></span>

<span data-ttu-id="de139-143">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="de139-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="de139-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de139-144">-Confirm</span></span>
<span data-ttu-id="de139-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de139-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de139-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de139-146">-WhatIf</span></span>
<span data-ttu-id="de139-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de139-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de139-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de139-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de139-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de139-149">CommonParameters</span></span>
<span data-ttu-id="de139-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de139-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de139-151">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de139-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de139-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de139-152">INPUTS</span></span>

### <span data-ttu-id="de139-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="de139-153">None</span></span>
<span data-ttu-id="de139-154">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="de139-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de139-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de139-155">OUTPUTS</span></span>

### <span data-ttu-id="de139-156">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="de139-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="de139-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de139-157">NOTES</span></span>

## <span data-ttu-id="de139-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de139-158">RELATED LINKS</span></span>

