---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: fa77808eddc0e51fa76a0883980b34552589f4ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930721"
---
# <span data-ttu-id="017a4-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="017a4-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="017a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="017a4-102">SYNOPSIS</span></span>
<span data-ttu-id="017a4-103">Skapar en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="017a4-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="017a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="017a4-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="017a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="017a4-105">DESCRIPTION</span></span>
<span data-ttu-id="017a4-106">**New-AzureRmSnapshot-** cmdleten skapar en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="017a4-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="017a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="017a4-107">EXAMPLES</span></span>

### <span data-ttu-id="017a4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="017a4-108">Example 1</span></span>
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

<span data-ttu-id="017a4-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="017a4-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="017a4-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="017a4-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="017a4-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="017a4-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="017a4-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="017a4-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="017a4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="017a4-113">PARAMETERS</span></span>

### <span data-ttu-id="017a4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="017a4-114">-AsJob</span></span>
<span data-ttu-id="017a4-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="017a4-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="017a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="017a4-116">-DefaultProfile</span></span>
<span data-ttu-id="017a4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="017a4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="017a4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="017a4-118">-ResourceGroupName</span></span>
<span data-ttu-id="017a4-119">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="017a4-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="017a4-120">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="017a4-120">-Snapshot</span></span>
<span data-ttu-id="017a4-121">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="017a4-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="017a4-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="017a4-122">-SnapshotName</span></span>
<span data-ttu-id="017a4-123">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="017a4-123">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="017a4-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="017a4-124">-Confirm</span></span>
<span data-ttu-id="017a4-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="017a4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="017a4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="017a4-126">-WhatIf</span></span>
<span data-ttu-id="017a4-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="017a4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="017a4-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="017a4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="017a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="017a4-129">CommonParameters</span></span>
<span data-ttu-id="017a4-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="017a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="017a4-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="017a4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="017a4-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="017a4-132">INPUTS</span></span>

### <span data-ttu-id="017a4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="017a4-133">System.String</span></span>
<span data-ttu-id="017a4-134">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="017a4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="017a4-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="017a4-135">OUTPUTS</span></span>

### <span data-ttu-id="017a4-136">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="017a4-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="017a4-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="017a4-137">System.Object</span></span>

## <span data-ttu-id="017a4-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="017a4-138">NOTES</span></span>

## <span data-ttu-id="017a4-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="017a4-139">RELATED LINKS</span></span>

