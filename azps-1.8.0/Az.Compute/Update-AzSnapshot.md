---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: eaf02348525cb1d6833ec52a0c4608e4a362ccd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754427"
---
# <span data-ttu-id="43aab-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="43aab-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="43aab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43aab-102">SYNOPSIS</span></span>
<span data-ttu-id="43aab-103">Uppdaterar en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="43aab-103">Updates a snapshot.</span></span>

## <span data-ttu-id="43aab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43aab-104">SYNTAX</span></span>

### <span data-ttu-id="43aab-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="43aab-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43aab-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="43aab-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43aab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43aab-107">DESCRIPTION</span></span>
<span data-ttu-id="43aab-108">Cmdleten **Update-AzSnapshot** uppdaterar en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="43aab-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="43aab-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43aab-109">EXAMPLES</span></span>

### <span data-ttu-id="43aab-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="43aab-110">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="43aab-111">Det första kommandot skapar ett lokalt, tomt ögonblicks bilds uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="43aab-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="43aab-112">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="43aab-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="43aab-113">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för objektet ögonblicks bild uppdatering.</span><span class="sxs-lookup"><span data-stu-id="43aab-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="43aab-114">Med det senaste kommandot tas ögonblicks bilden uppdatera objekt och en befintlig ögonblicks bild med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="43aab-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="43aab-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="43aab-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="43aab-116">Det här kommandot uppdaterar en befintlig ögonblicks bild med namnet ' Snapshot01 ' i resurs gruppen ' ResourceGroup01 ' till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="43aab-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="43aab-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="43aab-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="43aab-118">Dessa kommandon uppdaterar också en befintlig ögonblicks bild med namnet ' Snapshot01 ' i resurs gruppen ' ResourceGroup01 ' till 10 GB disk storlek.</span><span class="sxs-lookup"><span data-stu-id="43aab-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="43aab-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43aab-119">PARAMETERS</span></span>

### <span data-ttu-id="43aab-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43aab-120">-AsJob</span></span>
<span data-ttu-id="43aab-121">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="43aab-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="43aab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43aab-122">-DefaultProfile</span></span>
<span data-ttu-id="43aab-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43aab-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43aab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43aab-124">-ResourceGroupName</span></span>
<span data-ttu-id="43aab-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="43aab-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43aab-126">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="43aab-126">-Snapshot</span></span>
<span data-ttu-id="43aab-127">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="43aab-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43aab-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="43aab-128">-SnapshotName</span></span>
<span data-ttu-id="43aab-129">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="43aab-129">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43aab-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="43aab-130">-SnapshotUpdate</span></span>
<span data-ttu-id="43aab-131">Anger ett lokalt ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="43aab-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43aab-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43aab-132">-Confirm</span></span>
<span data-ttu-id="43aab-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43aab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43aab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43aab-134">-WhatIf</span></span>
<span data-ttu-id="43aab-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43aab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43aab-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43aab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43aab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43aab-137">CommonParameters</span></span>
<span data-ttu-id="43aab-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43aab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43aab-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43aab-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43aab-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43aab-140">INPUTS</span></span>

### <span data-ttu-id="43aab-141">System. String</span><span class="sxs-lookup"><span data-stu-id="43aab-141">System.String</span></span>

### <span data-ttu-id="43aab-142">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="43aab-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="43aab-143">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="43aab-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="43aab-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43aab-144">OUTPUTS</span></span>

### <span data-ttu-id="43aab-145">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="43aab-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="43aab-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43aab-146">NOTES</span></span>

## <span data-ttu-id="43aab-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43aab-147">RELATED LINKS</span></span>
