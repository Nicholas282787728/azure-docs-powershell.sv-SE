---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
ms.openlocfilehash: 1b0f223514e8d1f740c9341d29f78a4a5d08108d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924889"
---
# <span data-ttu-id="e883a-101">Set-AzDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e883a-101">Set-AzDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="e883a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e883a-102">SYNOPSIS</span></span>
<span data-ttu-id="e883a-103">Anger egenskaper för disk krypterings nycklar på ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="e883a-103">Sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="e883a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e883a-104">SYNTAX</span></span>

```
Set-AzDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e883a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e883a-105">DESCRIPTION</span></span>
<span data-ttu-id="e883a-106">Cmdleten **set-AzDiskDiskEncryptionKey** anger egenskaperna för disk krypterings nycklar på ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="e883a-106">The **Set-AzDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="e883a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e883a-107">EXAMPLES</span></span>

### <span data-ttu-id="e883a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e883a-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="e883a-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e883a-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="e883a-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="e883a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e883a-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="e883a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="e883a-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e883a-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e883a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e883a-113">PARAMETERS</span></span>

### <span data-ttu-id="e883a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e883a-114">-DefaultProfile</span></span>
<span data-ttu-id="e883a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e883a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e883a-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="e883a-116">-Disk</span></span>
<span data-ttu-id="e883a-117">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="e883a-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e883a-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="e883a-118">-SecretUrl</span></span>
<span data-ttu-id="e883a-119">Anger den hemliga URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="e883a-119">Specifies the secret Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e883a-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e883a-120">-SourceVaultId</span></span>
<span data-ttu-id="e883a-121">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="e883a-121">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e883a-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e883a-122">-Confirm</span></span>
<span data-ttu-id="e883a-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e883a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e883a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e883a-124">-WhatIf</span></span>
<span data-ttu-id="e883a-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e883a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e883a-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e883a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e883a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e883a-127">CommonParameters</span></span>
<span data-ttu-id="e883a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e883a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e883a-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e883a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e883a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e883a-130">INPUTS</span></span>

### <span data-ttu-id="e883a-131">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="e883a-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="e883a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e883a-132">System.String</span></span>

## <span data-ttu-id="e883a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e883a-133">OUTPUTS</span></span>

### <span data-ttu-id="e883a-134">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="e883a-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="e883a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e883a-135">NOTES</span></span>

## <span data-ttu-id="e883a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e883a-136">RELATED LINKS</span></span>
