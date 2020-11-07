---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotupdateconfig
schema: 2.0.0
ms.openlocfilehash: 033b183c763be266b29aadf47a57e760e2432452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930717"
---
# <span data-ttu-id="44c17-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="44c17-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="44c17-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44c17-102">SYNOPSIS</span></span>
<span data-ttu-id="44c17-103">Skapar ett konfigurerbart uppdaterings objekt för ögonblicks bilder.</span><span class="sxs-lookup"><span data-stu-id="44c17-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44c17-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44c17-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44c17-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44c17-105">DESCRIPTION</span></span>
<span data-ttu-id="44c17-106">Cmdleten **New-AzureRmSnapshotUpdateConfig** skapar ett konfigurerbart uppdaterings objekt för ögonblicks bilder.</span><span class="sxs-lookup"><span data-stu-id="44c17-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="44c17-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44c17-107">EXAMPLES</span></span>

### <span data-ttu-id="44c17-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="44c17-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="44c17-109">Det första kommandot skapar ett lokalt, tomt ögonblicks bilds uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="44c17-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="44c17-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="44c17-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="44c17-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för objektet ögonblicks bild uppdatering.</span><span class="sxs-lookup"><span data-stu-id="44c17-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="44c17-112">Med det senaste kommandot tas ögonblicks bilden uppdatera objekt och en befintlig ögonblicks bild med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="44c17-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="44c17-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="44c17-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="44c17-114">Det här kommandot uppdaterar en befintlig ögonblicks bild med namnet ' Snapshot01 ' i resurs gruppen ' ResourceGroup01 ' till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="44c17-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="44c17-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44c17-115">PARAMETERS</span></span>

### <span data-ttu-id="44c17-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c17-116">-DefaultProfile</span></span>
<span data-ttu-id="44c17-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44c17-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44c17-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="44c17-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="44c17-119">Anger disk krypterings nyckelvärdet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="44c17-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="44c17-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="44c17-120">-DiskSizeGB</span></span>
<span data-ttu-id="44c17-121">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="44c17-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="44c17-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="44c17-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="44c17-123">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="44c17-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="44c17-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="44c17-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="44c17-125">Anger Key Encryption Key för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="44c17-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="44c17-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="44c17-126">-OsType</span></span>
<span data-ttu-id="44c17-127">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="44c17-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="44c17-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="44c17-128">-SkuName</span></span>
<span data-ttu-id="44c17-129">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="44c17-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="44c17-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="44c17-130">-Tag</span></span>
<span data-ttu-id="44c17-131">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="44c17-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="44c17-132">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="44c17-132">For example:</span></span>

<span data-ttu-id="44c17-133">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="44c17-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="44c17-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="44c17-134">-Confirm</span></span>
<span data-ttu-id="44c17-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="44c17-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c17-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c17-136">-WhatIf</span></span>
<span data-ttu-id="44c17-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="44c17-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44c17-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="44c17-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c17-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c17-139">CommonParameters</span></span>
<span data-ttu-id="44c17-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c17-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c17-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44c17-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c17-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44c17-142">INPUTS</span></span>

### <span data-ttu-id="44c17-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="44c17-143">None</span></span>
<span data-ttu-id="44c17-144">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="44c17-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="44c17-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44c17-145">OUTPUTS</span></span>

### <span data-ttu-id="44c17-146">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="44c17-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="44c17-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44c17-147">NOTES</span></span>

## <span data-ttu-id="44c17-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44c17-148">RELATED LINKS</span></span>

