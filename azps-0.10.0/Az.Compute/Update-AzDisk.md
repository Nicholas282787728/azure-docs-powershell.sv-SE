---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 8925e294b329b76f996a21d24597a4a8b5388a74
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923026"
---
# <span data-ttu-id="ffa98-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="ffa98-101">Update-AzDisk</span></span>

## <span data-ttu-id="ffa98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ffa98-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa98-103">Uppdaterar en disk.</span><span class="sxs-lookup"><span data-stu-id="ffa98-103">Updates a disk.</span></span>

## <span data-ttu-id="ffa98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ffa98-104">SYNTAX</span></span>

### <span data-ttu-id="ffa98-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="ffa98-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffa98-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ffa98-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa98-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ffa98-107">DESCRIPTION</span></span>
<span data-ttu-id="ffa98-108">Cmdleten **Update-AzDisk** uppdaterar en disk.</span><span class="sxs-lookup"><span data-stu-id="ffa98-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="ffa98-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ffa98-109">EXAMPLES</span></span>

### <span data-ttu-id="ffa98-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ffa98-110">Example 1</span></span>
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

<span data-ttu-id="ffa98-111">Med det första kommandot skapas ett lokalt tomt disk uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ffa98-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ffa98-112">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="ffa98-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ffa98-113">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="ffa98-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="ffa98-114">Det sista kommandot tar emot disk uppdaterings objekt och uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ffa98-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ffa98-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ffa98-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="ffa98-116">Det här kommandot uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01" till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="ffa98-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="ffa98-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ffa98-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="ffa98-118">Dessa kommandon uppdaterar också en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01" till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="ffa98-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ffa98-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ffa98-119">PARAMETERS</span></span>

### <span data-ttu-id="ffa98-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffa98-120">-AsJob</span></span>
<span data-ttu-id="ffa98-121">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="ffa98-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa98-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa98-122">-DefaultProfile</span></span>
<span data-ttu-id="ffa98-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa98-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffa98-124">-Disk</span><span class="sxs-lookup"><span data-stu-id="ffa98-124">-Disk</span></span>
<span data-ttu-id="ffa98-125">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="ffa98-125">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa98-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ffa98-126">-DiskName</span></span>
<span data-ttu-id="ffa98-127">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="ffa98-127">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa98-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ffa98-128">-DiskUpdate</span></span>
<span data-ttu-id="ffa98-129">Anger ett uppdaterings objekt för lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="ffa98-129">Specifies a local disk update object.</span></span>

```yaml
Type: PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa98-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa98-130">-ResourceGroupName</span></span>
<span data-ttu-id="ffa98-131">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ffa98-131">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa98-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ffa98-132">-Confirm</span></span>
<span data-ttu-id="ffa98-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ffa98-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa98-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa98-134">-WhatIf</span></span>
<span data-ttu-id="ffa98-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ffa98-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa98-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ffa98-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa98-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa98-137">CommonParameters</span></span>
<span data-ttu-id="ffa98-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa98-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa98-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa98-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa98-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ffa98-140">INPUTS</span></span>

### <span data-ttu-id="ffa98-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ffa98-141">System.String</span></span>
<span data-ttu-id="ffa98-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="ffa98-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ffa98-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ffa98-143">OUTPUTS</span></span>

### <span data-ttu-id="ffa98-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="ffa98-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ffa98-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ffa98-145">NOTES</span></span>

## <span data-ttu-id="ffa98-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ffa98-146">RELATED LINKS</span></span>
