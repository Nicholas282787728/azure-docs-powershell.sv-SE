---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 9491c5292353678f3c8159b8c3cb1d960b7bb774
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103261"
---
# <span data-ttu-id="ab9ea-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="ab9ea-101">New-AzDisk</span></span>

## <span data-ttu-id="ab9ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ab9ea-103">Skapar en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-103">Creates a managed disk.</span></span>

## <span data-ttu-id="ab9ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab9ea-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab9ea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab9ea-105">DESCRIPTION</span></span>
<span data-ttu-id="ab9ea-106">Cmdleten **New-AzDisk** skapar en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="ab9ea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab9ea-107">EXAMPLES</span></span>

### <span data-ttu-id="ab9ea-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ab9ea-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="ab9ea-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ab9ea-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ab9ea-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="ab9ea-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ab9ea-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ab9ea-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ab9ea-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $diskConfig.EncryptionSettingsCollection = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsCollection

PS C:\> $encryptionSettingsElement1 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_1

PS C:\> $encryptionSettingsElement2 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_2

PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement1
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement2
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="ab9ea-114">Med kommandot ovan skapas en disk med två krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-114">The above command creates a disk with two encryption settings.</span></span>

## <span data-ttu-id="ab9ea-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab9ea-115">PARAMETERS</span></span>

### <span data-ttu-id="ab9ea-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab9ea-116">-AsJob</span></span>
<span data-ttu-id="ab9ea-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab9ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab9ea-118">-DefaultProfile</span></span>
<span data-ttu-id="ab9ea-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab9ea-120">-Disk</span><span class="sxs-lookup"><span data-stu-id="ab9ea-120">-Disk</span></span>
<span data-ttu-id="ab9ea-121">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-121">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab9ea-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ab9ea-122">-DiskName</span></span>
<span data-ttu-id="ab9ea-123">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-123">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab9ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab9ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab9ea-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab9ea-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab9ea-126">-Confirm</span></span>
<span data-ttu-id="ab9ea-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab9ea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab9ea-128">-WhatIf</span></span>
<span data-ttu-id="ab9ea-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab9ea-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab9ea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab9ea-131">CommonParameters</span></span>
<span data-ttu-id="ab9ea-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab9ea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab9ea-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab9ea-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab9ea-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab9ea-134">INPUTS</span></span>

### <span data-ttu-id="ab9ea-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ab9ea-135">System.String</span></span>

### <span data-ttu-id="ab9ea-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="ab9ea-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ab9ea-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab9ea-137">OUTPUTS</span></span>

### <span data-ttu-id="ab9ea-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="ab9ea-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ab9ea-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab9ea-139">NOTES</span></span>

## <span data-ttu-id="ab9ea-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab9ea-140">RELATED LINKS</span></span>
