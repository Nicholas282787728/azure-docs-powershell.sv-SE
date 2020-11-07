---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: 52f6a58f74312b96d09f8dacd8b6ced23db5c26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755262"
---
# <span data-ttu-id="b2408-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b2408-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="b2408-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2408-102">SYNOPSIS</span></span>
<span data-ttu-id="b2408-103">Ställer in egenskaper för disk krypterings nycklar i ett objekt för ögonblicks bilder.</span><span class="sxs-lookup"><span data-stu-id="b2408-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2408-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2408-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <SnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2408-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2408-105">DESCRIPTION</span></span>
<span data-ttu-id="b2408-106">Cmdleten **set-AzureRmSnapshotUpdateDiskEncryptionKey** anger egenskaperna för disk krypterings nycklar i ett ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="b2408-106">The **Set-AzureRmSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="b2408-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2408-107">EXAMPLES</span></span>

### <span data-ttu-id="b2408-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b2408-108">Example 1</span></span>
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

<span data-ttu-id="b2408-109">Det första kommandot skapar ett lokalt, tomt ögonblicks bilds uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="b2408-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b2408-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="b2408-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b2408-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för objektet ögonblicks bild uppdatering.</span><span class="sxs-lookup"><span data-stu-id="b2408-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="b2408-112">Med det senaste kommandot tas ögonblicks bilden uppdatera objekt och en befintlig ögonblicks bild med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b2408-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b2408-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2408-113">PARAMETERS</span></span>

### <span data-ttu-id="b2408-114">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="b2408-114">-SecretUrl</span></span>
<span data-ttu-id="b2408-115">Specifes hemlig webb adress.</span><span class="sxs-lookup"><span data-stu-id="b2408-115">Specifes the secret Url.</span></span>

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

### <span data-ttu-id="b2408-116">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b2408-116">-SnapshotUpdate</span></span>
<span data-ttu-id="b2408-117">Anger ett lokalt ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="b2408-117">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2408-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b2408-118">-SourceVaultId</span></span>
<span data-ttu-id="b2408-119">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="b2408-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="b2408-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b2408-120">-Confirm</span></span>
<span data-ttu-id="b2408-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2408-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2408-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2408-122">-WhatIf</span></span>
<span data-ttu-id="b2408-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b2408-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2408-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b2408-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2408-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2408-125">CommonParameters</span></span>
<span data-ttu-id="b2408-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2408-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2408-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2408-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2408-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2408-128">INPUTS</span></span>

### <span data-ttu-id="b2408-129">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b2408-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="b2408-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b2408-130">System.String</span></span>

## <span data-ttu-id="b2408-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2408-131">OUTPUTS</span></span>

### <span data-ttu-id="b2408-132">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b2408-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="b2408-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2408-133">NOTES</span></span>

## <span data-ttu-id="b2408-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2408-134">RELATED LINKS</span></span>

