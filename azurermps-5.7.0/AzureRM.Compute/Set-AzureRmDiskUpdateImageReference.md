---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 55a3a45cf22dd6558a9728a254531a0e01627e20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579572"
---
# <span data-ttu-id="cbcb1-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="cbcb1-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="cbcb1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbcb1-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcb1-103">Anger bild referens egenskaperna för ett disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbcb1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbcb1-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <DiskUpdate> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbcb1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbcb1-105">DESCRIPTION</span></span>
<span data-ttu-id="cbcb1-106">Cmdleten **set-AzureRmDiskUpdateImageReference** anger bild referens egenskaperna för ett disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="cbcb1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbcb1-107">EXAMPLES</span></span>

### <span data-ttu-id="cbcb1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cbcb1-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="cbcb1-109">Det första kommandot skapar ett uppdaterings objekt för lokala diskar med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="cbcb1-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="cbcb1-111">Det andra kommandot ställer in bild-ID och det logiska enhets numret 0 för disk uppdaterings objekt.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="cbcb1-112">Det sista kommandot tar emot disk uppdaterings objekt och uppdaterar en befintlig disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cbcb1-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cbcb1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbcb1-113">PARAMETERS</span></span>

### <span data-ttu-id="cbcb1-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="cbcb1-114">-DiskUpdate</span></span>
<span data-ttu-id="cbcb1-115">Anger ett uppdaterings objekt för lokala diskar.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcb1-116">-ID</span><span class="sxs-lookup"><span data-stu-id="cbcb1-116">-Id</span></span>
<span data-ttu-id="cbcb1-117">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="cbcb1-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="cbcb1-118">-Lun</span></span>
<span data-ttu-id="cbcb1-119">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="cbcb1-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcb1-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbcb1-120">-Confirm</span></span>
<span data-ttu-id="cbcb1-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbcb1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbcb1-122">-WhatIf</span></span>
<span data-ttu-id="cbcb1-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbcb1-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbcb1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcb1-125">CommonParameters</span></span>
<span data-ttu-id="cbcb1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcb1-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbcb1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcb1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbcb1-128">INPUTS</span></span>

### <span data-ttu-id="cbcb1-129">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="cbcb1-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="cbcb1-130">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cbcb1-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="cbcb1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbcb1-131">OUTPUTS</span></span>

### <span data-ttu-id="cbcb1-132">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="cbcb1-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="cbcb1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbcb1-133">NOTES</span></span>

## <span data-ttu-id="cbcb1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbcb1-134">RELATED LINKS</span></span>

