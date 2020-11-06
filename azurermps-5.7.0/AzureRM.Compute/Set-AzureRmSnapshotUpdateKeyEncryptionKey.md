---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: 8745202e860cb71d20e17d68203a9bc79b3167ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573519"
---
# <span data-ttu-id="78a57-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="78a57-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="78a57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78a57-102">SYNOPSIS</span></span>
<span data-ttu-id="78a57-103">Anger egenskaperna för Key Encryption Key för ett ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="78a57-103">Sets the key encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78a57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78a57-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <SnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78a57-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78a57-105">DESCRIPTION</span></span>
<span data-ttu-id="78a57-106">Cmdleten **set-AzureRmSnapshotUpdateKeyEncryptionKey** anger egenskaperna för Key Encryption Key för ett ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="78a57-106">The **Set-AzureRmSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="78a57-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78a57-107">EXAMPLES</span></span>

### <span data-ttu-id="78a57-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="78a57-108">Example 1</span></span>
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

<span data-ttu-id="78a57-109">Det första kommandot skapar ett lokalt, tomt ögonblicks bilds uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="78a57-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="78a57-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="78a57-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="78a57-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för objektet ögonblicks bild uppdatering.</span><span class="sxs-lookup"><span data-stu-id="78a57-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="78a57-112">Med det senaste kommandot tas ögonblicks bilden uppdatera objekt och en befintlig ögonblicks bild med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="78a57-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="78a57-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78a57-113">PARAMETERS</span></span>

### <span data-ttu-id="78a57-114">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="78a57-114">-KeyUrl</span></span>
<span data-ttu-id="78a57-115">Specifes webb adress.</span><span class="sxs-lookup"><span data-stu-id="78a57-115">Specifes the key Url.</span></span>

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

### <span data-ttu-id="78a57-116">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="78a57-116">-SnapshotUpdate</span></span>
<span data-ttu-id="78a57-117">Anger ett lokalt ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="78a57-117">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="78a57-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="78a57-118">-SourceVaultId</span></span>
<span data-ttu-id="78a57-119">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="78a57-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="78a57-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78a57-120">-Confirm</span></span>
<span data-ttu-id="78a57-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78a57-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78a57-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78a57-122">-WhatIf</span></span>
<span data-ttu-id="78a57-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78a57-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78a57-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78a57-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78a57-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a57-125">CommonParameters</span></span>
<span data-ttu-id="78a57-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a57-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a57-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a57-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a57-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78a57-128">INPUTS</span></span>

### <span data-ttu-id="78a57-129">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="78a57-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="78a57-130">System. String</span><span class="sxs-lookup"><span data-stu-id="78a57-130">System.String</span></span>

## <span data-ttu-id="78a57-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78a57-131">OUTPUTS</span></span>

### <span data-ttu-id="78a57-132">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="78a57-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="78a57-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78a57-133">NOTES</span></span>

## <span data-ttu-id="78a57-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78a57-134">RELATED LINKS</span></span>

