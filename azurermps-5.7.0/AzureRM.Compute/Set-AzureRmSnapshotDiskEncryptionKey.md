---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
ms.openlocfilehash: 05e48bc312dcbbf317906fadb63b9777765032ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575709"
---
# <span data-ttu-id="9b6b8-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9b6b8-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="9b6b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6b8-103">Ställer in egenskaper för disk krypterings nycklar i ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b6b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b6b8-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <Snapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b6b8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b6b8-105">DESCRIPTION</span></span>
<span data-ttu-id="9b6b8-106">Cmdleten **set-AzureRmSnapshotDiskEncryptionKey** anger egenskaperna för disk krypterings nycklar i ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="9b6b8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b6b8-107">EXAMPLES</span></span>

### <span data-ttu-id="9b6b8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b6b8-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="9b6b8-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="9b6b8-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="9b6b8-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="9b6b8-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="9b6b8-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9b6b8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b6b8-113">PARAMETERS</span></span>

### <span data-ttu-id="9b6b8-114">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="9b6b8-114">-SecretUrl</span></span>
<span data-ttu-id="9b6b8-115">Anger den hemliga URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-115">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="9b6b8-116">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="9b6b8-116">-Snapshot</span></span>
<span data-ttu-id="9b6b8-117">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-117">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b6b8-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="9b6b8-118">-SourceVaultId</span></span>
<span data-ttu-id="9b6b8-119">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="9b6b8-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b6b8-120">-Confirm</span></span>
<span data-ttu-id="9b6b8-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b6b8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b6b8-122">-WhatIf</span></span>
<span data-ttu-id="9b6b8-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b6b8-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b6b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6b8-125">CommonParameters</span></span>
<span data-ttu-id="9b6b8-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6b8-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b6b8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6b8-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b6b8-128">INPUTS</span></span>

### <span data-ttu-id="9b6b8-129">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="9b6b8-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="9b6b8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9b6b8-130">System.String</span></span>

## <span data-ttu-id="9b6b8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b6b8-131">OUTPUTS</span></span>

### <span data-ttu-id="9b6b8-132">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="9b6b8-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="9b6b8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b6b8-133">NOTES</span></span>

## <span data-ttu-id="9b6b8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b6b8-134">RELATED LINKS</span></span>

