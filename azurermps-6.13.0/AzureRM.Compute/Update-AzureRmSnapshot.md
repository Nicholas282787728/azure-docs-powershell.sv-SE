---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: fba3ec6f6ab78042a9e597a1c1074626afcddb25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756213"
---
# <span data-ttu-id="a6240-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6240-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="a6240-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6240-102">SYNOPSIS</span></span>
<span data-ttu-id="a6240-103">Uppdaterar en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="a6240-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6240-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6240-104">SYNTAX</span></span>

### <span data-ttu-id="a6240-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="a6240-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6240-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="a6240-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6240-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6240-107">DESCRIPTION</span></span>
<span data-ttu-id="a6240-108">Cmdleten **Update-AzureRmSnapshot** uppdaterar en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="a6240-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="a6240-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6240-109">EXAMPLES</span></span>

### <span data-ttu-id="a6240-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a6240-110">Example 1</span></span>
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

<span data-ttu-id="a6240-111">Det första kommandot skapar ett lokalt, tomt ögonblicks bilds uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="a6240-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="a6240-112">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="a6240-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a6240-113">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för objektet ögonblicks bild uppdatering.</span><span class="sxs-lookup"><span data-stu-id="a6240-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="a6240-114">Med det senaste kommandot tas ögonblicks bilden uppdatera objekt och en befintlig ögonblicks bild med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a6240-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a6240-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a6240-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="a6240-116">Det här kommandot uppdaterar en befintlig ögonblicks bild med namnet ' Snapshot01 ' i resurs gruppen ' ResourceGroup01 ' till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="a6240-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="a6240-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a6240-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="a6240-118">Dessa kommandon uppdaterar också en befintlig ögonblicks bild med namnet ' Snapshot01 ' i resurs gruppen ' ResourceGroup01 ' till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="a6240-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="a6240-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6240-119">PARAMETERS</span></span>

### <span data-ttu-id="a6240-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6240-120">-AsJob</span></span>
<span data-ttu-id="a6240-121">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="a6240-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6240-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6240-122">-DefaultProfile</span></span>
<span data-ttu-id="a6240-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a6240-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6240-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6240-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6240-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a6240-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a6240-126">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="a6240-126">-Snapshot</span></span>
<span data-ttu-id="a6240-127">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="a6240-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6240-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="a6240-128">-SnapshotName</span></span>
<span data-ttu-id="a6240-129">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="a6240-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="a6240-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a6240-130">-SnapshotUpdate</span></span>
<span data-ttu-id="a6240-131">Anger ett lokalt ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="a6240-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6240-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a6240-132">-Confirm</span></span>
<span data-ttu-id="a6240-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6240-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6240-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6240-134">-WhatIf</span></span>
<span data-ttu-id="a6240-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a6240-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6240-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a6240-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6240-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6240-137">CommonParameters</span></span>
<span data-ttu-id="a6240-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6240-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6240-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6240-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6240-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6240-140">INPUTS</span></span>

### <span data-ttu-id="a6240-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a6240-141">System.String</span></span>

### <span data-ttu-id="a6240-142">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a6240-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>
<span data-ttu-id="a6240-143">Parametrar: SnapshotUpdate (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a6240-143">Parameters: SnapshotUpdate (ByValue)</span></span>

### <span data-ttu-id="a6240-144">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6240-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>
<span data-ttu-id="a6240-145">Parametrar: ögonblicks bild (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a6240-145">Parameters: Snapshot (ByValue)</span></span>

## <span data-ttu-id="a6240-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6240-146">OUTPUTS</span></span>

### <span data-ttu-id="a6240-147">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6240-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="a6240-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6240-148">NOTES</span></span>

## <span data-ttu-id="a6240-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6240-149">RELATED LINKS</span></span>
