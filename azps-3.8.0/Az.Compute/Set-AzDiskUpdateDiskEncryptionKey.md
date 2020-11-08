---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 4ef0ffba83fdf24d9808880cda5a7942c1705c8e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088585"
---
# <span data-ttu-id="bea7e-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bea7e-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="bea7e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bea7e-102">SYNOPSIS</span></span>
<span data-ttu-id="bea7e-103">Anger egenskaper för disk krypterings nycklar på ett disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="bea7e-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="bea7e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bea7e-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bea7e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bea7e-105">DESCRIPTION</span></span>
<span data-ttu-id="bea7e-106">Cmdleten **set-AzDiskUpdateDiskEncryptionKey** anger egenskaper för disk krypterings nycklar på ett disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="bea7e-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="bea7e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bea7e-107">EXAMPLES</span></span>

### <span data-ttu-id="bea7e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bea7e-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="bea7e-109">Med det första kommandot skapas ett lokalt tomt disk uppdaterings objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="bea7e-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="bea7e-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="bea7e-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="bea7e-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="bea7e-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="bea7e-112">Det sista kommandot tar emot disk uppdaterings objekt och uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="bea7e-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bea7e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bea7e-113">PARAMETERS</span></span>

### <span data-ttu-id="bea7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea7e-114">-DefaultProfile</span></span>
<span data-ttu-id="bea7e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bea7e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bea7e-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="bea7e-116">-DiskUpdate</span></span>
<span data-ttu-id="bea7e-117">Anger ett uppdaterings objekt för lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="bea7e-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="bea7e-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="bea7e-118">-SecretUrl</span></span>
<span data-ttu-id="bea7e-119">Anger den hemliga URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="bea7e-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="bea7e-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="bea7e-120">-SourceVaultId</span></span>
<span data-ttu-id="bea7e-121">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="bea7e-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="bea7e-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bea7e-122">-Confirm</span></span>
<span data-ttu-id="bea7e-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bea7e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea7e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea7e-124">-WhatIf</span></span>
<span data-ttu-id="bea7e-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bea7e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bea7e-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bea7e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea7e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea7e-127">CommonParameters</span></span>
<span data-ttu-id="bea7e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea7e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea7e-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bea7e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea7e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bea7e-130">INPUTS</span></span>

### <span data-ttu-id="bea7e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="bea7e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="bea7e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bea7e-132">System.String</span></span>

## <span data-ttu-id="bea7e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bea7e-133">OUTPUTS</span></span>

### <span data-ttu-id="bea7e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="bea7e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="bea7e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bea7e-135">NOTES</span></span>

## <span data-ttu-id="bea7e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bea7e-136">RELATED LINKS</span></span>
