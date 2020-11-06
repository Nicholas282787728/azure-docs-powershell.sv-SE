---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: 5fd03c0c262500b79d40063bc1ad35898eda110f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574994"
---
# <span data-ttu-id="6ba02-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6ba02-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="6ba02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ba02-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba02-103">Anger egenskaperna för Key Encryption Key för ett ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="6ba02-103">Sets the key encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ba02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ba02-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ba02-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ba02-105">DESCRIPTION</span></span>
<span data-ttu-id="6ba02-106">Cmdleten **set-AzureRmSnapshotUpdateKeyEncryptionKey** anger egenskaperna för Key Encryption Key för ett ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="6ba02-106">The **Set-AzureRmSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="6ba02-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ba02-107">EXAMPLES</span></span>

### <span data-ttu-id="6ba02-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6ba02-108">Example 1</span></span>
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

<span data-ttu-id="6ba02-109">Det första kommandot skapar ett lokalt, tomt ögonblicks bilds uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="6ba02-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="6ba02-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="6ba02-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="6ba02-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för objektet ögonblicks bild uppdatering.</span><span class="sxs-lookup"><span data-stu-id="6ba02-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="6ba02-112">Med det senaste kommandot tas ögonblicks bilden uppdatera objekt och en befintlig ögonblicks bild med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6ba02-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6ba02-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ba02-113">PARAMETERS</span></span>

### <span data-ttu-id="6ba02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba02-114">-DefaultProfile</span></span>
<span data-ttu-id="6ba02-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6ba02-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ba02-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="6ba02-116">-KeyUrl</span></span>
<span data-ttu-id="6ba02-117">Specifes webb adress.</span><span class="sxs-lookup"><span data-stu-id="6ba02-117">Specifes the key Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba02-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6ba02-118">-SnapshotUpdate</span></span>
<span data-ttu-id="6ba02-119">Anger ett lokalt ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="6ba02-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba02-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6ba02-120">-SourceVaultId</span></span>
<span data-ttu-id="6ba02-121">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="6ba02-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba02-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6ba02-122">-Confirm</span></span>
<span data-ttu-id="6ba02-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6ba02-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ba02-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ba02-124">-WhatIf</span></span>
<span data-ttu-id="6ba02-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6ba02-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ba02-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6ba02-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ba02-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba02-127">CommonParameters</span></span>
<span data-ttu-id="6ba02-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ba02-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba02-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ba02-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba02-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ba02-130">INPUTS</span></span>

### <span data-ttu-id="6ba02-131">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6ba02-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="6ba02-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6ba02-132">System.String</span></span>

## <span data-ttu-id="6ba02-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ba02-133">OUTPUTS</span></span>

### <span data-ttu-id="6ba02-134">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6ba02-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="6ba02-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ba02-135">NOTES</span></span>

## <span data-ttu-id="6ba02-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ba02-136">RELATED LINKS</span></span>

