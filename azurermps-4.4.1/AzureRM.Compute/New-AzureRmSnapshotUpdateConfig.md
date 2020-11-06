---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
ms.openlocfilehash: 00519ec40e4f173c7ecfbb37189835711184f2e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585755"
---
# <span data-ttu-id="cff9a-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="cff9a-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="cff9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cff9a-102">SYNOPSIS</span></span>
<span data-ttu-id="cff9a-103">Skapar ett konfigurerbart uppdaterings objekt för ögonblicks bilder.</span><span class="sxs-lookup"><span data-stu-id="cff9a-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cff9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cff9a-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cff9a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cff9a-105">DESCRIPTION</span></span>
<span data-ttu-id="cff9a-106">Cmdleten **New-AzureRmSnapshotUpdateConfig** skapar ett konfigurerbart uppdaterings objekt för ögonblicks bilder.</span><span class="sxs-lookup"><span data-stu-id="cff9a-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="cff9a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cff9a-107">EXAMPLES</span></span>

### <span data-ttu-id="cff9a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cff9a-108">Example 1</span></span>
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

<span data-ttu-id="cff9a-109">Det första kommandot skapar ett lokalt, tomt ögonblicks bilds uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="cff9a-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="cff9a-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="cff9a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="cff9a-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för objektet ögonblicks bild uppdatering.</span><span class="sxs-lookup"><span data-stu-id="cff9a-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="cff9a-112">Med det senaste kommandot tas ögonblicks bilden uppdatera objekt och en befintlig ögonblicks bild med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cff9a-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="cff9a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cff9a-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="cff9a-114">Det här kommandot uppdaterar en befintlig ögonblicks bild med namnet ' Snapshot01 ' i resurs gruppen ' ResourceGroup01 ' till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="cff9a-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="cff9a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cff9a-115">PARAMETERS</span></span>

### <span data-ttu-id="cff9a-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="cff9a-116">-CreateOption</span></span>
<span data-ttu-id="cff9a-117">Anger om den här cmdleten skapar en ögonblicks bild på den virtuella datorn från en plattform eller en användar bild, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="cff9a-117">Specifies whether this cmdlet creates a snapshot in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff9a-118">-DefaultProfile</span></span>
<span data-ttu-id="cff9a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cff9a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff9a-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cff9a-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="cff9a-121">Anger disk krypterings nyckelvärdet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="cff9a-121">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="cff9a-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="cff9a-122">-DiskSizeGB</span></span>
<span data-ttu-id="cff9a-123">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="cff9a-123">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff9a-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="cff9a-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="cff9a-125">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="cff9a-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="cff9a-126">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="cff9a-126">-ImageReference</span></span>
<span data-ttu-id="cff9a-127">Anger bild referensen för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="cff9a-127">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="cff9a-128">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cff9a-128">-KeyEncryptionKey</span></span>
<span data-ttu-id="cff9a-129">Anger Key Encryption Key för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="cff9a-129">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="cff9a-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="cff9a-130">-OsType</span></span>
<span data-ttu-id="cff9a-131">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="cff9a-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="cff9a-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cff9a-132">-SkuName</span></span>
<span data-ttu-id="cff9a-133">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="cff9a-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff9a-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="cff9a-134">-SourceResourceId</span></span>
<span data-ttu-id="cff9a-135">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="cff9a-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="cff9a-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="cff9a-136">-SourceUri</span></span>
<span data-ttu-id="cff9a-137">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="cff9a-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="cff9a-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cff9a-138">-StorageAccountId</span></span>
<span data-ttu-id="cff9a-139">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="cff9a-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="cff9a-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cff9a-140">-Tag</span></span>
<span data-ttu-id="cff9a-141">Anger att resurser och resurs grupper kan märkas med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="cff9a-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="cff9a-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cff9a-142">-Confirm</span></span>
<span data-ttu-id="cff9a-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cff9a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cff9a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cff9a-144">-WhatIf</span></span>
<span data-ttu-id="cff9a-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cff9a-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cff9a-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cff9a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cff9a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff9a-147">CommonParameters</span></span>
<span data-ttu-id="cff9a-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff9a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff9a-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff9a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff9a-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cff9a-150">INPUTS</span></span>

### <span data-ttu-id="cff9a-151">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, version = 14.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cff9a-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="cff9a-152">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] system. Collections. hash-system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Compute</span><span class="sxs-lookup"><span data-stu-id="cff9a-152">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="cff9a-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cff9a-153">OUTPUTS</span></span>

### <span data-ttu-id="cff9a-154">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="cff9a-154">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="cff9a-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cff9a-155">NOTES</span></span>

## <span data-ttu-id="cff9a-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cff9a-156">RELATED LINKS</span></span>

