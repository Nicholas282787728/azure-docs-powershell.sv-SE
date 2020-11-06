---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 70ee169903ca70b539e8eda2043ffcd0fd2928c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586199"
---
# <span data-ttu-id="371c0-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="371c0-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="371c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="371c0-102">SYNOPSIS</span></span>
<span data-ttu-id="371c0-103">Skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="371c0-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="371c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="371c0-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="371c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="371c0-105">DESCRIPTION</span></span>
<span data-ttu-id="371c0-106">Cmdleten **New-AzureRmDiskConfig** skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="371c0-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="371c0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="371c0-107">EXAMPLES</span></span>

### <span data-ttu-id="371c0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="371c0-108">Example 1</span></span>
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

<span data-ttu-id="371c0-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="371c0-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="371c0-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="371c0-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="371c0-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="371c0-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="371c0-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="371c0-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="371c0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="371c0-113">PARAMETERS</span></span>

### <span data-ttu-id="371c0-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="371c0-114">-CreateOption</span></span>
<span data-ttu-id="371c0-115">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="371c0-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="371c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="371c0-116">-DefaultProfile</span></span>
<span data-ttu-id="371c0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="371c0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="371c0-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="371c0-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="371c0-119">Anger disk krypterings nyckelvärdet på en disk.</span><span class="sxs-lookup"><span data-stu-id="371c0-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="371c0-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="371c0-120">-DiskSizeGB</span></span>
<span data-ttu-id="371c0-121">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="371c0-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="371c0-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="371c0-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="371c0-123">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="371c0-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="371c0-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="371c0-124">-ImageReference</span></span>
<span data-ttu-id="371c0-125">Anger bild referensen på en disk.</span><span class="sxs-lookup"><span data-stu-id="371c0-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="371c0-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="371c0-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="371c0-127">Anger Key Encryption på en disk.</span><span class="sxs-lookup"><span data-stu-id="371c0-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="371c0-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="371c0-128">-Location</span></span>
<span data-ttu-id="371c0-129">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="371c0-129">Specifies a location.</span></span>

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

### <span data-ttu-id="371c0-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="371c0-130">-OsType</span></span>
<span data-ttu-id="371c0-131">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="371c0-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="371c0-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="371c0-132">-SkuName</span></span>
<span data-ttu-id="371c0-133">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="371c0-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="371c0-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="371c0-134">-SourceResourceId</span></span>
<span data-ttu-id="371c0-135">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="371c0-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="371c0-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="371c0-136">-SourceUri</span></span>
<span data-ttu-id="371c0-137">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="371c0-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="371c0-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="371c0-138">-StorageAccountId</span></span>
<span data-ttu-id="371c0-139">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="371c0-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="371c0-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="371c0-140">-Tag</span></span>
<span data-ttu-id="371c0-141">Anger att resurser och resurs grupper kan märkas med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="371c0-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="371c0-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="371c0-142">-Zone</span></span>
<span data-ttu-id="371c0-143">Anger listan med logiska zoner för disk.</span><span class="sxs-lookup"><span data-stu-id="371c0-143">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="371c0-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="371c0-144">-Confirm</span></span>
<span data-ttu-id="371c0-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="371c0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="371c0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="371c0-146">-WhatIf</span></span>
<span data-ttu-id="371c0-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="371c0-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="371c0-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="371c0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="371c0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="371c0-149">CommonParameters</span></span>
<span data-ttu-id="371c0-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="371c0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="371c0-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="371c0-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="371c0-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="371c0-152">INPUTS</span></span>

### <span data-ttu-id="371c0-153">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, version = 14.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="371c0-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="371c0-154">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] system. String system. Collections. hash-system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="371c0-154">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="371c0-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="371c0-155">OUTPUTS</span></span>

### <span data-ttu-id="371c0-156">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="371c0-156">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="371c0-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="371c0-157">NOTES</span></span>

## <span data-ttu-id="371c0-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="371c0-158">RELATED LINKS</span></span>

