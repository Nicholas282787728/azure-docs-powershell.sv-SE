---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
ms.openlocfilehash: e4ecb281382af308176f47462e086f69c18e6163
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389163"
---
# <span data-ttu-id="8e515-101">Set-AzSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8e515-101">Set-AzSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="8e515-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e515-102">SYNOPSIS</span></span>
<span data-ttu-id="8e515-103">Ställer in egenskaper för disk krypterings nycklar i ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="8e515-103">Sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="8e515-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e515-104">SYNTAX</span></span>

```
Set-AzSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e515-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e515-105">DESCRIPTION</span></span>
<span data-ttu-id="8e515-106">Cmdleten **set-AzSnapshotDiskEncryptionKey** anger egenskaperna för disk krypterings nycklar i ett SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="8e515-106">The **Set-AzSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="8e515-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e515-107">EXAMPLES</span></span>

### <span data-ttu-id="8e515-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8e515-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="8e515-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="8e515-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="8e515-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="8e515-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="8e515-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="8e515-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="8e515-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="8e515-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8e515-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e515-113">PARAMETERS</span></span>

### <span data-ttu-id="8e515-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e515-114">-DefaultProfile</span></span>
<span data-ttu-id="8e515-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e515-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e515-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="8e515-116">-SecretUrl</span></span>
<span data-ttu-id="8e515-117">Anger den hemliga URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="8e515-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="8e515-118">-Stillbild</span><span class="sxs-lookup"><span data-stu-id="8e515-118">-Snapshot</span></span>
<span data-ttu-id="8e515-119">Anger ett lokalt SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="8e515-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e515-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="8e515-120">-SourceVaultId</span></span>
<span data-ttu-id="8e515-121">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="8e515-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="8e515-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e515-122">-Confirm</span></span>
<span data-ttu-id="8e515-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e515-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e515-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e515-124">-WhatIf</span></span>
<span data-ttu-id="8e515-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e515-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e515-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e515-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e515-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e515-127">CommonParameters</span></span>
<span data-ttu-id="8e515-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e515-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e515-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e515-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e515-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e515-130">INPUTS</span></span>

### <span data-ttu-id="8e515-131">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="8e515-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="8e515-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8e515-132">System.String</span></span>

## <span data-ttu-id="8e515-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e515-133">OUTPUTS</span></span>

### <span data-ttu-id="8e515-134">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="8e515-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="8e515-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e515-135">NOTES</span></span>

## <span data-ttu-id="8e515-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e515-136">RELATED LINKS</span></span>
