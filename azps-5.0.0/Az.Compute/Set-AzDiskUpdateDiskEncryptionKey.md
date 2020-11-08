---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 51a501e2b01ef044685f4172d42bad5342cb462c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270738"
---
# <span data-ttu-id="962e5-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="962e5-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="962e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="962e5-102">SYNOPSIS</span></span>
<span data-ttu-id="962e5-103">Anger egenskaper för disk krypterings nycklar på ett disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="962e5-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="962e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="962e5-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="962e5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="962e5-105">DESCRIPTION</span></span>
<span data-ttu-id="962e5-106">Cmdleten **set-AzDiskUpdateDiskEncryptionKey** anger egenskaper för disk krypterings nycklar på ett disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="962e5-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="962e5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="962e5-107">EXAMPLES</span></span>

### <span data-ttu-id="962e5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="962e5-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="962e5-109">Med det första kommandot skapas ett lokalt tomt disk uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="962e5-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="962e5-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="962e5-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="962e5-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="962e5-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="962e5-112">Det sista kommandot tar emot disk uppdaterings objekt och uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="962e5-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="962e5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="962e5-113">PARAMETERS</span></span>

### <span data-ttu-id="962e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962e5-114">-DefaultProfile</span></span>
<span data-ttu-id="962e5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="962e5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="962e5-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="962e5-116">-DiskUpdate</span></span>
<span data-ttu-id="962e5-117">Anger ett uppdaterings objekt för lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="962e5-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="962e5-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="962e5-118">-SecretUrl</span></span>
<span data-ttu-id="962e5-119">Anger den hemliga URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="962e5-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="962e5-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="962e5-120">-SourceVaultId</span></span>
<span data-ttu-id="962e5-121">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="962e5-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="962e5-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="962e5-122">-Confirm</span></span>
<span data-ttu-id="962e5-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="962e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="962e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="962e5-124">-WhatIf</span></span>
<span data-ttu-id="962e5-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="962e5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="962e5-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="962e5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="962e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962e5-127">CommonParameters</span></span>
<span data-ttu-id="962e5-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="962e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962e5-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="962e5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962e5-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="962e5-130">INPUTS</span></span>

### <span data-ttu-id="962e5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="962e5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="962e5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="962e5-132">System.String</span></span>

## <span data-ttu-id="962e5-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="962e5-133">OUTPUTS</span></span>

### <span data-ttu-id="962e5-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="962e5-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="962e5-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="962e5-135">NOTES</span></span>

## <span data-ttu-id="962e5-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="962e5-136">RELATED LINKS</span></span>
