---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: c99ac5668bd45202532f852fac9ca41cbbb02fe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754475"
---
# <span data-ttu-id="27dbb-101">Set-AzSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="27dbb-101">Set-AzSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="27dbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="27dbb-103">Anger egenskaperna för Key Encryption Key för ett ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="27dbb-103">Sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="27dbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27dbb-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27dbb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27dbb-105">DESCRIPTION</span></span>
<span data-ttu-id="27dbb-106">Cmdleten **set-AzSnapshotUpdateKeyEncryptionKey** anger egenskaperna för Key Encryption Key för ett ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="27dbb-106">The **Set-AzSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="27dbb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27dbb-107">EXAMPLES</span></span>

### <span data-ttu-id="27dbb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="27dbb-108">Example 1</span></span>
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

<span data-ttu-id="27dbb-109">Det första kommandot skapar ett lokalt, tomt ögonblicks bilds uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="27dbb-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="27dbb-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="27dbb-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="27dbb-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för objektet ögonblicks bild uppdatering.</span><span class="sxs-lookup"><span data-stu-id="27dbb-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="27dbb-112">Med det senaste kommandot tas ögonblicks bilden uppdatera objekt och en befintlig ögonblicks bild med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="27dbb-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="27dbb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27dbb-113">PARAMETERS</span></span>

### <span data-ttu-id="27dbb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27dbb-114">-DefaultProfile</span></span>
<span data-ttu-id="27dbb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27dbb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27dbb-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="27dbb-116">-KeyUrl</span></span>
<span data-ttu-id="27dbb-117">Specifes webb adress.</span><span class="sxs-lookup"><span data-stu-id="27dbb-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="27dbb-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="27dbb-118">-SnapshotUpdate</span></span>
<span data-ttu-id="27dbb-119">Anger ett lokalt ögonblicks bild uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="27dbb-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="27dbb-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="27dbb-120">-SourceVaultId</span></span>
<span data-ttu-id="27dbb-121">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="27dbb-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="27dbb-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27dbb-122">-Confirm</span></span>
<span data-ttu-id="27dbb-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27dbb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27dbb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27dbb-124">-WhatIf</span></span>
<span data-ttu-id="27dbb-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="27dbb-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27dbb-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="27dbb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27dbb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27dbb-127">CommonParameters</span></span>
<span data-ttu-id="27dbb-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27dbb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27dbb-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27dbb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27dbb-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27dbb-130">INPUTS</span></span>

### <span data-ttu-id="27dbb-131">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="27dbb-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="27dbb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="27dbb-132">System.String</span></span>

## <span data-ttu-id="27dbb-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27dbb-133">OUTPUTS</span></span>

### <span data-ttu-id="27dbb-134">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="27dbb-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="27dbb-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27dbb-135">NOTES</span></span>

## <span data-ttu-id="27dbb-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27dbb-136">RELATED LINKS</span></span>
