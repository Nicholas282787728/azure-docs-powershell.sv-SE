---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: 963e6f4621276eda4fdf598d571f2c2171dbc4f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579599"
---
# <span data-ttu-id="657d3-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="657d3-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="657d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="657d3-102">SYNOPSIS</span></span>
<span data-ttu-id="657d3-103">Anger bild referens egenskaperna för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="657d3-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="657d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="657d3-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <Disk> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="657d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="657d3-105">DESCRIPTION</span></span>
<span data-ttu-id="657d3-106">Cmdleten **set-AzureRmDiskImageReference** anger bild referens egenskaperna för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="657d3-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="657d3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="657d3-107">EXAMPLES</span></span>

### <span data-ttu-id="657d3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="657d3-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="657d3-109">Med det första kommandot skapas ett lokalt disk objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="657d3-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="657d3-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="657d3-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="657d3-111">Det andra kommandot ställer in bild-ID och det logiska enhets numret 0 för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="657d3-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="657d3-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="657d3-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="657d3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="657d3-113">PARAMETERS</span></span>

### <span data-ttu-id="657d3-114">-Disk</span><span class="sxs-lookup"><span data-stu-id="657d3-114">-Disk</span></span>
<span data-ttu-id="657d3-115">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="657d3-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="657d3-116">-ID</span><span class="sxs-lookup"><span data-stu-id="657d3-116">-Id</span></span>
<span data-ttu-id="657d3-117">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="657d3-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="657d3-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="657d3-118">-Lun</span></span>
<span data-ttu-id="657d3-119">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="657d3-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="657d3-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="657d3-120">-Confirm</span></span>
<span data-ttu-id="657d3-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="657d3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="657d3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="657d3-122">-WhatIf</span></span>
<span data-ttu-id="657d3-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="657d3-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="657d3-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="657d3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="657d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="657d3-125">CommonParameters</span></span>
<span data-ttu-id="657d3-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="657d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="657d3-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="657d3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="657d3-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="657d3-128">INPUTS</span></span>

### <span data-ttu-id="657d3-129">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="657d3-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="657d3-130">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="657d3-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="657d3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="657d3-131">OUTPUTS</span></span>

### <span data-ttu-id="657d3-132">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="657d3-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="657d3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="657d3-133">NOTES</span></span>

## <span data-ttu-id="657d3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="657d3-134">RELATED LINKS</span></span>

