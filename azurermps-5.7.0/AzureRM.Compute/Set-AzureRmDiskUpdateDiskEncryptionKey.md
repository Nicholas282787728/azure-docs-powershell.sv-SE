---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 4d44bc014a3d38a89e6c9a6a6d755aa9353c052e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579588"
---
# <span data-ttu-id="2d848-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2d848-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="2d848-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d848-102">SYNOPSIS</span></span>
<span data-ttu-id="2d848-103">Anger egenskaper för disk krypterings nycklar på ett disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="2d848-103">Sets the disk encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d848-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d848-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateDiskEncryptionKey [-DiskUpdate] <DiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d848-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d848-105">DESCRIPTION</span></span>
<span data-ttu-id="2d848-106">Cmdleten **set-AzureRmDiskUpdateDiskEncryptionKey** anger egenskaper för disk krypterings nycklar på ett disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="2d848-106">The **Set-AzureRmDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="2d848-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d848-107">EXAMPLES</span></span>

### <span data-ttu-id="2d848-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2d848-108">Example 1</span></span>
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

<span data-ttu-id="2d848-109">Med det första kommandot skapas ett lokalt tomt disk uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="2d848-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="2d848-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="2d848-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="2d848-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="2d848-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="2d848-112">Det sista kommandot tar emot disk uppdaterings objekt och uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2d848-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2d848-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d848-113">PARAMETERS</span></span>

### <span data-ttu-id="2d848-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="2d848-114">-DiskUpdate</span></span>
<span data-ttu-id="2d848-115">Anger ett uppdaterings objekt för lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="2d848-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d848-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="2d848-116">-SecretUrl</span></span>
<span data-ttu-id="2d848-117">Anger den hemliga URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="2d848-117">Specifies the secret Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d848-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="2d848-118">-SourceVaultId</span></span>
<span data-ttu-id="2d848-119">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="2d848-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d848-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d848-120">-Confirm</span></span>
<span data-ttu-id="2d848-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d848-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d848-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d848-122">-WhatIf</span></span>
<span data-ttu-id="2d848-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d848-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d848-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d848-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d848-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d848-125">CommonParameters</span></span>
<span data-ttu-id="2d848-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d848-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d848-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d848-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d848-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d848-128">INPUTS</span></span>

### <span data-ttu-id="2d848-129">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="2d848-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="2d848-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2d848-130">System.String</span></span>

## <span data-ttu-id="2d848-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d848-131">OUTPUTS</span></span>

### <span data-ttu-id="2d848-132">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="2d848-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="2d848-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d848-133">NOTES</span></span>

## <span data-ttu-id="2d848-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d848-134">RELATED LINKS</span></span>

