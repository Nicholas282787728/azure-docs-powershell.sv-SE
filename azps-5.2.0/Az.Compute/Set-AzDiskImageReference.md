---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 78a6c3bf85fae4fab9c5b9a06c366760b55804fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395883"
---
# <span data-ttu-id="a0203-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="a0203-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="a0203-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0203-102">SYNOPSIS</span></span>
<span data-ttu-id="a0203-103">Anger bild referens egenskaperna för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="a0203-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="a0203-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0203-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0203-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0203-105">DESCRIPTION</span></span>
<span data-ttu-id="a0203-106">Cmdleten **set-AzDiskImageReference** anger bild referens egenskaperna för ett disk objekt.</span><span class="sxs-lookup"><span data-stu-id="a0203-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="a0203-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0203-107">EXAMPLES</span></span>

### <span data-ttu-id="a0203-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a0203-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="a0203-109">Med det första kommandot skapas ett lokalt disk objekt med storleken 10 GB i Premium_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a0203-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="a0203-110">Den anger också Windows OS-typ.</span><span class="sxs-lookup"><span data-stu-id="a0203-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="a0203-111">Det andra kommandot ställer in bild-ID och det logiska enhets numret 0 för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="a0203-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="a0203-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a0203-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a0203-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0203-113">PARAMETERS</span></span>

### <span data-ttu-id="a0203-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0203-114">-DefaultProfile</span></span>
<span data-ttu-id="a0203-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0203-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0203-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="a0203-116">-Disk</span></span>
<span data-ttu-id="a0203-117">Anger ett lokalt disk objekt.</span><span class="sxs-lookup"><span data-stu-id="a0203-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="a0203-118">-ID</span><span class="sxs-lookup"><span data-stu-id="a0203-118">-Id</span></span>
<span data-ttu-id="a0203-119">Anger ID.</span><span class="sxs-lookup"><span data-stu-id="a0203-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="a0203-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="a0203-120">-Lun</span></span>
<span data-ttu-id="a0203-121">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="a0203-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="a0203-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0203-122">-Confirm</span></span>
<span data-ttu-id="a0203-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0203-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0203-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0203-124">-WhatIf</span></span>
<span data-ttu-id="a0203-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0203-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0203-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0203-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0203-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0203-127">CommonParameters</span></span>
<span data-ttu-id="a0203-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0203-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0203-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0203-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0203-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0203-130">INPUTS</span></span>

### <span data-ttu-id="a0203-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="a0203-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="a0203-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a0203-132">System.String</span></span>

### <span data-ttu-id="a0203-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a0203-133">System.Int32</span></span>

## <span data-ttu-id="a0203-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0203-134">OUTPUTS</span></span>

### <span data-ttu-id="a0203-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="a0203-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="a0203-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0203-136">NOTES</span></span>

## <span data-ttu-id="a0203-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0203-137">RELATED LINKS</span></span>
