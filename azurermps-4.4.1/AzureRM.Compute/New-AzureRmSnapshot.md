---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
ms.openlocfilehash: c7d88f16ff9eb6bb32cdf286ef37a1aba17030cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585764"
---
# <span data-ttu-id="fef43-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="fef43-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="fef43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fef43-102">SYNOPSIS</span></span>
<span data-ttu-id="fef43-103">Skapar en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fef43-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fef43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fef43-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fef43-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fef43-105">DESCRIPTION</span></span>
<span data-ttu-id="fef43-106">**New-AzureRmSnapshot-** cmdleten skapar en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fef43-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="fef43-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fef43-107">EXAMPLES</span></span>

### <span data-ttu-id="fef43-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fef43-108">Example 1</span></span>
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

<span data-ttu-id="fef43-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="fef43-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="fef43-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="fef43-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="fef43-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fef43-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="fef43-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fef43-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fef43-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fef43-113">PARAMETERS</span></span>

### <span data-ttu-id="fef43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef43-114">-DefaultProfile</span></span>
<span data-ttu-id="fef43-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fef43-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fef43-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef43-116">-ResourceGroupName</span></span>
<span data-ttu-id="fef43-117">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fef43-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fef43-118">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="fef43-118">-Snapshot</span></span>
<span data-ttu-id="fef43-119">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="fef43-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fef43-120">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="fef43-120">-SnapshotName</span></span>
<span data-ttu-id="fef43-121">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fef43-121">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="fef43-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fef43-122">-Confirm</span></span>
<span data-ttu-id="fef43-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fef43-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fef43-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fef43-124">-WhatIf</span></span>
<span data-ttu-id="fef43-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fef43-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fef43-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fef43-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fef43-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef43-127">CommonParameters</span></span>
<span data-ttu-id="fef43-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fef43-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef43-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef43-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef43-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fef43-130">INPUTS</span></span>

### <span data-ttu-id="fef43-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fef43-131">System.String</span></span>
<span data-ttu-id="fef43-132">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="fef43-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="fef43-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fef43-133">OUTPUTS</span></span>

### <span data-ttu-id="fef43-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="fef43-134">System.Object</span></span>

## <span data-ttu-id="fef43-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fef43-135">NOTES</span></span>

## <span data-ttu-id="fef43-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fef43-136">RELATED LINKS</span></span>

