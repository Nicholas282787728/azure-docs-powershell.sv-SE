---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: e544007d8e23e20ed311f07eb33f98a5e2d6a409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756224"
---
# <span data-ttu-id="847fa-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="847fa-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="847fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="847fa-102">SYNOPSIS</span></span>
<span data-ttu-id="847fa-103">Anger bild referens egenskaperna för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="847fa-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="847fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="847fa-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="847fa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="847fa-105">DESCRIPTION</span></span>
<span data-ttu-id="847fa-106">Cmdleten **set-AzureRmDiskImageReference** anger bild referens egenskaperna för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="847fa-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="847fa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="847fa-107">EXAMPLES</span></span>

### <span data-ttu-id="847fa-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="847fa-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="847fa-109">Med det första kommandot skapas ett lokalt disk objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="847fa-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="847fa-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="847fa-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="847fa-111">Det andra kommandot ställer in bild-ID och det logiska enhets numret 0 för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="847fa-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="847fa-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="847fa-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="847fa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="847fa-113">PARAMETERS</span></span>

### <span data-ttu-id="847fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="847fa-114">-DefaultProfile</span></span>
<span data-ttu-id="847fa-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="847fa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="847fa-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="847fa-116">-Disk</span></span>
<span data-ttu-id="847fa-117">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="847fa-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="847fa-118">-ID</span><span class="sxs-lookup"><span data-stu-id="847fa-118">-Id</span></span>
<span data-ttu-id="847fa-119">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="847fa-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="847fa-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="847fa-120">-Lun</span></span>
<span data-ttu-id="847fa-121">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="847fa-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="847fa-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="847fa-122">-Confirm</span></span>
<span data-ttu-id="847fa-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="847fa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="847fa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="847fa-124">-WhatIf</span></span>
<span data-ttu-id="847fa-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="847fa-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="847fa-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="847fa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="847fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="847fa-127">CommonParameters</span></span>
<span data-ttu-id="847fa-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="847fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="847fa-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="847fa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="847fa-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="847fa-130">INPUTS</span></span>

### <span data-ttu-id="847fa-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="847fa-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="847fa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="847fa-132">System.String</span></span>

### <span data-ttu-id="847fa-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="847fa-133">System.Int32</span></span>

## <span data-ttu-id="847fa-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="847fa-134">OUTPUTS</span></span>

### <span data-ttu-id="847fa-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="847fa-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="847fa-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="847fa-136">NOTES</span></span>

## <span data-ttu-id="847fa-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="847fa-137">RELATED LINKS</span></span>
