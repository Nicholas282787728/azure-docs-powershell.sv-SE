---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 29090d0c59ef5c32dd74b622c2a79d477419c3b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103013"
---
# <span data-ttu-id="52061-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="52061-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="52061-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52061-102">SYNOPSIS</span></span>
<span data-ttu-id="52061-103">Anger egenskaper för Key Encryption Key på ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="52061-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="52061-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52061-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52061-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52061-105">DESCRIPTION</span></span>
<span data-ttu-id="52061-106">Cmdleten **set-AzDiskKeyEncryptionKey** anger egenskaperna för Key Encryption Key för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="52061-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="52061-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52061-107">EXAMPLES</span></span>

### <span data-ttu-id="52061-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52061-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskconfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1';
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="52061-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="52061-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="52061-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="52061-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="52061-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="52061-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="52061-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="52061-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="52061-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52061-113">PARAMETERS</span></span>

### <span data-ttu-id="52061-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52061-114">-DefaultProfile</span></span>
<span data-ttu-id="52061-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52061-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52061-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="52061-116">-Disk</span></span>
<span data-ttu-id="52061-117">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="52061-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52061-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="52061-118">-KeyUrl</span></span>
<span data-ttu-id="52061-119">Anger URL-adressen för den.</span><span class="sxs-lookup"><span data-stu-id="52061-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="52061-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="52061-120">-SourceVaultId</span></span>
<span data-ttu-id="52061-121">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="52061-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="52061-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52061-122">-Confirm</span></span>
<span data-ttu-id="52061-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52061-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52061-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52061-124">-WhatIf</span></span>
<span data-ttu-id="52061-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52061-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52061-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52061-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52061-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52061-127">CommonParameters</span></span>
<span data-ttu-id="52061-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52061-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52061-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52061-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52061-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52061-130">INPUTS</span></span>

### <span data-ttu-id="52061-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="52061-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="52061-132">System. String</span><span class="sxs-lookup"><span data-stu-id="52061-132">System.String</span></span>

## <span data-ttu-id="52061-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52061-133">OUTPUTS</span></span>

### <span data-ttu-id="52061-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="52061-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="52061-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52061-135">NOTES</span></span>

## <span data-ttu-id="52061-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52061-136">RELATED LINKS</span></span>
