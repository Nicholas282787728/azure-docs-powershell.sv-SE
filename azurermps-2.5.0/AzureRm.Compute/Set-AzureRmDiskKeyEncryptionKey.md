---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskkeyencryptionkey
schema: 2.0.0
ms.openlocfilehash: 1a3cbf9037f81d9387b1979472e50be940caa7d5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930293"
---
# <span data-ttu-id="bf3d2-101">Set-AzureRmDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bf3d2-101">Set-AzureRmDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="bf3d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="bf3d2-103">Anger egenskaper för Key Encryption Key på ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-103">Sets the key encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf3d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf3d2-104">SYNTAX</span></span>

```
Set-AzureRmDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf3d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf3d2-105">DESCRIPTION</span></span>
<span data-ttu-id="bf3d2-106">Cmdleten **set-AzureRmDiskKeyEncryptionKey** anger egenskaperna för Key Encryption Key för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-106">The **Set-AzureRmDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="bf3d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf3d2-107">EXAMPLES</span></span>

### <span data-ttu-id="bf3d2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bf3d2-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="bf3d2-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="bf3d2-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="bf3d2-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="bf3d2-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="bf3d2-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bf3d2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf3d2-113">PARAMETERS</span></span>

### <span data-ttu-id="bf3d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf3d2-114">-DefaultProfile</span></span>
<span data-ttu-id="bf3d2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf3d2-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="bf3d2-116">-Disk</span></span>
<span data-ttu-id="bf3d2-117">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="bf3d2-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="bf3d2-118">-KeyUrl</span></span>
<span data-ttu-id="bf3d2-119">Specifes webb adress.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-119">Specifes the key Url.</span></span>

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

### <span data-ttu-id="bf3d2-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="bf3d2-120">-SourceVaultId</span></span>
<span data-ttu-id="bf3d2-121">Anger käll valv-ID.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="bf3d2-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf3d2-122">-Confirm</span></span>
<span data-ttu-id="bf3d2-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf3d2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf3d2-124">-WhatIf</span></span>
<span data-ttu-id="bf3d2-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf3d2-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf3d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf3d2-127">CommonParameters</span></span>
<span data-ttu-id="bf3d2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf3d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf3d2-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf3d2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf3d2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf3d2-130">INPUTS</span></span>

### <span data-ttu-id="bf3d2-131">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="bf3d2-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="bf3d2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bf3d2-132">System.String</span></span>

## <span data-ttu-id="bf3d2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf3d2-133">OUTPUTS</span></span>

### <span data-ttu-id="bf3d2-134">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="bf3d2-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="bf3d2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf3d2-135">NOTES</span></span>

## <span data-ttu-id="bf3d2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf3d2-136">RELATED LINKS</span></span>

