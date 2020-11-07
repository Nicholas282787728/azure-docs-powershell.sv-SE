---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 81cf8a6d011575702f8eead878e8987a5a0fd456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758121"
---
# <span data-ttu-id="e3b1e-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="e3b1e-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="e3b1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b1e-103">Uppdaterar en disk.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3b1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3b1e-104">SYNTAX</span></span>

### <span data-ttu-id="e3b1e-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="e3b1e-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b1e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="e3b1e-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b1e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3b1e-107">DESCRIPTION</span></span>
<span data-ttu-id="e3b1e-108">Cmdleten **Update-AzureRmDisk** uppdaterar en disk.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="e3b1e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3b1e-109">EXAMPLES</span></span>

### <span data-ttu-id="e3b1e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e3b1e-110">Example 1</span></span>
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

<span data-ttu-id="e3b1e-111">Med det första kommandot skapas ett lokalt tomt disk uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e3b1e-112">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e3b1e-113">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="e3b1e-114">Det sista kommandot tar emot disk uppdaterings objekt och uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e3b1e-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e3b1e-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e3b1e-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="e3b1e-116">Det här kommandot uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01" till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="e3b1e-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="e3b1e-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="e3b1e-118">Dessa kommandon uppdaterar också en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01" till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="e3b1e-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3b1e-119">PARAMETERS</span></span>

### <span data-ttu-id="e3b1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b1e-120">-DefaultProfile</span></span>
<span data-ttu-id="e3b1e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3b1e-122">-Disk</span><span class="sxs-lookup"><span data-stu-id="e3b1e-122">-Disk</span></span>
<span data-ttu-id="e3b1e-123">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-123">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b1e-124">-DiskName</span><span class="sxs-lookup"><span data-stu-id="e3b1e-124">-DiskName</span></span>
<span data-ttu-id="e3b1e-125">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-125">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b1e-126">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e3b1e-126">-DiskUpdate</span></span>
<span data-ttu-id="e3b1e-127">Anger ett uppdaterings objekt för lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-127">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b1e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b1e-128">-ResourceGroupName</span></span>
<span data-ttu-id="e3b1e-129">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b1e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3b1e-130">-Confirm</span></span>
<span data-ttu-id="e3b1e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b1e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b1e-132">-WhatIf</span></span>
<span data-ttu-id="e3b1e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b1e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3b1e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b1e-135">CommonParameters</span></span>
<span data-ttu-id="e3b1e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b1e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b1e-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b1e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b1e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3b1e-138">INPUTS</span></span>

### <span data-ttu-id="e3b1e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b1e-139">System.String</span></span>
<span data-ttu-id="e3b1e-140">Microsoft. Azure. Management. Compute. Models. DiskUpdate Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="e3b1e-140">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="e3b1e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3b1e-141">OUTPUTS</span></span>

### <span data-ttu-id="e3b1e-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="e3b1e-142">System.Object</span></span>

## <span data-ttu-id="e3b1e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3b1e-143">NOTES</span></span>

## <span data-ttu-id="e3b1e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3b1e-144">RELATED LINKS</span></span>

