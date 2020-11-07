---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 09757005b8865652ef4c922c558dbf86e8c68cdc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924874"
---
# <span data-ttu-id="abbfd-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="abbfd-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="abbfd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abbfd-102">SYNOPSIS</span></span>
<span data-ttu-id="abbfd-103">Anger egenskaper för Key Encryption Key på ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="abbfd-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="abbfd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abbfd-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abbfd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abbfd-105">DESCRIPTION</span></span>
<span data-ttu-id="abbfd-106">Cmdleten **set-AzDiskKeyEncryptionKey** anger egenskaperna för Key Encryption Key för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="abbfd-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="abbfd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abbfd-107">EXAMPLES</span></span>

### <span data-ttu-id="abbfd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="abbfd-108">Example 1</span></span>
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

<span data-ttu-id="abbfd-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="abbfd-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="abbfd-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="abbfd-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="abbfd-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="abbfd-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="abbfd-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="abbfd-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="abbfd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abbfd-113">PARAMETERS</span></span>

### <span data-ttu-id="abbfd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abbfd-114">-DefaultProfile</span></span>
<span data-ttu-id="abbfd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abbfd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abbfd-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="abbfd-116">-Disk</span></span>
<span data-ttu-id="abbfd-117">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="abbfd-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="abbfd-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="abbfd-118">-KeyUrl</span></span>
<span data-ttu-id="abbfd-119">Specifes webb adress.</span><span class="sxs-lookup"><span data-stu-id="abbfd-119">Specifes the key Url.</span></span>

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

### <span data-ttu-id="abbfd-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="abbfd-120">-SourceVaultId</span></span>
<span data-ttu-id="abbfd-121">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="abbfd-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="abbfd-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abbfd-122">-Confirm</span></span>
<span data-ttu-id="abbfd-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abbfd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abbfd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abbfd-124">-WhatIf</span></span>
<span data-ttu-id="abbfd-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abbfd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abbfd-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abbfd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abbfd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abbfd-127">CommonParameters</span></span>
<span data-ttu-id="abbfd-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abbfd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abbfd-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abbfd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abbfd-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abbfd-130">INPUTS</span></span>

### <span data-ttu-id="abbfd-131">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="abbfd-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="abbfd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="abbfd-132">System.String</span></span>

## <span data-ttu-id="abbfd-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abbfd-133">OUTPUTS</span></span>

### <span data-ttu-id="abbfd-134">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="abbfd-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="abbfd-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abbfd-135">NOTES</span></span>

## <span data-ttu-id="abbfd-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abbfd-136">RELATED LINKS</span></span>

