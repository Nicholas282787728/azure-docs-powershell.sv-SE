---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: e73b1a316402722e03ff9c26fd27610cb916b060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756235"
---
# <span data-ttu-id="0f3e4-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="0f3e4-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="0f3e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f3e4-102">SYNOPSIS</span></span>
<span data-ttu-id="0f3e4-103">Skapar en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f3e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f3e4-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f3e4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f3e4-105">DESCRIPTION</span></span>
<span data-ttu-id="0f3e4-106">Cmdleten **New-AzureRmDisk** skapar en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="0f3e4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f3e4-107">EXAMPLES</span></span>

### <span data-ttu-id="0f3e4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0f3e4-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="0f3e4-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="0f3e4-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0f3e4-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="0f3e4-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0f3e4-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0f3e4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f3e4-113">PARAMETERS</span></span>

### <span data-ttu-id="0f3e4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f3e4-114">-AsJob</span></span>
<span data-ttu-id="0f3e4-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0f3e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f3e4-116">-DefaultProfile</span></span>
<span data-ttu-id="0f3e4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f3e4-118">-Disk</span><span class="sxs-lookup"><span data-stu-id="0f3e4-118">-Disk</span></span>
<span data-ttu-id="0f3e4-119">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-119">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f3e4-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="0f3e4-120">-DiskName</span></span>
<span data-ttu-id="0f3e4-121">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-121">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="0f3e4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f3e4-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f3e4-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0f3e4-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f3e4-124">-Confirm</span></span>
<span data-ttu-id="0f3e4-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f3e4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f3e4-126">-WhatIf</span></span>
<span data-ttu-id="0f3e4-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f3e4-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f3e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f3e4-129">CommonParameters</span></span>
<span data-ttu-id="0f3e4-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f3e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f3e4-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f3e4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f3e4-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f3e4-132">INPUTS</span></span>

### <span data-ttu-id="0f3e4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0f3e4-133">System.String</span></span>

### <span data-ttu-id="0f3e4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="0f3e4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>
<span data-ttu-id="0f3e4-135">Parametrar: disk (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f3e4-135">Parameters: Disk (ByValue)</span></span>

## <span data-ttu-id="0f3e4-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f3e4-136">OUTPUTS</span></span>

### <span data-ttu-id="0f3e4-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="0f3e4-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="0f3e4-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f3e4-138">NOTES</span></span>

## <span data-ttu-id="0f3e4-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f3e4-139">RELATED LINKS</span></span>
