---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskupdateconfig
schema: 2.0.0
ms.openlocfilehash: 790d366ced8b9466a906df2d3f1717ad9277ca9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930725"
---
# <span data-ttu-id="759ac-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="759ac-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="759ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="759ac-102">SYNOPSIS</span></span>
<span data-ttu-id="759ac-103">Skapar ett konfigurerbart disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="759ac-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="759ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="759ac-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="759ac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="759ac-105">DESCRIPTION</span></span>
<span data-ttu-id="759ac-106">Cmdleten **New-AzureRmDiskUpdateConfig** skapar ett konfigurerbart disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="759ac-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="759ac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="759ac-107">EXAMPLES</span></span>

### <span data-ttu-id="759ac-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="759ac-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="759ac-109">Med det första kommandot skapas ett lokalt tomt disk uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="759ac-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="759ac-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="759ac-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="759ac-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="759ac-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="759ac-112">Det sista kommandot tar emot disk uppdaterings objekt och uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="759ac-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="759ac-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="759ac-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="759ac-114">Det här kommandot uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01" till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="759ac-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="759ac-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="759ac-115">PARAMETERS</span></span>

### <span data-ttu-id="759ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="759ac-116">-DefaultProfile</span></span>
<span data-ttu-id="759ac-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="759ac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="759ac-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="759ac-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="759ac-119">Anger disk krypterings nyckelvärdet på en disk.</span><span class="sxs-lookup"><span data-stu-id="759ac-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="759ac-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="759ac-120">-DiskSizeGB</span></span>
<span data-ttu-id="759ac-121">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="759ac-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="759ac-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="759ac-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="759ac-123">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="759ac-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="759ac-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="759ac-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="759ac-125">Anger Key Encryption på en disk.</span><span class="sxs-lookup"><span data-stu-id="759ac-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="759ac-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="759ac-126">-OsType</span></span>
<span data-ttu-id="759ac-127">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="759ac-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="759ac-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="759ac-128">-SkuName</span></span>
<span data-ttu-id="759ac-129">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="759ac-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="759ac-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="759ac-130">-Tag</span></span>
<span data-ttu-id="759ac-131">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="759ac-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="759ac-132">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="759ac-132">For example:</span></span>

<span data-ttu-id="759ac-133">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="759ac-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759ac-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="759ac-134">-Confirm</span></span>
<span data-ttu-id="759ac-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="759ac-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="759ac-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="759ac-136">-WhatIf</span></span>
<span data-ttu-id="759ac-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="759ac-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="759ac-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="759ac-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="759ac-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="759ac-139">CommonParameters</span></span>
<span data-ttu-id="759ac-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="759ac-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="759ac-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="759ac-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="759ac-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="759ac-142">INPUTS</span></span>

### <span data-ttu-id="759ac-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="759ac-143">None</span></span>
<span data-ttu-id="759ac-144">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="759ac-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="759ac-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="759ac-145">OUTPUTS</span></span>

### <span data-ttu-id="759ac-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="759ac-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="759ac-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="759ac-147">NOTES</span></span>

## <span data-ttu-id="759ac-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="759ac-148">RELATED LINKS</span></span>

