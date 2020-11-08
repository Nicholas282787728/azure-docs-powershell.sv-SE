---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
ms.openlocfilehash: cd0a66d8f8d777df9a8ebc3791643234f0d15fb0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930294"
---
# <span data-ttu-id="d2445-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="d2445-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="d2445-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2445-102">SYNOPSIS</span></span>
<span data-ttu-id="d2445-103">Anger bild referens egenskaperna för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="d2445-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2445-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2445-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2445-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2445-105">DESCRIPTION</span></span>
<span data-ttu-id="d2445-106">Cmdleten **set-AzureRmDiskImageReference** anger bild referens egenskaperna för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="d2445-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="d2445-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2445-107">EXAMPLES</span></span>

### <span data-ttu-id="d2445-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d2445-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="d2445-109">Med det första kommandot skapas ett lokalt disk objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d2445-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d2445-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="d2445-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="d2445-111">Det andra kommandot ställer in bild-ID och det logiska enhets numret 0 för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="d2445-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="d2445-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d2445-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d2445-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2445-113">PARAMETERS</span></span>

### <span data-ttu-id="d2445-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2445-114">-DefaultProfile</span></span>
<span data-ttu-id="d2445-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2445-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2445-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="d2445-116">-Disk</span></span>
<span data-ttu-id="d2445-117">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="d2445-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="d2445-118">-ID</span><span class="sxs-lookup"><span data-stu-id="d2445-118">-Id</span></span>
<span data-ttu-id="d2445-119">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="d2445-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="d2445-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="d2445-120">-Lun</span></span>
<span data-ttu-id="d2445-121">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="d2445-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="d2445-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2445-122">-Confirm</span></span>
<span data-ttu-id="d2445-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2445-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2445-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2445-124">-WhatIf</span></span>
<span data-ttu-id="d2445-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2445-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2445-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2445-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2445-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2445-127">CommonParameters</span></span>
<span data-ttu-id="d2445-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2445-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2445-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2445-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2445-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2445-130">INPUTS</span></span>

### <span data-ttu-id="d2445-131">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="d2445-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="d2445-132">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d2445-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d2445-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2445-133">OUTPUTS</span></span>

### <span data-ttu-id="d2445-134">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="d2445-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="d2445-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2445-135">NOTES</span></span>

## <span data-ttu-id="d2445-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2445-136">RELATED LINKS</span></span>
