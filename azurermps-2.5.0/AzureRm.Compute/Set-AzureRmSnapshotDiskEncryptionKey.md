---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotdiskencryptionkey
schema: 2.0.0
ms.openlocfilehash: f78b680f5872301236c5d001ce9920d2edd61f02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929097"
---
# <span data-ttu-id="66f58-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="66f58-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="66f58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66f58-102">SYNOPSIS</span></span>
<span data-ttu-id="66f58-103">Ställer in egenskaper för disk krypterings nycklar i ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="66f58-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66f58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66f58-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66f58-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66f58-105">DESCRIPTION</span></span>
<span data-ttu-id="66f58-106">Cmdleten **set-AzureRmSnapshotDiskEncryptionKey** anger egenskaperna för disk krypterings nycklar i ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="66f58-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="66f58-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66f58-107">EXAMPLES</span></span>

### <span data-ttu-id="66f58-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="66f58-108">Example 1</span></span>
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

<span data-ttu-id="66f58-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="66f58-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="66f58-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="66f58-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="66f58-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="66f58-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="66f58-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="66f58-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="66f58-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66f58-113">PARAMETERS</span></span>

### <span data-ttu-id="66f58-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f58-114">-DefaultProfile</span></span>
<span data-ttu-id="66f58-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66f58-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66f58-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="66f58-116">-SecretUrl</span></span>
<span data-ttu-id="66f58-117">Anger den hemliga URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="66f58-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="66f58-118">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="66f58-118">-Snapshot</span></span>
<span data-ttu-id="66f58-119">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="66f58-119">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66f58-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="66f58-120">-SourceVaultId</span></span>
<span data-ttu-id="66f58-121">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="66f58-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="66f58-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="66f58-122">-Confirm</span></span>
<span data-ttu-id="66f58-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66f58-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66f58-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66f58-124">-WhatIf</span></span>
<span data-ttu-id="66f58-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="66f58-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66f58-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="66f58-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66f58-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f58-127">CommonParameters</span></span>
<span data-ttu-id="66f58-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66f58-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f58-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66f58-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f58-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66f58-130">INPUTS</span></span>

### <span data-ttu-id="66f58-131">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="66f58-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="66f58-132">System. String</span><span class="sxs-lookup"><span data-stu-id="66f58-132">System.String</span></span>

## <span data-ttu-id="66f58-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66f58-133">OUTPUTS</span></span>

### <span data-ttu-id="66f58-134">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="66f58-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="66f58-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66f58-135">NOTES</span></span>

## <span data-ttu-id="66f58-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66f58-136">RELATED LINKS</span></span>
