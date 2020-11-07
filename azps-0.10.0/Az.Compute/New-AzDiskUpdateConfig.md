---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: c346cebbc14a25b2afa8047deea3578ab8330d87
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925078"
---
# <span data-ttu-id="0a5e6-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0a5e6-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="0a5e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5e6-103">Skapar ett konfigurerbart disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="0a5e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a5e6-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a5e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a5e6-105">DESCRIPTION</span></span>
<span data-ttu-id="0a5e6-106">Cmdleten **New-AzDiskUpdateConfig** skapar ett konfigurerbart disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="0a5e6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a5e6-107">EXAMPLES</span></span>

### <span data-ttu-id="0a5e6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0a5e6-108">Example 1</span></span>
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

<span data-ttu-id="0a5e6-109">Med det första kommandot skapas ett lokalt tomt disk uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="0a5e6-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="0a5e6-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="0a5e6-112">Det sista kommandot tar emot disk uppdaterings objekt och uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0a5e6-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0a5e6-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0a5e6-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="0a5e6-114">Det här kommandot uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01" till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="0a5e6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a5e6-115">PARAMETERS</span></span>

### <span data-ttu-id="0a5e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5e6-116">-DefaultProfile</span></span>
<span data-ttu-id="0a5e6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a5e6-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0a5e6-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="0a5e6-119">Anger disk krypterings nyckelvärdet på en disk.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="0a5e6-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0a5e6-120">-DiskSizeGB</span></span>
<span data-ttu-id="0a5e6-121">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="0a5e6-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="0a5e6-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="0a5e6-123">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="0a5e6-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0a5e6-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="0a5e6-125">Anger Key Encryption på en disk.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="0a5e6-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="0a5e6-126">-OsType</span></span>
<span data-ttu-id="0a5e6-127">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="0a5e6-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0a5e6-128">-SkuName</span></span>
<span data-ttu-id="0a5e6-129">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="0a5e6-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0a5e6-130">-Tag</span></span>
<span data-ttu-id="0a5e6-131">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0a5e6-132">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="0a5e6-132">For example:</span></span>

<span data-ttu-id="0a5e6-133">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="0a5e6-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0a5e6-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a5e6-134">-Confirm</span></span>
<span data-ttu-id="0a5e6-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a5e6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a5e6-136">-WhatIf</span></span>
<span data-ttu-id="0a5e6-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a5e6-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a5e6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5e6-139">CommonParameters</span></span>
<span data-ttu-id="0a5e6-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5e6-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a5e6-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5e6-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a5e6-142">INPUTS</span></span>

### <span data-ttu-id="0a5e6-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="0a5e6-143">None</span></span>
<span data-ttu-id="0a5e6-144">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0a5e6-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a5e6-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a5e6-145">OUTPUTS</span></span>

### <span data-ttu-id="0a5e6-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="0a5e6-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="0a5e6-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a5e6-147">NOTES</span></span>

## <span data-ttu-id="0a5e6-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a5e6-148">RELATED LINKS</span></span>

